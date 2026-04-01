###manim安装
##### 1.系统依赖
```
brew install uv
brew install cairo pango harfbuzz fribidi pkg-config
brew install ffmpeg
brew install latex
```
##### 2.python安装
```
cd <your_project_directory>
```
```
uv init
uv python install 3.15
uv python pin 3.15
uv add manim
```
python版本通常使用最新版
