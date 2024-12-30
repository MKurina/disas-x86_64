# disas-x86_64
A disassembler for (x86_64). without ```ring0``` instructions.

## Resources
[x86 instruction reference](http://ref.x86asm.net/geek64.html) <br>
[OSDev x86 instruction encoding](https://wiki.osdev.org/X86-64_Instruction_Encoding). <br>
[Online assembler/disassembler](https://defuse.ca/online-x86-assembler.htm). <br>

## example output
```
0x000000:   6a 29                         PUSH    0x29
0x000002:   58                            POP     RAX
0x000003:   6a 02                         PUSH    0x2
0x000005:   5f                            POP     RDI
0x000006:   6a 01                         PUSH    0x1
0x000008:   5e                            POP     RSI
0x000009:   48 31 d2                      XOR     RDX, RDX
0x00000c:   0f 05                         SYSCALL RCX, R11L, SS
0x00000e:   50                            PUSH    RAX
0x00000f:   5f                            POP     RDI
0x000010:   52                            PUSH    RDX
0x000011:   52                            PUSH    RDX
0x000012:   66 68 11 5c                   PUSH    0x5c11
0x000016:   66 6a 02                      PUSH    0x2
0x000019:   6a 31                         PUSH    0x31
0x00001b:   58                            POP     RAX
0x00001c:   54                            PUSH    RSP
0x00001d:   5e                            POP     RSI
0x00001e:   b2 10                         MOV     DL, 0x10
0x000020:   0f 05                         SYSCALL RCX, R11L, SS
0x000022:   6a 32                         PUSH    0x32
0x000024:   58                            POP     RAX
0x000025:   6a 02                         PUSH    0x2
0x000027:   5e                            POP     RSI
0x000028:   0f 05                         SYSCALL RCX, R11L, SS
0x00002a:   6a 2b                         PUSH    0x2b
0x00002c:   58                            POP     RAX
0x00002d:   48 31 f6                      XOR     RSI, RSI
0x000030:   99                            CDQ     EDX, EAX
0x000031:   0f 05                         SYSCALL RCX, R11L, SS
0x000033:   50                            PUSH    RAX
0x000034:   5f                            POP     RDI
0x000035:   6a 02                         PUSH    0x2
0x000037:   5e                            POP     RSI
0x000038:   6a 21                         PUSH    0x21
0x00003a:   58                            POP     RAX
0x00003b:   0f 05                         SYSCALL RCX, R11L, SS
0x00003d:   48 ff ce                      DEC     RSI
0x000040:   79 f6                         JNS     [RIP-0xa]
0x000042:   6a 01                         PUSH    0x1
0x000044:   58                            POP     RAX
0x000045:   49 b9 50 61 73 73 77 64 3a 20 MOV     R9, 0x0
0x00004f:   41 51                         PUSH    R9
0x000051:   48 89 e6                      MOV     RSI, RSP
0x000054:   6a 08                         PUSH    0x8
0x000056:   5a                            POP     RDX
0x000057:   0f 05                         SYSCALL RCX, R11L, SS
0x000059:   48 31 c0                      XOR     RAX, RAX
0x00005c:   48 83 c6 08                   ADD     RSI, 0x8
0x000060:   0f 05                         SYSCALL RCX, R11L, SS
0x000062:   48 b8 31 32 33 34 35 36 37 38 MOV     RAX, 0x0
0x00006c:   56                            PUSH    RSI
0x00006d:   5f                            POP     RDI
0x00006e:   48 af                         SCASQ   es:RDI, RAX
0x000070:   75 1c                         JNE     [RIP-0x1c]
0x000072:   48 31 c0                      XOR     RAX, RAX
0x000075:   50                            PUSH    RAX
0x000076:   48 bb 2f 62 69 6e 2f 2f 73 68 MOV     RBX, 0x0
0x000080:   53                            PUSH    RBX
0x000081:   54                            PUSH    RSP
0x000082:   5f                            POP     RDI
0x000083:   50                            PUSH    RAX
0x000084:   54                            PUSH    RSP
0x000085:   5a                            POP     RDX
0x000086:   57                            PUSH    RDI
0x000087:   54                            PUSH    RSP
0x000088:   5e                            POP     RSI
0x000089:   6a 3b                         PUSH    0x3b
0x00008b:   58                            POP     RAX
0x00008c:   0f 05                         SYSCALL RCX, R11L, SS

```
