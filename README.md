# Motd_awa

服务器 MOTD 模组：从配置好的文案列表里，按设定间隔自动刷新服务器 MOTD（随机或顺序轮换）。

## 下载

| Minecraft | Mod 版本 | 文件 |
| --- | --- | --- |
| 26.1.2 | 1.2 | `motd_awa-fabric-26.1.2-1.2.jar` |
| 26.2 | 2.4 | `motd_awa-fabric-26.2-2.4.jar` |
| 26.3 | 2.5 | `motd_awa-fabric-26.3-2.5.jar` |

到 [Releases](https://github.com/niuniuyike/Motd_awa/releases) 下载对应游戏版本的构建。26.3 为当前源码版本（2.5）。

## 环境

| 依赖 | 版本 |
| --- | --- |
| Minecraft | 26.1.2 / 26.2 / 26.3（按构建选择） |
| Fabric Loader | 0.14.0+ |
| Java | 25 |

只需要装在**服务端**。

## 使用

1. 把对应版本的 `motd_awa-*.jar` 放进服务端 `mods/` 目录
2. 启动服务器，会自动生成 `config/motd_awa.json`

配置文件字段：

| 字段 | 说明 |
| --- | --- |
| `motdList` | MOTD 文案列表，支持 `§` 颜色代码，`\n` 表示换行；可写多行，例如 `§cM§6S§eU\n§7彩虹服务器` |
| `enableRandomMotd` | `true` 随机抽取，`false` 按顺序轮换 |
| `updateIntervalSeconds` | 刷新间隔（秒） |

命令：

| 命令 | 说明 |
| --- | --- |
| `/motd reload` | 重新读取配置，立即生效 |

## 构建

需要 JDK 25：

```bash
gradlew build
```

产物在 `build/libs/`。

---

本项目 95% 的代码由 AI 编写。本仓库从 [awa_mods](https://github.com/niuniuyike/awa_mods) 拆分而来。
