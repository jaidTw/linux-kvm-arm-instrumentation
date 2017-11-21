## linux-kvm-arm-instrumentation
This is an assignment of NTU virtual machine course 2017.

Instrumentation code for trap counting are added into ARM64's KVM(kernel virtual machine) in Linux kernel 3.14.
There are three type of trap counters:
* CPU trap counter
* IO trap counter
* Memory trap counter

## Usage
First, enable the tracing event
```
# echo 1 > /sys/kernel/debug/tracing/events/kvm/kvm_vm_hw2/enable
```
then boot the guest operating system using KVM.

Now, you may check the counters anytime from the host OS trace buffer.
```
# cat /sys/kernel/debug/tracing/trace
```

Please notice that ARMv8 has four exception levels(EL0 ~ EL4), and KVM is only capable to catch interrupt within EL2 (hypervisor mode), refer to manual for more information.
