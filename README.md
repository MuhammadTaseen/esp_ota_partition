| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-C6 | ESP32-S2 | ESP32-S3 |
| ----------------- | ----- | -------- | -------- | -------- | -------- | -------- |


# Example Version 1.0.0

The main application is simple a upgraded version of native_ota_example. Basic theme of this application is to download chunk by chunk data via http a .bin file and start writing on partition.

1. Partition writing data example
2. Can upgrade the .bin of any partition in partition table 


TODO: Work continue in this its a initial version for testing purpose only

# Output

```sh

I (0) cpu_start: App cpu up.
I (330) cpu_start: Pro cpu start user code
I (330) cpu_start: cpu freq: 160000000 Hz
I (331) cpu_start: Application information:
I (333) cpu_start: Project name:     native_ota
I (339) cpu_start: App version:      1
I (343) cpu_start: Compile time:     Sep 11 2024 01:04:43
I (349) cpu_start: ELF file SHA256:  58311d05ee427f38...
I (355) cpu_start: ESP-IDF:          v5.1.2-dirty
I (360) cpu_start: Min chip rev:     v0.0
I (365) cpu_start: Max chip rev:     v0.99
I (370) cpu_start: Chip rev:         v0.1
I (375) heap_init: Initializing. RAM available for dynamic allocation:
I (382) heap_init: At 3FC9F5E8 len 0004A128 (296 KiB): DRAM
I (388) heap_init: At 3FCE9710 len 00005724 (21 KiB): STACK/DRAM
I (395) heap_init: At 3FCF0000 len 00008000 (32 KiB): DRAM
I (401) heap_init: At 600FE010 len 00001FD8 (7 KiB): RTCRAM
I (408) spi_flash: detected chip: gd
I (411) spi_flash: flash io: dio
I (416) sleep: Configure to isolate all GPIO pins in sleep state
I (422) sleep: Enable automatic switching of GPIO sleep configuration
I (430) app_start: Starting scheduler on CPU0
I (434) app_start: Starting scheduler on CPU1
I (434) main_task: Started on CPU0
I (444) main_task: Calling app_main()
I (444) native_ota_partition_example: OTA example app_main start
I (454) native_ota_partition_example: SHA-256 for the partition table: : 11507c59bc54cd4578950838ee33d7703630c4a5a7e05459d2c6235147ae2fb8
I (474) native_ota_partition_example: SHA-256 for bootloader: : f30c5bc81194fe9b789aeff1ab2d9ab4d457d8bbf2eae764e1159a29d2394989
I (554) native_ota_partition_example: SHA-256 for current firmware: : bb9cf21771f7e48c4d03b99d2b35fd185e3c87e3398b18f5785affcaa9c4837e
I (594) example_connect: Start example_connect.
I (594) pp: pp rom version: e7ae62f
I (594) net80211: net80211 rom version: e7ae62f
I (604) wifi:wifi driver task: 3fca9a34, prio:23, stack:6656, core=0
I (604) wifi:wifi firmware version: 91b9630
I (604) wifi:wifi certification version: v7.0
I (614) wifi:config NVS flash: enabled
I (614) wifi:config nano formating: disabled
I (614) wifi:Init data frame dynamic rx buffer num: 32
I (624) wifi:Init static rx mgmt buffer num: 5
I (624) wifi:Init management short buffer num: 32
I (634) wifi:Init dynamic tx buffer num: 32
I (634) wifi:Init static tx FG buffer num: 2
I (634) wifi:Init static rx buffer size: 1600
I (644) wifi:Init static rx buffer num: 10
I (644) wifi:Init dynamic rx buffer num: 32
I (654) wifi_init: rx ba win: 6
I (654) wifi_init: tcpip mbox: 32
I (654) wifi_init: udp mbox: 6
I (664) wifi_init: tcp mbox: 6
I (664) wifi_init: tcp tx win: 5744
I (674) wifi_init: tcp rx win: 5744
I (674) wifi_init: tcp mss: 1440
I (674) wifi_init: WiFi IRAM OP enabled
I (684) wifi_init: WiFi RX IRAM OP enabled
I (684) phy_init: phy_version 620,ec7ec30,Sep  5 2023,13:49:13
I (734) wifi:mode : sta (34:85:18:97:cc:d8)
I (734) wifi:enable tsf
I (734) example_connect: Connecting to taseen...
I (734) example_connect: Waiting for IP(s)
I (3144) wifi:new:<11,0>, old:<1,0>, ap:<255,255>, sta:<11,0>, prof:1
I (3624) wifi:state: init -> auth (b0)
I (3624) wifi:state: auth -> assoc (0)
I (3644) wifi:state: assoc -> run (10)
I (3674) wifi:connected with taseen, aid = 1, channel 11, BW20, bssid = 50:20:65:20:2a:6f
I (3674) wifi:security: WPA2-PSK, phy: bgn, rssi: -63
I (3674) wifi:pm start, type: 1

I (3674) wifi:set rx beacon pti, rx_bcn_pti: 0, bcn_timeout: 25000, mt_pti: 0, mt_time: 10000
I (3684) wifi:AP's beacon interval = 102400 us, DTIM period = 2
I (4684) esp_netif_handlers: example_netif_sta ip: 192.168.43.22, mask: 255.255.255.0, gw: 192.168.43.1
I (4684) example_connect: Got IPv4 event: Interface "example_netif_sta" address: 192.168.43.22
I (5594) example_connect: Got IPv6 event: Interface "example_netif_sta" address: fe80:0000:0000:0000:3685:18ff:fe97:ccd8, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (5594) example_common: Connected to example_netif_sta
I (5604) example_common: - IPv4 address: 192.168.43.22,
I (5604) example_common: - IPv6 address: fe80:0000:0000:0000:3685:18ff:fe97:ccd8, type: ESP_IP6_ADDR_IS_LINK_LOCAL
I (5614) wifi:Set ps type: 0, coexist: 0

I (5624) native_ota_partition_example: Starting OTA example task
I (5624) native_ota_partition_example: Running partition type 0 subtype 16 (offset 0x00030000)
I (5644) main_task: Returned from app_main()
I (6114) native_ota_partition_example: Writing to partition subtype 130 at offset 0x583000
I (6374) wifi:<ba-add>idx:0 (ifx:0, 50:20:65:20:2a:6f), tid:0, ssn:9, winSize:64
I (10994) native_ota_partition_example: esp_ota_begin succeeded
I (11004) native_ota_partition_example: Written image(partition.bin) length 1024
I (11004) native_ota_partition_example: Written image(partition.bin) length 2048
I (11014) native_ota_partition_example: Written image(partition.bin) length 3072
I (11034) native_ota_partition_example: Written image(partition.bin) length 4096
I (11034) native_ota_partition_example: Written image(partition.bin) length 5120
I (11044) native_ota_partition_example: Written image(partition.bin) length 6144
I (11214) native_ota_partition_example: Written image(partition.bin) length 7168
I (11224) native_ota_partition_example: Written image(partition.bin) length 8192
I (11234) native_ota_partition_example: Written image(partition.bin) length 9216
I (11244) native_ota_partition_example: Written image(partition.bin) length 10240


```

# Native OTA example

This example is based on `app_update` component's APIs.

## Configuration

Refer the README.md in the parent directory for the setup details.