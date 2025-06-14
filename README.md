Fork自 [zsokami](https://github.com/zsokami/ACL4SSR)

规则上游自 [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master)

## ACL4SSR.ini

https://raw.githubusercontent.com/lizkes/clash-ruler/main/ruler.ini

和原配置只有一行差异：

```diff
- ruleset=🎯 国内,[]GEOIP,CN
+ ruleset=🎯 国内,[]GEOIP,CN,no-resolve
```

原配置不在已知名单中的（国内外）域名会先通过当地 DNS 服务器解析一次。

添加 no-resolve 后，不在已知名单中的（国内外）域名将直接🚀 代理。

---

url-test
- 延迟测试链接 http://www.gstatic.com/generate_204 -> https://i.ytimg.com/generate_204
- 间隔时间 300秒 -> 300秒
- 容差 50毫秒 -> 100毫秒
- 超市 3000毫秒