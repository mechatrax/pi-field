# pifield-bullseye-lite-armhf-20230511
Raspberry Pi OS (32-bit) Lite May 3rd 2023 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[pifield-bullseye-lite-armhf-20230511.img.xz](https://mechatrax.com/data/pi-field/pifield-bullseye-lite-armhf-20230511.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
454d5f325c320308d6150c4d16615bf404ab1abaf121155cde5077bae2d43322
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
  * Raspbian のパッケージを 20230511 時点の最新版に更新

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
    eject  
    mksh  
    gcc-8-base  
    gcc-9-base  
    libfribidi0  
    libident  
    libraspberrypi-doc  
    libreadline6  
    libsigc++-1.2-5c2  
    raspinfo  
    rng-tools
  
  * 常駐プロセス削減のため削除  
    triggerhappy  
    udisks2

