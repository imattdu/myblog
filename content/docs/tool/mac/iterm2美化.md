+++
title = "iterm2美化"
date = 2022-02-12T17:25:20+08:00
featured = false
comment = true
toc = true
reward = true
weight = 9
categories = [
  "tool"
]
tags = [
]
series = [
]
images = []
aliases = [
]

+++

常用快捷键

<!--more-->



![](https://raw.githubusercontent.com/imattdu/img/main/img/202202130255589.png)









终端配置代理





https://github.com/QuentinWatt/dark-flat-iterm-colors









```sh
cd ~
vim ./.zshrc
```



```sh
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```





```sh
source ./.zshrc
```





安装iterm2，[官网](https://iterm2.com/)下载安装即可 





安装 oh-my-zsh





```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```







安装 p10k

```sh
cd ./.oh-my-zsh/themes
git clone  https://github.com/romkatv/powerlevel10k.git
```





```sh
vi ~/.zshrc 
```







```sh
ZSH_THEME="powerlevel10k/powerlevel10k"
```











```sh
# 语法高亮
cd ~/.oh-my-zsh/custom/plugins/
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git


# 自动补全

cd ~/.oh-my-zsh/custom/plugins/
git clone https://github.com/zsh-users/zsh-autosuggestions
```



退出iterm2

```sh
exit
```







```sh
vim ./.zscrc
```





```sh
plugins=(
     git
     zsh-syntax-highlighting
     zsh-autosuggestions
)


HIST_STAMPS="yyyy-mm-dd"


# 文末添加
source ~/.zshrc.pre-oh-my-zsh
```







```sh
p10k configure

```

第一步会下载字体，如果失败记得配置代理







https://github.com/ryanoasis/nerd-fonts/releases

![](https://raw.githubusercontent.com/imattdu/img/main/img/202202130241326.png)









![](https://raw.githubusercontent.com/imattdu/img/main/img/202202130242317.png)





安装autojump





```sh
brew install autojump

```



打开 `~/.zshrc` 加一行代码：

```sh
[[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh
```



使用

```sh
j test
```





### **zsh-autosuggestions**

这个插件的作用很简单，就是像它名字一样，会在你输入命令的时候提示并且自动完成：







```sh
brew install zsh-autosuggestions
```









问题大致如下：

1. 这个符号看起来像钻石（旋转的正方形）吗？
2. 这个符号看起来像锁吗？
3. 这个符号看起来像 Debian logo 吗？
4. 这些图标都交叉分布在 X 之间吗？
5. 风格
6. 编码
7. 是否显示时间
8. 目录层级分隔符
9. 头部（左边）
10. 尾部（右边）
11. 是否换行
12. 左边和右边是否有连接线
13. 命令行和提示是否连接
14. 两行命令之间分布稀疏还是松散
15. 是否需要图标