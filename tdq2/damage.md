---
layout: math
title: TDQ2 打撃ダメージ計算
---

# 打撃ダメージ計算

$$x\pm{}10\%$$は$$0.9x \sim{} 1.1x$$の範囲内のランダム値

* $$\mathrm{ATK}$$: 攻撃力現在値
* $$\mathrm{DEF}$$: 守備力現在値
* $$\mathrm{BONUS}$$: 魔物の弱点を突いたときの攻撃力ボーナス
	* ドラゴンキラーならドラゴン系に+30
	* ゾンビキラーならニフラム無耐性の魔物に+30
* $$\mathrm{ATK}_B = (\mathrm{ATK}\pm{}10\%) + \mathrm{BONUS}$$.


## 通常打撃

* $$\mathrm{DEF} \lt \mathrm{ATK}_B$$の場合

$$
	\dfrac{\sqrt{\mathrm{ATK}_B^{2}-\mathrm{DEF}^{2}}}{2}\pm{}10\%
$$

* $$\mathrm{ATK}_B \le \mathrm{DEF} \lt 2\cdot{}\mathrm{ATK}_B$$の場合

$$
	2\sqrt{2\cdot\mathrm{ATK}_B-\mathrm{DEF}}\pm{}10\%
$$

* $$2\cdot{}\mathrm{ATK}_B \le \mathrm{DEF} \lt 3\cdot{}\mathrm{ATK}_B$$の場合

$$
	0 \sim{} \sqrt{3\cdot\mathrm{ATK}_B-\mathrm{DEF}}
$$

* その他

$$
	0 \sim{} 1
$$


## 会心／痛恨

* 会心: $$\mathrm{ATK}_B$$
* 痛恨: $$\mathrm{ATK}_B\times{}0.75$$


## 気合溜め／力溜め

打撃系ダメージの２倍
