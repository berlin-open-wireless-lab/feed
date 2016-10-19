#
# Copyright (C) 2014-2016 Alexander Couzens <lynxis@fe80.eu>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=wget-flasher
PKG_VERSION:=2016-10-19
PKG_RELEASE=$(PKG_SOURCE_VERSION)

PKG_MAINTAINER:=Alexander Couzens <lynxis@fe80.eu>

include $(INCLUDE_DIR)/package.mk

define Package/wget-flasher
  SECTION:=utils
  CATEGORY:=Base system
  TITLE:=wget-flasher
  DEPENDS:=+wget
endef

define Package/wget-flasher/description
 Download an image and flash it while device is in preinit.
endef

define Build/Compile
endef

define Package/wget-flasher/install
	$(INSTALL_DIR) $(1)/lib/preinit
	$(INSTALL_DATA) ./files/hook $(1)/lib/preinit/45_wget_openwrt_flasher
endef

$(eval $(call BuildPackage,wget-flasher))
