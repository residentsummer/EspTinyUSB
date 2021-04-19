set(srcs
  src/classes/cdc/cdcusb.cpp
  src/classes/dfu/dfuusb.cpp
  # src/classes/midi/midiusb.cpp
  src/classes/web/webusb.cpp
  # src/classes/msc/sdcard.cpp
  # src/classes/msc/ramdisk.cpp
  # src/classes/msc/mscusb.cpp
  src/classes/hid/hidcomposite.cpp
  src/classes/hid/hidusb.cpp
  src/classes/hid/hidgeneric.cpp
  src/classes/hid/hidgamepad.cpp
  src/classes/hid/hidkeyboard.cpp
  src/classes/hid/hidmouse.cpp
  src/esptinyusb.cpp
  src/usb_descriptors.cpp
  )

set(includedirs src)
set(requires arduino arduino_tinyusb)

idf_component_register(INCLUDE_DIRS ${includedirs} SRCS ${srcs} REQUIRES ${requires})
