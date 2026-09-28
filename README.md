# 豆瓣聚合仓

影视仓 / TVBox 系客户端用的一整套配置：一个配置地址拿到「豆瓣┃精选」+ 全部站点 + 直播源。

## 怎么用（手机端）

在影视仓「配置地址」里填：

```
https://cdn.jsdelivr.net/gh/KKKKKK66666688/douban-hub@main/douban.json
```

## 文件

| 文件 | 说明 |
| --- | --- |
| `douban.json` | 整仓配置（站点 + 直播 + 规则），客户端真正订阅的那一份 |
| `douban.js` | 豆瓣规则文件（榜单、评分、海报、4 条采集线路匹配） |
| `drpy2.min.js` 等 9 个文件 | 规则引擎及其依赖（取自影视仓自带版本） |

## 备用取用地址（主地址不通时改这一段即可）

| 方式 | 地址 | 特点 |
| --- | --- | --- |
| jsDelivr | https://cdn.jsdelivr.net/gh/KKKKKK66666688/douban-hub@main/douban.json | CDN，国内多数可达；分支地址有缓存，最长约 12 小时 |
| 代理 raw | https://git.yylx.win/https://raw.githubusercontent.com/KKKKKK66666688/douban-hub/refs/heads/main/douban.json | 更新即时生效 |
| 官方 raw | https://raw.githubusercontent.com/KKKKKK66666688/douban-hub/refs/heads/main/douban.json | 国内时好时坏 |

## 本次打包

- 打包时间：2026-09-28 11:54
- 站点数：199
- 直播分组：7 组
- douban.js：673,470 字节，sha256 73F3D125F0C9D22CB40F995157AB8C32B8229F3B0B5719E0F65A893538A8ABD1
