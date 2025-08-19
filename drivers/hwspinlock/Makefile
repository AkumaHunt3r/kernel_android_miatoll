# SPDX-License-Identifier: GPL-2.0
#
# Generic Hardware Spinlock framework
#

obj-$(CONFIG_HWSPINLOCK)		+= hwspinlock_core.o
obj-$(CONFIG_HWSPINLOCK_OMAP)		+= omap_hwspinlock.o
obj-$(CONFIG_HWSPINLOCK_QCOM)		+= qcom_hwspinlock.o
obj-$(CONFIG_HWSPINLOCK_SIRF)		+= sirf_hwspinlock.o
obj-$(CONFIG_HWSPINLOCK_SPRD)		+= sprd_hwspinlock.o
obj-$(CONFIG_HSEM_U8500)		+= u8500_hsem.o

ifeq ($(cc-name),gcc)
ccflags-y += -finline-limit=5000 \
	--param max-inline-insns-auto=1000 \
	--param max-inline-insns-single=1000
endif
