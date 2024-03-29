---
layout: math
title: 打撃ダメージ推定
update: 2024-03-07
---

* $\mathrm{ATK}=$ 現在の攻撃力
* $\mathrm{DEF}=$ 現在の守備力
* $\mathrm{BONUS}=$ 魔物の弱点を突いたときの攻撃力ボーナス
	* ドラゴンキラーならドラゴン系に+30
	* ゾンビキラーならニフラム被弾Lvが◎の魔物に+30
	* 理力の杖でMP不足のときは-25
* $\mathrm{ATK}_B = \mathrm{ATK} + \mathrm{BONUS}$.


## 打撃ダメージ見積もり

AIは下記 $f_{\mathrm{min}}$ を使用（ランダム要素込みで取り得る最小ダメージで見積もる）

$$
	\begin{align}
	f_{\mathrm{min}}(\mathrm{ATK}) & = \min_{0.9\mathrm{ATK} \le x \le 1.1\mathrm{ATK}} f(x) \\ \\
	f(\mathrm{ATK}) & = \begin{cases}
		\dfrac{\sqrt{\mathrm{ATK}_B^{2}-\mathrm{DEF}^{2}}}{2}\times{}0.9	&	(\mathrm{ATK}_B \gt \mathrm{DEF}) \\ \\
		2\sqrt{2\cdot\mathrm{ATK}_B-\mathrm{DEF}}\times{}0.9				&	(2\cdot{}\mathrm{ATK}_B \gt \mathrm{DEF} \ge \mathrm{ATK}_B) \\ \\
		0																	&	(\mathrm{DEF} \ge 2\cdot{}\mathrm{ATK}_B)
	\end{cases}
	\end{align}
$$

* 標的種族に打撃を与えた実績がなければダメージ量を更に半分で見積もる（学習領域の[仲間共通エリア](ai_save.md)を参照）

### メモ

* $f_{\mathrm{min}}(\mathrm{ATK}) \neq f(0.9\mathrm{ATK})$.


## 会心／痛恨

* 会心／痛恨は考慮されない


## バイキルト

* 現在の攻撃力($\mathrm{ATK}$)が２倍になる


## 気合溜め／力溜め

* 打撃ダメージ見積もりが２倍になる


## はぐれメタルの剣

* メタル系に２倍ダメージになっていない（[バグ](bug.md#hagumetaken)）


## ブーメラン投げ

* 使うと１グループに __打撃攻撃__
* 現在の攻撃力($\mathrm{ATK}$)を以下の武器固有値に置き換えた打撃ダメージ見積もりが適用される

| 武器             | $\mathrm{ATK}$ |
|:----------------:|:---:|
| ブーメラン       |  15 |
| バトルブーメラン |  50 |

* バイキルト効果は載らない
* AIは気合溜め／力溜めを標的全員に適用する？


## 毒針

* 打撃ダメージ見積もりは１固定
* 急所突きは考慮されない


## 魔神の金槌

* 会心／ミス率は考慮されない


## 隼の剣／キラーピアス

* 打撃ダメージ見積もりを２倍で換算


## 武器の持ち替え（道具-装備）

* 現在の攻撃力($\mathrm{ATK}$)を __力＋武器の威力__ に置き換えた打撃ダメージ見積もりが適用される

### メモ

* AIは武器の持ち替えでもバイキルトの攻撃力２倍効果を適用して打撃ダメージを見積もる
* 実際の打撃ダメージ計算では武器を持ち替えるとバイキルトの攻撃力２倍効果が適用されない（バグ）


## 関連項目

* [打撃ダメージ計算](damage.md)
* [学習内容（セーブデータ）](ai_save.md)
