# ipv6-test

用于 mihomo 的 IPv6 测试域名规则集，配合 `🌐 IPv6` 代理组使用。

默认走 DIRECT 使用 ISP 原生 IPv6 直连，需要验证节点时手动切换到 DMIT v6 节点。

## 使用方法

rule-providers 添加：

\```yaml
ipv6-test:
  type: http
  behavior: domain
  url: "https://raw.githubusercontent.com/liuqi008/ipv6-test/main/rules/ipv6-test.yaml"
  path: "./rule_provider/ipv6-test.yaml"
  interval: 86400
\```

rules 最前面添加：

\```yaml
- "RULE-SET,ipv6-test,🌐 IPv6"
\```
