# ZHOUSJ6 CLIProxyAPI Plugins Store

这是 ZHOUSJ6 自用的 CLIProxyAPI（CPA）插件商店。一个商店源统一提供以下插件：

| 插件 | 版本 | 用途 |
| --- | --- | --- |
| [`codex-workspace-usage`](https://github.com/ZHOUSJ6/cpa-plugin-codex-workspace-usage) | `0.3.1` | 在 CPA 管理中心显示 Codex workspace 日用量，并提供鉴权用量 API。 |
| [`codex-cyber-policy-cooldown`](https://github.com/ZHOUSJ6/codex-cyber-policy-cooldown) | `0.1.2` | 请求命中 `cyber_policy` 后，冷却整个 Codex 凭据。 |

## 在 CPA 中添加

把这个仓库的在线 `registry.json` 添加为自定义商店源：

```yaml
plugins:
  enabled: true
  store-sources:
    - https://raw.githubusercontent.com/ZHOUSJ6/CLIProxyAPI-Plugins-Store/main/registry.json
```

重启 CPA 或刷新插件商店后，按插件 ID 搜索并在线安装即可。各插件的具体配置请查看对应仓库。

## 商店维护方式

- 此仓库只登记 ZHOUSJ6 自己维护的插件。
- CPA 会自动加载官方商店，因此这里不会复制官方插件，避免相同插件 ID 出现在多个商店源后产生安装歧义。
- 插件的安装包和版本更新由各插件仓库的 GitHub Release 提供；这里的 `version` 是版本发现失败时的回退值。
- 新增、移除插件或修改展示信息时，更新 [`registry.json`](./registry.json)。

本仓库最初 fork 自 [`router-for-me/CLIProxyAPI-Plugins-Store`](https://github.com/router-for-me/CLIProxyAPI-Plugins-Store)，现在有意作为个人插件商店使用；官方商店内容仍由 CPA 自带的官方源提供。
