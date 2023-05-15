# My experience setting up a nook e-reader - fighting bitrot.

Terence Eden did the hard work of getting the nook simple touch to act as an information display and documented it in this [blog post](https://shkspr.mobi/blog/2020/02/turn-an-old-ereader-into-an-information-screen-nook-str/) .
However, since the time of writing there seems to have been some bit rot on barnes and nobles side such that some of the instructions don't work. This blog documents my experience. 

# Some irritations

I was hoping this would "just work". I picked the specific device that was described as working and linked through from pages. 

My main complaints are:

* Usb mini cables entering my life. This is acceptable since I am planning to leave the device plugged in an am not moving regularly.
* Unreliable cables. This means I have to buy multiple usb cables.

It might be easier to just "own everything" and a raspberrypi or similar but that requires a little hardware and would be of the order of 120 dollars rather than 30 dollars (though we shall see how many usb mini cables I have to buy)

## Hurdle: Device would not factory reset

The guide suggested factory resetting. When I tried this I got this error:

Device inform > Erase and Deregister Device > Erase and deregister device complained that 

```You are currently not connected to the network. Network connectivity is required to deregister this device```

despite being connected to the internet.

This issue is [described on this blog](https://joshuatz.com/posts/2022/nook-simple-touch-factory-reset-bypass-network-error/) and [on reddit](https://www.reddit.com/r/nook/comments/ex61b3/cant_setup_factory_reset_nook_simple_touch/) 

To do a reset I had to

1. Long press the power button and click the power off button in the popup
1. Long press the power button to switch on again
1. Immediately after the screen cleared, hold down both lower buttons on the side of the laptop (marked by raised lines of plastic on the surface)
1. Wait until a factory reset display came up
1. Press the n-shaped nook home button twice to reset the device
1. Wait for it to factory reset

After factory reset the same issue ocucred when registering the device. However, another post by [Terence Eden](https://shkspr.mobi/blog/2013/05/guide-to-using-the-nook-str-glow-without-a-bn-account-pictures/) describes how to skip the device registration process to get a working device. 

For protection against bit rot, I shall describe the process here.

1. Factory reset the device
1. Switch on the device
1. Select language
1. Hold the top right side button and swipe from left to right at the very top of the screen
1. A factory button will appear at the top level
1. Click this
1. Hold the top right button and click on the bottom right of the screen
1. A skip oboe button will appear
1. Press it and you are done

(In fairness, some of this is discussed in the blog above - or at least linked to)

## Hurdle firmware page discourages you from downloading firmware 
Downloading firmware. Some of the documentation muttered about automatic firmware downloads but you can still download the firmware [here](https://help.barnesandnoble.com/hc/en-us/articles/5583185727643-NOOK-Simple-Touch-Simple-Touch-with-GlowLight-Software-Updates under the manual download section)

I may well include the firmware here for posterity - though do you trust me to download firmware.

## Hurdle: Usb device not being detected
When I plugged in the nook it started charging, but I could not see the device from a mac. 

* This [blogpost](https://www.reddit.com/r/nook/comments/kj0lud/nook_first_edition_not_recognized_by_computer/) describes the issue suggested trying different cables.
* This [blogpost](https://www.reddit.com/r/nook/comments/o0x7w5/help_nook_doesnt_show_up_in_devices_but_still/) describes the issue and suggests using a different cable.
* This [blogpost](https://answers.microsoft.com/en-us/windows/forum/all/nook-simple-touch-not-detected-in-usb-port/f5340f3b-85a7-4970-90a5-3b09b9d1d9d2) also describes the issue. It reports success using old cables and an older windows machine.
* This [forum post](https://www.mobileread.com/forums/showthread.php?t=263852) discusses the issue for mac and describes pressing the power button the back several times fixing the issue.

I bought two more cables - neither device was detected on a mac. I wonder if it's the usb-c to usb-micro dongle.

## Hurdle: It is inclear precisely how to get the nook to detect the firmware
Also the first time I tried to copy the file, the nook device disappeared half way through, and then would no remount. I had to restart the nook to get this to work.

[This video](https://www.youtube.com/watch?v=xWaHlCxIpaw) describe "waiting a couple of minutes with an unpluged NOOK" until it falls asleep after unplugging it and reports that the firmware update takes around 5 minutes. I decided to go for a walk because I got bored of waiting.



