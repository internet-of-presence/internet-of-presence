# internet-of-presence
Main Index and Content Repo


## /osv - minimal system to run linux binarys on a hypervisor configurable via cloud-init
base for a small linux compatible operating system designed to be used as unikernel with cloud-init support contains also some interristing scripts and python code
to simulate EC2 (amazon) cloud-init 

we are working on ECMAScript Tooling to build and package applications for hypervisors (Clouds/PC). it is simply a additional package wrapper for Linux ELF64

## /firecracker - can run virtual machines with constaints on Linux KVM
KVM based VirtualMachine Monitore to enforce some security constaints and Jails on Linux Apps.

Note KVM based VirtualMachines are in many cases not more secure then a good Jailed Environment they get used to keep it simple and lower the overall risks while
not eliminating any risk.

so it is only usefull to package in that formart if you plan to run directly cloud instances with that.

## /graaljs includes graal-node
A JavaScript Implementation based on the Truffle Language Framework for the GraalVM Platform (JavaVM Compiler Extensions) used to run ECMAScript on the JVM can be bundled with the JVM and allows Language Interop on the JVM. It also comes with its own NodeJS Fork that replaced the v8 VM with the GraalVM Platform.

The GraalVM Platform is compile able to single file executables with static and dynamic linking.



## how to identify a 32bit linux
```
uname -m
```
x86_64

```
getconf LONG_BIT
```
64

```
file /bin/bash
```
/bin/bash: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=f140964f6907dad1e79169c98bab775302abe77e, for GNU/Linux 3.2.0, stripped

## Blocking Parts 32bit on 64bit
- Wine did not support wow64 the windows 32bit abi now it does 2022
- Linux did not support to easy compile for the 32bit Kernel ABI


# Containers
General information Containers and even the Container host do always run on a Virtual Machine on windows and Mac

## Podman - can run libcontainer isolated linux apps in a kubernetes like fashion

