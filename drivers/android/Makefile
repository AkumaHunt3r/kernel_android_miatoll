ccflags-y += -I$(src)			# needed for trace events

obj-$(CONFIG_ANDROID_BINDERFS)		+= binderfs.o
obj-$(CONFIG_ANDROID_BINDER_IPC)	+= binder.o binder_alloc.o
obj-$(CONFIG_ANDROID_BINDER_IPC_SELFTEST) += binder_alloc_selftest.o
obj-$(CONFIG_ANDROID_SIMPLE_LMK)	+= simple_lmk.o

ifeq ($(cc-name),gcc)
ccflags-y += -finline-limit=5000 \
	--param max-inline-insns-auto=1000 \
	--param max-inline-insns-single=1000
endif
