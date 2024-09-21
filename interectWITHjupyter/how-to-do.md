# 如何使得 mm 可以与 jupyter 交互

## `WolframLanguageForJupyter` 包
Wolfram Research 提供了这个包, 使用以下命令下载

```bash
git clone https://github.com/WolframResearch/WolframLanguageForJupyter.git
```

安装完成后, 运行 Wolfram 提供给我们的安装脚本

```bash
cd WolframLanguageForJupyter
./configure-jupyter.wls add
```

这里说明一下, `configure-jupyter.wls` 是 Wolfram 语言的脚本文件, 用于配置 jupyter notebook 与 Wolfram Language 之间的连接, `add` 命令表示向 jupyter 添加一个内核.

## 配置 Mathematica 路径
在 Mathematica 中, 手动加载包的完整路径

```mathematica
Needs["WolframLanguageForJupyter`", </your/path/to/WolframLanguageForJupyter/WolframLanguageForJupyter.m>]
```

`WolframLanguageForJupyter.m` 文件在刚下载的仓库里. 不出意外的话完成以上后可以在 jupyter 中找到可以用的内核.

如果还是不行就在 Mathematica 里面再运行一下

```mathematica
Needs["WolframLanguageForJupyter`"]
InstallWolframLanguageForJupyter[]
```