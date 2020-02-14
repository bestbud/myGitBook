# mac homebrew 安装速度慢

运行 `brew install [packageName]`卡在 `Updating Homebrew ...`很长时间，后续的安装过程也很慢

替换相关git仓库地址为国内镜像，可以改善这个问题



## brew.git 仓库地址:
```
// 进入git库目录
cd "$(brew --repo)"

// 设置为以下之一即可
// 阿里巴巴
git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git
// 中科大
git remote set-url origin https://mirrors.ustc.edu.cn/brew.git
// 清华 可能无法解析域名
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
// 还原
git remote set-url origin https://github.com/Homebrew/brew.git
```

## homebrew-core.git 仓库地址:
```
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"

// 设置为以下之一即可
// 阿里
git remote set-url origin https://mirrors.aliyun.com/homebrew/homebrew-core.git
// 中科大
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
// 清华
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git
// 还原
git remote set-url origin https://github.com/Homebrew/homebrew-core.git
```

## homebrew-cask.git 仓库地址

```
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-cask"
// 中科大
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git
// 还原
git remote set-url origin https://github.com/Homebrew/homebrew-cask.git
```


## 替换 homebrew-bottles 访问地址

```
// 阿里
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.aliyun.com/homebrew/homebrew-bottles' >> ~/.bash_profile

// 或者中科大
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile

source ~/.bash_profile

// 还原 homebrew-bottles :删除 HOMEBREW_BOTTLE_DOMAIN后运行：
source ~/.bash_profile
```

然后运行
```
brew update
```

## 一键修改brew、brew-core为ali镜像
```
cd "$(brew --repo)" && git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git && cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core" && git remote set-url origin https://mirrors.aliyun.com/homebrew/homebrew-core.git && brew update
```
