# SPEC.md - test-ipDisplay

## 1. 项目概述

- **项目名称**: test-ipDisplay (JOSP-ipDisplay)
- **项目类型**: Spring Boot 应用
- **核心功能**: 基于 ip2region 库的 IP 地址地理位置查询工具
- **目标用户**: 需要进行 IP 地理位置查询的开发者

## 2. 技术栈

| 组件 | 版本 |
|------|------|
| Spring Boot | 3.2.3 |
| Java | 17 |
| ip2region | 2.7.0 |

## 3. 功能规格

### 3.1 核心功能

- **离线 IP 查询**: 使用 ip2region xdb 数据库进行离线 IP 地理位置查询
- **高速查询**: 微秒级查询速度
- **地理位置信息**: 支持国家、省份、城市、运营商信息

### 3.2 项目结构

```
src/main/java/wo1261931780/JOSPipDisplay/
├── JospIpDisplayApplication.java          # Spring Boot 启动类
├── demo/
│   └── testIp.java                         # IP 查询演示类
└── (resources/)
    └── ip2region.xdb                        # IP 数据库文件
```

### 3.3 核心代码

**testIp.java** - IP 查询演示:
- 加载离线 xdb 数据库文件
- 使用 Searcher 类进行 IP 查询
- 返回格式: `{region: 国家|省份|城市|运营商, ioCount: IO次数, took: 微秒数}`

## 4. 配置信息

- **Java 版本**: 17
- **端口**: 默认 8080

## 5. 编译信息

- **Maven 编译**: 通过
- **打包方式**: JAR

## 6. README.md 状态

- 存在，但内容过于复杂，描述了前后端分离架构、Vue.js 前端等
- 实际项目仅为简单的 Spring Boot 演示项目，包含一个 testIp.java 主程序
- README.md 内容与实际代码不符，需要简化

## 7. .gitignore 状态

- 存在但不够完整，缺少内容同其他项目
