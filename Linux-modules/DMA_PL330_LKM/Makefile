#Name of the module
obj-m := DMA_PL330.o
#Files composing the module
DMA_PL330-objs :=  DMA_PL330_LKM.o alt_dma.o alt_dma_program.o alt_address_space.o

#guest architecture
ARCH := arm

#compiler
CROSS_COMPILE := arm-linux-gnueabihf-

#path to the compiled kernel
ROOTDIR := /home/mkihr/mnt/Downloads/linux-socfpga

MAKEARCH := $(MAKE) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE)

all: modules
modules:
	$(MAKEARCH) -C $(ROOTDIR) M=${shell pwd} modules
clean:
	$(MAKEARCH) -C $(ROOTDIR) M=${shell pwd} clean
