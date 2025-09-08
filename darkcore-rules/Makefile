include $(TOPDIR)/rules.mk

PKG_NAME:=darkcore-rules
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/darkcore-rules
	SECTION:=net
	CATEGORY:=DarkCore
	TITLE:=Darkcore Rules
endef

define Build/Compile
  true
endef

define Package/darkcore-rules/install
	$(INSTALL_DIR) $(1)/etc/darkcorerules/
	$(INSTALL_BIN) ./files/nftables.rulesv46 $(1)/etc/darkcorerules/
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/darkcorerules $(1)/etc/init.d/darkcorerules
endef

$(eval $(call BuildPackage,darkcore-rules))