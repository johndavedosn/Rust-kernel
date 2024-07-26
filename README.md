# Rust-kernel
An x86_64 simple kernel made with Rust and bootimage.


# Recommendation
Compile with a nightly toolchain in order to give access for experimental features, The kernel might not compile without this.

# Building

Since the kernel uses bootimage you can use : 

```
$ cargo bootimage 
```
it will produce a bootable x86_64 .bin kernel in your ``target/x86_64-target/`` directory, Use something like QEMU in ordor to boot it.

## Booting with QEMU

Install it if you haven't alreadt and then run : 

```
qemu-system-x86_64 -drive format=raw,file=path/to/lernel
```
If everything goes right you should see a QEMU windows saying "Hello World!".