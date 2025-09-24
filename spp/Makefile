include $(TOPDIR)/rules.mk

PKG_NAME:=spp
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/EyitopeIO/spp.git
PKG_SOURCE_VERSION:=main

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Shell preprocessor
  DEPENDS:=+libstdcpp
endef

define Package/$(PKG_NAME)/description
  Like the C preprocessor but for shell files with dedicated syntax
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/spp $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
