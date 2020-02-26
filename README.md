# README

#  usersテーブル
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
|great|references|foreign_key: { to_table: :evaluation } |
|natural|references|foreign_key: { to_table: :evaluation } |
|bad|references|foreign_key: { to_table: :evaluation } |

##  Association
- belongs_to :place
- has_many :items
- has_many :goods
- has_many :sells
- has_many :buys
- has_many :evaluations


# itemsテーブル
|Column|Type|Options|
|------|----|-------|
|image|string|null: false|
|name|string|null: false|
|description|text|null: false|
|large_category|references|null: false, foreign_key: true|
|medium_category|references|null: false, foreign_key: true|
|small_category|references|null: false, foreign_key: true|
|brand|references|null: false, foreign_key: true|
|condition|references|null: false, foreign_key: true|
|postage|references|null: false, foreign_key: true|
|shipping-day|references|null: false, foreign_key: true|
|price|integer|null: false|
|good|references|null: false, foreign_key: true|
|evaluation|references|null: false, foreign_key: true|
|status|references|null: false|
|seller|references|null: false, foreign_key: { to_table: :users }|
|buyer|references|foreign_key: { to_table: :users }|


## Association
- belongs_to :large_category
- belongs_to :medium_category
- belongs_to :small_category
- belongs_to :brand
- belongs_to :condition
- belongs_to :postage
- belongs_to :shipping-day
- belongs_to :user
- has_many :goods
- belongs_to :evaluation
- belongs_to :status

#  conditionテーブル

|Column|Type|Options|
|------|----|-------|
|name|string| |
|item|references| |

##  Association
- has_many :items

#  postageテーブル

|Column|Type|Options|
|------|----|-------|
|item|references| |
|send|string| |

## Association
- has_many :items

# large_categoryテーブル

|Column|Type|Options|
|------|----|------|
|item|reference|foreign_key: true, null: false|
|name|string|

## Association
- has_many :items


# medium_categoryテーブル

|Column|Type|Options|
|------|----|------|
|item|reference|foreign_key: true, null: false|
|name|string|

## Association
- has_many :items


# small_categoryテーブル

|Column|Type|Options|
|------|----|-------|
|item|reference|foreign_key: true, null: false|
|name|string|

## Association
- has_many :items


# brandテーブル

|Column|Type|Options|
|------|----|-------|
|item|reference|foreign_key: true, null: false|
|name|string|

## Association
- has_many :items

# placeテーブル

|Column|Type|Option|
|------|----|------|
|user|reference|foreign_key: true, null: false|
|postalcodes|integer|
|Prefectures|string|
|Municipalities|string|
|numbers|string|
|buildings|string|
|emergency contact|integer|

## Association
- belongs_to :user

# goodテーブル

|Column|Type|Option|
|------|----|------|
|user|reference|foreign_key: true, null: false|
|item|reference|foreign_key: true, null: false|

## Association
- belongs_to :user
- belongs_to :item

# evaluationテーブル

|Column|Type|Option|
|------|----|------|
|user|reference|foreign_key: true, null: false|
|item|reference|foreign_key: true, null: false|
|evaluation||

## Association
- has_many :users
- has_many :items
