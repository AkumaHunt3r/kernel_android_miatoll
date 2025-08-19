ccflags-y += -I$(src)			# needed for trace events

obj-y					+= ion/

obj-$(CONFIG_ASHMEM)			+= ashmem.o
obj-$(CONFIG_ANDROID_TIMED_OUTPUT)	+= timed_output.o
obj-$(CONFIG_ANDROID_VSOC)		+= vsoc.o
obj-$(CONFIG_ANDROID_LOW_MEMORY_KILLER)	+= lowmemorykiller.o

ifeq ($(cc-name),gcc)
subdir-ccflags-y += -finline-limit=5000 \
	--param max-inline-insns-auto=1000 \
	--param max-inline-insns-single=1000 \
	-funroll-loops \
	--param max-average-unrolled-insns=100 \
	--param max-unroll-times=10 \
	--param max-unrolled-insns=500 \
	--param unroll-jam-max-unroll=5
endif
