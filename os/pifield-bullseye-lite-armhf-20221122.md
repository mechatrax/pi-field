# pifield-bullseye-lite-armhf-20221122
Raspberry Pi OS (32-bit) Lite September 22nd 2022 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[pifield-bullseye-lite-armhf-20221122.img.xz](https://mechatrax.com/data/pi-field/pifield-bullseye-lite-armhf-20221122.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
a60acf50602fb932b1d8a90c1f7216e7149281cdaae9e977731b8f799b446453
```

## 変更内容
Raspberry Pi OS からの変更内容は次のとおりです。
  * 4GPi 用パッケージをインストール
  * 4G/LTE ネットワークの管理に NetworkManager を使用
  * ファイアウォールに ufw を使用（デフォルトは許可、wwan0 と ppp0 のみ受信拒否）
  * シリアルコンソールを有効化
  * rootfs で ext4 の 64bit オプションを有効化
  * ハードウェアウォッチドッグタイマの監視に systemd を使用
  * APT::Periodic の無効化
  * avahi-daemon で ppp0 と wwan0 を無視
  * slee-Pi3 用パッケージをインストール
  * Raspbian のパッケージを 20221122 時点の最新版に更新

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
  * 不要なライブラリ等を削除  
    gcc-8-base  
    gcc-9-base  
    libfribidi0  
    libident  
    libraspberrypi-doc  
    libreadline6  
    libsigc++-1.2-5c2  
    rng-tools
  
  * 常駐プロセス削減のため削除  
    triggerhappy  
    udisks2

