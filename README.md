# Patches to add current gstreamer + gmrender-resurrect to OpenWRT

Based on [gmediarender-resurrect](https://github.com/hzeller/gmrender-resurrect), [OpenWrt-gmediarender](https://github.com/JiapengLi/OpenWrt-gmediarender/blob/master/README.md) and various patches on the [OpenWRT patch tracker](http://patchwork.openwrt.org/project/openwrt/list/).

## HOW TO

This HOWTO assumes that you already have a configured OpenWRT Buildroot or SDK

	cd openwrt/trunk
	./scripts/feeds update -a
	./scripts/feeds install -a
	cd feeds/packages
	patch -p1 < <path to patchfile>
	cd ../..
	./scripts/feeds update -i
	./scripts/feeds install <package name>
  
	make menuconfig
	// Select appropriate package

	make package/<package name>/compile V=s
	make package/<package name>/install V=s
	make package/index

