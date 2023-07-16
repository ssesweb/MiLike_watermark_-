# MiLike_watermark

这个 Python 程序用于给图片添加类似小米徕卡风格的水印并保存到指定的输出目录。

## 写在最前

1. 目前本程序只支持打开 **`.jpg`** 格式照片(这也是最常见的直出格式)，如需支持其他格式，请自行修改代码。

2. **`logos`** 文件夹中存放了部分相机、手机品牌的logo，也提供了 **`logo.psd`** 方便各位自行设计logo样式，文件名称与EXIF信息中的品牌信息一致即可。本人仅在富士、佳能、小米照片上测试过机型名称，如其他品牌请自行测试、调整。

3. 已知BUG: 经测试，富士XS-10 部分竖拍照片，可能无法正常在照片底部输出水印，具体表现为会将照片顺时针旋转90°后再增加水印，但佳能ES 5的竖拍照片没有该问题，待研究修复。

## 安装依赖

在运行这个程序之前，请确保你已经安装了以下依赖：

- Python 3.x
- Pillow 库（用于图像处理）
- exifread 库（用于读取图片的 EXIF 信息）

你可以使用以下命令安装依赖：

```
pip install Pillow exifread
```

## 使用方法

1. 将待处理的图片文件放置在 `input` 文件夹中。
2. 运行 `main.py` 脚本。
3. 在 `output` 文件夹中查找处理后的图片。

## 配置

- 可以在 `main.py` 脚本中修改以下配置变量：
  - `FONT`：字体文件的路径。默认为 `./font/MiSans-Normal.ttf`。（小米字体，可自行更换，但不保证更换后最终输出水印文本位置准确。）
  - `INPUT_DIR`：输入目录的路径。默认为 `./input/`。
  - `OUTPUT_DIR`：输出目录的路径。默认为 `./output/`。
  - `LOGO_DIR`：标志文件目录的路径。默认为 `./logos/`。

## 注意事项

- 请确保输入目录中包含要处理的图片文件，否则程序会输出相应的提示信息。
- 如果输出目录不存在，程序会自动创建。
- 请确保字体文件和标志文件存在，并与配置变量中的路径匹配。
- 请正确使用本软件，如因使用该软件引起的任何纠纷，均应由使用者自行承担责任。
- 本软件中默认包含的logo图像仅为用于输出照片拍摄机型信息，请勿用于其他商用行为。

## 许可证

这个程序采用 MIT 开源许可证。详细信息请参阅 [LICENSE](./LICENSE) 文件。

---
