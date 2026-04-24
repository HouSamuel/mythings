清除下载标签`sudo xattr -d com.apple.quarantine <your_app_path>`
```bash
sudo xattr -d com.apple.quarantine
```
homebrew苹果电脑安装脚本：
```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```
homebrew苹果电脑卸载脚本：
```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/HomebrewUninstall.sh)"
```
homebrew卸载所有已安装的软件
```bash
brew list --formula | xargs brew uninstall --ignore-dependencies  &&  brew list --cask | xargs brew uninstall --cask --force
```
