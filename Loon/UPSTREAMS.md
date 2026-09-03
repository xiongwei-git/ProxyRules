# 上游规则来源

下表是 Loon 镜像的维护清单。更新时先获取对应 URL，与此仓库的本地文件比较；有变更时只替换对应镜像文件，并在提交中记录上游提交号。

| 本地文件 | 上游原始地址 | 同步时上游提交 |
| --- | --- | --- |
| `Loon/Google.list` | `https://raw.githubusercontent.com/Loon0x00/LoonLiteRules/main/proxy/Google.list` | `184bd13b7398` |
| `Loon/YouTube.list` | `https://raw.githubusercontent.com/Loon0x00/LoonLiteRules/main/proxy/YouTube.list` | `184bd13b7398` |
| `Loon/Telegram.list` | `https://raw.githubusercontent.com/Loon0x00/LoonLiteRules/main/proxy/Telegram.list` | `184bd13b7398` |
| `Loon/GlobalAI.list` | `https://raw.githubusercontent.com/VPSDance/ai-proxy-rules/main/rules/loon/global.list` | `62b95727da89` |
| `Loon/Global.list` | `https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Loon/Proxy/Proxy.list` | `e1ae9f9ca4de` |

`Clash/ProxyGFWlist.list` 是本仓库既有的通用代理基线，由 `.github/workflows/update.yml` 自动生成和更新；不要为了消除重复项手工删改它。专用策略通过 `[Remote Rule]` 的配置顺序优先于它即可。

个人规则只能在 `Loon/personal/` 中维护，不能混入任何上游镜像。涉及私有域名、家庭网络或个人 IP-CIDR 时，保留在 Loon 本地 `[Rule]`，不要写入公开仓库。
