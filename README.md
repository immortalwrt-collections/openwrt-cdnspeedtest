## CloudflareSpeedTest on OpenWrt

### 项目地址：[XIU2/CloudflareSpeedTest](https://github.com/XIU2/CloudflareSpeedTest)

### 项目简介

> 国外很多网站都在使用 Cloudflare CDN，但分配给中国访客的 IP 并不友好（高延迟/高丢包/速度慢等）。
> 虽然 Cloudflare 公开了所有 IP 段 ，但想要在这么多 IP 中找到适合自己的，怕是要累死，所以就有了这个软件。
>
> 该软件可以测试 Cloudflare CDN 延迟和速度，获取最快 IP (IPv4+IPv6)！觉得好用请点个⭐鼓励一下下~
>
> 本项目也适用于其他 CDN，但是需要自行寻找 CDN IP 段及下载测速地址（否则只能延迟测速）。

- - -

### 使用方法

由于维护问题，不再单独建立一个仓库，如有需要可以参考：[immortalwrt/packages/cdnspeedtest](https://github.com/immortalwrt/packages/tree/master/net/cdnspeedtest)。

- ~~从 [Releases](https://github.com/immortalwrt-collections/openwrt-cdnspeedtest/releases) 下载对应的预编译软件包~~
- 从 [ImmortalWrt 下载站](https://downloads.immortalwrt.org/) 下载对应的预编译软件包
- 自行编译
  ```bash
  # 进入 OpenWrt buildroot 根目录
  $ mkdir -p "package/cdnspeedtest"
  $ curl -fL "https://raw.githubusercontent.com/immortalwrt/packages/master/net/cdnspeedtest/Makefile" | sed 's,../../lang,$(TOPDIR)/feeds/packages/lang,' > "package/cdnspeedtest/Makefile"

  # 进入 buildroot menuconfig 配置界面
  $ make menuconfig
  # 选中 Network -> cdnspeedtest
  Network  --->
  <*> cdnspeedtest.............. Getting the fastest ips to your network of CDN
  ```
