# Sukka → Egern Conversion Report

Converter: **V1.3.0 iOS Lite & Semantic Compression**

Upstream: https://ruleset.skk.moe/

## Conversion totals

| Item | Count |
|---|---:|
| Generated Egern rulesets | 60 |
| Clean source rules | 378806 |
| Removed Sukka markers | 65 |
| Removed duplicate rules | 0 |
| Covered domain suffixes removed | 0 |
| Covered exact domains removed | 0 |
| IPv4 CIDR networks compressed | 0 |
| IPv6 CIDR networks compressed | 1 |
| Conversion coverage | 99.9691% |
| no_resolve rulesets | 11 |
| Mixed no_resolve source files | 1 |
| Strict semantic companion files | 2 |
| Deprecated source files | 3 |
| Empty source files | 7 |
| Unsupported source rules | 117 |
| Invalid source rules | 0 |
| iOS Lite rulesets | 56 |
| iOS Lite total rules | 20711 |
| iOS Lite excluded files | 4 |

## Marker cleanup by category

- `domainset`: 10
- `ip`: 19
- `non_ip`: 36

## Marker cleanup by type

- `domain_marker`: 64
- `keyword_marker`: 1

## iOS Lite output

- `lite/domain`: 6
- `lite/ip`: 16
- `lite/non_ip`: 34

## iOS Lite excluded rulesets

- `domain/reject.yaml`: large_base_ad_block_list
- `domain/reject_extra.yaml`: large_extra_ad_block_list
- `domain/reject_phishing.yaml`: large_phishing_list
- `non_ip/reject-url-regex.yaml`: high_cost_url_regex_ruleset

## iOS Lite URL regex removals

- `non_ip/ai.yaml`: removed 1 URL regex rules
- `non_ip/download.yaml`: removed 1 URL regex rules
- `non_ip/microsoft_cdn.yaml`: removed 2 URL regex rules
- `non_ip/reject.yaml`: removed 3 URL regex rules

## Upstream safety guard

- Previous full rulesets: 60
- Current full rulesets: 60
- Ruleset decrease: 0.00%
- Source rule decrease: 0.00%
- Manual override: False

## Mixed no_resolve semantics

The original filename remains compatible with V1.1.3.
For exact DNS behavior, reference the following companion files
in the displayed order and assign all of them the same policy:

- Source: `ip/reject.conf`
  1. `ip/reject.no_resolve.yaml` (42 rules; DNS resolution disabled)
  2. `ip/reject.resolve.yaml` (737 rules; normal DNS behavior)
  - Compatibility filename: `ip/reject.yaml`

## Rulesets with no_resolve

- `ip/ai.yaml`
- `ip/apple_services.yaml`
- `ip/domestic.yaml`
- `ip/download.yaml`
- `ip/neteasemusic.yaml`
- `ip/reject.no_resolve.yaml`
- `ip/reject.yaml`
- `ip/stream.yaml`
- `ip/telegram.yaml`
- `non_ip/apple_services.yaml`
- `non_ip/reject.yaml`

## Active files without a known marker

- `ip/stream_biliintl.conf`
- `non_ip/stream_biliintl.conf`

## Skipped source files

- `DEPRECATED: domainset/reject_sukka.conf`
- `DEPRECATED: non_ip/apple_cdn.conf`
- `EMPTY: non_ip/cloudmounter.conf`
- `DEPRECATED: non_ip/global_plus.conf`
- `EMPTY: ip/stream_eu.conf`
- `EMPTY: ip/stream_hk.conf`
- `EMPTY: ip/stream_jp.conf`
- `EMPTY: ip/stream_kr.conf`
- `EMPTY: ip/stream_tw.conf`
- `EMPTY: ip/stream_us.conf`

## Unsupported source rules

- `non_ip/apple_services.conf:30: PROCESS-NAME,com.apple.geod`
- `non_ip/apple_services.conf:31: PROCESS-NAME,mapspushd`
- `non_ip/apple_services.conf:32: PROCESS-NAME,com.apple.Maps`
- `non_ip/apple_services.conf:33: PROCESS-NAME,apsd`
- `non_ip/apple_services.conf:34: PROCESS-NAME,fmfd`
- `non_ip/apple_services.conf:35: PROCESS-NAME,findmydevice-user-agent`
- `non_ip/apple_services.conf:36: PROCESS-NAME,CoreLocationAgent`
- `non_ip/apple_services.conf:37: PROCESS-NAME,WeatherWidget`
- `non_ip/cloudmounter.conf:12: AND,((DOMAIN-SUFFIX,sharepoint.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:13: AND,((DOMAIN-SUFFIX,sharepoint.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:14: AND,((DOMAIN-SUFFIX,sharepoint.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:15: AND,((DOMAIN-SUFFIX,sharepoint.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:16: AND,((DOMAIN-SUFFIX,graph.microsoft.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:17: AND,((DOMAIN-SUFFIX,graph.microsoft.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:18: AND,((DOMAIN-SUFFIX,graph.microsoft.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:19: AND,((DOMAIN-SUFFIX,graph.microsoft.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:20: AND,((DOMAIN,www.googleapis.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:21: AND,((DOMAIN,www.googleapis.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:22: AND,((DOMAIN,www.googleapis.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:23: AND,((DOMAIN,www.googleapis.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:24: AND,((DOMAIN,api.onedrive.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:25: AND,((DOMAIN,api.onedrive.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:26: AND,((DOMAIN,api.onedrive.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:27: AND,((DOMAIN,api.onedrive.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:28: AND,((DOMAIN-SUFFIX,storage.live.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:29: AND,((DOMAIN-SUFFIX,storage.live.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:30: AND,((DOMAIN-SUFFIX,storage.live.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:31: AND,((DOMAIN-SUFFIX,storage.live.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:32: AND,((DOMAIN-SUFFIX,files.1drv.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:33: AND,((DOMAIN-SUFFIX,files.1drv.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:34: AND,((DOMAIN-SUFFIX,files.1drv.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:35: AND,((DOMAIN-SUFFIX,files.1drv.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:36: AND,((DOMAIN-SUFFIX,my.microsoftpersonalcontent.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:37: AND,((DOMAIN-SUFFIX,my.microsoftpersonalcontent.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:38: AND,((DOMAIN-SUFFIX,my.microsoftpersonalcontent.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:39: AND,((DOMAIN-SUFFIX,my.microsoftpersonalcontent.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:40: AND,((DOMAIN-WILDCARD,*-medi*.svc.ms),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:41: AND,((DOMAIN-WILDCARD,*-medi*.svc.ms),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:42: AND,((DOMAIN-WILDCARD,*-medi*.svc.ms),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:43: AND,((DOMAIN-WILDCARD,*-medi*.svc.ms),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:44: AND,((DOMAIN-SUFFIX,upload.box.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:45: AND,((DOMAIN-SUFFIX,upload.box.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:46: AND,((DOMAIN-SUFFIX,upload.box.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:47: AND,((DOMAIN-SUFFIX,upload.box.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/cloudmounter.conf:48: AND,((DOMAIN-SUFFIX,upload.app.box.com),(PROCESS-NAME,*CloudMounter))`
- `non_ip/cloudmounter.conf:49: AND,((DOMAIN-SUFFIX,upload.app.box.com),(SRC-IP,10.0.0.0/8))`
- `non_ip/cloudmounter.conf:50: AND,((DOMAIN-SUFFIX,upload.app.box.com),(SRC-IP,172.16.0.0/12))`
- `non_ip/cloudmounter.conf:51: AND,((DOMAIN-SUFFIX,upload.app.box.com),(SRC-IP,192.168.0.0/16))`
- `non_ip/direct.conf:196: PROCESS-NAME,v2ray`
- `non_ip/direct.conf:197: PROCESS-NAME,xray`
- `non_ip/direct.conf:198: PROCESS-NAME,ss-local`
- `non_ip/direct.conf:199: PROCESS-NAME,clash`
- `non_ip/direct.conf:200: PROCESS-NAME,ClashX`
- `non_ip/direct.conf:201: PROCESS-NAME,trojan`
- `non_ip/direct.conf:202: PROCESS-NAME,trojan-go`
- `non_ip/direct.conf:203: PROCESS-NAME,privoxy`
- `non_ip/direct.conf:204: PROCESS-NAME,cloudflared`
- `non_ip/direct.conf:205: PROCESS-NAME,aria2c`
- `non_ip/direct.conf:206: PROCESS-NAME,fdm`
- `non_ip/direct.conf:207: PROCESS-NAME,Folx`
- `non_ip/direct.conf:208: PROCESS-NAME,NetTransport`
- `non_ip/direct.conf:209: PROCESS-NAME,Thunder`
- `non_ip/direct.conf:210: PROCESS-NAME,ThunderVIP`
- `non_ip/direct.conf:211: PROCESS-NAME,Transmission`
- `non_ip/direct.conf:212: PROCESS-NAME,transmission-daemon`
- `non_ip/direct.conf:213: PROCESS-NAME,transmission-qt`
- `non_ip/direct.conf:214: PROCESS-NAME,BitComet`
- `non_ip/direct.conf:215: PROCESS-NAME,uTorrent`
- `non_ip/direct.conf:216: PROCESS-NAME,qbittorrent*`
- `non_ip/direct.conf:217: PROCESS-NAME,DownloadService`
- `non_ip/direct.conf:218: PROCESS-NAME,qBittorrent`
- `non_ip/direct.conf:219: PROCESS-NAME,qbittorrent-nox`
- `non_ip/direct.conf:220: PROCESS-NAME,WebTorrent`
- `non_ip/direct.conf:221: PROCESS-NAME,WebTorrent Helper`
- `non_ip/direct.conf:222: PROCESS-NAME,amuled`
- `non_ip/direct.conf:223: PROCESS-NAME,LocalSend`
- `non_ip/direct.conf:224: PROCESS-NAME,UUBooster`
- `non_ip/direct.conf:225: PROCESS-NAME,tailscaled`
- `non_ip/direct.conf:226: PROCESS-NAME,parsecd`
- `non_ip/direct.conf:227: PROCESS-NAME,SunloginClient_Desktop`
- `non_ip/direct.conf:228: PROCESS-NAME,SunloginClient_Helper`
- `non_ip/direct.conf:229: PROCESS-NAME,BaiduNetdisk_mac`
- `non_ip/direct.conf:230: PROCESS-NAME,Logi Options`
- `non_ip/direct.conf:231: PROCESS-NAME,Logi Options Daemon`
- `non_ip/my_direct.conf:13: PROCESS-NAME,nmap`
- `non_ip/my_reject.conf:57: PROCESS-NAME,Tencent Lemon`
- `non_ip/my_reject.conf:58: PROCESS-NAME,LemonMonitor`
- `non_ip/my_reject.conf:59: PROCESS-NAME,LemonDaemon`
- `non_ip/my_reject.conf:60: PROCESS-NAME,LemonAgent`
- `non_ip/my_reject.conf:61: PROCESS-NAME,LemonService`
- `non_ip/my_reject.conf:63: AND,((DOMAIN-KEYWORD,genuine), (DOMAIN-KEYWORD,autodesk))`
- `non_ip/reject-no-drop.conf:57: AND,((PROTOCOL,UDP), (DOMAIN-SUFFIX,googlevideo.com))`
- `non_ip/sogouinput.conf:25: PROCESS-NAME,SogouInput`
- `non_ip/sogouinput.conf:26: PROCESS-NAME,SogouTaskManager`
- `non_ip/sogouinput.conf:27: PROCESS-NAME,SogouServices`
- `non_ip/stream.conf:394: PROCESS-NAME,com.amazon.avod.thirdpartyclient`
- `non_ip/stream.conf:395: PROCESS-NAME,tv`
- `non_ip/stream.conf:396: PROCESS-NAME,music`
- `non_ip/stream.conf:397: PROCESS-NAME,com.bstar.intl`
- `non_ip/stream.conf:398: PROCESS-NAME,com.hulu.plus`
- `non_ip/stream.conf:399: PROCESS-NAME,com.tencent.ibg.joox`
- `non_ip/stream.conf:400: PROCESS-NAME,com.linecorp.linetv`
- `non_ip/stream.conf:401: PROCESS-NAME,com.netflix.mediaclient`
- `non_ip/stream.conf:402: PROCESS-NAME,com.twgood.android`
- `non_ip/stream.conf:403: PROCESS-NAME,tv.twitch.android.app`
- `non_ip/stream.conf:404: PROCESS-NAME,com.viu.pad`
- `non_ip/stream.conf:405: PROCESS-NAME,com.viu.phone`
- `non_ip/stream.conf:406: PROCESS-NAME,com.vuclip.viu`
- `non_ip/stream.conf:407: PROCESS-NAME,com.hktve.viutv`
- `non_ip/stream_biliintl.conf:17: PROCESS-NAME,com.bstar.intl`
- `non_ip/stream_hk.conf:49: PROCESS-NAME,com.viu.pad`
- `non_ip/stream_hk.conf:50: PROCESS-NAME,com.viu.phone`
- `non_ip/stream_hk.conf:51: PROCESS-NAME,com.vuclip.viu`
- `non_ip/stream_hk.conf:52: PROCESS-NAME,com.hktve.viutv`
- `non_ip/stream_hk.conf:53: PROCESS-NAME,com.bstar.intl`
- `non_ip/stream_tw.conf:58: PROCESS-NAME,com.linecorp.linetv`
- `non_ip/stream_us.conf:77: PROCESS-NAME,com.hulu.plus`

## Invalid source rules

- None

## Category warnings

- `NON_IP_CONTAINS_IP: non_ip/apple_services.conf`
- `NON_IP_CONTAINS_IP: non_ip/reject.conf`
- `IP_CONTAINS_DOMAIN: ip/stream_biliintl.conf`
