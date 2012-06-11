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

PKG_MD5SUM:=6593ab6a894d24b2109a2562b5406b3a
PKG_CAT:=zcat
PKG_SOURCE_VERSION:=$(PKG_VERSION)
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=http://dl.dropbox.com/u/424049
PKG_SOURCE:=extract-xiso_v2.7_src_110930_by_somski.tar.gz

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/extract-xiso
  SUBMENU:=compression
  SECTION:=utils
  CATEGORY:=Utilities
#  DEPENDS:=+libxml2 +libpar2 +libpthread
  URL:=https://github.com/plato79/extract-xiso
  TITLE:=extract-xiso X360 ISO extractor
endef

define Package/extract-iso/description
A command-line X360 ISO extractor.
endef

define Build/Compile
$(MAKE) -C $(PKG_BUILD_DIR) \
CC="$(TARGET_CROSS)gcc"
endef

define Package/extract-xiso/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/extract-xiso $(1)/usr/bin/
endef

$(eval $(call BuildPackage,extract-xiso))
