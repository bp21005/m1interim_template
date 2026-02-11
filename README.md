# M1中間発表 予稿テンプレート

修士1年 中間発表用の予稿LaTeXテンプレートです。

## ファイル構成

| ファイル | 説明 |
|---------|------|
| `m1interim.cls` | ドキュメントクラス（体裁定義） |
| `main.tex` | 予稿本体（編集対象） |
| `refs.bib` | 参考文献データベース |

## 体裁仕様

- 用紙: A4
- 本文: 10pt、2段組（段間 6mm）
- 余白: 上 20mm、下 25mm、左右 20mm
- 欧文フォント: Times New Roman
- 和文フォント: MS 明朝（本文）/ MS ゴシック（見出し）
- ページ番号なし

## 予稿の構成

1. 背景
2. 方法
3. 結果
4. 考察
5. 結論
6. 参考文献

※ 2〜4は研究分野に応じて異なる構成でも可。

## 使い方

### 1. `main.tex` のメタ情報を編集

```latex
\jptitle{日本語タイトル}
\entitle{English Title Goes Here}
\department{システム理工学専攻}
\studentid{MF23000}
\studentname{芝浦　太郎}
\labname{○○○○○○○○研究室}
\supervisor{芝浦　工大郎}
```

### 2. 各セクションの本文を記述

### 3. コンパイル（LuaLaTeX + BibTeX）

```bash
latexmk -lualatex main.tex
```

`latexmk` を使わない場合:

```bash
lualatex main.tex
bibtex main
lualatex main.tex
lualatex main.tex
```

## 注意事項

- **LuaLaTeX** が必須です（pLaTeX / upLaTeX では動作しません）
- MS 明朝・MS ゴシックがシステムにインストールされている必要があります
- 参考文献スタイルは `unsrt`（引用順）です
