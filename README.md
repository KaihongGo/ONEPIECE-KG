# ONEPICE-KG

ONEPICE-KG 是一个面向《海贼王》领域数据的知识图谱项目。

本项目内容包括数据采集、知识存储、知识抽取、知识计算、知识应用五大部分

## 数据采集

本次项目主要采集构建了两个知识图谱和一个关系抽取数据集

* 人物知识图谱：主要包含各个人物的信息
* 关系抽取数据集：标注出自然语言中存在的实体以及他们之间的关系
* 实体关系知识图谱：构建《海贼王》中各个实体之间关系的知识图谱

## 知识存储

尝试使用了三元组数据库**Apace Jena**和原生图数据库**Neo4j**，并分别使用RDF结构化查询语言**SPARQL**和属性图查询语言**Cypher**，在知识图谱上进行查询。

## 知识抽取

基于之间构建的关系抽取数据集，利用**deepke**中提供的工具进行关系抽取实践，测试了包括PCNN、GCN、BERT等模型在我们构建数据集上的效果

## 知识计算

* 图计算：在Neo4j上对实体关系知识图谱进行了图挖掘，包括最短路径查询、权威结点发现、社区发现等
* 知识推理：在Apache Jena上对关系知识图谱进行了知识推理，补全了一部分的数据

## 知识应用

* 智能问答：基于**REfO**实现一个对于《海贼王》中人物的知识库问答系统(KBQA)。
* 可视化图片：通过D3对实体关系图片进行可视化，并整合了人物知识图谱中的信息，进行展示。

各个部分的具体内容和使用方法，可以参见 `docs` 文件夹下的[项目文档](docs/report.pdf))

实体关系**可视化页面**可以参见项目的[GitHub Pages](https://mrbulb.github.io/ONEPIECE-KG/)