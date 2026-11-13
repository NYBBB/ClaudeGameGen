# fable52-fps-repro 提示词

## 01-audio：程序化音效

```
你在独立完成一个创作任务。用户只给一次需求，之后不会再回答任何问题，所有决定你自己做，直到作品完成。
- 产物只写到任务指定的目录。
- 可以用 `agent-browser`（open / screenshot / eval / console）在本机 Chrome 里打开自己的页面截图自检，发现问题就改。截图前先用 eval 读一次 WebGL renderer 字符串，如果是 SwiftShader 等软件渲染，在最终汇报里写明。
- 涉及声音时，你听不到声音：用 OfflineAudioContext 渲染后检查峰值、削波和静音段，在汇报里写明「未经人耳试听」。
- 完成后用 3–6 行汇报：做了什么、文件路径、已知问题。

用纯 WebAudio 代码合成一套 FPS 游戏音效，不许用任何音频文件、采样或外部音频库，所有声音都从振荡器、噪声和滤波器算出来。

要有：步枪单发（室外、室内两种尾音）、换弹三段（退弹匣、上弹匣、拉枪栓）、弹壳落地、脚步（水泥、金属、积水各一种）、子弹掠过耳边、跳弹、持续的雨声、远处的雷声、一段 30 秒左右的紧张配乐。每个音效至少 3 个随机变体，连按不会听起来一模一样。

品质要像 3A 游戏的音效，不要 8-bit 芯片音那种味道。

做成一个单文件 HTML 音效台：每个声音一个按钮，播放时显示波形和频谱，界面要好看。
输出到：./demos/01-audio/index.html
```

## 02-materials：程序化材质

```
你在独立完成一个创作任务。用户只给一次需求，之后不会再回答任何问题，所有决定你自己做，直到作品完成。
- 产物只写到任务指定的目录。
- 可以用 `agent-browser`（open / screenshot / eval / console）在本机 Chrome 里打开自己的页面截图自检，发现问题就改。截图前先用 eval 读一次 WebGL renderer 字符串，如果是 SwiftShader 等软件渲染，在最终汇报里写明。
- 涉及声音时，你听不到声音：用 OfflineAudioContext 渲染后检查峰值、削波和静音段，在汇报里写明「未经人耳试听」。
- 完成后用 3–6 行汇报：做了什么、文件路径、已知问题。

用 Three.js（从 CDN 引入，只允许这一个库）做一个材质展示页，所有贴图都必须在代码里程序化生成，不许加载任何图片文件。

材质：雨后湿漉漉带积水反光的混凝土地面、刷漆后生锈的集装箱瓦楞钢板（带喷涂的箱号和标识）、镀锌钢、黑色橡胶、木托盘、带做旧痕迹的金属铭牌。

光照是雨夜码头的氛围：钠灯暖光加冷色天光，环境反射也要程序化生成。画面要接近照片级写实，可以慢慢转动查看每个材质。

做成单文件 HTML，输出到：./demos/02-materials/index.html
```

## 03-models：纯代码建模

```
你在独立完成一个创作任务。用户只给一次需求，之后不会再回答任何问题，所有决定你自己做，直到作品完成。
- 产物只写到任务指定的目录。
- 可以用 `agent-browser`（open / screenshot / eval / console）在本机 Chrome 里打开自己的页面截图自检，发现问题就改。截图前先用 eval 读一次 WebGL renderer 字符串，如果是 SwiftShader 等软件渲染，在最终汇报里写明。
- 涉及声音时，你听不到声音：用 OfflineAudioContext 渲染后检查峰值、削波和静音段，在汇报里写明「未经人耳试听」。
- 完成后用 3–6 行汇报：做了什么、文件路径、已知问题。

用 Three.js（从 CDN 引入，只允许这一个库）纯代码建模，不许加载任何模型文件或图片：
1. 一台集装箱码头的岸桥起重机（桁架、吊具、司机室、钢缆都要有）
2. 一艘停靠的集装箱货船，甲板上堆着集装箱
3. 一把第一人称视角的突击步枪，带红点瞄具，细节要经得起近看

结构比例要像真的，细节越多越好。做成单文件 HTML 模型查看器，可以切换三个模型、鼠标旋转缩放。
输出到：./demos/03-models/index.html
```

## 04-fps：一段话做完整FPS

```
你在独立完成一个创作任务。用户只给一次需求，之后不会再回答任何问题，所有决定你自己做，直到作品完成。
- 产物只写到任务指定的目录。
- 可以用 `agent-browser`（open / screenshot / eval / console）在本机 Chrome 里打开自己的页面截图自检，发现问题就改。截图前先用 eval 读一次 WebGL renderer 字符串，如果是 SwiftShader 等软件渲染，在最终汇报里写明。
- 涉及声音时，你听不到声音：用 OfflineAudioContext 渲染后检查峰值、削波和静音段，在汇报里写明「未经人耳试听」。
- 完成后用 3–6 行汇报：做了什么、文件路径、已知问题。
- 用 agent-browser 时一律加 `--session game04`，不要动默认会话。

Build me a FPS. Insanely detailed quality pls, something that looks visually like it can keep up with AAA. Make it small in scope (like a tiny level) but otherwise impressive photorealistic graphics

（环境说明：做成浏览器里能玩的单文件 HTML，只能从 CDN 引入库，不能加载外部模型、图片、音频文件。输出到 ./demos/04-fps/index.html）
```

