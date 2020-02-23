##  usersテーブル

|Column|Type|Options|
|------|----|-------|
|item|references||
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
|profile|text| |
|image|string| |
|credit|references| |
|place|references| |
|sales|integer| |
|sex|string|null: false|
|good|references||
|sell|string|null: false|　
|buy|string|null: false, foreign_key: true|

  Association
- be_longs :place
- has_many :items
- has_many :goods
- has_many :sells
- has_many :buys

##  conditionテーブル

|Column|Type|Options|
|------|----|-------|
|name|string| |
|item|references| |

  Association
- has_many :items

##  postageテーブル

|Column|Type|Options|
|------|----|-------|
|item|references| |
|send|string| |

  Association
- has_many :items