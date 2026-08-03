## Terminal, TTY and Bash

- _Terminal (The Visual Wrapper)_
  - A Terminal is a graphical application that provides a user interface. It has no understanding of commands like ls or cd.
- _TTY (The OS Link)_
  - TTY stands for TeleTypeWriter. In modern OS a TTY is a abstract software device insides the IS kernel. It acts a middleman that handle the flow of text data between your Terminal application and the shell. Like An HTTP Request.
- _Bash(The Brain)_
  - Bourne-Again Shell is the actual command-line interpreter software. it is a user space application that sits waiting for text input. When you type a command and hit enter Bash parses the string, determines what you to achieve with the OS kernel to execute it, and the passes the result back.
