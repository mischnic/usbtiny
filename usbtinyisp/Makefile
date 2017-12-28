# ======================================================================
# Makefile for USBtinyISP AVR programmer
#
# Copyright 2006-2010 Dick Streefland
#
# This is free software, licensed under the terms of the GNU General
# Public License as published by the Free Software Foundation.
# ======================================================================

#
# To upload the firmware edit the avrdude arguments below and run:
# 	make fuses flash
#

USBTINY		= ../usbtiny
TARGET_ARCH	= -mmcu=attiny2313a
OBJECTS		= main.o
FLASH_CMD	= avrdude -c arduino -b 115200 -P /dev/tty.port -pt2313 -U flash:w:main.hex
FUSES_CMD	= avrdude -c arduino -b 115200 -P /dev/tty.port -pt2313 -U hfuse:w:0xdf:m -U lfuse:w:0xef:m
STACK		= 32
FLASH		= 2048
SRAM		= 128
SCHEM		= 

include $(USBTINY)/common.mk
