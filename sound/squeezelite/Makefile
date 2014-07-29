include $(TOPDIR)/rules.mk

PKG_NAME:=squeezelite
PKG_VERSION:=1.6.3-git
PKG_RELEASE:=1

PKG_RELEASE:=$(PKG_SOURCE_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://code.google.com/p/squeezelite/
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=75a72d5f86e1675b5c5892ee5fb2278bbe8dc695


include $(INCLUDE_DIR)/package.mk

define Package/squeezelite
  SECTION:=sound
  CATEGORY:=Sound
  TITLE:=lightweight headless squeezebox emulator
  URL:=http://www.squeezelite/
  DEPENDS:= +AUDIO_SUPPORT:alsa-lib \
        +libvorbis +libflac \
        +libfaad2 +libffmpeg +libmad +libmpg123 +libpthread
endef

define Package/squeezelite/description
 lightweight headless squeezebox emulator
endef


define Package/squeezelite/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_BUILD_DIR)/squeezelite $(1)/usr/bin/
endef

$(eval $(call BuildPackage,squeezelite))
