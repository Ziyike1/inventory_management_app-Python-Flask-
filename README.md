基于Python的出入库管理软件

1. 简介
该软件旨在实现对产品的进货、出货和库存的自动统计与管理，并生成每月及每年的使用统计表。软件将使用Python进行界面和逻辑控制，数据库使用MySQL或SQLite进行数据存储。

2. 功能需求
2.1 初期设置
产品信息设置：录入产品的初始信息，包括产品编号、名称、规格、单位等。

2.2 日常操作
进货操作：记录每次进货的信息，包括产品编号、数量、进货日期、供应商等。
出货操作：记录每次出货的信息，包括产品编号、数量、出货日期、去向等。
库存统计：自动更新库存数量，根据进货和出货操作实时更新。

2.3 数据统计
月度统计：生成每月的产品进货、出货和库存统计表，包括每种产品的进货总量、出货总量和期末库存。
年度统计：生成每年的产品进货、出货和库存统计表，包括每种产品的年度进货总量、出货总量和年末库存。

3. 系统需求

3.1 硬件需求
个人电脑
硬盘空间：至少500MB

3.2 软件需求
操作系统：Windows
数据库：MySQL 或 SQLite
开发环境：Python 3.9

4. 用户界面需求
4.1 主界面
导航菜单：包括初期设置、进货操作、出货操作、统计查询等功能模块的链接。
状态栏：显示当前用户、系统时间等信息。

4.2 初期设置界面
产品信息表单：用于录入和编辑产品的初始信息。

4.3 进货操作界面
进货记录表单：用于录入进货信息，包括产品编号、数量、进货日期、供应商等。

4.4 出货操作界面
出货记录表单：用于录入出货信息，包括产品编号、数量、出货日期、去向等。

4.5 统计查询界面
月度统计表：展示每月的进货、出货和库存统计数据。
年度统计表：展示每年的进货、出货和库存统计数据。

5. 数据库设计
5.1 数据表
5.1.1 产品表 (Products)
| 字段名 | 类型 | 描述 |
| ProductID | INT | 产品编号 |
| ProductName | VARCHAR(255) | 产品名称 |
| Specification | VARCHAR(255) | 规格 |
| Unit | VARCHAR(50) | 单位 |

5.1.2 进货表 (PurchaseRecords)
| 字段名 | 类型 | 描述 |
| RecordID | INT | 记录编号 |
| ProductID | INT | 产品编号 |
| Quantity | INT | 数量 |
| PurchaseDate | DATE | 进货日期 |
| Supplier | VARCHAR(255) | 供应商 |

5.1.3 出货表 (SalesRecords)
| 字段名 | 类型 | 描述 |
| RecordID | INT | 记录编号 |
| ProductID | INT | 产品编号 |
| Quantity | INT | 数量 |
| SalesDate | DATE | 出货日期 |
| Destination | VARCHAR(255) | 去向 |

5.2 数据库连接
使用VBA连接MySQL或SQLite数据库，进行数据的增删改查操作。

6. 安全需求
用户权限管理：根据用户角色分配不同的操作权限。
数据备份：定期进行数据库备份，防止数据丢失。
