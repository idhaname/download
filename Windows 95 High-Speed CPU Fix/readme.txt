Translate from Google translate.
使用Google翻译进行翻译。
After translate:
翻译后的文本：

-------------------------------------------------- ------------
Windows 95高速处理器支持v。3.0 by LoneCrusader
-------------------------------------------------- ------------

此套餐内容：
-------------------------

README.TXT-自我解释。

FIX95CPU.EXE-自解压可引导软盘映像。

FIX95CPU.IMA-可引导软盘的标准映像。
（对于虚拟机。）

FIX95CPU.ISO-标准可启动CD映像。
（对于虚拟机或没有软盘驱动器的系统。）

VMM2XUPD.EXE-带有Windows 95 B OSR2更新VMM.VXD的HotFix。
（安装完成后，在Windows 95 B OSR2中安装。）

-------------------------

笔记：

本自述文件的第一部分将解释所解决的问题
通过这个补丁。如果您熟悉这些问题，则可以跳至
第二部分提供了分步说明。


第一节：
------------

Windows 95在处理处理器时有两个特定的错误
速度高于350 MHz。有点耐心，
这两个错误都是可以修复的。


第一个错误发生在大于350 MHz的处理器上。
Microsoft发布了针对此错误的补丁AMDK6UPD.EXE。这
补丁不仅适用于AMD处理器。它将适用于英特尔
奔腾4处理器也是如此。微软补丁的问题
是必须从Windows内部运行。当您的系统
遇到此错误，您将无法启动Windows。
在系统重新启动期间，第一次重新启动时会显示此错误。
安装过程。

这是错误的文本：

      初始化设备IOS时：
      Windows保护错误。您需要重新启动计算机。

解决此错误的唯一方法是手动安装文件
包含在Microsoft AMDK6UPD.EXE修补程序中。该程序包自动执行
为您准备的过程，因此我将不对此做进一步详细介绍
在这里发行。


第二个错误发生在大于2.1 GHz的处理器上。
此问题还影响了Windows 98（第一版）和Microsoft
针对Windows 98发行了HotFix，但针对Windows 95发行了。
Microsoft，Windows 95中没有针对此问题的修复程序。错误！
此错误与上一个错误非常相似，并且也会
安装完成后，在安装过程的第一次重新启动时显示
修复了先前的错误。

这是错误的文本：

      初始化设备NDIS时：
      Windows保护错误。您需要重新启动计算机。

通过DUN14-95.EXE中包含的更新文件可以纠正此错误。
Windows 95的拨号网络1.4更新。此程序包自动执行
为您准备的过程，因此我将不对此做进一步详细介绍
在这里发行。


笔记：
此更新使AMDK6UPD.EXE补丁过时，
安装其中包含的某些系统文件的较新版本
AMDK6UPD.EXE。虽然此更新的主要目的是
为了启用高速处理器，我决定包括
已经有任何可用的较新版本的系统文件
包含在此补丁中。


此更新修复的问题列表（MSKB文章）：
-------------------------------------------------- --

Q192841-使用AMD K6-2或Athlon中央处理器的困难
Q234259-修订AMD K6-2 / 350中央处理器更新
Q312108-CPU速度超过2.1 GHz的NDIS中的Windows保护错误
Q231942-无法取消对具有LS-120可移动驱动器的笔记本计算机的对接
Q175629-大型IDE硬盘可能在兼容模式下运行
Q274175-在CD-ROM上打开/复制文件/文件夹八层错误
Q159153-备份到某些软盘驱动器时的错误消息


此更新还包括使用PTCHCDFS的CDFS.VXD的修补程序版本，
Rudolph Loew（rloew）的免费更新，以修复错误的大小值
Windows 9X针对DVD的报告（1.99GB）。

Windows 95 RTM / A中存在一个单独的错误，该错误导致DVD大小超过
4GB无法正确显示其字节数，显示“ ---”
相反，但仍会显示正确的DVD总大小。
为Windows 95 RTM / A安装其他更新程序包可能会产生
解决方案，但尚未经过测试。


此版本中还包括HotFix VMM2XUPD.EXE，它会安装
Windows 95 B OSR2的最新版本的VMM.VXD。这个包裹应该
Windows 95 B OSR2安装程序完成后，请进行安装。此更新将
不能在Windows 95 RTM / A上运行，并且在Windows 95 C OSR2.5上不是必需的。


积分和其他信息：
----------------------------

Rudolph Loew还创建了一个免费的UDF文件系统驱动程序以进行读取
在Windows 95中UDF格式的CD / DVD可以从他的网站获得。
在{http://rloew1.no-ip.com}或在{http://rloew.limewebs.com}镜像。

非常感谢Rudolph Loew为该项目提供的帮助！

同样值得赞扬的是MSFN的Petr，它为95 RTM提供了补丁文件。

最后，归功于MSFN的Queue来创建ANSI Windows徽标。

有关更多信息和更新，请在MSFN论坛上访问此主题：
http://www.msfn.org/board/index.php?showtopic=141402

该软件包利用了常规替换（GR）文本替换实用程序
由安德鲁·沙拉德（Andrew Sharrad）创建，可以在以下位置找到：
http://www.sharradsoftware.co.uk



第二节：
------------

请按照以下说明来启动和运行Windows 95。

你会需要：

空白软盘或空白CD
FIX95CPU.ZIP中包含的文件

笔记：
如果您的系统没有软盘驱动器，则FIX95CPU.ISO
可以使用此软件包中的可引导CD映像（与Nero或
类似的CD刻录程序）来创建可启动CD，
用于代替软盘。

笔记：
这些说明和FIX95CPU安装程序假定
您正在将Windows 95安装到C：\ Drive，但是您可以
使用除C：\ WINDOWS以外的目录。


 1.在另一台计算机上，使用自解压软盘映像
（FIX95CPU.EXE）或可启动CD映像（FIX95CPU.ISO）
FIX95CPU.ZIP中提供的以创建自定义启动磁盘
将包含此补丁。

 2.准备系统并运行Windows 95安装程序。

 3.当Windows 95要求您重新启动时，插入启动盘或
使用附带的映像创建的启动CD，然后单击
结束。您应该已插入启动盘或启动CD。
Windows安装程序继续之前，并显示IOS错误
为了通过结合.VXD来加快启动过程
WININIT.EXE，但是此版本允许安装
在显示IOS错误之后。

 4.引导盘将以DOS模式启动计算机。按空格键，然后
您将有机会查看此README文件。
选择Y或N，然后您需要做的就是再次按空格键
调出自述文件的下一页，或应用补丁。
该程序将其操作输出到屏幕，以便您可以看到
正在做什么。

任何时候按CTRL-C都会终止FIX95CPU程序。

 5.完成后，按空格键重新启动系统，然后卸下
启动盘或启动CD，以便Windows 95安装程序可以正常继续。


如果要安装Windows 95 RTM / A或C OSR2.5，则说明已完成。

仅对于Windows 95 B OSR2：


 6.安装程序完成并且Windows桌面加载后，运行
VMM2XUPD.EXE将VMM.VXD更新到最新版本，您
将提示您重新启动。

Windows 95 C OSR2.5上不需要此更新。

如果您有Windows 95 RTM / A或C OSR2.5，请跳过此步骤。
VMM2XUPD.EXE将不会安装在Windows 95 RTM / A上。

VMM2XUPD.EXE更新解决了以下问题：
Q179897-奔腾处理器的内存管理问题


您已成功完成所有步骤。

安装适用于您的硬件和程序的驱动程序。


玩得开心！


---------------------------------------

已知的问题：
-------------

 1.如果您打算将Microsoft USB Supplement安装到Windows
95 OSR2（USBSUPP.EXE），请注意，此更新有时会
覆盖文件C：\ WINDOWS \ SYSTEM \ VMM32 \ NTKERN.VXD不
提示您保留由此安装的更新文件
修补。如果发生这种情况，将显示以下错误：

初始化设备NTKERN时：
Windows保护错误。您需要重新启动计算机。

可以通过重新复制其中包含的NTKERN.VXD来更正此问题。
此补丁程序到您的系统。


---------------------------------------


法律信息：
-----------

此软件免费提供，绝对不提供任何担保
或保证。
使用此软件，即表示您同意以自己的风险使用它，并且
您自己的免费将。
本软件的作者不对任何事情负责
由于使用或滥用本软件而导致。
如果您修改此软件，请记住以记入原文
原始概念的作者。

---------------------------------------

    该软件由Conner McCoy（LoneCrusader）为您提供
                  鲁道夫·洛伊（rloew）的协助。

---------------------------------------

Before translate:
原文：

--------------------------------------------------------------
Windows 95 High-Speed Processor Support v. 3.0 By LoneCrusader
--------------------------------------------------------------

CONTENTS OF THIS PACKAGE:
-------------------------

README.TXT - Self Explanatory.

FIX95CPU.EXE - Self-Extracting Bootable Floppy Disk image.

FIX95CPU.IMA - A standard image of the Bootable Floppy.
	(For Virtual Machines.)

FIX95CPU.ISO - A standard Bootable CD image.
	(For Virtual Machines, or systems without a floppy drive.)

VMM2XUPD.EXE - HotFix with updated VMM.VXD's for Windows 95 B OSR2.
	(Install in Windows 95 B OSR2 after Setup has completed.)

-------------------------

NOTE:

The first section of this README will explain the issues addressed
by this patch. If you are familiar with these issues, you may skip to
the second section for step-by-step instructions.


SECTION ONE:
------------

Windows 95 has two specific errors when dealing with processors
with speeds higher than 350 MHz. With a little patience however,
both of these errors are fixable.


The first error occurs with processors greater than 350 MHz.
Microsoft released a patch for this error, AMDK6UPD.EXE. This
patch IS NOT just for AMD processors. It will work for Intel
Pentium 4 processors as well. The problem with Microsoft's patch
is that it must be run from within Windows. When your system
encounters this error, you will not be able to boot into Windows.
This error will be displayed on the first reboot during the
installation process.

Here is the text of the error:

      While initializing device IOS:
      Windows Protection Error.  You need to restart your computer.

The only way to fix this error is to manually install the files
contained in the Microsoft AMDK6UPD.EXE patch. This package automates
the process for you, so I will not go into further detail on that
issue here.


The second error occurs with processors greater than 2.1 GHz.
This problem also affected Windows 98 (First Edition), and Microsoft
issued a HotFix for Windows 98, but not for Windows 95. According to
Microsoft, there is no fix for this problem in Windows 95... WRONG!
This error is very similar to the previous one, and it will also be
displayed on the first reboot of the install process, after you have
fixed the previous error.

Here is the text of the error:

      While initializing device NDIS:
      Windows Protection Error.  You need to restart your computer.

This error is corrected by an updated file contained in the DUN14-95.EXE
Dial-Up Networking 1.4 Update for Windows 95. This package automates
the process for you, so I will not go into further detail on that
issue here.


NOTE:
	This update renders the AMDK6UPD.EXE patch OBSOLETE, as it
	installs newer versions of some system files contained within
	AMDK6UPD.EXE. While the main purpose of this update is to
	enable the use of High-Speed Processors, I decided to include
	any available newer versions of the system files already
	contained in this patch.


List of Issues (MSKB Articles) FIXED by this update:
----------------------------------------------------

Q192841 - Difficulties Using AMD K6-2 or Athlon Central Processing Unit
Q234259 - Revision to AMD K6-2/350 Central Processing Unit Update
Q312108 - Windows Protection Error in NDIS with CPU Faster Than 2.1 GHz
Q231942 - Cannot Undock Notebook Computer with LS-120 Removable Drive
Q175629 - Large IDE Hard Disk May Run In Compatibility Mode
Q274175 - Error Opening/Copying File/Folder Eight Levels Deep on CD-ROM
Q159153 - Error Messages While Backing Up to Some Floppy Disk Drives


This update also includes a patched version of CDFS.VXD using PTCHCDFS,
a free update by Rudolph Loew (rloew) to fix the incorrect size value
(1.99GB) reported by Windows 9X for DVD's.

A separate bug exists in Windows 95 RTM/A that causes DVD sizes over
4GB to not have their byte counts displayed properly, showing "---"
instead, but the correct total size of the DVD will still be displayed.
Installing other update packages for Windows 95 RTM/A may yield a
solution to this, but has not been tested.


Also included in this version is a HotFix, VMM2XUPD.EXE, which installs
the latest version of VMM.VXD for Windows 95 B OSR2. This package should
be installed when Windows 95 B OSR2 Setup has completed. This update will
not run on Windows 95 RTM/A and is not required on Windows 95 C OSR2.5.


Credits & Other Information:
----------------------------

Rudolph Loew has also created a free UDF filesystem driver for reading
UDF formatted CD's/DVD's in Windows 95. It can be obtained from his site
at {http://rloew1.no-ip.com} or mirror at {http://rloew.limewebs.com}.

Many thanks go out to Rudolph Loew for his assistance with this project!

Credit also goes to Petr at MSFN for providing patched files for 95 RTM.

And finally credit to Queue at MSFN for creating the ANSI Windows Logo.

For further information and updates, visit this topic at MSFN Forums:
http://www.msfn.org/board/index.php?showtopic=141402

This package makes use of the General Replace (GR) text replace utility
created by Andrew Sharrad, which can be found at:
http://www.sharradsoftware.co.uk



SECTION TWO:
------------

Follow these Instructions to get Windows 95 up and running.

You Will Need:

	Blank Floppy Disk or Blank CD
	Files Contained In FIX95CPU.ZIP

NOTE:
	If your system does not have a floppy drive, the FIX95CPU.ISO
	Bootable CD image in this package can be used (with Nero or
	a similar CD burning program) to create a bootable CD that can
	be used instead of a floppy.

NOTE:
	These instructions and the FIX95CPU installer assume that
	you are installing Windows 95 to C:\ Drive, however you can
	use a directory other than C:\WINDOWS.


 1. On another computer, use the self-extracting Floppy Disk image
	(FIX95CPU.EXE) or the Bootable CD image (FIX95CPU.ISO)
	provided in FIX95CPU.ZIP to create a custom Boot Disk
	that will contain this patch.

 2. Prepare your system and run Windows 95 Setup.

 3. When Windows 95 asks you to Restart, insert the Boot Disk or
	Boot CD that you created with the enclosed image, and click
	Finish. You should have the Boot Disk or Boot CD inserted
	BEFORE Windows Setup continues and the IOS error is displayed
	in order to speed up the boot process by combining .VXD's
	with WININIT.EXE, but this version allows for installation
	after the IOS error has been displayed.

 4. The Boot Disk will start your computer in DOS mode. Press SPACE and
	you will be given an opportunity to view this README file.
	Choose Y or N, and then all you need to do is press SPACE again
	to bring up the next page of the README, or to apply the patch.
	The program will output its actions to the screen so you can see
	what is being done.
	
	Pressing CTRL-C at any time will terminate the FIX95CPU program.

 5. When finished, press SPACE to reboot your system, then remove the
	Boot Disk or Boot CD so Windows 95 Setup can continue normally.


If you are installing Windows 95 RTM/A or C OSR2.5, you are finished.

For Windows 95 B OSR2 ONLY:


 6. When Setup is complete and your Windows Desktop loads, run
	VMM2XUPD.EXE to update VMM.VXD to the latest version, and you
	will be prompted to restart.

	This update is not necessary on Windows 95 C OSR2.5.

	If you have Windows 95 RTM/A or C OSR2.5, skip this step.
	The VMM2XUPD.EXE will not install on Windows 95 RTM/A.

	The VMM2XUPD.EXE update addresses the following issue:
	Q179897 - Memory Management Problems with Pentium Processors


You have successfully completed all steps.

Install the drivers for your hardware and your programs.


	Have Fun!


---------------------------------------

KNOWN ISSUES:
-------------

 1. If you plan to install the Microsoft USB Supplement to Windows
	95 OSR2 (USBSUPP.EXE), be aware that this update will sometimes
	overwrite the file C:\WINDOWS\SYSTEM\VMM32\NTKERN.VXD without
	prompting you to keep the newer file already installed by this
	patch. If this occurs, the following error will be displayed:

	While initializing device NTKERN:
	Windows Protection Error.  You need to restart your computer.

	This can be corrected by recopying the NTKERN.VXD contained in
	this patch to your system.


---------------------------------------


LEGAL INFO:
-----------

THIS SOFTWARE IS PROVIDED FREE OF CHARGE WITH ABSOLUTELY NO WARRANTIES
	OR GUARANTEES.
BY USING THIS SOFTWARE, YOU AGREE THAT YOU USE IT AT YOUR OWN RISK AND
	OF YOUR OWN FREE WILL.
THE AUTHOR(S) OF THIS SOFTWARE SHALL NOT BE HELD LIABLE FOR ANYTHING
	RESULTING FROM THE USE OR MISUSE OF THIS SOFTWARE.
IF YOU MODIFY THIS SOFTWARE, PLEASE REMEMBER TO CREDIT THE ORIGINAL
	AUTHOR(S) FOR THE ORIGINAL CONCEPT(S).

---------------------------------------

    This software brought to you by Conner McCoy (LoneCrusader) with
                  assistance from Rudolph Loew (rloew).

---------------------------------------
