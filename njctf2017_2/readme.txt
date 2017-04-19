题目难度：
decoder比较难，第一天没人做出来，第二题一队做了出来。
company比较简单，pwn入门题，估计是临时改的。

加固：

company：
把"call    eax ; shellcode"这句nop掉就可以了。
.text:08048657                 push    3FFh            ; nbytes
.text:0804865C                 push    offset shellcode ; buf
.text:08048661                 push    0               ; fd
.text:08048663                 call    _read
.text:08048668                 add     esp, 10h
.text:0804866B                 mov     eax, offset shellcode
.text:08048670                 call    eax ; shellcode



