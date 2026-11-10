# 设计阶段 UML 图（实验二）

本目录存放《设计规格说明书》使用的 24 张图，源文件为 PlantUML（`.puml`），渲染结果为同名 `.png`。

## 图的分类

### 1. 总体设计（2.1）

| 图号 | 文件 | 说明 |
|---|---|---|
| 图 2-1 | `architecture-package.puml` / `.png` | 系统逻辑架构包图：表示层、接入层、应用层（接口/应用/领域/基础设施 + common）、数据层 |
| 图 2-2 | `architecture-deployment.puml` / `.png` | 系统物理架构部署图：开发环境与 Docker Compose 演示环境 |

### 2. 模块设计（2.2）

| 图号 | 文件 | 说明 |
|---|---|---|
| 图 2-3 | `design-class-diagram.puml` / `.png` | 设计类图（实体类与关系） |
| 图 2-4 / 2-5 | `robustness-uc06.puml` / `sequence-uc06.puml` | UC-06 支付问诊费：鲁棒图 / 顺序图 |
| 图 2-6 / 2-7 | `robustness-uc07.puml` / `sequence-uc07.puml` | UC-07 接诊与拒诊：鲁棒图 / 顺序图 |
| 图 2-8 / 2-9 | `robustness-uc08.puml` / `sequence-uc08.puml` | UC-08 图文问诊：鲁棒图 / 顺序图 |
| 图 2-10 / 2-11 | `robustness-uc09.puml` / `sequence-uc09.puml` | UC-09 开具处方（草稿）：鲁棒图 / 顺序图 |
| 图 2-12 / 2-13 | `robustness-uc10.puml` / `sequence-uc10.puml` | UC-10 提交处方审核：鲁棒图 / 顺序图 |
| 图 2-14 / 2-15 | `robustness-uc11.puml` / `sequence-uc11.puml` | UC-11 审核处方通过：鲁棒图 / 顺序图 |
| 图 2-16 / 2-17 | `robustness-uc12.puml` / `sequence-uc12.puml` | UC-12 驳回处方：鲁棒图 / 顺序图 |
| 图 2-18 / 2-19 | `robustness-uc14.puml` / `sequence-uc14.puml` | UC-14 核销处方：鲁棒图 / 顺序图 |
| 图 2-20 | `activity-payment.puml` / `.png` | 活动图：问诊订单支付（UC-06） |
| 图 2-21 | `activity-prescription-submit.puml` / `.png` | 活动图：提交处方审核（UC-10） |
| 图 2-22 | `activity-review-cycle.puml` / `.png` | 活动图：审方、驳回与修改重提（UC-11/12/13） |
| 图 2-23 | `activity-dispense.puml` / `.png` | 活动图：核销发药与过期作废（UC-14） |

### 3. 数据库设计（3）

| 图号 | 文件 | 说明 |
|---|---|---|
| 图 2-24 | `database-er.puml` / `.png` | 数据库 ER 图（10 张表） |

## 重新渲染

```bash
# 需要 Java 21 与 plantuml.jar
java -Djava.awt.headless=true -jar plantuml.jar -charset UTF-8 -tpng *.puml
```

> 渲染时务必加 `-charset UTF-8`，否则中文会乱码；图中字体使用 `Microsoft YaHei`，Windows 环境可直接渲染。
