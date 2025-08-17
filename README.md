[firstprogram.txt](https://github.com/user-attachments/files/21824714/firstprogram.txt)


[firstprogram.txt](https://github.com/user-attachments/files/21824711/firstprogram.txt)

1. Thought Process:

 
 ![firstAL](https://github.com/user-attachments/assets/70157da8-a4b3-4fa0-99ae-3c0021456629)

Challenges: 
One of the main challenges was getting the NASM assembler & linker commands to work correctly. Paying attention to every detail was also challenging, in order to get the code to compile correctly.


Working Code:


[Upmsg1 db "I came,", 10
    len1 equ $ - msg1

    msg2 db "I saw,", 10
    len2 equ $ - msg2

    msg3 db "I conquered.", 10
    len3 equ $ - msg3

section .text
    global _start

_start:
    ; Print msg1
    mov eax, 4          ; sys_write
    mov ebx, 1          ; stdout
    mov ecx, msg1
    mov edx, len1
    int 0x80

    ; Print msg2
    mov eax, 4
    mov ebx, 1
    mov ecx, msg2
    mov edx, len2
    int 0x80

    ; Print msg3
    mov eax, 4
    mov ebx, 1
    mov ecx, msg3
    mov edx, len3
    int 0x80

    ; Exit
    mov eax, 1          ; sys_exit
    xor ebx, ebx        ; status 0
    int 0x80
loading firstprogram.txt…]()



![firstprogramA](https://github.com/user-attachments/assets/bd7e45cb-1453-4f7e-b25c-5b644adc6470)
