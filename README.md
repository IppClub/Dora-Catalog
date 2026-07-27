# Dora SSR Community Resource Catalog

这是 Dora SSR 社区资源的 Git 目录仓库。

本仓库只保存资源说明、原始 Git 仓库链接和可选预览图，不保存游戏资源本身，也不生成资源汇总文件。下载器同步本仓库后，直接扫描 `projects` 下的项目目录。

## 目录结构

```text
projects/
└── <resource-id>/
    ├── resource.json
    └── banner.jpg       # 可选
```

- 每个项目使用一个独立目录。
- 目录名必须和 `resource.json` 中的 `id` 完全一致。
- `resource.json` 必须符合 `schema/resource-v1.schema.json`。
- `banner.jpg` 可选；没有预览图时由客户端使用默认图片。
- `tags` 用于客户端识别特殊资源类型；Mini 游戏使用 `minigame`。
- 项目资源始终从 `versions[].sources[].url` 指向的公开 Git 仓库取得。
- 每个可安装版本必须记录完整的 40 位 Git commit。

## 添加项目

1. 在 `projects` 下建立以资源 ID 命名的目录。
2. 添加 `resource.json`，填写中英文名称、描述、分类、Git 来源和固定 commit。
3. 如果有预览图，在同一目录添加 `banner.jpg`。
4. 运行以下检查：

```bash
jq empty projects/*/resource.json
```

资源许可证尚未明确时使用：

```json
{
  "license": {
    "status": "pending"
  }
}
```

资源可以先收录，再联系作者补充 SPDX 标识和许可证文件。确认后把状态改为 `confirmed`。

## 更新项目

直接编辑对应目录中的 `resource.json`：

- 发布新版本时，在 `versions` 开头添加一项，并锁定完整 commit。
- 上游地址失效时，将项目设为 `unavailable`，或添加能提供同一 commit 的新来源。
- 只修改说明或预览图时，不需要改变资源版本。

本仓库不会修改用户已经下载的工作树。资源首次 clone 后保留 `.git`，后续同步、分支和本地修改由用户自行通过 Git 完成。

## 仓库镜像

正式发布后，本仓库使用相同 Git 历史同步到：

- `https://github.com/ippclub/Dora-Catalog.git`
- `https://gitcode.com/ippclub/Dora-Catalog.git`（AtomGit 项目页：`https://atomgit.com/ippclub/Dora-Catalog`）

## 发布签名

正式目录提交使用专用 Ed25519 密钥通过 Git SSH 签名。客户端只接受内置受信公钥签署的提交，并要求新提交是本地 last-known-good 的后继。

- 发布公钥指纹：`SHA256:V0yAalaHApJH0f2r7mS45dUMjKq+uLzoUemdKdAtVjg`
- 两个镜像必须发布完全相同的签名 commit。
- 私钥不保存在本仓库中。
