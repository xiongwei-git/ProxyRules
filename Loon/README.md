# Loon 远程规则

本目录是 Loon 专用规则的唯一公开发布入口。上游规则以原文件快照保存；个人规则与上游规则分离，避免更新时互相覆盖。

## Loon 配置

将以下内容放入 Loon 的 `[Remote Rule]` 段，并保持这个顺序。规则按先后匹配，专用策略必须位于通用代理列表之前。

```ini
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/personal/personalDirect.list, policy=DIRECT, tag=Personal Direct, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/personal/personalBybitSG.list, policy=SG, tag=Personal Bybit SG, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/personal/personalProxy.list, policy=Available, tag=Personal Proxy, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/YouTube.list, policy=YouTube, tag=YouTube, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/Telegram.list, policy=Telegram, tag=Telegram, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/GlobalAI.list, policy=GlobalAI, tag=GlobalAI, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/Google.list, policy=Available, tag=Google, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Loon/Global.list, policy=Available, tag=Global, enabled=true
https://raw.githubusercontent.com/xiongwei-git/ProxyRules/master/Clash/ProxyGFWlist.list, policy=Available, tag=ProxyGFWlist, enabled=true
```

保留当前 Loon 本地 `[Rule]` 中的私有域名和个人 IP-CIDR；它们不应提交到这个公开仓库。`personalBybitHK.inactive.list` 是当前未启用的备用规则，不能与 `personalBybitSG.list` 同时启用，因为二者匹配相同的域名。

上游来源、固定的同步提交和更新方式见 [UPSTREAMS.md](UPSTREAMS.md)。
