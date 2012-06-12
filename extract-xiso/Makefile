#
# Copyright (C) 2009-2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=extract-xiso
PKG_VERSION:=2.7.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=$(PKG_VERSION)
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=git://github.com/plato79/extract-xiso.git
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/extract-xiso
  SUBMENU:=compression
  SECTION:=utils
  CATEGORY:=Utilities
  URL:=https://github.com/plato79/extract-xiso
  TITLE:=extract-xiso X360 ISO extractor
endef

define Package/extract-iso/description
A command-line X360 ISO extractor.
endef

define Build/Compile
CC="$(TARGET_CROSS)gcc"
$(MAKE) -C $(PKG_BUILD_DIR) \
endef

define Package/extract-xiso/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/extract-xiso $(1)/usr/bin/
endef

$(eval $(call BuildPackage,extract-xiso))
