# 水利大数据课程作业

本仓库用于整理和提交水利大数据课程作业，保存可运行的 Python 代码、数据、分析结果与说明文档。

## 作业目录

| 目录 | 内容 | 状态 |
| --- | --- | --- |
| [homework-01](homework-01/) | 大坝安全监测数据回归分析：垂线数据基础档 | 已完成 |
| [homework-02](homework-02/) | 第二次作业 | 待布置 |
| [final-project](final-project/) | 课程期末项目 | 待开展 |

## 仓库结构

```text
shuili_bigdata/
├── README.md
├── .gitignore
├── homework-01/
│   ├── README.md
│   ├── analysis.py
│   ├── requirements.txt
│   ├── requirements-tested.txt
│   ├── data/
│   │   └── 垂线数据.xlsx
│   └── outputs/          # Word报告、指标、预测、模型参数和图表
├── homework-02/
│   └── README.md
└── final-project/
    └── README.md
```

## 运行第一次作业

需要 Python 3.10 或以上版本。在仓库根目录执行：

```bash
python -m venv .venv
# Windows PowerShell：.venv\Scripts\Activate.ps1
# macOS / Linux：source .venv/bin/activate
python -m pip install -r homework-01/requirements.txt
python homework-01/analysis.py
```

脚本按自身位置定位输入数据，结果保存到 `homework-01/outputs/`。第一次运行需要安装依赖，之后分析无需网络服务或密钥。

## 第一次作业提交文件

- [Python分析代码](homework-01/analysis.py)
- [Word说明文档](homework-01/outputs/垂线数据回归分析报告.docx)
- [详细说明与结果文件索引](homework-01/README.md)

## 下载方法

**整个仓库：** 在 GitHub 仓库首页点击绿色 **Code → Download ZIP**，下载后解压。

**单个文件：** 打开对应文件，点击右上方的 **Download raw file** 下载按钮；文本代码也可点击 **Raw**，再使用浏览器“另存为”。Word 和 Excel 请使用下载按钮保存原文件。

**使用 Git：**

```bash
git clone https://github.com/18855012331-a11y/shuili_bigdata.git
```

以后同步更新时，在本地仓库目录运行 `git pull`。

## 说明

原始数据来自课程作业附件。回归结果用于课程学习与方法展示，不能替代工程安全鉴定。学习体会应结合本人理解补充和修改。
