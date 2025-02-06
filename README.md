# WPF Redis Database Viewer

## 介绍

此应用程序是一个基于 WPF (Windows Presentation Foundation) 和 StackExchange.Redis 的简单 Redis 数据库浏览器。它允许用户连接到一个 Redis 实例，并查看指定 Redis 数据库中所有键的信息，包括每个键的类型和数据项数量。
![image](https://github.com/user-attachments/assets/b3b55e52-97a9-421b-aa0f-eb080fa89a9e)



### 功能
- 从 Redis 服务器中读取指定数据库的所有键。
- 根据 Redis 键的类型，统计并显示数据项数量。
- 支持字符串、列表、哈希、集合和有序集合类型。
- 在 WPF 应用程序的界面中，使用 `DataGrid` 显示 Redis 键及其相关信息。

---

## 系统要求

- **.NET 5.0** 或更高版本
- **StackExchange.Redis** NuGet 包（已通过项目引用）
- **Microsoft.Extensions.Configuration** NuGet 包（用于读取配置文件）

---

## 配置说明

### 配置文件 `appsettings.json`

在项目的根目录中，`appsettings.json` 配置文件用于存储 Redis 连接信息。文件内容格式如下：

```json
{
  "Redis": {
    "Host": "localhost",        // Redis 服务器的主机地址
    "Port": "6379",             // Redis 服务器端口
    "Password": "yourpassword", // Redis 密码（如果有）
    "DefaultDb": "0"            // 默认数据库索引
  }
}
```
***
# 代码提交规范
* feat: 新增功能（feature）
* fix: 修复 Bug
* docs: 修改文档（如 README 文件等）
* style: 代码样式的更改（如空格、格式化等，不影响逻辑）
* refactor: 代码重构（既不修复 Bug 也不添加功能）
* perf: 性能优化
* test: 增加/修改测试代码
* chore: 其他杂项修改（如依赖更新、构建工具配置等）
