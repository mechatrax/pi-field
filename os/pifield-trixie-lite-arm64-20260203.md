# pifield-trixie-lite-arm64-20260203
Raspberry Pi OS (64-bit) Lite December 4th 2025 を元に変更を加えています。

## イメージファイル
イメージファイルは次のリンクからダウンロードできます。  
[pifield-trixie-lite-arm64-20260203.img.xz](https://mechatrax.com/data/pi-field/pifield-trixie-lite-arm64-20260203.img.xz)  

イメージファイルの SHA256 ハッシュ値は次のとおりです。
```
4d90432e54fe72442a2ad9f3b09b4acf2022e2a7f7ecaac31a8e60ab92e0d08d
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
  * パッケージを 20260203 時点の最新版に更新

## インストールパッケージ
  * Raspbian パッケージ  
    jo  
    jq  
    ufw

  * 独自パッケージ  
    4gpi-utils  
    4gpi-net-mods  
    4gpi-networkmanager  
    python-sleepi  
    sleepi3-utils  
    sleepi3-monitor  
    sleepi3-firmware  
    sleepi3-dkms

  * その他パッケージ  
    soracom

## 削除パッケージ  
  * 常駐プロセス削減のため削除  
    udisks2
