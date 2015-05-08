ata
===
hello word
```c
int main(void)
{
        asm("jmp msg\n\t"
                "back:\n\t"
                "popq %rsi\n\t"
                "movq $4, %rax\n\t"
                "movq $1, %rbx\n\t"
                "movq %rsi, %rcx\n\t"
                "movq $18, %rdx\n\t"
                "int $0x80\n\t"
                "movq $1, %rax\n\t"
                "int $0x80\n\t"
                "msg:\n\t"
                "call back\n\t"
                ".string \"welcome to ata\"");
}
```
我是测试
