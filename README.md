## itemsテーブル
|Column|Type|Options|
|------|----|-------|
|image|string|null: false|
|name|string|null: false|
|description|text|null: false|
|large_category_id|references|null: false, foreign_key: true|
|medium_category_id|references|null: false, foreign_key: true|
|small_category_id|references|null: false, foreign_key: true|
|brand_id|references|null: false, foreign_key: true|
|condition_id|references|null: false, foreign_key: true|
|postage_id|references|null: false, foreign_key: true|
|shipping-days_id|references|null: false, foreign_key: true|
|price|integer|null: false|
|good_id|references|null: false, foreign_key: true|
|evaluation_id|references|null: false, foreign_key: true|
|status_id|references|null: false|


#Association
-belongs_to :user
-has_many :goods
-has_one :price







