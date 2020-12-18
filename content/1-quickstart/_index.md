---
title: "クイックスタート"
date: 2019-02-11T11:33:07+09:00
draft: false
categories: ["", ""]
description: ""
image: ""
tags: ["", ""]
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
動画１
1. マテリアルを作成
2. シェーダーを `ArxCharacterShaders/Opaque` に設定
3. マテリアルインスペクタを開き、`Common/Main Texture` にテクスチャを設定
3. 完成！
### 3.少し設定に工夫をしてみる
#### 現実世界に沿った表現
動画２（無機物）
##### 金属と布の塗り分け例
#### イラストチックな表現の例
動画３（キャラクター：イラストチック）
1. シェーダーを`ArxCharacterShaders/Opaque`に設定
2. `Shading / Shadow`カテゴリで以下の設定をする
   1. `Border & Range`の`Border`を0.55に、`Range`を0に設定
   2. `Default color shading`を0に設定
   3. `Custom color shading`の`Use texture`をオフにし
      - `Hue Shift`を`-0.04`に設定
      - `Saturation`を`1.5`に設定
      - `Value`を`0.825`に設定
   4. `Ambient Light / Intensity`は`0.75`のまま
#### アニメチックな（セルルックな）表現の例
動画４（キャラクター：セルルック）
1. シェーダーを`ArxCharacterShaders/Outline/Opaque`に設定
2. `Outline`カテゴリで以下の設定をする
   1. ほげ
   2. ふが
3. `Shading / Shadow`カテゴリで以下の設定をする
   1. `Border & Range`の`Border`を0.55に、`Range`を0に設定
   2. `Default color shading`を0に設定
   3. `Custom color shading`の`Use texture`をオフにし
      - `Hue Shift`を`-0.04`に設定
      - `Saturation`を`1.5`に設定
      - `Value`を`0.825`に設定
   4. `Ambient Light / Intensity`は`0.75`のまま
#### 半透明のあるメッシュの表現の例
動画５（メッシュの一部に半透明なところがある）
1. シェーダーを `Fade` のつくものに変更
2. `Common/Main Texture`にアルファ情報のあるテクスチャを設定するか、  
色設定ダイアログでアルファ値を変更する

{{% notice info %}}
半透明に設定したメッシュを重ねた場合、予期しない描画結果を招く場合があります。`fade`を使ったマテリアルは最低限とし、可能な限り`AlphaCutout`または`Opaque`の利用を推奨します。
{{% /notice %}}