## ファイルの説明

### grbl_settings_default.txt
`grbl_settings_default.txt` は、Arduino UNOに書き込む、GRBLの設定ファイルです。

### smile.html
`smile.html` は、Gコードをハードコードしたものです。
このhtmlファイルだけでスマイルを描くテストができます。

### test.html
`test.html` は、Gコードをファイルから読み込んでテストするものです。
任意のGコードを書かせることができます。

#### Gコードを準備する際の注意
- キャンバスサイズは 10 x 10 なので、それを守る必要があります。
- また、ペンを下す（ON）時のGコードは `M3 S90`、上げる（OFF）時のGコードは `M3 S180` を使う必要があります。
- 送る時の速度は `F` で指定できます。300ほどが良いかもしれません。なお、ハード側の設定で500以上の速度は出ないようになっています。（`grbl_settings_default.txt`参照）

### picasso.gcode
`picasso.gcode` は、ピカソのロゴを描くことのできるGコードです。ご自由にお使いください。

## テスト手順

### 1. リポジトリをクローン

```
git clone https://github.com/picasso-studio/gcode-serial-test.git
```

### 2. ArduinoとPC接続

ペンプロッタのArduino UnoとPCをUSBで接続してください。

### 3. ペンプロッタ電源ON

ペンプロッタのCNCシールドに繋がっているDC電源をONにしてください。

### 4. `smile.html` / `test.html` を開く

`smile.html`（簡易テスト用）または `test.html`（任意のGコード用）をブラウザで開いてください。  
手順通りに進めれば、描画ができるはずです。  
なお、`test.html` を使う場合は、`picasso.gcode` を読み込ませることで、ピカソのロゴを描画させることができます。
