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

define Package/darkcorerules/install
	$(INSTALL_DIR) $(1)/etc/darkcorerules/
	$(INSTALL_BIN) $(CURDIR)/files/nftables.rulesv46 $(1)/etc/darkcorerules/

	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_BIN) $(CURDIR)/files/darkcorerules $(1)/etc/init.d/darkcorerules
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
