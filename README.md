# COVID‑19全球疫情数据分析

## 一、项目简介

### 1.1 项目目标
读取全球新冠疫情时间序列数据集（确诊、死亡、康复三份csv），完成数据清洗、地域名称修正、中英文映射，统计全球及中国的确诊/死亡/治愈/现有确诊指标，输出：
1. 汇总统计表
2. 世界地图疫情分布图
3. 时间轮播地图（Timeline）展示疫情历史演变
4. 各国/各省确诊Top20横向柱状轮播图
5. 新增、现有确诊趋势折线图

### 1.2 技术栈
| 工具 | 用途 |
|---|---|
| pandas | csv读取、数据清洗、分组聚合统计 |
| pyecharts | Table、Map、Timeline、Bar、Line可视化 |
| Jupyter Notebook | 交互式渲染图表（`render_notebook()`） |

### 1.3 数据集说明
三份输入文件：
- `time_series_covid19_confirmed_global.csv`：全球各地区每日确诊
- `time_series_covid19_deaths_global.csv`：全球各地区每日死亡
- `time_series_covid19_recovered_global.csv`：全球各地区每日治愈

> 注意：数据集存在缺陷，美国无治愈数据，会造成全球、美国现有确诊、治愈率统计偏差，代码注释中已标注该问题。
