---
title: "クイックスタート"
date: 2019-02-11T11:33:07+09:00
draft: false
categories: ["", ""]
description: "ArxCharacterShaderのダウンロードから最初のマテリアル設定までの流れと、いくつかの設定例を紹介"
image: ""

author: ""
weight: 1
---
### 1.ダウンロード＆インポート
[BOOTHのページ](https://booth.pm/ja/items/2493539)より、最新版をダウンロードし、  
お使いのUnityプロジェクトにインポートしてください
{{% notice tip %}}
既にArxCharacterShadersが存在する場合、一度プロジェクト上のArxCharacterShadersフォルダを削除の上、
再インポートすることを推奨します。
{{% /notice %}}
### 2.マテリアルの設定
{{< figure src="wear.gif" >}}
1. マテリアルを作成
2. シェーダーを `ArxCharacterShaders/Opaque` に設定
3. マテリアルインスペクタを開き、`Common/Main Texture` にテクスチャを設定
3. メッシュに適用して、完成！
### 3.少し設定に工夫をしてみる
ArxCharacterShadersには様々な機能があります。  
その中の一部をご紹介
{{% children style="h4" description="true" %}}