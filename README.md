# Reset IME on macOS
Reset input method editor to U.S. English

----

## 缘起

Kros: 在 vim 下，在各种模式间切换时，你怎么解决中文输入法切换问题的

ETiV: 用得不多…

Kros: 你个伪 vimmer

ETiV: 多按下 <kbd>cmd</kbd> + <kbd>space</kbd> 又不会死 _（内心还是挺膈应的）_

## 方案

需要: **BetterTouchTool**，以及本项目 src 下的编译产物（假设已经安装到了 `/usr/local/bin/reset-ime`）

1. 在 BetterTouchTool 中，新增一个键盘方案，App 可以选择 **iTerm2**、**Sublime Text**、**Code**，亦或是「All Apps」
2. 在 **Click here to record a shortcut** 处，录入 <kbd>Ecs</kbd> 键，作为启动键
3. 激活下方的 **Prevent recursive triggers**
4. 而后，为其设定 actions:
    - 第一个 action 设定为： **ESC (Escape Key, respects pressed modifiers)**
    - 第二个 action 设定为： **Execute Terminal Command (Async, non-blocking)**，下方的输入框填入 `/usr/local/bin/reset-ime`

即可完成设置
