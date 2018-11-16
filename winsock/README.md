
| 要点 | __cdecl | __stdcall | __fastcall |
| :-: | :-: | :-: | :-: |
| 参数传递方式 | 右 -> 左 | 右 -> 左 | 右边开始的两个不大于4字节（DWORD）的参数分别放在ECX和EDX寄存器，其余的参数自右向左压栈传送 |

| 清理栈方 | 调用者清理 | 被调用函数清理 | 被调用函数清理 |
| 适用场合 | C/C++、MFC的默认方式; 可变参数的时候使用 | Win API | 要求速度快 |
| C编译修饰约定 | \_functionname | \_functionname@number | @functionname@number |