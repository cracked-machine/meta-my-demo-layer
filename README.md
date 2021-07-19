#### Summary

This is a Yocto layer for adding device tree files to the OpenSTLinux-5.10-dunfell-mp1-21-03-31 distribution build.

#### Instructions

1. Clone this into your layers/meta-st
2. Create a symlink to the root directory of your STM32CubeIDE project in the `mx` directory
3. Add the path to the device tree files and device tree file name (without extension) to the CUBEMX_PROJECT and CUBEMX_DTB variables - respectively - in conf/machine/<layer>.conf file. For example
  
```
CUBEMX_DTB = "stm32mp157f-mp157fab_custom-mx"
CUBEMX_PROJECT = "mx/mp157fab_custom/CA7/DeviceTree/mp157fab_custom"
```  
  
#### Example STM32CubeIDE projects

ST DevKit - STM32MP157F DK2:
  
- [STM32MP157F DK2](https://github.com/cracked-machine/fdk2_161)
  
  [Hardware design for the DK2 board](https://www.st.com/en/evaluation-tools/stm32mp157f-dk2.html)

Custom Board - STM32MP157xAB:
  
- [Custom STM32MP157FAB board](https://github.com/cracked-machine/mp157fab_custom)
- [Custom STM32MP157DAB board](https://github.com/cracked-machine/mp157dab_custom)

  [Hardware design for the custom board](https://github.com/cracked-machine/STM32MP1_TestBoard_RevB)
