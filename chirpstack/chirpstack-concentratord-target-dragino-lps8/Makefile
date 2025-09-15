include $(TOPDIR)/rules.mk

PKG_NAME:=chirpstack-concentratord-target-dragino-lps8
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/chirpstack-concentratord-target-dragino-lps8
	SECTION:=chirpstack
	CATEGORY:=ChirpStack
	TITLE:=ChirpStack Concentratord (Dragino LPS8)
	URL:=https://github.com/chirpstack/chirpstack-concentratord
	DEPENDS:=+chirpstack-concentratord-sx1301
endef

define Package/chirpstack-concentratord-target-dragino-lps8/description
	ChirpStack Concentratord (dragino-lps8)
endef

define Package/chirpstack-concentratord-target-dragino-lps8/conffiles
	/etc/config/chirpstack-concentratord
endef

define Package/chirpstack-concentratord-target-dragino-lps8/install
	$(INSTALL_DIR) $(1)/etc/config
	$(INSTALL_CONF) ./files/chirpstack-concentratord.config $(1)/etc/config/chirpstack-concentratord

	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/chirpstack-concentratord.init $(1)/etc/init.d/chirpstack-concentratord

	# Early spidev binder
	$(INSTALL_BIN) ./files/spidev-bind $(1)/etc/init.d/spidev-bind
endef

define Build/Compile
	# Nothing to do
endef

$(eval $(call BuildPackage,chirpstack-concentratord-target-dragino-lps8))


