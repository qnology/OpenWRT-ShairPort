include $(TOPDIR)/rules.mk

PKG_NAME:=squeezelite
PKG_VERSION:=1.6.3-git
PKG_RELEASE:=1

PKG_RELEASE:=$(PKG_SOURCE_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://code.google.com/p/squeezelite/
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=HEAD


include $(INCLUDE_DIR)/package.mk

define Package/squeezelite/Default
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=squeezelite
  URL:=https://code.google.com/p/squeezelite/
endef


define Package/squeezelite
  $(Package/squeezelite/Default)
  DEPENDS:= +libvorbis +libflac +libfaad2 +libffmpeg +libmad +libpthread
endef


define Package/squeezelite/description
 lightweight headless squeezebox emulator
endef


define Package/squeezelite/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_BUILD_DIR)/squeezelite $(1)/usr/bin/
endef

$(eval $(call BuildPackage,squeezelite))
