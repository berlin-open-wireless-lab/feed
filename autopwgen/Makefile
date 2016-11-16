#
# Copyright (C) 2014-2016 Alexander Couzens <lynxis@fe80.eu>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=autopwgen
PKG_VERSION:=2016-11-16
PKG_RELEASE=2

PKG_MAINTAINER:=Alexander Couzens <lynxis@fe80.eu>

include $(INCLUDE_DIR)/package.mk

define Package/autopwgen
  SECTION:=utils
  CATEGORY:=Base system
  TITLE:=autopwgen
  DEPENDS:=
endef

define Package/autopwgen/description
 Autogenerates a password if not set.
endef

define Build/Compile
endef

define Package/autopwgen/install
	$(INSTALL_DIR) $(1)/lib/preinit
	$(INSTALL_DATA) ./files/hook $(1)/lib/preinit/98_autopwgen
endef

$(eval $(call BuildPackage,autopwgen))
