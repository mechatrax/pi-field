# pifield-bookworm-lite-arm64-20241111
Raspberry Pi OS (64-bit) Lite October 22nd 2024 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[pifield-bookworm-lite-arm64-20241111.img.xz](https://mechatrax.com/data/pi-field/pifield-bookworm-lite-arm64-20241111.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
e3b6fe1003a4c944d61c286eeac3019c9cc2ddbf9b265a9cdb53ca41e33db441
```

## 変更内容
Raspberry Pi OS からの変更内容は次のとおりです。
  * 4GPi 用パッケージをインストール
  * ファイアウォールに ufw を使用（デフォルトは許可、wwan0 と ppp0 のみ受信拒否）
  * シリアルコンソールを有効化
  * rootfs で ext4 の 64bit オプションを有効化
  * ハードウェアウォッチドッグタイマの監視に systemd を使用
  * APT::Periodic の無効化
  * avahi-daemon で ppp0 と wwan0 を無視
  * slee-Pi3 用パッケージをインストール
  * NetworkManager の radio 設定にて WiFi を無効化
  * パッケージを 20241111 時点の最新版に更新

## インストールパッケージ
  * Raspbian パッケージ  
    jo  
    jq  
    ufw

  * 独自パッケージ  
    4gpi-utils  
    4gpi-net-mods  
    4gpi-networkmanager  
    mechatrax-archive-keyring  
    python-sleepi  
    sleepi3-utils  
    sleepi3-monitor  
    sleepi3-firmware

  * その他パッケージ  
    soracom

## 削除パッケージ  
  * 常駐プロセス削減のため削除  
    triggerhappy  
    udisks2

