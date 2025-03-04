---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# OS なしオプション
{: #bm-no-os}

オペレーティング・システムなしのベア・メタル・サーバーを注文するためのオプションです。

## OS なしのベア・メタル・サーバーを注文する方法

[SoftLayer.com](https://www.softlayer.com) または[カスタマー・ポータル](https://control.softlayer.com)から、ベア・メタル・サーバーを注文することから開始します。

1. **「システム構成」>「オペレーティング・システム」**で**「その他」**を選択します。
2. **「オペレーティング・システムなし」**を選択します。

## OS なしのサーバーにオペレーティング・システムをインストールする方法

オペレーティング・システムなしのベア・メタル・サーバーにオペレーティング・システムをインストールする方法は 2 つあります。

### オプション 1: PXE サーバー

オペレーティング・システムなしのベア・メタル・サーバーは、PXE セットアップから OS をブートしてロードするようにセットアップできます (詳しくは、『[Preboot Execution Environment](https://ja.wikipedia.org/wiki/Preboot_Execution_Environment)』を参照)。 単に、PXE セットアップを持つネットワーク環境にベア・メタル・サーバーをデプロイして (通常、このために DHCP および TFTP デーモンを実行します)、ネットワーク・アダプターからブートするように新規ベア・メタル・サーバーの BIOS を構成します。 OS オプションが正しく機能しない場合、PXE セットアップをベアメタル・サーバーと同じ VLAN 内に配置するか、DHCP フォワードを使用する必要があります。

**注:** このオプションを機能させるには、スイッチ・ポートを基本モードで再グループ化するように要求するサポート・チケットをオープンしなければならない場合があります。これは、PXE プロトコルでは、リンク集約 (つまり、LACP です。『[Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation)』を参照) との互換性が不要であるためです。現在、リンク集約は、冗長性を提供するための標準的機能です。別のオプションとしては、未結合アップリンクを備えたサーバー (リンク集約なし) を注文し、OS のインストール後にそれらのアップリンクを冗長アップリンクに変更するという方法があります。

### オプション 2: IPMI デバイス

含まれている IPMI デバイスを介して ISO からブートすることで、オペレーティング・システムなしのベア・メタル・サーバーにオペレーティング・システムをインストールします。 ISO からのブートについて詳しくは、[ここ](mount-iso-bare-metal-server.html)をクリックしてください。
