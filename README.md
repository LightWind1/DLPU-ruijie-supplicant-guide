# 大连工业大学校园网锐捷认证指南

本校锐捷认证会检验MAC地址，但是不会检验硬盘SN，目前mentohust及[minieap](https://github.com/AutoCONFIG/minieap)不需要额外抓包，均能够直接认证校园网。 <br>
最早版本的xrgsu也可以正常使用。<br>
<br>
EAP broadcast address为锐捷私有地址，心跳包间隔建议设置为15秒，DHCP认证方式必须为DHCP before Auth。<br>
<br>
minieap命令参考: `minieap -u 学号 -p 密码 -n 你的网卡 --module printer --module rjv3 -d 3` <br>
<br>
## 路由器上使用
padavan可以使用自带的mentohust<br>
openwrt上推荐使用[openwrt-proto-minieap](https://github.com/LightWind1/openwrt-proto-minieap)与[luci-proto-minieap](https://github.com/LightWind1/luci-proto-minieap)认证，实测下来感觉minieap更稳定些。<br>
