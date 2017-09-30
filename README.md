## Welcome to Kyogi14's XMR Mining Guide

After spending a few weeks trying to get started with mining altcoins, I have found there are tons of resources out there, but most of the key information is scattered across the web and hard to find. Here I am attempting to establish a comprehensive guide and repository of tips and tracks for getting the most out of your mining hardware.

Please feel free to make Pull Requests or submit issues to improve this guide.

If you find this content valuable or if it has helped you squeeze a few extra hash per second out of your equipment, please consider donating.

### Donations: 
BTC: 15LfjG2pk7dUMswxx3P6kG7yf9i9y4Zg5N
Eth: 0xAae463b781464EDc60c5B9f2B651c5f0e105511f
XMR: 47ALHhbe8PUU3mT7Ek38drXmVuqQ7U2df59kR1VUaaB12Q7bow2MAE9jLYw7nLvzgVJKagKspsDu2KTB9URmhnBU3DWvWP8
LTC: LMC4ubwsfSfUFQZhqZDvmM6Fp7UPMnuj3s
# Mining Software
## XMR-STAK-AMD
## Claymore's Miner
## SG-Miner
# Mining Equipment
## GPUs
### AMD
#### RX Vega
The RX Vega (all versions) can hit 1800+ h/s on Windows 10 fairly reliably.  If you are not hitting this hashrate, please check the following.
- Using (Blockchain Drivers)
- Use (XMR-STAK-AMD) Miner - other miners are not yet fast enough or we have not found a sweet spot configuration for other miners yet.
- Use the following pool settings to use 2 thread per vega card with intensity 2016 and 1600 (can possibly go up to 1800).  Don't start mining until you enable HBCC below.
- Ensure you have at least 16GB or more of Virtual Memory configured in Windows.
- Use AMD Radeon Settings to enable HBCC (It appears as though you need at least 8GB of System RAM for 1 card and 16GB of RAM to enable this setting for 2 or more cards.) Unfortunately, HBCC is very unstable on the Blockchain driver.  You must re-enable it each time you boot your machine, and possibly ehenever you make any resolution change, turn monitor on/off, or sometimes whenever your mining software accesses your GPU in a way that trips it off(sometimes seen when closing mining software abruptly). Try enabling this in the Global Settings of AMD Settings and turn the slider all the way up. If AMD settings indicates it is already enabled, try turning the slider down and back up and then re-apply to truly enable. After applying changes to HBCC, AMD settings should dissappear and then come back within about 20-30 seconds.  When it returns, you should see your settings displayed if you navigate to the vega global settings for the card you just changed.  If you do not see any change, please reboot your machine and try again. This setting seems to become unresponsive if you have more than 4 AMD cards in the system.  Please remove extra cards and try again. The Pixel Patcher tool also seems to prevent HBCC from working properly if applied to the blockchain driver, even if you only apply the bios signature check option. 
- Tune Core Frequency down -30% in wattman
- Tune Memory Frequency to 920 or greater. 
  RX Vega 56 should use 920-950 using the highest value you can reach without your wattman settings automatically reverting during mining or hitting a blue screen. RX Vega 64 and Liquid can hold 1100.  Vega 56 with 64 Liquid Bios applied can also hold 1100 but there seems to be little if any improvement to hashrate.
- Set Fan Speed to 3000+ to keep memory cool.  Auto fan will only monitor core temperature, but memory must be kept below 70C to maintain good hash rates.
- Set Power Level Max to -20 if you can run stable at this value to reduce power consumption. 
- Be sure you have your windows power management settings set to keep your display on and not turn off after x minutes or you can use a dummy plug in your integrated graphics port or one of your gpus to maintain your hashrate without a powered on display connected. Otherwise, you can lose 250-300 h/s when the display turns off.  Simply powering the display back on and restarting xmr-stak-amd should return the hashrate to normal.  If it doesn't come back, your HBCC probably reset.  Try to restore HBCC settings by modifying the slider and setting it back to full.  If it still doesn't return, you will likely need to reboot.
#### RX 470
#### RX 580
### Nvidia
## Motherboards
## CPU's
## Storage
## RAM
## M.2 PCI Adapters
## Risers
## Frames and Enclosures
## Other
### Kill-a-watt
### Smartplugs
# Pools
### Dwarfpool
### MineXMR
### Nanopool
