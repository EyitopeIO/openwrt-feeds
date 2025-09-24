include $(TOPDIR)/rules.mk

PKG_NAME:=bizzare
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/EyitopeIO/Bizzare.git
PKG_SOURCE_VERSION:=main

PKG_MAINTAINER:=Eyitope Adelowo
PKG_LICENSE:=MIT

include $(INCLUDE_DIR)/uclibc++.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/bizzare
  SECTION:=net
  CATEGORY:=Network
  TITLE:=bizzare
  DEPENDS:=+libnetfilter-conntrack $(CXX_DEPENDS) +libsqlite3
  SUBMENU:=Firewall
endef


define Package/bizzare/description
  Predict device network usage
endef

define Package/bizzare/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bizzare $(1)/usr/bin
endef

$(eval $(call BuildPackage,bizzare))
