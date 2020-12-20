---
title: "Shading / Shadow"
menuTitle: "Shading / Shadow"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 60
---
### できること
マテリアルの陰に関する調整ができます  
陰の強さだけではなく、陰の諧調、また陰にかかったテクスチャの色などを指定できます  
（※作例画像/gif動画準備中）

<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Border & Range
メッシュ上のある地点が「陰」かどうかを決定します
{{% notice info %}}
「他のオブジェクトから受ける影（落ち影）」についてはこちらの設定に関係なく受けます  
影を受けたくない場合は、`Skinned Mesh Renderer`の`Receive Shadows`のチェックを外してください
{{% /notice %}}
##### Border
陰の境目となる地点を設定します  
`0`でメッシュ上から陰が消えます（※落ち影は消えません）
##### Range & Mask
陰の境目をどの程度ぼかすかを設定します  
ぼけている部分の光～陰の推移は後述の`Shading Ramp`で設定します
##### Ramp in Range
`Border & Range`で設定した陰の境目の範囲に対し、  
どのような光の受け方をさせるかを段階的(Ramp)なテクスチャで設定します  
{{% notice note %}}
よく分からない場合は`Revert`ボタンをクリックし、ArxCharacterShadersに同梱されている各種Rampテクスチャを割り当ててみてください
{{% /notice %}}
#### Shadow Receiving
※ `Fade`以外のバリエーションで表示  
他のオブジェクトから受ける「影（落ち影）」の強度をスライダー＋マスクテクスチャで指定します
{{% notice note %}}
落ち影はマテリアルが設定されているオブジェクトの`Mesh Renderer`の`Receive Shadows`がオンであること、  
Sceneに配置されたリアルタイムライトの`Shadow Type`が`Hard Shadows`または`Soft Shadows`であることで発生します  
{{% /notice %}}
{{% notice info %}}
そもそもメッシュ全体で影を受けたく無い場合は、このスライダーを0にするより  
`Mesh Renderer`の`Receive Shadows`をオフにすれば低コストに済みます
{{% /notice %}}
#### Default color shading
##### Strength & Mask
`Border & Range`により決定した陰部分に適用する陰色の強度を設定します  
ここで用いられる陰の色は空間の色を重視した無機的なものであるため、  
任意の色を出したい場合は `0` を設定し、後述の `Custom color shading`を利用してください
#### Custom color shading
`Border & Range`により決定した陰部分に適用する色を直接設定します
##### Use Texture
陰用のテクスチャがある場合は、こちらをオンにすることで、テクスチャを設定できます  
テクスチャを使わない場合は`Hue Shift/Saturation/Value`の各スライダーで  
基本色（`Common`で設定した色）から変更した色を陰色として設定します
#### Ambient Light
##### Intensity
陰側に空間の色をどの程度加味させるかを設定します  
目に見えた変化はあまりないので、これといった拘りが無い場合は基本的にデフォルトの`0.75`で良いと思います  