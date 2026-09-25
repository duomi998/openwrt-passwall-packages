include $(TOPDIR)/rules.mk

PKG_NAME:=naiveproxy
PKG_VERSION:=154.0.8037.49
PKG_RELEASE:=2

ARCH_PREBUILT:=$(ARCH_PACKAGES)

# intel 80386 & riscv64 & cortex-a76
ifeq ($(ARCH_PREBUILT),aarch64_cortex-a76)
  ARCH_PREBUILT:=aarch64_generic
else ifeq ($(ARCH_PREBUILT),i386_pentium-mmx)
  ARCH_PREBUILT:=x86
else ifeq ($(ARCH_PREBUILT),i386_pentium4)
  ARCH_PREBUILT:=x86
else ifeq ($(ARCH_PREBUILT),mipsel_24kc_24kf)
  ARCH_PREBUILT:=mipsel_24kc
else ifeq ($(ARCH_PREBUILT),mipsel_74kc)
  ARCH_PREBUILT:=mipsel_24kc
else ifeq ($(ARCH_PREBUILT),riscv64_riscv64)
  ARCH_PREBUILT:=riscv64
endif

PKG_SOURCE:=naiveproxy-v$(PKG_VERSION)-$(PKG_RELEASE)-openwrt-$(ARCH_PREBUILT).tar.xz
PKG_SOURCE_URL:=https://github.com/klzgrad/naiveproxy/releases/download/v$(PKG_VERSION)-$(PKG_RELEASE)/

ifeq ($(ARCH_PREBUILT),aarch64_cortex-a53)
  PKG_HASH:=48d383edb5da670de89d500d4b7380e17977942f80db167860d7194717be3951
else ifeq ($(ARCH_PREBUILT),aarch64_cortex-a72)
  PKG_HASH:=f402da04a623aa67cde64ab86948bf5f91e0968ce12c007c575ebff94b9780e6
else ifeq ($(ARCH_PREBUILT),aarch64_generic)
  PKG_HASH:=0c071e7632d6df2031661ec92956fe303d31eae9f2f7343c78b74f632b45cab3
else ifeq ($(ARCH_PREBUILT),arm_arm1176jzf-s_vfp)
  PKG_HASH:=c38b1b218420a817d340f99a7c719415cdff2c6f6dc1ab0d28b7245c20db7336
else ifeq ($(ARCH_PREBUILT),arm_arm926ej-s)
  PKG_HASH:=2eb18eb5985963bcf138d1da2f6cad2c5d13744fd2716ad90b12873a56e498a2
else ifeq ($(ARCH_PREBUILT),arm_cortex-a15_neon-vfpv4)
  PKG_HASH:=5af572abd30320b99ab933df3e5208e8df3b6499daed33efbde3b2065a560853
else ifeq ($(ARCH_PREBUILT),arm_cortex-a5_vfpv4)
  PKG_HASH:=fae5b1218eaeeb39b59b16a933092e91b01225bbea472e88ff02773d332d79fc
else ifeq ($(ARCH_PREBUILT),arm_cortex-a7)
  PKG_HASH:=6ac9e3222de2cc079e3c6cd465d8922031e4970ff05c50d3726e8e08a2c80d75
else ifeq ($(ARCH_PREBUILT),arm_cortex-a7_neon-vfpv4)
  PKG_HASH:=d432aa1c7ea9cc8782d62d7812a733f3ac966f04c022f92487d64ebc2c625fe7
else ifeq ($(ARCH_PREBUILT),arm_cortex-a7_vfpv4)
  PKG_HASH:=9d6453f6693dc1f25483ae7004dc2cf15b8365afe2407dcfec8371957a2f84a6
else ifeq ($(ARCH_PREBUILT),arm_cortex-a8_vfpv3)
  PKG_HASH:=c6c6d7ae66af91b2398e32b0e839e71feade78a4175e8c97c56d5b06dd135506
else ifeq ($(ARCH_PREBUILT),arm_cortex-a9)
  PKG_HASH:=2aafcb1169336924ce22eef37fef72a2e3b0504c83effc5c18a030e2e79245f8
else ifeq ($(ARCH_PREBUILT),arm_cortex-a9_neon)
  PKG_HASH:=4f119877f9b9326b8648b3015f129ed27f0eab3c1bf14ad59f4bd34b41c1a7ab
else ifeq ($(ARCH_PREBUILT),arm_cortex-a9_vfpv3-d16)
  PKG_HASH:=d47b762719889870d0ecb1b700fd444b840757c34845bd9008031bcbe564dada
else ifeq ($(ARCH_PREBUILT),arm_mpcore)
  PKG_HASH:=04d609af80585520ecb96a512f203c375f2483b41256c5c220c6d687297619d1
else ifeq ($(ARCH_PREBUILT),arm_xscale)
  PKG_HASH:=b98fcc755b4e542965707cae3fd87fb01e5fded09c3279f54825d917f9f0c9e2
else ifeq ($(ARCH_PREBUILT),mipsel_24kc)
  PKG_HASH:=c7c3f3482818fea9d72598d17a03b065b9bd8bccfbe7c8226860a8ab68b12e22
else ifeq ($(ARCH_PREBUILT),mipsel_mips32)
  PKG_HASH:=733ef1bfb67b12111ff05df38c4ee0b14228589f48be5f1f967efe04cffd7ce2
else ifeq ($(ARCH_PREBUILT),riscv64)
  PKG_HASH:=3b9cea024b0d8c79927c463741845f1623be9544dd3b7767fc9d55b0d7c564f4
else ifeq ($(ARCH_PREBUILT),x86)
  PKG_HASH:=ae4e441cddf775c99ff1bd5b901c387f778e45a69774d826a797ba8f9abbbad8
else ifeq ($(ARCH_PREBUILT),x86_64)
  PKG_HASH:=5fce9437c84c2cec6322753c424c5f2f5621cc91d6aa3743650e6d7b54407a44
else
  PKG_HASH:=dummy
endif

PKG_LICENSE:=BSD 3-Clause
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=sbwml <admin@cooluc.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/naiveproxy-v$(PKG_VERSION)-$(PKG_RELEASE)-openwrt-$(ARCH_PACKAGES)

include $(INCLUDE_DIR)/package.mk

define Package/naiveproxy
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Web Servers/Proxies
  TITLE:=Make a fortune quietly
  URL:=https://github.com/klzgrad/naiveproxy
  DEPENDS:=@(aarch64||arm||i386||mipsel||riscv64||x86_64) +libatomic
endef

define Package/naiveproxy/description
  NaïveProxy uses Chrome's network stack to camouflage traffic with strong
  censorship resistance and low detectability. Reusing Chrome's stack also
  ensures best practices in performance and security.
endef

define Package/naiveproxy/conffiles
/etc/config/naiveproxy
endef

define Build/Prepare
	$(TAR) --strip-components=1 -C $(PKG_BUILD_DIR) -xJf $(DL_DIR)/naiveproxy-v$(PKG_VERSION)-$(PKG_RELEASE)-openwrt-$(ARCH_PREBUILT).tar.xz
endef

define Build/Compile
endef

define Package/naiveproxy/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/naive $(1)/usr/bin/naive
	$(INSTALL_DIR) $(1)/etc/config $(1)/etc/init.d
	$(INSTALL_CONF) $(CURDIR)/files/naiveproxy.config $(1)/etc/config/naiveproxy
	$(INSTALL_BIN) $(CURDIR)/files/naiveproxy.init $(1)/etc/init.d/naiveproxy
endef

$(eval $(call BuildPackage,naiveproxy))
