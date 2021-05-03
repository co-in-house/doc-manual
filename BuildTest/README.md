# Buildしたアプリの実機テストマニュアル
## Android
1. GoogleDriveに存在する任意の.apkファイルをandroid端末ダウンロード
2. 初めに『このアプリケーションは信頼できません』と表示されるが、それでもインストールするを選択。
3. 『このアプリケーションを報告しますか？』と表示されるが『いいえ』を選択
4. しばらくするとインストールが始まれるので終了し次第アプリを起動
<br><br><br>
## iOS
### 前提条件 : Macユーザーのみ対象
### 事前準備
- PCとiPhoneを繋ぐケーブル
- appStoreよりXcodeをインストール<br>
[インストールはこちらから](https://apps.apple.com/jp/app/xcode/id497799835?mt=12)
- AppleIDの取得　iPhoneをお持ちの場合そのAppleアカウントを使用<br>
[取得はこちらから](https://support.apple.com/ja-jp/HT204316)
1. Xcodeを起動して以下の手順でappleIDを登録する
    1.  ケーブルとiphoneを繋ぐ。その際にiphoneのロックを解除して以下の画像が出てきたら『信頼する』をタップ。これをしないとiPhoneとPCをつなげられません。
    ![TrustComfirmImage](Images/BuildTestImages/TrustComfirmImage.jpg)
    2. Xcode上の上部バーの Xcode -> Preferences... をクリック
    ![PreferencesInXcode](./Images/BuildTestImages/PreferencesInXcode.png)
    3. 以下のタブが出てきたら『Accounts』を選択
    ![AccountInPreferences](./Images/BuildTestImages/AcountsInPreferences.png)
    4. 左下隅にある[追加] ボタン (+) をクリック
    5. 『Add Apple ID』をクリック
    ![AddAccount](./Images/BuildTestImages/AddAccount.png)
    6. 表示されたダイアログから用意したAppleID & PassWordを入力し Sign Inをクリック
    7. 3のように自分のアカウントが表示されたら完了。
2. ????から任意のフォルダをダウンロード
3. 2でダウンロードしたフォルダの中の(〜.xcode　　もしそのファイルがない場合、〜.xcodeproj)をXcodeで開く
4. 左上にある自分が開いているファイルの中の一番親のファイルをクリックする
![FilePosition](./Images/BuildTestImages/FilePosition.png)
5. そして出てきた画面の『General』=> 『SignIn』を押し、Teamの中に自分が設定したアカウント情報を入力
6. 5が終わったら左上の三角ボタンをクリック
7. ここでiPhoneとMacの信頼を聞かれるメッセージがくるのでクリア
8. ここで以下のようにエラーが出たらiPhoneで設定 => 一般 => デバイス管理を開く
![ErrorTrust](./Images/BuildTestImages/ErrorTrust.png)
9. そこに登録したAppleIdがあるので『信頼する』をタップ
