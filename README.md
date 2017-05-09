# FactorioKanji
  FactorioKanjiはFactorioChatのフォークからはじまり、Factorioにおいて
  日本語入力をするためにダイアログを出すためのAutoHotkeyスクリプトです。
  Windows NT系統なら動作すると思いますが、メインはWindows10で動作確認しております。

## ダウンロード・インストール
  <https://github.com/horensor/FactorioKanji/releases>
  からsource zipをダウンロード、解凍しfactoriokanji.exeを実行してください。

## 使用方法
- 起動
  1. factoriokanji.exeを起動
  2. 日本語を入力したい際に半角/全角キーを押す
    (チャットの前には@キーで入力状態にしてから半角/全角キーを押してください)
  3. 送信したい文字を打ったら`Send`ボタンを押して送信

- 終了
  Exitボタンで終了します。
  確認ダイアログは10秒で自動で閉じますがOKボタンですぐに終了できます。

- 起動キーを変更する
  - プルダウンから{f1}{Ins}などを選ぶとそれぞれF1(ファンクション1)、Ins(Insert)キーで起動するようになります。変更後更新ボタンを押してください。
  - 全角半角がうまく効かない場合、全角半角2~5もお試しください。
  - http://ahkwiki.net/KeyList のキーが使えます。

- アンインストール
  FactorioKanjiを終了し解凍したフォルダを削除してください。

## AutoHotkeyのスクリプトとして実行したい場合
 AutoHotkey<https://autohotkey.com/>をインストールし facoriokanji.ahk を読み込んでください。

## 参考:Optionについて
- デフォルトではタスクバーの通知領域のアイコンを表示しなくなりました
  Windowsでは通知領域に表示したアイコンをレジストリに記憶していますが、アンインストールなどで特定のソフトのみそのリストから削除できない仕様のようで、実行時のフォルダーの違いで別ソフトと認識されるなどでFactorioKanjiが重複して記憶されたりしても、レジストリの書き換えによるリセットなどでしか対処できない模様でした。
  そのためデフォルトではHideは常駐化ではなくウィンドウを非アクティブにするのみで、起動中はタスクバーに表示されるように変更しました。
  Optionで「通知領域にアイコンを表示」にチェックを入れると、通知領域にアイコンを表示し、Hideなどで非アクティブになるとタスクバーに表示されなくなります。アイコンを右クリックで終了することができます。
- チャットモードについて
  FactorioKanjiの端緒はFactorioChatというTakuma Niiharaさんの書かれたスクリプトを、駅名など任意の場所で漢字入力できるように変更したものです。
  FactorioChatでは@キーに呼応してダイアログが表示され、入力後チャット発言されるようになっていました。チャットモードはこれを再現したもので、チャットしか使用しない場合半角/全角キーなどで呼び出す必要のないモードです。
  Factorioの設定でLuaコンソールをGRAVEから変更している場合、Optionのチャット開始キーを変更してください。(/evolutionボタンなどでもこれを参照しています)

## License
  GPL2とMITのデュアルライセンスですが、バイナリーについてはAHKがGPL2となります。
