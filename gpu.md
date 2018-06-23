```shell
$ lspci | grep ' VGA ' | cut -d" " -f 1 | xargs -i lspci -v -s {}
00:02.0 VGA compatible controller: Intel Corporation 3rd Gen Core processor Graphics Controller (rev 09) (prog-if 00 [VGA controller])
        Subsystem: Lenovo 3rd Gen Core processor Graphics Controller
        Flags: bus master, fast devsel, latency 0, IRQ 30
        Memory at e0000000 (64-bit, non-prefetchable) [size=4M]
        Memory at d0000000 (64-bit, prefetchable) [size=256M]
        I/O ports at 5000 [size=64]
        [virtual] Expansion ROM at 000c0000 [disabled] [size=128K]
        Capabilities: <access denied>
        Kernel driver in use: i915
        Kernel modules: i915
```
