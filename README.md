# CL 考试系统 · 产物仓库

**只放安装包与更新清单，不放源码。** 源码在私有仓库。

## 更新清单

四个产品各一份，位置固定。清单里的 `url` 指向**具体 tag**，不用 `releases/latest`
（四个产品独立发版时，`latest` 会被别的产品顶掉）：

| 文件 | 产品 | tag 形如 |
|---|---|---|
| `client.json` | 学生客户端 | `client-v0.1.0` |
| `admin.json` | 服务端 | `server-v0.1.0` |
| `editor.json` | 试卷编辑器 | `editor-v0.1.0` |
| `grader.json` | 判题器 | `grader-v0.1.0` |

清单字段：`product` / `version` / `url` / `sha256` / `notes` / `publishedAt`。

## 安装包

每个产品独立发版，安装包作为该 tag 的资产：

```
https://github.com/block255/CL-exam-system-release/releases/download/<tag>/<安装包文件名>
```

每个 release 另附 `SHA256SUMS.txt`。

## 约定

- 四个产品独立版本号，不设统一版本；
- 程序只在用户点「检查更新」时联网，**不自动下载、不自动安装**；
- 下载后先校验 `sha256`，再显示路径，装不装由人决定；
- 每个 tag 与仓库里对应清单的 `version` 必须一致。