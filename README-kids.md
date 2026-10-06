# 豆瓣聚合仓 · 儿童版

面向电视/儿童使用的独立配置：一个配置地址拿到「豆瓣┃儿童」站点 + 直播源。
与大人版（douban.json）互不影响，两台设备可以分别订阅。

## 怎么用（电视端）

在影视仓「配置地址」里填：

```
https://cdn.jsdelivr.net/gh/KKKKKK66666688/douban-hub@main/douban-kids.json
```

## 与大人版的区别

| 项 | 大人版 douban.json | 儿童版 douban-kids.json |
| --- | --- | --- |
| 站点 | 豆瓣┃精选 + 其余第三方站点 | 豆瓣┃儿童 + 5 个教育类站点（急救/少儿/小学/初中/高中）|
| 过滤 | 不额外过滤 | 按类型白名单过滤，再叠加两份人工名单 |
| 直播 | 7 组 | 同样 7 组（内容一致） |

## 名单怎么改（不用动代码）

改完重新跑一次更新即生效：

- `儿童版-排除名单.txt`：一行一条 `豆瓣id | 片名备注`，命中即从儿童版剔除（优先级最高）
- `儿童版-放行名单.txt`：格式同上；被类型规则误杀的好片写这里放回

## 文件

| 文件 | 说明 |
| --- | --- |
| `douban-kids.json` | 儿童版配置（客户端真正订阅的那一份） |
| `douban-kids.js` | 儿童版规则文件（内嵌过滤后的 13 个分类数据池） |
| `drpy2.min.js` 等 9 个文件 | 规则引擎及其依赖（取自影视仓自带版本，与大人版同一批） |

## 备用取用地址（主地址不通时改这一段即可）

| 方式 | 地址 | 特点 |
| --- | --- | --- |
| jsDelivr | https://cdn.jsdelivr.net/gh/KKKKKK66666688/douban-hub@main/douban-kids.json | CDN，国内多数可达；分支地址有缓存，最长约 12 小时 |
| 代理 raw | https://git.yylx.win/https://raw.githubusercontent.com/KKKKKK66666688/douban-hub/refs/heads/main/douban-kids.json | 更新即时生效 |
| 官方 raw | https://raw.githubusercontent.com/KKKKKK66666688/douban-hub/refs/heads/main/douban-kids.json | 国内时好时坏 |

## 本次打包

- 打包时间：2026-10-06 18:00
- 站点数：6（key douban_kids + Aid/少儿教育/小学课堂/初中课堂/高中教育）
- 直播分组：7 组
- douban-kids.js：396,592 字节，sha256 C8C9EB57B60BE481261390BE600CCC7E820C4B7BAC21446034C2A4DA655097BC
