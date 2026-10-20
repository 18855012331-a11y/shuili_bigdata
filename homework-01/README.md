# 第一次作业：大坝安全监测数据回归分析

**选择档位：垂线数据（基础档）。**

本次作业包含可运行的 Python 代码和 Word 说明文档，分析5个垂线测点，比较水位线性、二次和加入季节周期与时间趋势的回归模型。

## 提交内容

- [Python代码](analysis.py)
- [Word报告](outputs/垂线数据回归分析报告.docx)
- [原始数据](data/垂线数据.xlsx)
- [模型指标](outputs/model_metrics.csv)

按训练期交叉验证选择的模型在测试集上的 R² 为0.957～0.994；测试期未参与模型选择。

## 运行

需要 Python 3.10 或以上。在解压后的项目目录运行：

```bash
python -m pip install -r requirements.txt
python analysis.py
```

`requirements-tested.txt`记录本次成功运行的主要依赖版本。

指定路径：

```bash
python analysis.py --data "data/垂线数据.xlsx" --out outputs
```

## 文件

- `analysis.py`：数据处理、三个模型比较、时间序列交叉验证、绘图和Word报告生成。
- `data/垂线数据.xlsx`：原始数据，来自用户提供的附件。
- `outputs/垂线数据回归分析报告.docx`：可编辑的说明文档，可直接用Word打开。
- `outputs/model_metrics.csv`：5个测点、3种模型的实际指标。
- `outputs/data_quality.csv`：清洗和划分记录。
- `outputs/*_predictions.csv`：各模型的逐条预测，含训练/测试标识。
- `outputs/*_coefficients.csv`、`model_summary.json`：选定模型参数。系数基于中心化水位，时间单位为年；不要直接代入原始水位。
- `outputs/*.png`：全时段拟合、测试散点和测试残差图；图内采用英文以避免中文字体缺失。

训练采用按时间前80%的记录，后20%保留测试；模型选择仅使用训练期内4折时间序列交叉验证。结果不能代替工程安全鉴定。报告中的学习体会请结合个人实际理解修改。

脚本会覆盖指定输出目录中同名的分析结果，不修改原始Excel。无需运行附件中其他示例代码。
