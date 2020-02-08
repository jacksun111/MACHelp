## MAC Help 

### Homebrew

下载Homebrew在国内经常被墙，最好使用 VPN . 官网地址 (https://brew.sh/)
```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

然后更换为中科大的源
```
    cd "$(brew --repo)"
    git remote set-url origin https://mirrors.ustc.edu.cn/brew.git
    cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
    git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
    cd "$(brew --repo)/Library/Taps/homebrew/homebrew-cask"
    git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git
    brew update
    echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
```
可以在github上拉取代码。

需要 homebrew-core , homebrew-cask 
homebrew-cask 去官网下载zip, git clone 实在是慢

### iterm2

```
    brew cask install iterm2

    commans: 
        brew update 
        brew doctor 
        brew cask doctor
```

### oh my zsh

`sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`

#### incr: 
    提示补全目录
    ```
    mkdir ~/.oh-my-zsh/plugins/incr
    wget http://mimosa-pudica.net/src/incr-0.2.zsh -O ~/.oh-my-zsh/plugins/incr/incr.plugin.zsh
    source ~/.oh-my-zsh/plugins/incr/incr.plugin.zsh
    source ~/.zshrc

    ```

#### zsh-autosuggestions
    提示上一次的命令
```
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    brew install zsh-autosuggestions
    source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh
```




