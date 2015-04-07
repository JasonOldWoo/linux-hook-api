# Destination #
The main purpose is to develop a Hook API for linux. There are similar hooks for windows.
The objects to be hooked are running processes.
# Framework #
  1. ccess process' memory
  1. et process' virtual memory structure
  1. odify access point
# Accessing process' virtual memory #
The file /proc/pid/mm provides a easy access to the process' virtual memory. The file can be read as a normal plain text file. File operations like open(), read(), write() and lseek() can all be applied to this file. First byte of the file is the first bytes of the process' virtual memory address, which is 0x00000000.