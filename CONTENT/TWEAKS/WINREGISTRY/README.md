## Windows Registry

### How to set cpu affinity through the Windows Registry ?
By default, the processes uses mostly the core 0, though this can lead to bad performances because the other cores are not used a lot.
To solve this problem there is a user-friendly program called [Interrupt Affinity Policy Tool](https://github.com/littleunixcorn/Unicorns/raw/main/assets/programs/interrupt_affinity_policy_tool.msi).

<details><summary>Findings and Analysis</summary>
Set affinity through the program named above is easy, understandable but lead to a lost of time.
To solve this, you can use the registry, it is fast and requires only a click.
Here is a list of the values that you may need to use:
<hr>

**DevicePolicy**

```
IrqPolicyMachineDefault: 0x00
IrqPolicyAllCloseProcessors: 0x01
IrqPolicyOneCloseProcessor: 0x02
IrqPolicyAllProcessorsInMachine: 0x03
IrqPolicySpecifiedProcessors: 0x04
IrqPolicySpreadMessagesAcrossAllProcessors: 0x05
```

**AssignmentSetOverride**

Please visit this [website](<https://bitsum.com/tools/cpu-affinity-calculator/>).

**Regedit path to the devices**

`
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\]
`
<hr>

Example:

```
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\PCI\[DEVICE HW ID]\Device Parameters\Interrupt Management\Affinity Policy]
"DevicePolicy"=dword:00000004
"AssignmentSetOverride"=hex:08
```

The device will be set with the policy `IrqPolicySpecifiedProcessors` on the core 2 (`0x4`) of the processor.
</details>
