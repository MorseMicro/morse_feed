#
# Copyright 2023 Morse Micro
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk


PKG_NAME:=persistent-vars-storage-bcm2711
PKG_RELEASE=1

PKG_MAINTAINER:=Morse Micro

include $(INCLUDE_DIR)/package.mk

define Package/persistent-vars-storage-bcm2711
	SECTION:=Utilities
	CATEGORY:=Utilities
	PROVIDES:=persistent-vars-storage
	TITLE:=Reads (or maybe writes in future) key-value pairs from(/into) the RPi 4 EEPROM memory
	DEPENDS:= +bcm27xx-userland @TARGET_bcm27xx_bcm2711
endef

define Build/Compile

endef

define Package/persistent-vars-storage-bcm2711/install
	$(INSTALL_DIR) $(1)/sbin
	$(INSTALL_BIN) ./files/sbin/persistent_vars_storage.sh $(1)/sbin/persistent_vars_storage.sh
endef

$(eval $(call BuildPackage,persistent-vars-storage-bcm2711))
