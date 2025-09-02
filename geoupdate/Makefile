include $(TOPDIR)/rules.mk

PKG_NAME:=geoupdate
PKG_VERSION:=0.0.5
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/ytreu111/geoupdate/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=skip

PKG_BUILD_DIR:=$(BUILD_DIR)/geoupdate-$(PKG_VERSION)
PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_BUILD_FLAGS:=no-mips16

GO_PKG:=github.com/ytreu111/geoupdate
GO_PKG_BUILD_PKG:=github.com/ytreu111/geoupdate/main

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/golang/golang-package.mk

define Package/geoupdate
	SECTION:=utils
	CATEGORY:=DarkCore
	TITLE:=Geosite and Geoip updater
	DEPENDS:=$(GO_ARCH_DEPENDS)
endef

define Package/geoupdate/install
	$(call GoPackage/Package/Install/Bin,$(PKG_INSTALL_DIR))
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/main $(1)/usr/bin/geoupdate
endef

$(eval $(call GoBinPackage,$(PKG_NAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
