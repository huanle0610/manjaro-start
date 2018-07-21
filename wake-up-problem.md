# log


```bash
# export LANG=en_US.UTF-8
# journalctl --list-boots
-11 c41c67ac4e7e41a79629e04e68874308 Sun 2018-06-24 12:31:17 CST—Sun 2018-06-24 13:24:31 CST
-10 da6db0e453cf4b6fbebdbae5eae57f17 Sun 2018-06-24 13:24:51 CST—Fri 2018-07-06 21:34:51 CST
 -9 c94c1bf44e004a93b657173e81cb947f Fri 2018-07-06 21:35:26 CST—Fri 2018-07-06 21:35:58 CST
 -8 c7a47d3200e948d8b0009b91474e0312 Fri 2018-07-06 21:36:32 CST—Fri 2018-07-06 22:22:44 CST
 -7 11fc5ecd4aa349b3b808fbef0ec7482f Fri 2018-07-06 22:23:02 CST—Mon 2018-07-09 22:13:54 CST
 -6 87eb23ba76e94d67871136a6705219ef Mon 2018-07-09 22:14:14 CST—Sun 2018-07-15 16:35:56 CST
 -5 5d64b62eee2c476ea5f8de3de6207689 Sun 2018-07-15 16:36:08 CST—Sun 2018-07-15 22:27:29 CST
 -4 0ab7a8eda5e34b1782f249d0dfe22910 Thu 2018-07-19 05:53:11 CST—Thu 2018-07-19 07:02:32 CST
 -3 5327bac2745e4dd686cb95004697d4d4 Thu 2018-07-19 21:11:16 CST—Fri 2018-07-20 01:13:07 CST
 -2 21f64db8c8784b5e9d3c32e235420f30 Fri 2018-07-20 07:54:42 CST—Sat 2018-07-21 13:23:52 CST
 -1 34ec6b6b2099403592703c8c268e9bad Sat 2018-07-21 15:08:24 CST—Sat 2018-07-21 15:18:47 CST
  0 903a24d8acf949babb0209b025309acb Sat 2018-07-21 15:20:47 CST—Sat 2018-07-21 16:00:14 CST
```

```bash
[amtf@amtf-s3 ~]$ journalctl --boot=-1 | tail -n15 | cut -d' ' -f1-
7月 21 15:18:46 amtf-s3 ksmserver[1475]: CreateNotify: 2097188
7月 21 15:18:46 amtf-s3 ksmserver[1475]: MapNotify: 18874375
7月 21 15:18:46 amtf-s3 systemd[1]: Starting TLP suspend/resume...
7月 21 15:18:46 amtf-s3 ksmserver[1475]: CreateNotify: 2097195
7月 21 15:18:46 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:46 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:47 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:47 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:47 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:47 amtf-s3 plasmashell[1686]: QXcbClipboard: SelectionRequest too old
7月 21 15:18:47 amtf-s3 systemd[1]: Started TLP suspend/resume.
7月 21 15:18:47 amtf-s3 systemd[1]: Reached target Sleep.
7月 21 15:18:47 amtf-s3 systemd[1]: Starting Suspend...
7月 21 15:18:47 amtf-s3 systemd-sleep[10751]: Suspending system...
7月 21 15:18:47 amtf-s3 kernel: PM: suspend entry (deep)
```

```bash
[amtf@amtf-s3 ~]$ journalctl --boot=0 | head -n15 | cut -d' ' -f1-
-- Logs begin at Sun 2018-06-24 12:31:17 CST, end at Sat 2018-07-21 15:36:32 CST. --
7月 21 15:20:47 amtf-s3 kernel: microcode: microcode updated early to revision 0x1f, date = 2018-02-07
7月 21 15:20:47 amtf-s3 kernel: Linux version 4.18.0-1-MANJARO (builduser@development) (gcc version 8.1.1 20180531 (GCC)) #1 SMP PREEMPT Fri Jul 6 19:55:18 UTC 2018
7月 21 15:20:47 amtf-s3 kernel: Command line: BOOT_IMAGE=/boot/vmlinuz-4.18-x86_64 root=UUID=c3b63e0b-6bd6-4bc9-9fd4-1605ab444f2c rw quiet resume=UUID=a2ec2f85-9b43-46e6-a356-e6df9acf102d
7月 21 15:20:47 amtf-s3 kernel: KERNEL supported cpus:
7月 21 15:20:47 amtf-s3 kernel:   Intel GenuineIntel
7月 21 15:20:47 amtf-s3 kernel:   AMD AuthenticAMD
7月 21 15:20:47 amtf-s3 kernel:   Centaur CentaurHauls
7月 21 15:20:47 amtf-s3 kernel: x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'
7月 21 15:20:47 amtf-s3 kernel: x86/fpu: Supporting XSAVE feature 0x002: 'SSE registers'
7月 21 15:20:47 amtf-s3 kernel: x86/fpu: Supporting XSAVE feature 0x004: 'AVX registers'
7月 21 15:20:47 amtf-s3 kernel: x86/fpu: xstate_offset[2]:  576, xstate_sizes[2]:  256
7月 21 15:20:47 amtf-s3 kernel: x86/fpu: Enabled xstate features 0x7, context size is 832 bytes, using 'standard' format.
7月 21 15:20:47 amtf-s3 kernel: BIOS-provided physical RAM map:
7月 21 15:20:47 amtf-s3 kernel: BIOS-e820: [mem 0x0000000000000000-0x000000000009cfff] usable
```


```bash
6月 24 21:45:58 amtf-s3 kernel: PM: suspend entry (deep)
6月 24 21:45:58 amtf-s3 kernel: PM: Syncing filesystems ... done.
6月 25 20:50:43 amtf-s3 kernel: Freezing user space processes ... (elapsed 0.003 seconds) done.
6月 25 20:50:43 amtf-s3 kernel: OOM killer disabled.
6月 25 20:50:43 amtf-s3 kernel: Freezing remaining freezable tasks ... (elapsed 0.001 seconds) done.
6月 25 20:50:43 amtf-s3 kernel: Suspending console(s) (use no_console_suspend to debug)
6月 25 20:50:43 amtf-s3 kernel: sd 1:0:0:0: [sdb] Synchronizing SCSI cache
6月 25 20:50:43 amtf-s3 kernel: sd 1:0:0:0: [sdb] Stopping disk
6月 25 20:50:43 amtf-s3 kernel: sd 0:0:0:0: [sda] Synchronizing SCSI cache
6月 25 20:50:43 amtf-s3 kernel: sd 0:0:0:0: [sda] Stopping disk
6月 25 20:50:43 amtf-s3 kernel: [drm] probing gen 2 caps for device 8086:151 = 261ac82/6
6月 25 20:50:43 amtf-s3 kernel: [drm] enabling PCIE gen 2 link speeds, disable with radeon.pcie_gen2=0
6月 25 20:50:43 amtf-s3 kernel: [drm] PCIE GART of 2048M enabled (table at 0x0000000000040000).
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: WB enabled
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: fence driver on ring 0 use gpu addr 0x0000000040000c00 and cpu>
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: fence driver on ring 1 use gpu addr 0x0000000040000c04 and cpu>
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: fence driver on ring 2 use gpu addr 0x0000000040000c08 and cpu>
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: fence driver on ring 3 use gpu addr 0x0000000040000c0c and cpu>
6月 25 20:50:43 amtf-s3 kernel: radeon 0000:01:00.0: fence driver on ring 4 use gpu addr 0x0000000040000c10 and cpu>
6月 25 20:50:43 amtf-s3 kernel: [drm] ring test on 0 succeeded in 1 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ring test on 1 succeeded in 1 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ring test on 2 succeeded in 1 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ring test on 3 succeeded in 4 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ring test on 4 succeeded in 3 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ib test on ring 0 succeeded in 0 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ib test on ring 1 succeeded in 0 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ib test on ring 2 succeeded in 0 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ib test on ring 3 succeeded in 0 usecs
6月 25 20:50:43 amtf-s3 kernel: [drm] ib test on ring 4 succeeded in 0 usecs
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: interrupt blocked
6月 25 20:50:43 amtf-s3 kernel: ACPI: Preparing to enter system sleep state S3
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: event blocked
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: EC stopped
6月 25 20:50:43 amtf-s3 kernel: PM: Saving platform NVS memory
6月 25 20:50:43 amtf-s3 kernel: Disabling non-boot CPUs ...
6月 25 20:50:43 amtf-s3 kernel: smpboot: CPU 1 is now offline
6月 25 20:50:43 amtf-s3 kernel: smpboot: CPU 2 is now offline
6月 25 20:50:43 amtf-s3 kernel: smpboot: CPU 3 is now offline
6月 25 20:50:43 amtf-s3 kernel: ACPI: Low-level resume complete
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: EC started
6月 25 20:50:43 amtf-s3 kernel: PM: Restoring platform NVS memory
6月 25 20:50:43 amtf-s3 kernel: Enabling non-boot CPUs ...
6月 25 20:50:43 amtf-s3 kernel: x86: Booting SMP configuration:
6月 25 20:50:43 amtf-s3 kernel: smpboot: Booting Node 0 Processor 1 APIC 0x1
6月 25 20:50:43 amtf-s3 kernel:  cache: parent cpu1 should not be sleeping
6月 25 20:50:43 amtf-s3 kernel: CPU1 is up
6月 25 20:50:43 amtf-s3 kernel: smpboot: Booting Node 0 Processor 2 APIC 0x2
6月 25 20:50:43 amtf-s3 kernel:  cache: parent cpu2 should not be sleeping
6月 25 20:50:43 amtf-s3 kernel: CPU2 is up
6月 25 20:50:43 amtf-s3 kernel: smpboot: Booting Node 0 Processor 3 APIC 0x3
6月 25 20:50:43 amtf-s3 kernel:  cache: parent cpu3 should not be sleeping
6月 25 20:50:43 amtf-s3 kernel: CPU3 is up
6月 25 20:50:43 amtf-s3 kernel: ACPI: Waking up from system sleep state S3
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: interrupt unblocked
6月 25 20:50:43 amtf-s3 kernel: ACPI: EC: event unblocked
6月 25 20:50:43 amtf-s3 kernel: sd 0:0:0:0: [sda] Starting disk
6月 25 20:50:43 amtf-s3 kernel: sd 1:0:0:0: [sdb] Starting disk
```

```bash
kernel: PM: suspend entry (deep)

kernel: PM: suspend exit
```