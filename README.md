# mobFaceMaker
2020プロジェクト学習, Creative Ai, 視覚班  
漫画のキャラクターの顔パーツ(６種)からmobキャラクターの顔を自動生成する  
## 方法(仮)
6種類の顔パーツ群を組み合わせて入力されたタグ(年齢, 性別)から指定された枚数をpngで出力する
## 環境(仮)
ubuntu(wsl)  
python 3.8.2  
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
    1. ワークスペースにさっきのリポジトリを追加
## メモ
画像データ群は重いので完成まで仮置  
30キャラ×6パーツぐらい  
入出力の画像が沢山あるので保存場所と管理方法要検討
とりあえずローカルでのフォーマットだけ決めちゃって最後にマージかな？

- 構成
    - app <-メインのフォルダ
        - メインのコード
        - 画像データのjson
        - result <-出力先
    - data <-画像データ
        - 本番環境
        - テスト環境
        
- 画像データフォルダ構成
    - charName_parts.png x 6
    - (dataMemo.txt)
    
- ubuntu内のファイルの場所
    - ubuntuからwindowsのとき
        - /mnt/c/Users/[ユーザ名]
    - windowsからubuntuのとき
        - エクスプローラに`\\wsl$\Ubuntu\home[ユーザ名]`を入力
        
- gitの使い方
    - brachについて
        - branch一覧`git branh`
        - branch作成`git branch [branch名]`
        - branchに入る`git checkout [branch名]`
        - branch削除`git -D [branch名]`
        - branch一覧(仮)
            - master <-一番触らない
            - dev1 <-２番めに使う
            - feature-* <-1番に使う
    - プルリクまでのフロー(とりあえずわかんなくて大丈夫？)
        1. `git add .`
        1. `git commit -m "コメント"`
        1. `git push origin [branch名]`
        1. web上のgithubのプロジェクトに移動
        1. Compare & Pull requestからプルリクを送信(多分LINEに通知行く)
        1. アサインされた人が変更内容見て良かったらマージ
※どっかでメアドとユーザ名聞かれる
