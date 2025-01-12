# TJA tools
日本語版の説明書。H,Iなどは知らないのでミスもあるかもしれない<br>
[中文](README-CH.md) [English](README-EN.md)

TJAファイルを譜面画像へ変換します。[snack](https://github.com/Snack-X)の[tja-tools](https://github.com/Snack-X/tja-tools)からフォークしています。

# Run
https://whmhammer.github.io/tja-tools

# 作成
Node: https://nodejs.org/zh-cn/download をインストールし、以下のコマンドを実行します
```
git clone https://github.com/WHMHammer/tja-tools
cd tja-tools
npm i
npm run build
```
次に、ブラウザでwebpack-dist/index.html（src/index.htmlではない）を開くか、npm startを実行します

# 例
![](doc/img/示例.png)

![](doc/img/示例-春节序曲-谱面.png)

![](doc/img/示例-春节序曲-统计.png)

# 進捗

- [x] 自分の選択した文字コードでのエンコード
- [ ] 異なる譜面分岐の同時表示
- メタ情報(一般)
    - [x] `TITLE`
    - [x] `SUBTITLE`
    - [x] `BPM`
    - [x] `MAKER`
    - [ ] `GENRE`
- メタ情報（各難易度）
    - `COURSE`
        - [x] `Easy` / `0`
        - [x] `Normal` / `1`
        - [x] `Hard` / `2`
        - [x] `Oni` / `3`
        - [x] `Edit` / `Ura` / `4`
        - [ ] `Tower` / `5`
        - [ ] `Dan` / `6`
    - [x] `LEVEL`
    - [x] `BALLOON`
    - [ ] `STYLE`
    - [x] `NOTESDESIGNER0` ~ `NOTESDESIGNER6` (0~4のみ有効)
    - [x] `TTROWBEAT`（画像処理の場合1小節あたりの最大拍数）
- 音符
    - [x] `0`（休符）
    - [x] `1`（ドン）
    - [x] `2`（カッ）
    - [x] `3`（ドン(大)）
    - [x] `4`（カッ(大)）
    - [x] `5`（黄色連打）
    - [x] `6`（黄色連打(大)）
    - [x] `7`（風船、ゲキ連打開始）
    - [x] `8`（連打、風船終了）
    - [x] `9`（芋連打、くす玉開始）
    - [x] `A`（手つなぎ音符(ドン)）
    - [x] `B`（手つなぎ音符(カッ)）
    - [x] `C`（爆弾音符）
    - [x] `D`（ヒューズ(ストーリーモードの紫連打?)）
    - [x] `F`（隠し音符(?)）
    - [x] `G`（紫/緑音符(面縁同時押し)）
    - [ ] `H`（連打か面連打開始）
    - [ ] `I`（連打か縁連打開始）
- 指令
    - [x] `#START`
    - [x] `#END`
    - [x] `#MEASURE`
    - [x] `#BPMCHANGE`
    - [ ] `#DELAY`
    - [x] `#SCROLL`
    - [x] `#GOGOSTART`
    - [x] `#GOGOEND`
    - [x] `#BARLINEOFF`
    - [x] `#BARLINEON`
    - [x] `#BRANCHSTART` (もっとも難しい分岐のみ表示)
    - [x] `#N`
    - [x] `#E`
    - [x] `#M`
    - [x] `#BRANCHEND`
    - [ ] `#LYRIC`
    - [ ] `#LEVELHOLD`
    - [ ] `#NEXTSONG`
    - [x] `#TTBREAK`（見やすいように小節の改行）
