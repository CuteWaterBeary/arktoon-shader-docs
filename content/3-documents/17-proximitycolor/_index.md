---
title: "Proximity Color Override"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 170
---
### できること
カメラからの距離に応じて、指定された色または透明度を上書きしていくカテゴリです  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Begin(far)
変色を開始するカメラからの距離を設定します
#### End(near)
変色を終了する（完全に指定された色になる）カメラからの距離を設定します  
`Begin(far)`よりも高い値を設定すると、色の遷移が逆転します
#### Override Color
接近時の色をもともとの色からのHSV変換で指定します
#### Alpha
※Fade系バリエーションのみ  
接近時の透明度を、もともとの透明度からの乗算で指定します