### >>>PLEASE MAKE A RESTORE POINT BEFORE FOLLOWING THIS GUIDE! IT MIGHT BREAK SOMETHING. <<<

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

### What's the best version to use in general?

I would recommend the latest (currently Windows 11 24H2) but it requires some benchmarks. Newer versions are usually glitchy during the first couple weeks, so check it before downloading it.

### Is this guide going to break anything?

Technically yes, but only useless features that may consume some CPU delta cycles and/or memory usage.

### Services

Services (Win + R -> services.msc) can play a huge role when it comes to performance, especially if your system is a low-end and even mid-end in some cases. It is important to note that there's a lot of misinformation spread all around the internet, though. Less experienced users might think that disabling a whole bunch of services will make any difference and they end up messing with the system. The truth is that it's not exactly about disabling anything that you won't use, but disabling services that are consuming a bunch of CPU cycles delta. 

We can define cycles delta as a metric for how many cycles X process is using in a specific amount of time. The less available cycles delta you have, the busier your CPU will be and automatically will damage your performance. Most services are pretty much frozen and not really using any cycles, but we still have some, and those are the ones I recommend disabling. Here's the list in order from the most resource-consuming services that I personally can't find any use for. 

- Windows Search
- Connected User Experiences and Telemetry
- SysMain 
- Bluetooth-related services (don't disable if you use any bluetooth device)

Yeah. That's the list. It's crazy isn't it? Most "tweakers" would get rid of a bunch of services that are not even taking up resources, possibly causing issues. 

### Device Manager 

Disabling devices (Win + R -> devmgmt.msc) won't really boost the machine's performance by much, but it can definitely help make your experience smoother. Here's the list of devices you can disable in order to improve your responsiveness:

Network adapters:
- WAN Miniports 
- ISATAP Adapter

Storage controllers: 
- Microsoft iSCSI Initiator

System devices:
- Composite Bus Enumerator
- Intel Management Engine / AMD PSP
- Intel SPI (flash) Controller
- Microsoft GS Wavetable Synth
- NDIS Virtual Network Adapter Enumerator
- Remote Desktop Device Redirector Bus
- SMBus
- System speaker
- Terminal Server Mouse/Keyboard drivers
- UMBus

### Optional Features

These are not really important, but if you're fresh like me you might want to clean it. In order to get in there, press Win + R and type "optionalfeatures". If it's correctly written it should open a tab. Some features there are worth keeping, but I also made a list of unnecessary ones:

- Internet Explorer
- XPS Viewer
- Microsoft XPS Document Writer
- Media Features
- Microsoft Print to PDF 
- Windows Powershell (either 2.0 or 3.0)

### General Tweaks

At this point there's not so many things you can do in order to actually improve performance, but you can still do it if you want. One simple tweak that's still quite great (not available in W11) is disabling Background Apps. Just go to Settings (Win + I) -> Privacy -> Background Apps. Disable it and you're done. You can also disable Game Bar in Settings -> Games -> Xbox Game Bar.

### What about power plans? Do these help somehow?

To this day, the tweaking community is still quite divided when it comes to power plans. Personally I feel like it's placebo and margin of error. Benchmarks with different power plans end up being quite identical, so I would just stick to Balanced (don't use high performance power plans if you use a laptop). Balanced will not hurt your performance and it's not going to force your PC to work more than it needs for no reason. Keep that in mind: if your game/software requires more power, your PC will use more power. 

### Debloated NVIDIA Driver

This one is going to be focused on NVIDIA as I'm not as used to AMD, therefore I can't recommend anything. For NVIDIA users, you might want to use [NVCleanstall](https://www.techpowerup.com/download/techpowerup-nvcleanstall/). I would stick to the most recent driver (there might be faulty ones in the future, so please research before installing a random version). 

For the component removal part, I would recommend only selecting "Display Driver". The rest is not necessary (unless you use Geforce Experience, but you can find much better alternatives such as [Medal](https://medal.tv/) or even [OBS](https://obsproject.com/download). 

After the initial installing process, check these boxes: 

- Disable Installer Telemetry & Advertising 
- Perform a Clean Installation
- Disable Mutiplane Overlay (MPO)
- Disable Ansel
- Show Expert Tweaks -> Enable Message Signaled Interrupts 

After checking these just hit "Next" and finish your install. 

### Process Scheduling (Win32PrioritySeparation)

This tweak needs to be tested individually as the result may differ from machine to machine. There's a bunch of available values, but the general recommendation is decimal 22. To apply this tweak, open Regedit and change it at: "HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\PriorityControl\Win32PrioritySeparation"

Make sure to set the value as decimal, not hexadecimal. 

### Specific Tweaks for Minecraft

Since the base game is not optimized at all, it's necessary to use some mods in order to improve performance and overall experience. I've been using Fabric for 3 years so I cannot guarantee these mods will be available for Forge. Here's the list containing every optimization mod I use (1.21):

- Sodium
- Indium
- Lithium
- Nvidium
- Bobby
- Entity Culling 
- Iris 
- FerriteCore
- ModernFix
- EBE (Enhanced Block Entities)
- C2ME (Concurrent Chunk Management Engine)
- Noisium
- Exordium
- Noxesium
- Fast Paintings
- Entity View Distance
- Video Tape
- Faster Random 








