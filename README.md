# WPM-MAJIC-ENTRY-POINT-INJECTION
This exploit is utilising AddressOfEntryPoint of process which is RX and using WriteProcessMemory internal magic to change the permission and write the shellcode. Exploit also using direct syscalls to bypass user-mode hooking of AV/EDRs. This technique is avoiding the usage of VirtualAlloc, VirtualProtect APIs directly inside the code. The working of VirtualProtect will be covered by WPM magic.


## WORKING FLOW
1) Get PEB address and pointer to image base address
2) Get process image base address
3) Read target process image headers
4) Get AddressOfEntryPoint which is by-default RX
5) Write shellcode to image entry point and execute it (WPM MAGIC HERE)

## USAGE
1) Compile the code in Visual Studio and execute  Simple :)
2) If you guys face any error while compilation, please make sure MASM should be enabled in your solution file build customization.


https://github.com/user-attachments/assets/7ef9c545-7d98-4243-8808-2f009f514ff8

### ONLY FOR EDUCATIONAL PURPOSES

