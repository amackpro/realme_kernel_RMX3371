KBUILD_OPTIONS += CONFIG_OPLUS_SECURE_COMMON=y
KBUILD_OPTIONS += OPLUS_OUT_OF_TREE_KO=y

ifeq ($(CHIPSET_COMPANY), QCOM)
KBUILD_OPTIONS += CONFIG_OPLUS_SECURE_QCOM=y
KBUILD_OPTIONS += CONFIG_QCOM_QSEELOG_ENCRYPT=y
else ifeq ($(CHIPSET_COMPANY), MTK)
KBUILD_OPTIONS += CONFIG_OPLUS_SECURE_MTK=y
endif

KERNEL_SRC ?= /lib/modules/$(shell uname -r)/build
M ?= $(shell pwd)
modules modules_install clean:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $(KBUILD_OPTIONS) $(@)
