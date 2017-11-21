## linux-kvm-arm-instrumentation
This is an assignment of NTU virtual machine course 2017.

Instrumentation code for trap counting are added into ARM64's KVM in Linux kernel 3.14.
There are three type of trap counters:
* CPU trap counter
* IO trap counter
* Memory trap counter

Please notice that ARMv8 has four exception levels(EL0 ~ EL4), and KVM is only capable to catch interrupt within EL2 (hypervisor mode), refer to manual for more information.
