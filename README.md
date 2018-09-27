# surge rule-set sample
```
[Rule]
PROCESS-NAME,storedownloadd,DIRECT // Mac App Store
USER-AGENT,com.apple.appstored*,DIRECT // iOS App Store
DOMAIN,xp.apple.com,Proxy // iOS & macOS System Upgrade
DOMAIN,iosapps.itunes.apple.com,DIRECT
DOMAIN-SUFFIX,store.apple.com,DIRECT
# Rulesets
RULE-SET,SYSTEM,DIRECT
RULE-SET,https://github.com/scomper/surge-list/raw/master/apple.list,Proxy
RULE-SET,adblock.list,REJECT
RULE-SET,https://github.com/scomper/surge-list/raw/master/reject.list,REJECT-TINYGIF
RULE-SET,https://github.com/scomper/surge-list/raw/master/cn.list,nProxy
RULE-SET,https://github.com/scomper/surge-list/raw/master/blocked.list,Proxy
RULE-SET,https://github.com/scomper/surge-list/raw/master/netflix.list,Proxy
RULE-SET,https://github.com/scomper/surge-list/raw/master/telegram.list,Proxy
RULE-SET,LAN,DIRECT
# GeoIP CN
GEOIP,CN,DIRECT
FINAL,Proxy,dns-failed