# Wahtari Adjustments

- `avt_build/jetson_build/files/bootloader/config` added Wahtari nCam Jetson configuration
- `hardware/nvidia/platform/t19x/jakku/kernel-dts/Makefile` added Wahtari nCam Jetson DTB files
- `hardware/nvidia/platform/t19x/jakku/kernel-dts/` added several Wahtari nCam DTSI files to directory
    - `tegra194-p3668-0000-p3509-0000-wahtari-ncam-jetson.dts` includes custom common wahtari dtsi files
    - `tegra194-p3668-0001-p3509-0000-wahtari-ncam-jetson.dts` includes custom common wahtari dtsi files
    - `common/tegra194-p3668-common-wahtari-ncam-jetson.dtsi`:
        - set usb2-0 to host-only mode
        - removed suspend_gpio & leds (GPIO04 TEGRA194_AON_GPIO(CC, 1))
        - removed SPI
    - `common/tegra194-p3509-0000-a00-wahtari-ncam-jetson.dtsi`:
        - removed display include
        - removed spi
        - removed pwm-fan & thermal-fan-est & tachometer