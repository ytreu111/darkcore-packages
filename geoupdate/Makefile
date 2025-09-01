include $(TOPDIR)/rules.mk

PKG_NAME:=geoupdate
PKG_VERSION:=0.0.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/ytreu111/geoupdate/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=skip

PKG_BUILD_DIR:=$(BUILD_DIR)/geoupdate-$(PKG_VERSION)
PKG_BUILD_DEPENDS:=rust/host
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/package/feeds/packages/rust/rust-package.mk

define Package/geoupdate
	SECTION:=utils
	CATEGORY:=DarkCore
	TITLE:=Geosite and Geoip updater
	DEPENDS:=$(RUST_ARCH_DEPENDS) +wget
endef

define Package/geoupdate/description
	A utility to update Geosite and GeoIP databases.
endef

define Build/Compile
	$(call Build/Compile/Cargo)
endef

define Package/geoupdate/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/target/$(RUSTC_TARGET_ARCH)/release/geoupdate $(1)/usr/bin/
endef

$(eval $(call BuildPackage,geoupdate))
