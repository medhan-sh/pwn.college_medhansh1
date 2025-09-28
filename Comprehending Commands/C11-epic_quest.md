# Comprehending Commands 

### An epic file system Quest 

**Flag:** `pwn.college{ohtbblXNFljjw3uwVSzgmcxwMK2.QX5IDO0wiN2kjNzEzW}`

It was an epic quest indeed took me a few tries to get it right i was going astray by going through random directories with no relevance by few iterations of trial and error to get into the right directory. Read through the clues and picked visually odd options to clear through levels. 

```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
TEASER  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin     challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat TEASER
Lucky listing!
The next clue is in: /usr/share/icons/hicolor/scalable/places
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/icons/hicolor/scalable/places
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/hicolor/scalable/places$ ls
INFO
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/hicolor/scalable/places$ cat INFO 
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/arm/mach-omap1/include

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/hicolor/scalable/places$ ls /opt/linux/linux-5.4/arch/arm/mach-omap1/include
CLUE  mach
hacker@commands~an-epic-filesystem-quest:/usr/share/icons/hicolor/scalable/places$ cd /opt/linux/linux-5.4/arch/arm/mach-omap1/include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-omap1/include$ cat CLUE
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/platform/x86
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-omap1/include$ cd /opt/linux/linux-5.4/drivers/platform/x86
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ ls 
Kconfig             dell-rbtn.h            hp_accel.c               intel_oaktrail.c           pmc_atom.c
Makefile            dell-smbios-base.c     huawei-wmi.c             intel_pmc_core.c           pmc_atom.o
NUGGET              dell-smbios-smm.c      i2c-multi-instantiate.c  intel_pmc_core.h           samsung-laptop.c
acer-wireless.c     dell-smbios-wmi.c      ibm_rtl.c                intel_pmc_core_pltdrv.c    samsung-q10.c
acer-wmi.c          dell-smbios.h          ideapad-laptop.c         intel_pmc_ipc.c            sony-laptop.c
acerhdf.c           dell-smo8800.c         intel-hid.c              intel_punit_ipc.c          surface3-wmi.c
alienware-wmi.c     dell-wmi-aio.c         intel-rst.c              intel_scu_ipc.c            surface3_button.c
amilo-rfkill.c      dell-wmi-descriptor.c  intel-smartconnect.c     intel_scu_ipcutil.c        surfacepro3_button.c
apple-gmux.c        dell-wmi-descriptor.h  intel-vbtn.c             intel_speed_select_if      tc1100-wmi.c
asus-laptop.c       dell-wmi-led.c         intel-wmi-thunderbolt.c  intel_telemetry_core.c     thinkpad_acpi.c
asus-nb-wmi.c       dell-wmi.c             intel_atomisp2_pm.c      intel_telemetry_debugfs.c  topstar-laptop.c
asus-wireless.c     dell_rbu.c             intel_bxtwc_tmu.c        intel_telemetry_pltdrv.c   toshiba-wmi.c
asus-wmi.c          eeepc-laptop.c         intel_cht_int33fe.c      intel_turbo_max_3.c        toshiba_acpi.c
asus-wmi.h          eeepc-laptop.o         intel_chtdc_ti_pwrbtn.c  lg-laptop.c                toshiba_bluetooth.c
built-in.a          eeepc-wmi.c            intel_int0002_vgpio.c    mlx-platform.c             toshiba_haps.c
classmate-laptop.c  fujitsu-laptop.c       intel_ips.c              msi-laptop.c               touchscreen_dmi.c
compal-laptop.c     fujitsu-tablet.c       intel_ips.h              msi-wmi.c                  wmi-bmof.c
dcdbas.c            gpd-pocket-fan.c       intel_menlow.c           mxm-wmi.c                  wmi.c
dcdbas.h            hdaps.c                intel_mid_powerbtn.c     panasonic-laptop.c         xiaomi-wmi.c
dell-laptop.c       hp-wireless.c          intel_mid_thermal.c      pcengines-apuv2.c          xo1-rfkill.c
dell-rbtn.c         hp-wmi.c               intel_mrfld_pwrbtn.c     peaq-wmi.c                 xo15-ebook.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cat NUGGET
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/tools/pcmcia

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ ls /opt/linux/linux-5.4/tools/pcmcia
Makefile  REVELATION-TRAPPED  crc32hash.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cat /opt/linux/linux-5.4/tools/pcmcia/REVELATION-TRAPPED
Great sleuthing!
The next clue is in: /usr/share/perl/5.30.0/TAP/Parser/Scheduler

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ ls /usr/share/perl/5.30.0/TAP/Parser/Scheduler
Job.pm  Spinner.pm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ ls -a /usr/share/perl/5.30.0/TAP/Parser/Scheduler
.  ..  .POINTER  Job.pm  Spinner.pm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cat /usr/share/perl/5.30.0/TAP/Parser/Scheduler/.POINTER
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/gui-lib/hierlist

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ ls /usr/share/racket/pkgs/gui-lib/hierlist
DISPATCH-TRAPPED  compiled  hierlist.rkt
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cat /usr/share/racket/pkgs/gui-lib/hierlist/DISPATCH-TRAPPED

bash: s: command not found
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cat /usr/share/racket/pkgs/gui-lib/hierlist/DISPATCH-TRAPPED
Tubular find!
The next clue is in: /usr/lib/python3.8/concurrent/futures

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/platform/x86$ cd /usr/lib/python3.8/concurrent/futures
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/concurrent/futures$ ls
ALERT  __init__.py  __pycache__  _base.py  process.py  thread.py
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/concurrent/futures$ cat ALERT
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/sympy/vector/tests/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/concurrent/futures$ ls -a /usr/local/lib/python3.8/dist-packages/sympy/vector/tests/__pycache__
.                        test_coordsysrect.cpython-38.pyc     test_implicitregion.cpython-38.pyc    test_printing.cpython-38.pyc
..                       test_dyadic.cpython-38.pyc           test_integrals.cpython-38.pyc         test_vector.cpython-38.pyc
.README                  test_field_functions.cpython-38.pyc  test_operators.cpython-38.pyc
__init__.cpython-38.pyc  test_functions.cpython-38.pyc        test_parametricregion.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3.8/concurrent/futures$ cat /usr/local/lib/python3.8/dist-packages/sympy/vector/tests/__pycache__/.README
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{ohtbblXNFljjw3uwVSzgmcxwMK2.QX5IDO0wiN2kjNzEzW}
```

## What I learned

1. Using multiple commands depending upon the situation .
2. Adapting to the the clue the delayed, trapped, hidden clues required specific commands  to be accessed
3. Using absolute and relative paths systematically.
4. Moreover a clearer understanding of directories and accessing them. 

## References

NONE
