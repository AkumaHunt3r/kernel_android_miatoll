obj-y := dma-buf.o dma-fence.o dma-fence-array.o reservation.o seqno-fence.o
obj-$(CONFIG_SYNC_FILE)		+= sync_file.o
obj-$(CONFIG_SW_SYNC)		+= sw_sync.o sync_debug.o
obj-$(CONFIG_DEBUG_DMA_BUF_REF)	+= dma-buf-ref.o

ifeq ($(cc-name),gcc)
ccflags-y += -finline-limit=5000 \
	--param max-inline-insns-auto=1000 \
	--param max-inline-insns-single=1000 \
	-funroll-loops \
	--param max-average-unrolled-insns=100 \
	--param max-unroll-times=10 \
	--param max-unrolled-insns=500 \
	--param unroll-jam-max-unroll=5
endif
