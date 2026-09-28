# 数据源

## 行情与指数

- A股/个股：腾讯 `https://qt.gtimg.cn/q=sz002466`、新浪 `https://hq.sinajs.cn/list=sz002466`（需 Referer，见 cn-company-fundamentals/references/data-sources.md）
- 美股指数（腾讯接口同样支持）：`https://qt.gtimg.cn/q=usDJI,usIXIC,usSPX`（道指/纳指/标普500）
- 中概：纳斯达克金龙指数 `https://qt.gtimg.cn/q=usHXC`
- 美元指数：`https://qt.gtimg.cn/q=usDINIW`；离岸人民币：`https://qt.gtimg.cn/q=usUSDCNH`
- 大宗：原油 `https://qt.gtimg.cn/q=usCL`（NYMEX）、黄金 `https://qt.gtimg.cn/q=usGC`、铜 `https://qt.gtimg.cn/q=usHG`
- 以上腾讯指数代码未逐一实测，失败时改用网页搜索当日收盘数据并注明来源

## A股复盘与板块

- 网页搜索：`上证指数 收盘 涨跌 成交额`、`领涨板块`，取新浪财经/东方财富/同花顺快讯，注明来源与时间

## 今日看点

- 新股申购/解禁/分红除权除息：东方财富数据中心 `https://data.eastmoney.com/` 相关栏目（页面读取），或搜索 `今日新股申购`、`今日限售解禁`
- 重要公告：复用 cn-announcement-monitor 的东财公告接口
- 宏观事件日历：搜索 `本周财经日历`、`今日重要财经数据`，以权威财经媒体日历为准

## 兜底规则

接口失败或数据对不上时，一律用网页搜索补足并注明来源；补不到的标注"待确认"，不编造数字。
