# はじめに

```{only} html
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![made-with-numpy](https://img.shields.io/badge/Made%20with-NumPy-1f425f.svg)](https://numpy.org/)
[![made-with-matplotlib](https://img.shields.io/badge/Made%20with-Matplotlib-1f425f.svg)](https://matplotlib.org/)
[![made-with-scikit-learn](https://img.shields.io/badge/Made%20with-scikit--learn-1f425f.svg)](https://scikit-learn.org/)
[![made-with-tensorflow](https://img.shields.io/badge/Made%20with-TensorFlow-1f425f.svg)](https://tensorflow.org/)
![Colab](https://colab.research.google.com/assets/colab-badge.svg)
%[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yamada-kd/binds-training/blob/main)
```

## この教材について
この教材はデジタルトランスフォーメーション（DX）インフルエンサ養成プログラムの講義「グーグルコラボラトリーを利用した Kaggle 課題解決」の教材です．

:::{panels}
:container:
:column: col-lg-6 px-2 py-2
:card:

---
**対象者**
^^^
DXインフルエンサ養成プログラムのステージ2を受講している全員．プログラミングの基礎的な知識や機械学習法の基本的な利用方法を習得している人．

---
**Kaggle**
^^^
<img src="image/kaggle.jpg">

<br>
Kaggle とは，企業や研究機関が主催するデータ科学のコンペティションです．参加者は提供されたデータセットに基づいてモデルを訓練し，そのモデルの予測精度を競います．上位の参加者やチームは賞金を獲得することができます．データ科学を学んだ人にとって良い腕試しの場となります．

この講義では Kaggle に参加して，実際のデータ科学の問題を解決します．参加するためにグーグルコラボラトリーというクラウドサービスを利用します．GPU を利用可能です．これを利用して Kaggle に直接解答を提出することもできます．

---
**グループワーク**
^^^
<img src="image/collaboration.jpg">

<br>
実際の課題解決は，グループワークにて行います．グループ内では助け合い，グループ間では競い合うことによって，データ科学的な解析能力を磨きます．


---
**助け合いと競い合い**
^^^
<img src="image/group.jpg">

<br>
グループは図のように分けます．各グループにいくつかの課題が与えられます．この課題は各グループで同じものが出題されます．

グループのメンバーはどれかひとつの課題を選択して解きます．各課題の評価値の総合点で最終的なグループ間の勝敗を決定します．

グループ内では助け合う必要があり，グループ間では競い合うことになります

:::

### このコンテンツで学ぶこと
このコンテンツの目的は，ウェブベースの計算環境である Jupyter Notebook（このウェブページを形作っているもの）を利用して，Python や機械学習ライブラリの基本的な動作を習得することです．このコンテンツは東北大学大学院情報科学研究科のプログラミング初学者向けの授業「ビッグデータスキルアップ演習（Big Data Skillup Training）」の内容の一部を日本語の e-learning コンテンツとして再構築したものです．
```{note}
つまり，このコンテンツに間違いが含まれていても山田はまったく悪くなくて元の作成者が悪いです．
```
### この環境について
Jupyter Notebook は Python を実行するための環境です．メモを取りながら Python のコードを実行することができます．この環境は，Python プログラムがコマンドライン上で実行される実際の環境とは少し異なるのですが，Python プログラムがどのように動くかということを簡単に確認しながら学習することができます．

## 教材の利用方法
この教材は Google Colaboratory（グーグルコラボラトリー）を利用して作られています．グーグルコラボラトリーは Jupyter Notebook のファイルをウェブブラウザから使えるように Google が用意してくれたアプリです．各ページの上部にロケットのアイコン <i class="fa fa-rocket" aria-hidden="true"></i> があるのでこれをクリックして各ページのファイルを Google Colaboratory 上で開いて利用してください．

### GPU の利用方法

グーグルコラボラトリーで GPU を利用するには上のメニューの「ランタイム」から「ランタイムのタイプを変更」と進み，「ハードウェアアクセラレータ」の「GPU」を選択します

### 開始前に行うこと

```{hint}
グーグルコラボラトリー自体の一番上の「ファイル」をクリックし，さらにポップアップで出てくる項目から「ドライブにコピーを保存」をクリックし，自身のグーグルドライブにこのウェブページ全体のソースを保存します（グーグルのアカウントが必要です）．こうすることによって，自分で書いたプログラムを実行することができるようになります．また，メモ等を自由に以下のスペースに追加することができるようになります．
```

### 進め方

上から順番に読み進めます．Python のコードが書かれている場合は実行ボタンをクリックして実行します．コード内の値を変えたり，関数を変えたりして挙動を確かめてみてください．

### コードセル

コードセルとは，Python のコードを書き込み実行するためのセルです．以下のような灰色のボックスで表示されていますす．ここにコードを書きます．実行はコードセルの左に表示される「実行ボタン」をクリックするか，コードセルを選択した状態で `Ctrl + Enter` を押します．環境によっては行番号が表示されていると思いますので注意してください（行番号の数字はプログラムの構成要素ではありません）．

```python
print("This is a code cell.")
```
