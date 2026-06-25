# 左右反転画像 生成プログラム flip.py

## 1.概要
引数で使用した画像の左右反転画像を作成する python3 で動作するプログラムです。

## 2.ソースコード
```python
# このプログラムは python3用です。
# あらかじめ pip install pillow で pillow をインストールしてきます。
from PIL import Image
import sys

# コマンドライン引数から入力画像と出力画像のファイル名を取得
input_image = sys.argv[1]
output_image = sys.argv[2]

# 画像の読み込み
img = Image.open(input_image)

# 画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.save(output_image)
```

## 3.使い方
### 3.1.実行例
- コマンドラインフォーマット
```python
python3 flip.py <input_image_path> <output_image_path>
```
- 利用例
```python
python3 flip.py input.jpg output.jpg
```
### 3.2.出力結果
- 以下のように入力画像の左右反転画像出力されます。

| 入力画像(input.jpg) | 出力画像（output.jpg) |
|--------------------|----------------------|
|<img width="640" height="468" alt="input" src="https://github.com/user-attachments/assets/ac969052-a75b-4e20-9c49-8f9af6391d92" /> | <img width="640" height="468" alt="output" src="https://github.com/user-attachments/assets/256d9d3e-3a75-4beb-a808-ebdd739f858f" /> |

以上


