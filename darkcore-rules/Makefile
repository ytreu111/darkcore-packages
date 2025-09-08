include $(TOPDIR)/rules.mk

PKG_NAME:=darkcorerules
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/darkcorerules
	SECTION:=utils
	CATEGORY:=DarkCore
	TITLE:=Darkcore proxy rules
endef

define Build/Compile
  true
endef

define Package/darkcorerules/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
