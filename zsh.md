# zsh 配置

## 安装 [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

或者

```sh
  sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 安装 [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)

它会根据历史记录和完成情况提示命令。

1. clone 代码到 `$ZSH_CUSTOM/plugins` (默认是 `~/.oh-my-zsh/custom/plugins`)

   ```sh
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   ```

2. 添加 `zsh-autosuggestions` 到 _Oh My Zsh_ 的插件列表：

   `plugins=(zsh-autosuggestions)`

## 安装 [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

高亮你输入的指令

1. clone 代码到 `$ZSH_CUSTOM/plugins` (默认是 `~/.oh-my-zsh/custom/plugins`)

   ```sh
   git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
   ```

2. 添加 `zsh-syntax-highlighting` 到 _Oh My Zsh_ 的插件列表的**最后一项**:

   `plugins=( [plugins...] zsh-syntax-highlighting)`

## 安装 [autojump](autojump)

快速转到目标文件/文件夹

# 安装 [atuin](https://github.com/atuinsh/atuin#install)
✨ Magical shell history


