# Hermes 客户端路由

只在当前客户端为 Hermes，或需要为 Hermes 安装、检查或刷新当前副本时读取本文件。

## 安装

从中心安装某个 Skill：

```bash
hermes skills install \
  miracloon/my-skill-repo/<skill_collection>/<skill_name> \
  --force
```

例如：

```bash
hermes skills install \
  miracloon/my-skill-repo/skills-hermes/ry-hermes-agent-design \
  --force
```

`--force` 用于在 Hermes 的安全扫描阻断时继续安装，不表示覆盖已安装副本。

## 检查与刷新

```bash
hermes skills check <skill_name>
hermes skills update <skill_name>
```

`update --force` 会覆盖本地已编辑的副本。只有用户明确要求放弃本地修改时才使用它；正常的 `source` 更新不以 `--force` 覆盖当前副本。

命令不可用或执行失败时，如实报告，不以手工复制伪装为 Hermes 原生安装或更新成功。
