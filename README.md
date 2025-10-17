# ForeSight 

> **ARMA • GHTBLM • STM • Informer** 等时间序列模型实现与对比
> *A curated collection of classic & modern time‑series forecasting models.*

![GitHub last commit](https://img.shields.io/github/last-commit/jhlucc/ForeSight)
![GitHub stars](https://img.shields.io/github/stars/jhlucc/ForeSight)
![License](https://img.shields.io/github/license/jhlucc/ForeSight)
  
---  
## 📖 项目简介 | Overview

ForeSight 旨在把常见 **统计学方法**、**机器学习模型** 和 **深度学习 Transformer 系列** 的时间序列预测实现集中于一个仓库，便于快速上手、横向对比与二次开发。每类模型都提供：
 
1. **理论笔记 / Paper 速览**
2. **Jupyter Notebook 演示**  
3. **可复现实验脚本**  
4. **数据与指标**
   
--- 

## 🗂️ 目录结构 | Repository Structure

| 路径                         | 说明                 | 典型内容                                             |
| -------------------------- | ------------------ | ------------------------------------------------ |
| `data/`                    | 数据与预处理             | `prophet` 示例数据集等                                 |
| `statistics time series/`  | 经典统计模型             | `ARMA`, `VAR`, `SARIMA`…                         |
| `ml time series/`          | 机器学习方法             | `LightGBM`, `XGBoost`, `RandomForest`…           |
| `transformer time series/` | 深度学习 / Transformer | `Informer`, `FEDformer`, `Autoformer`, `GPT‑TS`… |
| `paper/`                   | 阅读笔记 & 资料          | 数据集介绍、论文摘要                                       |
| `README.md`                | 项目说明               | ——                                               |

---

## 🚀 快速开始 | Quick Start

```bash
# 1. 克隆仓库
git clone https://github.com/jhlucc/ForeSight.git
cd ForeSight

# 2. 创建 Python 环境 
python -m venv .venv
source .venv/bin/activate     

# 3. 安装依赖
pip install -r requirements.txt
# 若未提供 requirements.txt，可手动安装常用库：
# pip install numpy pandas scikit-learn matplotlib statsmodels torch pytorch-lightning

# 4. 运行示例（以 Informer 为例）
jupyter lab                    # 打开 Notebook
# 或
python "transformer time series/run_informer.py" --cfg configs/informer.yaml
```

---

## 🔍 数据集 | Datasets

* **电力负荷**：`ElectricityLoadDiagrams`
* **交通流量**：`PEMS‑Bay` / `PEMS‑D7`
* **气象数据**：`Weather`、`ETTh1/ETTm1`
* **金融行情**：自采股票 / 加密货币 K 线

下载脚本与预处理说明见 `data/` 及子目录。

---

## 📊 评估指标 | Metrics

* **回归**：MAE · RMSE · MAPE · sMAPE
* **概率预测**：CRPS · Pinball Loss
* **异常检测**：Precision · Recall · F1

实验结果示例请见各 Notebook 末尾或 `results/`。

---

## 🧠 已实现模型 | Implemented Models

| 类别          | 名称（部分）                                                                         |
| ----------- | ------------------------------------------------------------------------------ |
| 统计          | ARMA · ARIMA · SARIMA · VAR · GARCH                                            |
| ML          | LGBM · XGBoost · CatBoost · SVR · RandomForest                                 |
| DL          | LSTM · Seq2Seq · TCN · N‑Beats                                                 |
| Transformer | **Informer · FEDformer · Autoformer · ETSformer · Non‑stationary Transformer** |
| 其它          | Prophet · NeuralProphet · GHTBLM · STM                                         |

---

## 📌 TODO

* [ ] 增加 **时序分类 / 异常检测** 任务
* [ ] 引入 **多变量多步长** 统一评测框架
* [ ] 提供 Docker 镜像与 CLI 工具

欢迎 Issue / PR！

---

## 🤝 贡献指南 | Contributing

1. **Fork** → 新建分支 → **提交 PR**
2. 代码需通过 `flake8` / `black` 检查并附单元测试
3. 提交前请确保 Notebook 能自顶向下顺利运行

---

## 📝 引用 | References

* Box G., Jenkins G. **Time Series Analysis: Forecasting and Control**
* Haoyi Zhou *et al.* **Informer: Beyond Efficient Transformer for Long Sequence Time‑Series Forecasting** (AAAI 2021)
* Tianqi Zhu *et al.* **FEDformer: Frequency Enhanced Decomposed Transformer for Long‑term Series Forecasting** (ICLR 2022)
* *更多文献见* `paper/`

---

## ⚖️ 许可证 | License

本项目采用 **GPL‑3.0** 许可证。详见 [LICENSE](./LICENSE)。

---

## 🔗 联系方式 | Contact

* **Author**: [@jhlucc](https://github.com/jhlucc)

觉得有用就 **Star ✨**，欢迎交流合作！
