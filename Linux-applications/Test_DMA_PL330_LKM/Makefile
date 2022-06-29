#
TARGET = test_DMA_PL330_LKM

#Compile with the toolchain from Angstrom 2013.12 compilation
CROSS_COMPILE := arm-linux-gnueabihf-
#Compile from SOC EDS toolchain (from Altera Embedded Command Shell )
#CROSS_COMPILE := arm-linux-gnueabihf-

CFLAGS = -g -Wall  -I ${SOCEDS_DEST_ROOT}/ip/altera/hps/altera_hps/hwlib/include
LDFLAGS =  -g -Wall
CC = $(CROSS_COMPILE)gcc
ARCH= arm

build: $(TARGET)

$(TARGET): test_DMA_PL330_LKM.o
	$(CC) $(LDFLAGS)   $^ -o $@

%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@

.PHONY: clean
clean:
	rm -f $(TARGET) *.a *.o *~
