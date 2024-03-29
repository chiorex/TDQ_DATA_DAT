---
layout: math
title: 呪文・ブレスダメージ軽減
update: 2024-03-07
---

※ $x\pm{}10\\%$ は $0.9x \sim{} 1.1x$ の範囲内のランダム値を表すものとする

__呪文・ブレスダメージ＝(威力±10%)×軽減率__

* 威力は[特技一覧](skill_id.md)を参照


## 軽減率

軽減率は重複する

|                  | デ | ヒ | バ | イ | ギ | メ | 炎 | 吹 | 備考 |
|:-----------------|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:-----|
| 敵→味方         | 75%| 75%| 75%| 75%| 75%| 75%| -  | -  | 魔物の呪文を被弾した場合 |
| 魔法の法衣       | 75%| 75%| 75%| 75%| 75%| 75%| -  | -  |
| アラキの法衣     | 75%| 75%| 75%| 75%| 75%| 75%| 75%| 75%|
| 水の羽衣         | -  | -  | -  | 75%| 75%| 75%| 75%| -  | 炎系呪文／ブレスのみ |
| ドラゴンメイル   | -  | -  | -  | -  | -  | -  | 75%| 75%|
| ドラゴンシールド | -  | -  | -  | -  | -  | -  | 75%| 75%|
| ミラーシールド   | 75%| 75%| 75%| 75%| 75%| 75%| -  | -  | 25%ダメージ反射 |
| カロシスの盾     | 75%| 75%| 75%| 75%| 75%| 75%| -  | -  | 1/3の確率でしか軽減しない（軽減時25%ダメージ反射） |
| フバーハ         | -  | -  | -  | -  | -  | -  | 50%| 50%|
| 炎系ブレス耐性   | -  | -  | -  | -  | -  | -  | 50%| -  | 被弾Lvが メラ×ギラ× または メラ×ギラ○ |
| 吹雪系ブレス耐性 | -  | -  | -  | -  | -  | -  | -  | 50%| 被弾Lvが イオ× または イオ○ |
| 安らぎのローブ   | 75%| 75%| 75%| 75%| 75%| 75%| 75%| 75%| 安らぎ状態のみ（麻痺または寝る） |


### メモ

* 魔法の鎧に呪文／ブレス軽減効果がない


## 例外

* 守備力1000超の場合はブレスダメージが1固定
* アラキの法衣は何らかの特技ダメージを半減するかもしれない（詳細不明）
* ブレス無効になる条件が存在する？（詳細不明）


## 関連項目

* [特技一覧](skill_id.md)
* [呪文命中率](spell_hit_rate.md)
