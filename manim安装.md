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
##### 3.验证
编辑main.py
```python
from manim import *

class SquareToCircle(Scene):
    def construct(self):
        square = Square(color=BLUE)
        self.play(Create(square))
        self.play(Transform(square, Circle(color=RED)))
        self.wait(1)
```
```bash
uv run manim -pql main.py SquareToCircle
```
