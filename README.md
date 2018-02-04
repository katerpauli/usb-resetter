<p align='center'>
<img width='35%' src='https://usb-resetter.github.io/images/logo.png' />
</p>
<h3 align='center'>
USB resetting is the closest equivalent to physically unplugging and re-plugging a USB device. you might ask , How is that useful ? In my case, it helps with accessing my slightly damaged old USB external hard drive after a mount in unix-like OSes without any i/o issues. There most be more, that it can help with. So try it to know.
</h3>
<hr />
<p align='center'>
<img src='https://usb-resetter.github.io/images/template.png' width='70%' />
</p>

## Setup:
#### - From the source:
> `git clone https://github.com/mrf345/usb-resetter` <br />
> `cd usb-resetter` <br />
> `pip install -r requirements.txt` <br />
> `python run.py`

#### - With executable:
> - You can get an executable that's suitable to your OS from : <br />
> https://sourceforge.net/projects/usb-resetter/

## OS support:
#### - Windows:
> This tool is based on PyUsb, an open source python library that requires some extra USB drivers to allow us to interact with USB devices. One of those drives is libusb, there's an old but still working perfectly window version of it on : <br />
> https://sourceforge.net/projects/libusb-win32/files/libusb-win32-releases/1.2.6.0/libusb-win32-devel-filter-1.2.6.0.exe/download

#### - MacOS:
> Since MacOS is actually a unix-like OS, the bundled libusb driver seems to work perfectly. Only issue that might accrue here, is not knowing exactly which device you want to reset, due to the short descriptors and unintended vague categories. So you can make use of the command <mark> system_profiler SPUSBDataType</mark> in terminal to get the idvendor, idproduct. Which are used to identify the devices in usb-resetter.

#### - GNU/Linux:
> Has no issue in running the bundled libusb drive, and using <mark>lsusb</mark> command to get the exact idvendor and idproduct, in case you confused the device. Another thing, some might consider it an issue, is the need for <mark>sudo</mark> since interacting with USB devices requires a higher permissions.

<br />
<p align='center'>
<img src='https://usb-resetter.github.io/images/gui.gif' />
</p>
