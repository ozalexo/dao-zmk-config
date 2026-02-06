# ZMK Firmware for Dao keyboard

ZMK config repository for **Dao Choc BLE 44** keyboard. Uses the [zmk-keyboard-dao](https://github.com/ozalexo/zmk-keyboard-dao) module for board definitions.

## Branches

- **[dao44](https://github.com/ozalexo/dao-zmk-config/tree/dao44)** — stable branch for Dao44
- **[dao44-dev](https://github.com/ozalexo/dao-zmk-config/tree/dao44-dev)** — development branch for Dao44

## Build

Firmware is built for two boards: `dao_left` and `dao_right`. GitHub Actions build runs on push; get `firmware.zip` with `dao_left-zmk.uf2` and `dao_right-zmk.uf2` from the Actions tab.

## Default keymap

Dao44 layout is inspired by [Jian](https://github.com/KGOH/Jian-Info).

Visual representation in Keyboard Layout Editor: [KLE](http://www.keyboard-layout-editor.com/#/gists/c6ba0634e5b92366be9f324775394e66)

Keymap file: [config/boards/arm/dao/dao.keymap](config/boards/arm/dao/dao.keymap)

## FAQ

### How to change the keymap?

1. Fork this repository: https://github.com/ozalexo/dao-zmk-config
2. Edit [config/boards/arm/dao/dao.keymap](config/boards/arm/dao/dao.keymap) in your fork
3. Commit and push
4. Open the **Actions** tab and wait for the workflow to finish
5. Download **firmware.zip** — it contains `dao_left-zmk.uf2` and `dao_right-zmk.uf2`

### How to flash the keyboard?

1. Get **firmware.zip** (from Actions or a release)
2. Unzip — you should have `dao_left-zmk.uf2` and `dao_right-zmk.uf2`
3. Turn off the half you want to flash (power slider to **OFF**)
4. Connect that half to the PC via USB-C
5. Press **RESET** twice to enter DFU mode (a new USB drive should appear)
6. Copy the matching firmware file to the root of that drive
7. Disconnect; repeat steps 3–6 for the other half

### How to pair halves?

1. Turn off both halves (power slider to **OFF**)
2. Turn on both halves (power slider to **ON**)
3. Press **RESET** once on both halves **at the same time**

### Problems

#### File Transfer Error after copying firmware

This is normal. See [ZMK troubleshooting](https://zmk.dev/docs/troubleshooting#file-transfer-error).
