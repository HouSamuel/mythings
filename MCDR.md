## 1.安装homebrew
```bash
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```
延迟homebrew安装
```bash
brew


Example usage:
  brew search TEXT|/REGEX/
  brew info [FORMULA|CASK...]
  brew install FORMULA|CASK...
  brew update
  brew upgrade [FORMULA|CASK...]
  brew uninstall FORMULA|CASK...
  brew list [FORMULA|CASK...]
Troubleshooting:
  brew config
  brew doctor
  brew install --verbose --debug FORMULA|CASK
Contributing:
  brew create URL [--no-fetch]
  brew edit [FORMULA|CASK...]
Further help:
  brew commands
  brew help [COMMAND]
  man brew
  https://docs.brew.sh
```
## 2.安装python
```bash
brew install python@3.9
```
验证安装
```python
python3             

Python 3.9.6 (default, Dec  2 2025, 07:27:58) 
[Clang 17.0.0 (clang-1700.6.3.2)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
## 3.创建虚拟环境
创建新文件夹`mkdir <name>`
```bash
mkdir my_mcdr_server 
```
进入该目录`cd <path>`
```bash
cd /Users/qqhou/Desktop/my_mcdr_server 
```
创建虚拟环境`python3 -m venv <name>`
```python
python3 -m venv venv
```
## 4.进入虚拟环境
`source <name>/bin/activate`
```python
source venv/bin/activate
```
## 5.安装MCDR
```python
pip3 install mcdreforged -i https://mirrors.aliyun.com/pypi/simple/
```
验证安装
```python
mcdreforged
```
## 6.启动+配置
```python
mcdreforged init
```
在server文件夹中放入[fabric服务器端](https://fabricmc.net/use/server/)，启动安装程序，同意用户协议
配置mcdr文件
改语言
改启动配置
```java
java -Xmx2G -jar fabric-server-mc.1.21-loader.0.16.14-launcher.1.0.3.jar
```
配置启动文件
```bash
#!/bin/bash

# 获取脚本目录并切换
SCRIPT_DIR=“$(cd “$(dirname “${BASH_SOURCE[0]}”)” && pwd)”

echo “=====进入目录$SCRIPT_DIR =====“
cd “$SCRIPT_DIR” || exit
wait

Echo “===== 启动虚拟环境 =====“
source venv/bin/activate
wait
Echo “=====虚拟环境已激活=====“

Echo “===== 启动服务器 =====“
mcdreforged
```