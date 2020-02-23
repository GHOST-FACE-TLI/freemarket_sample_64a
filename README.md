  usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|nickname|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false|
|last name｜string｜null: false｜
<!-- 苗字 -->
|name|string｜null: false｜
<!-- 下の名前 -->
|kana|string｜null: false｜
<!-- カタカナ -->
|birthday|integer|null: false｜
|phone|integer|null: false|
|address|string|null: false|
|profile|string| |
|image|string| |
<!-- 写真 -->
|credit|integer| |
<!-- クレジットカード -->
|place|string| |
<!-- 発送元 -->
|sales|integer| |
<!-- 売り上げ -->
|sex|string|null: false|
|good|integer||
<!-- いいね -->
|sell|string|null: false|　
<!-- 出品 -->
|purchase|string|null: false, foreign_key: true|
<!-- 購入者 -->

  Association
- has_many :item
- has_many :good
- has_many :sell
- has_many :buy

  conditionテーブル

|Column|Type|Options|
|------|----|-------|
|condition_id|integer| |
|name|string| |
|item_id|integer| |

  Association
- has_many :item

  postageテーブル

|Column|Type|Options|
|------|----|-------|
|item_id|integer| |
|postage_id|integer| |
|price|integer| |

  Association
- has_many :item