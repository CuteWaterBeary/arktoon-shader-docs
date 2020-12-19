---
title: "シェーダーのバリエーション"
menuTitle: "バリエーション"
date: 2020-12-16T17:18:04+09:00
draft: false
categories: ["", ""]
description: "ArxCharacterShadersに含まれているシェーダーの種類を雑に紹介"
image: ""

author: ""
weight: 2
---

### 基本バリエーション
ArxCharacterShadersのベースとなるバリエーションです
#### ArxCharacterShaders/Opaque
Opaque = 不透明  
透明・半透明な部分が一切存在しないメッシュの場合、最も効率良く描画できるバリエーションです
#### ArxCharacterShaders/AlphaCutout
アルファ値でカットアウト（切り抜く）バリエーションです  
メッシュが不透明または完全に透明の２パターンで構成されている場合、これを利用してください
#### ArxCharacterShaders/Fade
メッシュに半透明な部分がある場合、こちらのバリエーションを使用してください  
{{% notice info %}}
`Opaque`や`AlphaCutout`と比較し、下記の制約があります  
・`Outline`バリエーション(後述)と併用できない  
・他のオブジェクトからの影（落ち影）を受けることができない  
・`Fade`を使った別のメッシュや他の半透明オブジェクトが同じ位置にあった場合に、描画に崩れが発生することがある
{{% /notice %}}
#### ArxCharacterShaders/FadeRefracted
基本的に `Fade` と同じですが、透けた先を屈折させることができるバリエーションです  
負荷はそこそこ高いため、使う場合は必要最小限に留めてください
### Stencilバリエーション
各基本バリエーションにステンシルバッファの操作機能を持たせたバリエーションです  
画面上に存在する見えないレイヤーみたいなもので、メッシュを描画する時にそのバッファを書き換えたり、書き換えた内容を参照したりすることで、  
複数のメッシュをまたいだ複雑な表現をすることができます。  
#### ArxCharacterShaders/_StencilWriter
ステンシルバッファを書き換えることのできるバリエーションです
#### ArxCharacterShaders/_StencilReader
ステンシルバッファを参照し、その内容に応じた描画の判断ができるバリエーションです
### EmissiveFreakバリエーション
上記の基本バリエーションとStencilバリエーションの各シェーダーに、様々なカラーエフェクトを設定する機能を持たせたバリエーションです
#### ArxCharacterShaders/_EmissiveFreak
特定のアニメーションが設定可能な２つのテクスチャを追加で利用できる、特殊バリエーションです
- 色&テクスチャを指定可能
- マスクを指定可能（後述のスクロール・深度等のエフェクトの影響を受けない。）
- 色&テクスチャをスクロール
- 色&テクスチャに奥行きをつける(Parallaxed Emissionと同じ効果)
- いくつかの発光エフェクトと、それぞれの適用度を設定可能（ブリージング・ブリンク）
- カラーシフトアニメーションを設定可能(Hue Shift)
### Outlineバリエーション
上記の基本・Stencil・EmissiveFreakの各シェーダーに、メッシュを囲むような外枠（アウトライン）を設定する機能を持たせたバリエーションです
{{% notice info %}}
`Outline`バリエーション以下には処理上の問題で`Fade`の基本バリエーションは含まれません  
（要望が多い場合は検討します）
{{% /notice %}}
#### ArxCharacterShaders/_Outline
上で説明した通りの内容です  
ここまで説明した`Fade`以外の全てのバリエーションが含まれます
<!-- {{< figure src="/images/variant_opaque.jpg" >}} -->
