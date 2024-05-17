# pifield-bookworm-lite-arm64-20240517
Raspberry Pi OS (64-bit) Lite March 15th 2024 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[pifield-bookworm-lite-arm64-20240517.img.xz](https://mechatrax.com/data/pi-field/pifield-bookworm-lite-arm64-20240517.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
63997948ce8a29134cff750ee7ca942639e65669e8ead8f36bd6952eac9b5fa9
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
  * パッケージを 20240517 時点の最新版に更新

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

