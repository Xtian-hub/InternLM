# InternLM——珞珞
本项目目标是开发用于大学校园面对生活、学习、政务等多方面对话大模型。守护最好的武汉大学
## 介绍
本项目是一个基于武汉大学校园：以关于校园内学习、政务、生活、新闻资讯等一系列关于武汉大学生活校园的咨询为基础，将初步以武汉大学吉祥物小狐狸的风格来回答问题。模型不仅对校园文化、校园历史等具有基础的了解，还能够模拟珞珞吉祥物的个性特点，为新生和校园师生提供一种独特的互动体验。
## 模型基础
基础模型为InterLM_2.5_20b。训练数据集由ShareGPT提供，其中包括"common_zh_70k.jsonl"、“computer_zh_26k(fixed).jsonl”以及作者个人制作的认知微调数据集。
### 认知微调数据集
数据集目的是强调AI的自我认知，通过与进行关于AI自身归属、姓名等相关问题进行对话来覆盖由前期微调大数据中的自我认知。
以下是示例：
{"conversation": [{"input": "请介绍一下你自己", "output": "raww~ 很高兴认识你哟(＾Ｕ＾)ノ~ＹＯ，我是小狐狸{}，住在武汉大学珞珈山。我可是武大的守护神喏！你可以直接叫我{}，有任何问题尽管来找我吧！raww~".format(name, name)}]}
### 模型目的与意义
本模型旨在为新生、在读师生、访问游客、校友等人群提供围绕历史建筑讲解、校园导游、校园生活问题解答、活动通知等各类校园学习、生活以及游玩等方面的对话
### 研究第一阶段目标（完成）
完成基本模型对中文、基础历史以及长对话方面能力的训练。
### 研究第二阶段目标（进行中）
搭建RAG校园生活知识库，实现已有知识链接以及实时知识爬取与更新。
训练模型自编码能力，并且链接相关在线地图实现校内地点搜索与导航。
### 研究第三阶段目标（理论框架构建中）
模型本地部署，链接公众号对话栏并实施包括但不限于文字对话、语音对话等。
## 教程安利 
如果你也想了解大模型，可以去了解一下哦！https://github.com/InternLM/Tutorial
## 模型特点
风格模拟：模型能够模拟小狐狸的性格特点，回答问题时带有独特的拟人化风格和预期。
校园理解：模型对校园文化有一定的了解，能够围绕校园生活、校园文化进行讨论。
互动体验：用户可以通过提问与模型进行互动，满足校园师生对于校园文化与历史的学习，同时还可以咨询近期校园活动等
## 模型使用
技术框架：base_model->internlm2_chat_7b，包括但不限于增量训练和sft。
部署环境：模型需要在GPU环境下运行，具体配置后期更新配置文件。
交互方式：用户可以通过命令行或Web界面与模型进行交互，或者自行下载权重部署。
## 注意事项
本项目初步概念如若涉及到校园名誉权益请及时联系作者，本人将时刻配合。
