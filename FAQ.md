For support see [the FAQ](https://github.com/tmux/tmux/wiki/FAQ)

# FAQ

> Nicholas Marriott edited this page on 8 Jun 2017 .3 revisions

PLEASE NOTE: most display problems are due to incorrect TERM! Before
reporting problems make SURE that TERM settings are correct inside and
outside tmux.

```chinese
请记住：显示出来的错误信息大多数是由于不正确的终端设置！在说明这个问题之前请确定tmux的内部和外部的设置是正确的。
```

Inside tmux TERM must be "screen" or similar (such as "screen-256color").
Don't bother reporting problems where it isn't!

```chinese
tmux里面的错误信息必须是屏幕显示出来的或者是类似术语（例如"screen-256color"）。否则不要上报这个问题。
```

Outside, it must match your terminal: particularly, use "rxvt" for rxvt
and derivatives.

```chinese
在系统内一定要兼容你的终端:特别是使用名为“rxvt”的终端匹配rxvt和其衍生产品
```

### How is tmux different from GNU screen?

tmux and GNU screen have many similarities and similar goals but now many
differences. Most things that can be achieved in one can be achieved in the
other, however.

```chinese
GNUscreen终端和tmux终端有什么区别？
tmux和GNU screen存在许多相同点和相同的目的，但是现在有了很多的不同之处。然而能在一个终端上面实现的也能在另一个终端上面实现。
```
What is TERM and what does it do?

The environment variable TERM tells applications the name of a terminaldescription to read from the terminfo(5) database. Each description consists ofa number of named capabilities which tell applications what to send to controlthe terminal. For example, the "cup" capability contains the escape sequenceused to move the cursor up.

It is important that TERM points to the correct description for the terminal anapplication is running in - if it doesn't, applications may misbehave.

The infocmp(1) command shows the contents of a terminal description and thetic(1) command builds and installs a description from a file (the -x flag isnormally required with both).

```什么是TERM并且它的作用是什么？
多变的终端环境会告诉应用终端所描述的命令名称，这些命令来自于命令库。
```
