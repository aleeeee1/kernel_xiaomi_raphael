ifeq ($(CONFIG_ARCH_TRINKET), y)
include $(srctree)/techpack/audio/config/trinketauto.conf
export $(shell sed 's/=.*//' $(srctree)/techpack/audio/config/trinketauto.conf)
endif

# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/audio/include/uapi \

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/audio/include/uapi \
                -I$(srctree)/techpack/audio/include

ifeq ($(CONFIG_ARCH_TRINKET), y)
LINUXINCLUDE    += \
                -include $(srctree)/techpack/audio/config/trinketautoconf.h
endif

obj-y += soc/
obj-y += dsp/
obj-y += ipc/
obj-y += asoc/
