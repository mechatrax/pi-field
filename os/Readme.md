# OS イメージ
ここでは、Pi-field 用の SD カードの OS イメージに関する技術資料等を公開しています。

## 概要
OS には Raspberry Pi OS (Raspbian) を採用し、Pi-field の動作に必要なツールをセットアップしています。

4G/LTE のネットワークの管理に NetworkManager を使用しています。  
使用する SIM に応じて[接続設定](https://github.com/mechatrax/4gpi/wiki/%E3%81%9D%E3%81%AE%E4%BB%96#%E6%8E%A5%E7%B6%9A%E8%A8%AD%E5%AE%9A)を行ってください。

ファイアウォールに ufw を使用しています。  
標準で 4GPi の受信ポートをブロックしています。

詳細についてはリリースノートのリンク先を参照してください。

ansible を使用して同等の環境を構築することもできます。  
詳細はリンク先を参照してください。  
https://github.com/mechatrax/ansible-mechatrax-playbook

## 初期ログイン情報カード
Pi-field 用 microSD カードに付属している初期ログイン情報カードの .pdf ファイルを公開しています。  
次のリンクから直接ファイルをダウンロードできます。  
[初期ログイン情報カード](../../../raw/main/os/login.pdf)

## リリースノート
Pi-field 用 microSD カードにインストールされている OS イメージのリリースノートを公開しています。

* ### pifield-bullseye-lite-20220208
  2022/02/08  以降に出荷された製品には本リリースの OS イメージがインストールされています。  
  詳細は、[pifield-bullseye-lite-20220208.md](./pifield-bullseye-lite-20220208.md) を参照してください。

* ### pifield-bullseye-lite-20220127
  2022/01/27 以降に出荷された製品には本リリースの OS イメージがインストールされています。  
  詳細は、[pifield-bullseye-lite-20220127.md](./pifield-bullseye-lite-20220127.md) を参照してください。  
