  usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|nickname|string|null: false|
|email|string|null: false, unique: true|
|password|string|null: false|
|last name|string|null: false|
|fastname|string|null: false|
|kana lastname|string|null: false|
|kana fastname|string|null: false|
|birthday|integer|null: false|
|phone|integer|null: false|
|address|string|null: false|
|profile|string| |
|image|string| |
|credit|integer| |
|place|string| |
|sales|integer| |
|sex|string|null: false|
|good|integer||
|sell|string|null: false|　
|purchase|string|null: false, foreign_key: true|

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