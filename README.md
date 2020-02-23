## itemsテーブル
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
- has_many :evaluations
- belongs_to :status








