对于使用LlamaIndex架构的应用,目录结构通常包含以下几个主要部分:

1. 数据目录

通常会有一个专门用于存储原始数据文件的目录,例如命名为"data"或"documents"。这个目录中可能包含各种格式的文件,如PDF、TXT、Markdown等[1][3]。

2. 索引目录 

用于存储生成的索引文件的目录,可能命名为"index"或"indexes"。这里会保存LlamaIndex创建的各种索引结构,如向量索引等[4]。

3. 源代码目录

包含应用程序主要逻辑的Python源代码文件,通常命名为"src"或直接使用应用名称。

4. 配置文件

可能会有一个配置文件(如config.yaml或.env)用于存储API密钥、模型参数等配置信息。

5. 依赖管理文件

如requirements.txt或Pipfile,用于管理项目依赖。

6. 主程序文件

如main.py或app.py,作为应用程序的入口点。

7. 工具脚本

可能包含一些辅助脚本,如数据预处理、索引构建等。

一个典型的目录结构可能如下所示:

```
my_llamaindex_app/
├── data/
│   ├── document1.pdf
│   ├── document2.txt
│   └── ...
├── indexes/
├── src/
│   ├── __init__.py
│   ├── indexing.py
│   ├── querying.py
│   └── ...
├── config.yaml
├── requirements.txt
├── main.py
└── README.md
```

这种结构可以根据具体应用的需求进行调整。重要的是要保持良好的组织,将数据、索引、源代码等分开存储,以便于管理和维护[2]。

在使用SimpleDirectoryReader时,你可以直接指定data目录作为输入源,例如:

```python
from llama_index import SimpleDirectoryReader

reader = SimpleDirectoryReader(input_dir="data/")
documents = reader.load_data()
```

这样可以方便地加载和处理存储在data目录中的所有文档[3][5]。

总之,LlamaIndex的应用结构应该清晰地分离数据、索引和代码,同时提供灵活性以适应不同的项目需求。

Citations:
[1] https://www.restack.io/docs/llamaindex-knowledge-llamaindex-simpledirectoryreader-pdf
[2] https://towardsdatascience.com/llamaindex-the-ultimate-llm-framework-for-indexing-and-retrieval-fa588d8ca03e?gi=7ba897d52aa5
[3] https://docs.llamaindex.ai/en/stable/examples/data_connectors/simple_directory_reader/
[4] https://docs.llamaindex.ai/en/stable/module_guides/indexing/
[5] https://github.com/run-llama/llama_index/discussions/11970