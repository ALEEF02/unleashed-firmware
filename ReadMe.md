<h3 align="center">
<a href="https://github.com/DarkFlippers/unleashed-firmware">
<img src="https://user-images.githubusercontent.com/10697207/186202043-26947e28-b1cc-459a-8f20-ffcc7fc0c71c.png" align="center" alt="fzCUSTOM" border="0">
</a>
</h3>

### Welcome to the Flipper Zero Unleashed Firmware repo! 

#### **This firmware is a fork from** [flipperdevices/flipperzero-firmware](https://github.com/flipperdevices/flipperzero-firmware)

<br>

### Most stable custom firmware focused on new features and improvements of original firmware components, with almost no UI changes

<br>

##### This software is for experimental purposes only and is not meant for any illegal activity/purposes. <br> We do not condone illegal activity and strongly encourage keeping transmissions to legal/valid uses allowed by law. <br> Also, this software is made without any support from Flipper Devices and is in no way related to the official devs. 

<br>
Our Discord Community:
<br>
<a href="https://discord.unleashedflip.com"><img src="https://discordapp.com/api/guilds/937479784148115456/widget.png?style=banner4" alt="Unofficial Discord Community" target="_blank"></a>

<br>
<br>
<br>

## Dev builds (unstable)
- https://dev.unleashedflip.com/
- https://t.me/kotnehleb
## Releases in Telegram
- https://t.me/unleashed_fw

# What's changed
* Sub-GHz regional TX restrictions removed
* Sub-GHz frequency range can be extended in settings file (Warning: It can damage Flipper's hardware)
* Many rolling code protocols now have the ability to save & send captured signals
* FAAC SLH (Spa) & BFT Mitto (keeloq secure with seed) manual creation
* Sub-GHz static code brute-force plugin
* LFRFID Fuzzer plugin
* Custom community plugins and games added + all known working apps can be downloaded in extra pack in every release
* Extra Sub-GHz frequencies + extra Mifare Classic keys
* Picopass/iClass plugin included in releases
* Recompiled IR TV Universal Remote for ALL buttons
* Universal remote for Projectors, Fans, A/Cs and Audio(soundbars, etc.)
* Customizable Flipper name **Update! Now can be changed in Settings->Desktop** (by @xMasterX and @Willy-JL)
* Text Input UI element -> Cursor feature (by @Willy-JL)
- **BadBT** plugin (BT version of BadKB) [(by Willy-JL, ClaraCrazy, XFW contributors)](https://github.com/ClaraCrazy/Flipper-Xtreme/tree/dev/applications/main/bad_kb) - (See in Applications->Tools) - (aka BadUSB via Bluetooth)
- BadUSB -> Keyboard layouts [(by rien > dummy-decoy)](https://github.com/dummy-decoy/flipperzero-firmware/tree/dummy_decoy/bad_usb_keyboard_layout)
- Sub-GHz -> External CC1101 module support - [(by quen0n)](https://github.com/DarkFlippers/unleashed-firmware/pull/307)
- Sub-GHz -> `Add manually` menu extended with new protocols
- Sub-GHz -> New frequency analyzer - [(by ClusterM)](https://github.com/DarkFlippers/unleashed-firmware/pull/43)
- Sub-GHz -> Save last used frequency [(by derskythe)](https://github.com/DarkFlippers/unleashed-firmware/pull/77)
- Sub-GHz -> Press OK in frequency analyzer to use detected frequency in Read modes [(by derskythe)](https://github.com/DarkFlippers/unleashed-firmware/pull/77)
- Sub-GHz -> Long press OK button in Sub-GHz Frequency analyzer to switch to Read menu [(by derskythe)](https://github.com/DarkFlippers/unleashed-firmware/pull/79)
- Lock device with pin(or regular lock if pin not set) by holding UP button on main screen [(by an4tur0r)](https://github.com/DarkFlippers/unleashed-firmware/pull/107)
* Sub-GHz -> Short press OK in frequency analyzer to save detected frequency for usage in Read modes
* Sub-GHz -> Long press OK button in Sub-GHz Frequency analyzer to switch to Read menu and automatically use selected frequency
* SubGHz -> New option to use timestamps + protocol name when you saving file, instead of random name - Enable in `Radio Settings -> Time in names = ON`
* SubGHz Bruteforcer plugin -> Time delay (between signals) setting (hold Up in main screen(says Up to Save)) + configure repeats in protocols list by pressing right button on selected protocol
* SubGHz -> Read mode UI improvements (scrolling text, + shows time when signal was received) (by @wosk)
* Sub-GHz -> External CC1101 module support (Hardware SPI used)
* SubGHz -> **Hold right in received signal list to delete selected signal**
* SubGHz -> **Custom buttons for Keeloq / Alutech AT4N / Nice Flor S / Somfy Telis / Security+ 2.0 / CAME Atomo** - now you can use arrow buttons to send signal with different button code
* SubGHz -> BFT Mitto / Somfy Telis / Nice Flor S / CAME Atomo, etc.. manual creation with programming new remote into receiver (use button 0xF for BFT Mitto, 0x8 (Prog) on Somfy Telis)
* SubGHz -> Debug mode counter increase settings (+1 -> +5, +10, default: +1)
* SubGHz -> Debug PIN output settings for protocol development
* Infrared -> `RCA` Protocol
* Infrared -> Debug TX PIN output settings
* Other small fixes and changes throughout
* See other changes in readme below

Also check the changelog in releases for latest updates!

### Current modified and new Sub-GHz protocols list:
Thanks to Official team (to their SubGHz Developer, Skorp) for implementing decoders for these protocols in OFW.

Keeloq [Not ALL systems supported for decode or emulation yet!] - [Supported manufacturers list](https://0bin.net/paste/VwR2lNJY#WH9vnPgvcp7w6zVKucFCuNREKAcOij8KsJ6vqLfMn3b)

Encoders or sending made by @xMasterX:
- Nero Radio 57bit (+ 56bit encoder improvements)
- CAME 12bit/24bit encoder fixes (Fixes now merged in OFW)
- Keeloq: HCS101
- Keeloq: AN-Motors
- Keeloq: JCM Tech
- Keeloq: MHouse
- Keeloq: Nice Smilo
- Keeloq: DTM Neo
- Keeloq: FAAC RC,XT
- Keeloq: Mutancode
- Keeloq: Normstahl
- Keeloq: Beninca + Allmatic
- Keeloq: Stilmatic
- Keeloq: CAME Space
- Keeloq: Aprimatic (model TR and similar)
- Keeloq: Centurion Nova (thanks Carlos !)

Encoders or sending made by @Eng1n33r(first implementation in Q2 2022) & @xMasterX (current version):
- CAME Atomo -> Update! check out new [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)
- Nice Flor S -> How to create new remote - [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)
- FAAC SLH (Spa) [External seed calculation required (For info contact me in Discord: @mmx7)] 
- Keeloq: BFT Mitto -> Update! check out new [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)
- Star Line
- Security+ v1 & v2 (encoders was made in OFW)

Encoders made by @assasinfil & @xMasterX:
- Somfy Telis -> How to create new remote - [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)
- Somfy Keytis
- KingGates Stylo 4k
- Alutech AT-4N -> How to create new remote - [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)
- Nice ON2E (Nice One) -> How to create new remote - [instructions](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)

## Please support development of the project
The majority of this project is developed and maintained by me, @xMasterX.
I'm unemployed, and the only income I receive is from your donations.
Our team is small and the guys are working on this project as much as they can solely based on the enthusiasm they have for this project and the community.
- @gid9798 - SubGHz, Plugins, many other things
- @assasinfil - SubGHz protocols
- @Svaarich - UI design and animations
- @amec0e & @Leptopt1los - Infrared assets
- Community moderators in Telegram, Discord, and Reddit
- And of course our GitHub community. Your PRs are a very important part of this firmware and open-source development.

The amount of work done on this project is huge and we need your support, no matter how large or small. Even if you just say, "Thank you Unleashed firmware developers!" somewhere. Doing so will help us continue our work and will help drive us to make the firmware better every time.
Also, regarding our releases, every build has and always will be free and open-source. There will be no paywall releases or closed-source apps within the firmware. As long as I am working on this project it will never happen.
You can support us by using links or addresses below:
* **Boosty** (patreon alternative): https://boosty.to/mmxdev
* cloudtips (only RU payments accepted): https://pay.cloudtips.ru/p/7b3e9d65
* YooMoney (only RU payments accepted): https://yoomoney.ru/fundraise/XA49mgQLPA0.221209
* USDT(TRC20): `TSXcitMSnWXUFqiUfEXrTVpVewXy2cYhrs`
* BCH: `qquxfyzntuqufy2dx0hrfr4sndp0tucvky4sw8qyu3`
* ETH/BSC/ERC20-Tokens: `darkflippers.eth` (or `0xFebF1bBc8229418FF2408C07AF6Afa49152fEc6a`)
* BTC: `bc1q0np836jk9jwr4dd7p6qv66d04vamtqkxrecck9`
* DOGE: `D6R6gYgBn5LwTNmPyvAQR6bZ9EtGgFCpvv`
* LTC: `ltc1q3ex4ejkl0xpx3znwrmth4lyuadr5qgv8tmq8z9`
* XMR (Monero): `41xUz92suUu1u5Mu4qkrcs52gtfpu9rnZRdBpCJ244KRHf6xXSvVFevdf2cnjS7RAeYr5hn9MsEfxKoFDRSctFjG5fv1Mhn`
* TON: `EQCOqcnYkvzOZUV_9bPE_8oTbOrOF03MnF-VcJyjisTZmpGf`

### Community apps included:

#### See full list and sources here: https://github.com/xMasterX/all-the-plugins/tree/dev


# Instructions
## [- How to install firmware](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/HowToInstall.md)

## [- How to build firmware](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/HowToBuild.md)

## [- How to connect external CC1101 module](https://github.com/quen0n/flipperzero-ext-cc1101)

## [- BadUSB: how to add new keyboard layouts](https://github.com/dummy-decoy/flipperzero_badusb_kl)

## [- How to change Flipper name](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/CustomFlipperName.md)

## [- How to use Mifare Nested plugin to recover keys](https://github.com/AloneLiberty/FlipperNested#how-to-use-it)

## [- How to make captures to add them into Universal IR remotes](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/InfraredCaptures.md)

### **Sub-GHz**

## [- Transmission is blocked? - How to extend Sub-GHz frequency range](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/DangerousSettings.md)

## [- How to add extra Sub-GHz frequencies](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzSettings.md)

## [- How to use Flipper as new remote (Nice FlorS, BFT Mitto, Somfy Telis, Aprimatic, AN-Motors, etc..)](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemoteProg.md)

## [- Configure Sub-GHz Remote App](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SubGHzRemotePlugin.md)

### **Plugins**

## [- 🎲 Download Extra plugins for Unleashed](https://github.com/xMasterX/all-the-plugins)

## [- TOTP (Authenticator) config description](https://github.com/akopachov/flipper-zero_authenticator/blob/master/docs/conf-file_description.md)

## [- Barcode Generator](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/BarcodeGenerator.md)

## [- Multi Converter](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/MultiConverter.md)

## [- WAV Player sample files & how to convert](https://github.com/UberGuidoZ/Flipper/tree/main/Wav_Player#readme)

## [- Sub-GHz playlist generator script](https://github.com/darmiel/flipper-scripts/blob/main/playlist/playlist_creator_by_chunk.py)

### **Plugins that works with external hardware**

## [- How to use: Unitemp - Temperature sensors reader](https://github.com/quen0n/unitemp-flipperzero#readme)

## [- How to use: [NMEA] GPS](https://github.com/xMasterX/all-the-plugins/blob/dev/base_pack/gps_nmea_uart/README.md)

## [- How to use: i2c Tools](https://github.com/xMasterX/all-the-plugins/blob/dev/base_pack/flipper_i2ctools/README.md)

## [- How to use: [NRF24] plugins](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/NRF24.md)

## [- How to use: [WiFi] Scanner](https://github.com/SequoiaSan/FlipperZero-WiFi-Scanner_Module#readme)

## [- How to use: [ESP8266] Deauther](https://github.com/SequoiaSan/FlipperZero-Wifi-ESP8266-Deauther-Module#readme)

## [- How to use: [ESP32] WiFi Marauder](https://github.com/UberGuidoZ/Flipper/tree/main/Wifi_DevBoard)

## [- How to use: [ESP32-CAM] Camera Suite](https://github.com/CodyTolene/Flipper-Zero-Camera-Suite)

## [- [WiFi] Scanner - Web Flasher for module firmware](https://sequoiasan.github.io/FlipperZero-WiFi-Scanner_Module/)

## [- [ESP8266] Deauther - Web Flasher for module firmware](https://sequoiasan.github.io/FlipperZero-Wifi-ESP8266-Deauther-Module/)

## [- Windows: How to Upload .bin to ESP32/ESP8266](https://github.com/SequoiaSan/Guide-How-To-Upload-bin-to-ESP8266-ESP32)

## [- How to use: [GPIO] SentrySafe plugin](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/SentrySafe.md)

<br>
<br>

# Where I can find IR, Sub-GHz, ... files, DBs, and other stuff?
## [UberGuidoZ Playground - Large collection of files - Github](https://github.com/UberGuidoZ/Flipper)
## [Awesome Flipper Zero - Github](https://github.com/djsime1/awesome-flipperzero)

<br>
<br>

# Links

* Unofficial Discord: [discord.unleashedflip.com](https://discord.unleashedflip.com)
* Hello world - plugin tutorial (English): [https://github.com/DroomOne/Flipper-Plugin-Tutorial](https://github.com/DroomOne/Flipper-Plugin-Tutorial)
* Hello world - plugin tutorial (in Russian): [https://yakovlev.me/hello-flipper-zero/](https://yakovlev.me/hello-flipper-zero/)
* CLion IDE - How to setup workspace for flipper firmware development: [https://krasovs.ky/2022/11/01/flipper-zero-clion.html](https://krasovs.ky/2022/11/01/flipper-zero-clion.html)
* Docs by atmanos / How to write your own app (outdated API): [https://flipper.atmanos.com/docs/overview/intro](https://flipper.atmanos.com/docs/overview/intro)

* Official Docs: [http://docs.flipperzero.one](http://docs.flipperzero.one)
* Official Forum: [forum.flipperzero.one](https://forum.flipperzero.one/)

# Project structure

- `applications`    - Applications and services used in firmware
- `assets`          - Assets used by applications and services
- `furi`            - Furi Core: OS-level primitives and helpers
- `debug`           - Debug tool: GDB-plugins, SVD-file and etc
- `documentation`   - Documentation generation system configs and input files
- `firmware`        - Firmware source code
- `lib`             - Our and 3rd party libraries, drivers and etc...
- `site_scons`      - Build helpers
- `scripts`         - Supplementary scripts and python libraries home

Also, pay attention to the `ReadMe.md` files inside those directories.
