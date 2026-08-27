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
- v1 兼容格式仍记录完整的 40 位 Git commit；它表示目录收录时观察到的参考快照，不是客户端安装锁。
- `entrypoints[].path` 是 Dora 运行入口，可以使用 `AI Fighter/init` 这样的无扩展名模块路径；不要求仓库存在同名的无扩展名文件。

## 添加项目

1. 在 `projects` 下建立以资源 ID 命名的目录。
2. 添加 `resource.json`，填写中英文名称、描述、分类、Git 来源和收录时的参考 commit。
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

- 发布新版本时，在 `versions` 开头添加一项并更新参考 commit；如需安装指定历史版本，应同时提供对应 tag。
- 上游地址失效时，将项目设为 `unavailable`，或添加内容语义一致的新来源。
- 只修改说明或预览图时，不需要改变资源版本。

客户端按顺序尝试资源来源，安装默认分支当前 HEAD 或目录指定的 tag，不因实际 HEAD 与参考 commit 不同而拒绝安装。目录入口只用于生成运行元数据，入口文件暂时不存在也不阻断仓库安装。

本仓库不会修改用户已经下载的工作树。资源首次 clone 后保留 `.git`，实际 HEAD 记录在本地安装状态中；后续同步、分支和本地修改由用户自行通过 Git 完成。

## 仓库镜像

正式发布后，本仓库使用相同 Git 历史同步到：

- `https://github.com/ippclub/Dora-Catalog.git`
- `https://gitcode.com/ippclub/Dora-Catalog.git`（AtomGit 项目页：`https://atomgit.com/ippclub/Dora-Catalog`）

## 同步与信任边界

两个默认目录镜像应发布相同的 Git commit，避免不同网络环境看到不同目录内容。这是发布一致性要求，不是客户端信任边界。

客户端不内置目录签名公钥，不验证提交签名或历史继承关系。客户端只检查目录 schema、字段和文件结构；资源安装时另行检查实际资源树，拒绝不支持的 symlink、submodule 和 `.gitmodules`。
