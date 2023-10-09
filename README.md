# HarcaChartEditor
Harca用譜面作成補助ツール  

## インストール方法
Windows→このリポジトリをクローン/ダウンロード  
Mac→[こちら](https://drive.google.com/drive/folders/1zv9JD1nJiAAYpeTOMu8oAf8iTCHX7h3Z?usp=sharing)  
セキュリティで弾かれるかもしれないので、その場合は実行許可を与えてください。  
.chartはテキストエディタを用いて手入力で編集することを想定して開発されましたが、それでもやはり全部手入力で作るのは大変なので、譜面作成を補助するツールを作りました。  
テキストエディタと本ツールを併用して譜面作成を行うことを推奨します。  
.chartの仕様については[こちら](./chart.md)  
編集画面では1小節分の譜面データを編集することができます。

## 用語など
- ID
    - 譜面を識別するためのID。任意の英数字文字列。
- オフセット	
    - 譜面の再生開始に対して音源の再生開始を遅らせる秒数。負の値を指定することが多い。
- LPB		
    - 1小節を等分する数。
- BPM		
    - 1分間の拍数。
- ScrollSpeed	
    - 譜面の流れる速度。基本は1
- Difficulty	
    - EASY,NORMAL,HARDで表される難易度。
- Level		
    - 1以上の整数で表されるレベル。
- Beat		
    - 拍子。
- Delay		
    - その小節以降、ノーツの流れを指定秒数だけ遅らせる事ができる。

## 操作
- 上段と下段
    - 上の4段は上段に流れるノーツ、下の4段は下段に流れるノーツを編集します。上下に同時ノーツを配置することはできません。
- LPBの変更			
    - LPBの入力欄に直接入力 / 入力欄の上のボタンで増減 / 上下キーで増減 / Shift + マウスホイール
    - LPBを変更すると編集中の小節情報が破棄されるのでご注意ください。
- BPMの変更			
    - 「高度な編集」より「BPMの変更」にチェックを入れ、BPM入力欄に入力。途中の小節からの変更も可能。小数の指定も可能
- 拍子の変更			
    -「高度な編集」より「Beatの変更」にチェックを入れ、 Beat入力欄に自然数を入力。途中からの変更も可能。
- 通常ノーツの配置		
    - 配置したい場所で左クリック
- ロングノーツを配置		
    - 配置したい場所で右クリック その後伸ばす拍数を入力(小数可)
- ノーツの消去			
    - 配置されているノーツを左クリック
- 音源を再生/停止		
    - スペースキーを入力

## その他のボタンなど
- 「上書き保存」		
    - 譜面をファイルに上書き保存する。ファイルは最初から読み込まれている場合はそのファイルに上書き保存、新規作成の場合はwavファイルと同じディレクトリに保存される。idがファイル名になる。
- 「外部編集」		
    - 譜面を一旦上書き保存し、そのファイルを外部エディタなどで開く。.chartファイルにテキストエディタを紐づけておくとよい。macでは動作しないかも。その場合は自分で.chartファイルを開いてください。
- リロード
    - 緑の丸い矢印のボタン。外部で編集された譜面を本ツールで再読込する。
- 「テストプレイ」		
    - 編集中の小節からテストプレイを実行することが出来ます。テストプレイ中はESCでポーズできます。F1を押すとSEが鳴ります。macだと鳴らないかも

このツールでできないorやりにくい編集をしたい場合は「譜面を開く」でテキストエディタなどで譜面を開いて編集し、「譜面読み込み」で編集した譜面を本ツールで再度読み込むといいです。

## 注意
このエディタで譜面ファイルを編集する前に、必ず譜面ファイルのバックアップを取っておいてください。「上書き保存」を押した時以外に、「譜面を開く」「テストプレイ」を押したときにも.chartファイルが上書きされるのでご注意ください。
