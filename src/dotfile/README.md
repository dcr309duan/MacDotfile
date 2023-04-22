# MacDotFile

本仓库存储了我所使用的 Mac 下部分软件的配置文件，例如 `vim` 的配置文件。

## 如何使用

首先将仓库以 bare 的方式 clone 到本地：

```bash
git clone --bare git@github.com:dcr309duan/MacDotfile.git $HOME/.cfg
```

然后在 shell 的配置文件中，添加如下别名方法：

```bash
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

然后执行 `checkout` 来同步配置文件：

```bash
config checkout
```

因为本地可能已经有同名的配置文件，所以可能会存在冲突，需要我们将对应的文件备份到其他目录中，再执行上面的 checkout 方法。
