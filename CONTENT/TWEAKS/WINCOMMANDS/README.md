## Windows Commands

### Boot Configuration Data and its commands explained.
Boot Configuration Data (a.k.a bcdedit) is a command utility executable which allows you to edit boot parameters.

<details><summary>Findings and Analysis</summary>
In this section I will only explain the settings of `bcdedit /set` because they are the most important and can lead to a lower latency and higher performance, the values that I provide are the ones that you want to use if you are entirely focused on performances.

You can also take a look at the [Microsoft's bcdedit page](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/bcd-boot-options-reference).
<hr>

#### Boot settings
**bootlog**: no ; this parameter adds system initialization log in the %WINDIR% directory with a file named `Ntbtlog.txt`.

**bootmenupolicy**: Standard (default value) ; related to advanced options menu. [AVAILABLE SINCE / FROM WINDOWS 8]

**bootstatuspolicy**: IgnoreAllFailures ; this setting is only useful if you face some errors in your OS.

**quietboot**: on ; controls the display of the GUI boot.

**sos**: off ; controls the display of the names of the drivers as they are loaded during the boot process.

**lastknowngood**: off ; this setting lets your Windows to boot to the last known good configuration if it fails to boot but this can add bloated registry keys.

#### Display Settings
**bootuxdisabled**: on ; related to GUI boot.

**graphicsmodedisabled**: on ; related to GUI boot.

**novga**: on ; disables the use of VGA.

**vga**: off ; disables the use of VGA driver.

#### Verification Settings
**disableelamdrivers**: yes ; a security feature which analyzes drivers initialized at system startup for malicious code. [AVAILABLE SINCE / FROM WINDOWS 8]

**nx**: AlwaysOff ; a security feature containing a set of hardware and software technologies designed to prevent harmful code from running in protected memory locations.

#### Additional Settings
**disabledynamictick**: yes ; related to [HPET](https://en.wikipedia.org/wiki/High_Precision_Event_Timer). [AVAILABLE SINCE / FROM WINDOWS 8]

**tpmbootentropy**: ForceDisable ; a security feature which is designed to protect hardware through integrated cryptographic keys.

**tscsyncpolicy**: Enhanced ; I get better latency with it set as Enhanced. You might want to test Legacy. [AVAILABLE SINCE / FROM WINDOWS 8]

**useplatformclock**: no ; you may want to delete the value instead of setting it to no because it forces the clock to not be in use, related to [HPET](https://en.wikipedia.org/wiki/High_Precision_Event_Timer). 

**useplatformtick**: no ; this value can cause stutters if set to yes.

**x2apicpolicy**: enable ; this is better than legacy apic and can lead to better performances.
</details>
