# ChartEditor
しつび音ゲー譜面作成補助ツール  
Windows→このリポジトリをクローン  
Mac→[こちら](https://drive.google.com/drive/folders/1h4NkWfYNPcbn56fEwqFK5xSdvgPGSJMz?usp=sharing)  
.chartは手入力で編集することを想定して開発されましたが、それでもやはり全部手入力で作るのは大変なので、譜面作成を補助するツールを作りました。  
.chartの仕様については[こちら](./chart.md)  
編集画面では1小節分の譜面データを編集することができます。

## 用語など
- ID
    - 譜面を識別するためのID。任意の英数字文字列。
- オフセット	
    - 譜面の再生開始に対して音源の再生開始を遅らせる秒数。負の数も指定できる。
-LPB		
    - 1小節を等分する数。
- BPM		
    - 1分間の拍数。
- ScrollSpeed	
    - 譜面の流れる速度。基本は1
- Difficulty	
    - EASY,NORMAL,HARDで表される難易度。
- Level		
    - 整数で表されるレベル。
- Beat		
    - 拍子。
- Delay		
    - その小節以降、ノーツの流れを指定秒数だけ遅らせる事ができる。

## 操作
- LPBの変更			
    - LPBの入力欄に直接入力 / 入力欄の上のボタンで増減 / 上下キーで増減
- BPMの変更			
    - BPM入力欄に直接入力。途中の小節からの変更も可能。小数の指定も可能
- 拍子の変更			
    - Beat入力欄に自然数を直接入力。途中からの変更も可能。
- 通常ノーツの配置		
    - 左右キーで選択位置を移動して、該当キーを入力 / 配置したい場所で左クリック
- スペース同時押しノーツの配置	
    - ctrl+該当キー / 右クリック
- ロングノーツを配置		
    - shift+該当キー / マウスホイールクリック その後伸ばす拍数を入力(小数可)
- ノーツの消去			
    - 該当キーの入力 / 配置されているノーツを左クリック
- 音源を再生/停止		
    - スペースキーを入力

## その他のボタンなど
- 「上書き保存」		
    - 譜面をファイルに上書き保存する。ファイルは最初から読み込まれている場合はそのファイルに上書き保存、新規作成の場合はwavファイルと同じディレクトリに保存される。idがファイル名になる。
- 「譜面を開く」		
    - 譜面を一旦上書き保存し、そのファイルを外部エディタなどで開く。.chartファイルにテキストエディタを紐づけておくとよい。
- 「譜面読み込み」	
    - 外部で編集された譜面を本ツールで読み込む。
- 「テストプレイ」		
    - 試験的機能(色々と未実装)です。編集中の小節からテストプレイを実行することが出来ます。テストプレイ中はESCでポーズできます。

このツールでできないorやりにくい編集をしたい場合は「譜面を開く」でテキストエディタなどで譜面を開いて編集し、「譜面読み込み」で編集した譜面を本ツールで再度読み込むといいです。

## 注意
このエディタで譜面ファイルを編集する前に、必ず譜面ファイルのバックアップを取っておいてください。「上書き保存」を押した時以外に、「譜面を開く」「テストプレイ」を押したときにも.chartファイルが上書きされるのでご注意ください。
