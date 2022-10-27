# Crostini日本語化用のメモ

## フォントのインスコ (全部コピペでおｋ)
sudo apt update && sudo apt install task-japanese locales-all fonts-noto-cjk -y && sudo localectl set-locale LANG=ja_JP.UTF-8 LANGUAGE="ja_JP:ja" && source /etc/default/locale

## Fcitx-Mozcのインスコ
sudo apt install fcitx-mozc -y

## 環境変数の設定
sudo -e /etc/environment.d/fcitx.conf

iキーで挿入モード
Shift+Ctrl+Vでペースト
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx
GDK_BACKEND=x11
入力後、Escからの大文字ZZ

## 自動起動
echo "/usr/bin/fcitx-autostart" >> ~/.sommelierrc

## Fcitxの設定
Mozcを上に上げて、英語を削除

## でおｋ
