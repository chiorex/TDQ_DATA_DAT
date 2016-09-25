---
layout: math
title: TDQ1 打撃ダメージ計算
---

# {{ page.title }}

※ \\( x\pm{}10\% \\) は \\( 0.9x \sim{} 1.1x \\) の範囲内のランダム値を表すものとする

* \\( \mathrm{ATK}= \\) 現在の攻撃力
* \\( \mathrm{DEF}= \\) 現在の守備力
* \\( \mathrm{ATK}_B = (\mathrm{ATK}\pm{}10\%) \\).


## 通常打撃

* \\( \mathrm{ATK}_B \gt \mathrm{DEF} \\)の場合
\\[
	\dfrac{\sqrt{\mathrm{ATK}_B^{2}-\mathrm{DEF}^{2}}}{2}\pm{}10\%
\\]
* \\( 2\cdot{}\mathrm{ATK}_B \gt \mathrm{DEF} \ge \mathrm{ATK}_B \\)の場合
\\[
	2\sqrt{2\cdot\mathrm{ATK}_B-\mathrm{DEF}}\pm{}10\%
\\]
* \\( 3\cdot{}\mathrm{ATK}_B \gt \mathrm{DEF} \ge 2\cdot{}\mathrm{ATK}_B\\)の場合
\\[
	0 \sim{} \sqrt{3\cdot\mathrm{ATK}_B-\mathrm{DEF}}
\\]
* その他
\\[
	0 \sim{} 1
\\]


## 会心／痛恨

* 会心: \\( \mathrm{ATK}_B \\)
* 痛恨: \\( \mathrm{ATK}_B \\)

※バイキルトの効果は載らない。


## 気合溜め／力溜め

打撃ダメージが２倍になる。
次の行動が通常打撃に確定する。