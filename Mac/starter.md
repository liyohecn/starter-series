# Mac 软件环境

## HomeBrew
安装
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
卸载
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/HomebrewUninstall.sh)"

## SF mono字体
cp -R /System/Applications/Utilities/Terminal.app/Contents/Resources/Fonts/*.otf ~/Library/Fonts/


## iTem2
https://iterm2.com/

## Core Tunnel
AppStore安装

## Postman
https://www.postman.com/

## 终端代理脚本
function proxy_off(){
    unset http_proxy
    unset https_proxy
    echo -e "已关闭代理"
}

function proxy_on() {
    export http_proxy="http://127.0.0.1:9981" https_proxy="http://127.0.0.1:9981"
	export https_proxy=$http_proxy
    echo -e "已开启代理"
}

function proxy_status() {
    echo $https_proxy
    curl cip.cc
}
