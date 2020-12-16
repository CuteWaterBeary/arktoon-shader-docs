---
title: "シェーダーのバリエーション"
menuTitle: "バリエーション"
date: 2020-12-16T17:18:04+09:00
draft: false
categories: ["", ""]
description: ""
image: ""
tags: ["", ""]
author: ""
weight: 10
---

## 基本バリエーション
ArxCharacterShadersのベースとなるバリエーションです
### ArxCharacterShaders/Opaque
ふが
### ArxCharacterShaders/AlphaCutout
ふが
### ArxCharacterShaders/Fade
ふが
### ArxCharacterShaders/FadeRefracted
ふが
## Stencilバリエーション
各基本バリエーションにステンシルバッファの操作機能を持たせたバリエーションです
### ArxCharacterShaders/_StencilWriter
ふが
### ArxCharacterShaders/_StencilReader
ふが
## EmissiveFreakバリエーション
基本バリエーション・Stencilバリエーションの各シェーダーに、様々なカラーエフェクトを設定する機能を持たせたバリエーションです
### ArxCharacterShaders/_EmissiveFreak
ふが
下記機能が設定できる、アニメーション付きの発光テクスチャを2枚使用できる、特殊バリエーションです。  

- 色&テクスチャを指定可能
- マスクを指定可能（後述のスクロール・深度等のエフェクトの影響を受けない。）
- 色&テクスチャをスクロール
- 色&テクスチャに奥行きをつける(Parallaxed Emissionと同じ効果)
- いくつかの発光エフェクトと、それぞれの適用度を設定可能（ブリージング・ブリンク）
- カラーシフトアニメーションを設定可能(Hue Shift)
## Outlineバリエーション
ここまで説明してきた全てのシェーダーに、メッシュを囲むような外枠（アウトライン）を設定する機能を持たせたバリエーションです
## ArxCharacterShaders/_Outline
へげ
{{< figure src="/images/variant_opaque.jpg" >}}
