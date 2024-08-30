# text2mysql
基于InternLM进行微调的一个text2sql的数据库助手大模型
## 介绍
mysql是专门需要处理大量数据的非计算机技术领域人员训练的大模型，mysql小助手通过internlm的训练和微调，采用中英文的text2sql对话数据集，实现快速准确地获取数据库中的数据以支持决策。
基于InternLM地大模型学习项目，欢迎大家也来参加书生大模型实战项目（http://github.com/internLM/tutorial）
## 项目目标
* 精准、快速地将自然语言转换为sql语言
* 支持中文数据库查询
* 高效感知数据库项目名称、类别
* 接入agent实现自然语言输入->sql语言生成->sql执行->获得所需数据
## 产品功能
自然语言转换为sql语句，使非专业人员可直接使用对数据库进行查询和处理
## 架构图
![image](c797a66dab1a1b3e342c3b4a5c5fd63.png)
## 技术细节
* 数据收集与处理：搜集text2sql对话数据集，包括中文和英文
* 模型训练：使用XTuner对IternLM 2.5 7B模型进行训练和微调，确保模型地专用性
* 模型部署：使用LMDeploy部署框架，同时采用KV cache 和 W4A16减小模型部署的内存负载
* RAG技术：采用RAG方式使大模型精准识别数据库名称 类别，给出准确的指令
## 对话效果示例
![image](c797a66dab1a1b3e342c3b4a5c5fd63.png)
![image](c797a66dab1a1b3e342c3b4a5c5fd63.png)
![image](c797a66dab1a1b3e342c3b4a5c5fd63.png)
![image](c797a66dab1a1b3e342c3b4a5c5fd63.png)
