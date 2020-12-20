---
title: "Stencil Writer / Reader"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 140
---
## Stencil Writer
### できること
ステンシルバッファを書き込むシェーダーです  
`Stencil Reader`や、その他ステンシルを読み取るシェーダーの利用が前提になります。
{{% notice info %}}
AXCSのStencilWriter系シェーダーのRenderQueueは一律`AlphaTest(2450)`です
{{% /notice %}}
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Stencil Number
ステンシルバッファに書き込む値
#### Stencil Mask & Range
メッシュの一部だけステンシルを書き込む場合はマスクテクスチャを指定  
またスライダーで境界を微調整できます
#### Alpha(Dither)
ステンシルバッファの透明度を指定します  
ステンシル自体に透明度の概念はなく、ディザリング加工で疑似的に半透明を表現します
## Stencil Reader
書き込まれているステンシルバッファを読み取り、プロパティで指定した計算結果に基づいて描画の有無を決めて描画します  
`Stencil Writer`またはその他ステンシル操作系のシェーダーの利用が前提です
{{% notice info %}}
AXCSのStencilReader系シェーダーのRenderQueueは以下の通りとなっており、  
これらより前のRenderQueueで描画されたステンシルバッファを参照できます  
・`*/_StencilReader/AlphaCutout`: AlphaTest + 1 (2451)  
・`*/_StencilReader/Fade`: Transparent-100 (2900)  
・`*/_StencilReader/DoubleFade`: Transparent-100 (2900)  
・`*/_StencilReader/FadeRefracted`: Transparent (3000)
{{% /notice %}}
### 各項目について
#### Stencil Number
ステンシルバッファとの計算に使う数値を指定します
#### Compare Action
`Stencil Number`で指定した値と、描画地点にあるステンシルバッファを比較する式を指定します  
指定した式が成立する場合に、本マテリアルの描画が実施され、成立しない場合はマテリアルは描画されません  
以下は計算式の一例です
- NotEqual: `Stencil Number`の値とバッファの値が異なる場合に描画します
- Equal: `Stencil Number`の値とバッファの値が同じ場合に描画します
- Always: 常に描画します
- Never: 常に描画しません
- Greater: `Stencil Number`の値がバッファの値よりも大きい場合に描画します
- Less: `Stencil Number`の値がバッファの値よりも小さい場合に描画します