#
# Copyright (C) 2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=shairport
PKG_VERSION:=0.05
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git://github.com/skaman/shairport.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=fd50ed068cbf0ab275d2ff0f25ed73ebf793927f
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk


define Package/shairport/Default
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=ShairPort
  URL:=http://mafipulation.org/
endef


define Package/shairport
  $(Package/shairport/Default)
  DEPENDS:= +libopenssl +alsa-lib +libavahi-client +avahi-utils
endef

define Package/shairport/description
  ShairPort is server software that implements the RAOP protocol for
  playback of music streamed from a compatible remote client.
endef


define Package/shairport/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/{hairtunes,shairport} $(1)/usr/bin/
	$(INSTALL_BIN) ./files/airplay $(1)/etc/init.d/
endef


$(eval $(call BuildPackage,shairport))
