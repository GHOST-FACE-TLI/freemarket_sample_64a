 usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|nickname|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false|
|last name｜string｜null: false｜
|name|string｜null: false｜
|kana|string｜null: false｜
|birthday|integer|null: false｜
|phone|integer|null: false|
|address|string|null: false|
|profile|string| |
|image|string| |
<!-- 写真 -->
|credit|integer| |
<!-- クレジットカード -->
|shipping origin|string| |
<!-- 発送元 -->
|sales|integer| |
<!-- 売り上げ -->
|sex|string|null: false|
|good|integer||
<!-- いいね -->
|exhibition|string|null: false|　
<!-- 出品 -->
|purchase|string|null: false, foreign_key: true|
<!-- 購入者 -->

  Association
- has_many :item
- belongs_to :good
