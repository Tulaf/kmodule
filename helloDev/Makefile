ifneq ($(KERNELRELEASE),)
obj-m := helloworld.o
else
	PWD := $(shell pwd)
KDIR:= /lib/modules/3.10.0-1127.el7.x86_64/build
#KDIR := /lib/modules/`uname -r`/build
all:
	make -C $(KDIR) M=$(PWD)
clean:
	rm -rf *.o *.ko *.mod.c *.symvers *.c~ *~
endif

