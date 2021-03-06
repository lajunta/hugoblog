---
title: "Basic vscode usage"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["vscode"]
---
基本用法
===


多光标编辑
---

  - 盒子选择 按`shift+alt` 拖选 文本块
  - 按`shift+alt+方向键上` 或者 `shift+alt+方向键下`选择在当前光标上或下插入新光标
  - 按`alt+click`在任意地方添加光标
  - 按`ctrl+shift+L`,可以选定当前的选择的字符的所的实例。
  - 按`ctrl+F2`,可以选定当前的选择的字符的所的实例。

智能提示
---

`ctrl+space` 可以出现提示框，显示相应的函数和填充选择

行操作
---

- `ctrl+c` 拷贝光标当前行
- `alt+向上/向下` 移动当前行或选择的多行
- `ctrl+shift+k` 删除当前行或者选择的多行
- `ctrl+shift+alt+向上/向下` 向上或者向下复制一行或者多行
- `ctrl+/` 注释或者取消 当前行或者多行

重命名
---

- 在某个单词或字符串上按 `F2` 可以选择并修改它，对整个工程文件夹有效

- 也可以右键进行重命名

文档格式化(美化排版)
---

- 按 `ctrl+shift+I`对整篇文档进行重新排版
- 按 `ctrl+k` `ctrl+f` 对选择的内容进行排版

代码折叠
---

- 在要折叠的行 按`ctrl+shift+[` 进行折叠,按`ctrl+shift+]`展开
- 也可以在点击行号后面的 `向下箭头`进行折叠
- `ctrl+k` `ctrl+0` 折叠全部 , `ctrl+k` `ctrl+j`展开全部 

跳转
---

- `Ctrl+P` 在多个文档间跳转
- `F12` 跳转到符号定义, 在符号上方按住 `Ctrl` 可不跳转查看说明或预览
- `Ctrl+F12` 跳转到实现
- `Ctrl+shift+0` 在当前文件的符号间进行跳转
- `Ctrl+T` 在多文件中查找函数或者符号定义

错误和警告
---

    按 `F8`依次跳到不同的出错点进行检查并修改

JavaScript类型检查
---

使用 `// @ts-check` 进行检查 ,`// @ts-nocheck` 忽略检查

```js
// @ts-nocheck

let easy = true;
easy = 42;

```