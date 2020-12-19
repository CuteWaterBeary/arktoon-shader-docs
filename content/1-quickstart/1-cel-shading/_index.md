---
title: "陰の設定"
date: 2019-02-11T11:33:07+09:00
draft: false
categories: ["", ""]
description: "ぱきっとセルルックに決まった陰と、柔らかい陰の設定例"
image: ""

author: ""
weight: 1
---
### アニメチックな（セルルックな）表現の例
{{< figure src="cel-shading.gif" >}}
1. シェーダーを`ArxCharacterShaders/Outline/Opaque`に設定
2. `Outline`カテゴリで以下の設定をする
   1. `Width & Mask` を `0.1`～`0.3`
   2. `Texture & Color`の`Base color mix`を`0.5`程度
3. `Shading / Shadow`カテゴリで以下の設定をする
   1. `Border & Range`の`Border`を`0.55`に、`Range`を`0`に設定
   2. `Default color shading`を`0`に設定
   3. `Custom color shading`の`Use texture`をオフにし
      - `Hue Shift`を`-0.04`に設定
      - `Saturation`を`1.5`に設定
      - `Value`を`0.825`に設定
   4. `Ambient Light / Intensity`は`0.75`のまま

### 柔らめのイラストチックな表現例
{{< figure src="yawaraka-shading.gif" >}}
上の[アニメチックな（セルルックな）表現の例]({{< ref "#アニメチックなセルルックな表現の例" >}})から  
`Shading / Shadow`カテゴリの`Border & Range`の`Border`を`0.65`に、`Range`を`0.75`に設定すると、  
柔らかいイラストチックな印象になります