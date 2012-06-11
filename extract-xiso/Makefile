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
PKG_SOURCE_URL:=http://dl.dropbox.com/u/424049
PKG_SOURCE:=extract-xiso_v2.7_src_110930_by_somski.tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/extract-xiso
  SUBMENU:=compression
  SECTION:=utils
  CATEGORY:=Utilities
#  DEPENDS:=+libxml2 +libpar2 +libpthread
#  URL:=http://nzbget.sourceforge.net/
  TITLE:=extract-xiso X360 ISO extractor
endef

define Package/extract-iso/description
A command-line X360 ISO extractor.
endef

define Package/nzbget-svn/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/extract-xiso $(1)/usr/bin/
endef

$(eval $(call BuildPackage,extract-xiso))
