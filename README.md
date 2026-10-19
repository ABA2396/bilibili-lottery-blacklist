# bilibili-lottery-blacklist

B 站抽奖脚本号黑名单，多项目共用。由 MAA 抽奖维护者发起，各项目自愿采用。

用途：抽奖活动的抽池阶段直接排除名单内账号，被排除者不中奖、不消耗补抓名额。

## 数据

[`blacklist.json`](blacklist.json)，数组，每条：

| 字段 | 说明 |
|---|---|
| mid | B 站 UID，唯一键（昵称可改，uname 仅拉黑时快照参考） |
| uname | 拉黑时昵称 |
| reason | 事由（如「抽奖脚本」） |
| date | 裁定日期 |
| source | 来源动态/视频链接 |

## 接入

拉取 raw JSON 喂进你的抽奖流程即可：

```
https://raw.githubusercontent.com/ABA2396/bilibili-lottery-blacklist/main/blacklist.json
```

## 贡献

欢迎其他项目维护者补充条目，请提 issue 或 PR，格式照 `blacklist.json` 字段，并附上判定依据（动态页链接、关注时间证据等）。

由维护者人工审核后合入：黑名单是对具体账号的公开定性，所有条目（包括 PR 内容）统一经维护者裁定后从源头发布，PR 不会直接 merge——合入后下一次发布会自动覆盖等价内容，届时关闭 PR 即可。

## 数据口径

- 条目均为抽奖场景下的行为裁定（脚本自动参与、批量小号等），与 B 站账号本身的封禁状态无关；
- 名单只增不自动清除，异议请提 issue 附证据。
