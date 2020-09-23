# mobFaceMaker
2020プロジェクト学習, Creative Ai, 視覚班  
漫画のキャラクターの顔パーツ(６種)からmobキャラクターの顔を自動生成する。
## 環境(仮)
ubuntu(wsl)  
python  
openCV  
VScode ←便利
## 環境構築の手順(仮)
- 前提
    - VScodeインストール済み
    - VScode日本語化済み
1. WSLの有効化
    1. コントロールパネルから[プログラム] > [Windowsの機能の有効化または無効化] を選択し
    1. 表示されたダイアログの中から「Windows Subsystem for Linux」にチェックを入れて有効化
1. ubuntuインストール
    1. Microsoft StoreからUbuntuをインストール
    1. Ubuntuの起動
    1. ユーザ名とパスワードの設定
    1. 再起動
1. pythonoのインストール
    1. `sudo apt update`
    1. `sudo apt upgrade`
    1. `sudo apt install python3 python3-pip -y`
    1. `sudo pip3 install pip -U`
    1. `python3 --version`でバージョン確認
1. openCVのインストール
    1. `sudo apt-get install libopencv-dev python3-opencv`
1. repositryのダウンロード
    1. `git clone https://github.com/SAITOman/mobFaceMaker.git`
1. VScodeとubuntuの連携
    1. `. code`
    1. VScode上でターミナルを開く
    1. Ubuntuに接続されているか確認
## メモ
画像データ群は重いので完成まで仮置  
30キャラ×6パーツぐらい
- 構成
    - app <-メインのフォルダ
    - data <-画像データ
        - 本番環境
        - テスト環境
- 画像データフォルダ構成
    - charName_parts.png x 6
    - (dataMemo.txt)
