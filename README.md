## itemsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, presence: true, index:true|
|description|text|null: false, presence: true|
|large_category|references|null: false, foreign_key: true, presence: true, index:true|
|medium_category|references|null: false, foreign_key: true, presence: true, index:true|
|small_category|references|null: false, foreign_key: true, presence: true, index:true|
|brand|references|null: false, foreign_key: true, index:true|
|condition|references|null: false, foreign_key: true, presence: true, index:true|
|postage|references|null: false, foreign_key: true, presence: true, index:true|
|shipping-day|references|null: false, foreign_key: true, presence: true|
|price|integer|null: false, presence: true, index:true|
|good|references|null: false, foreign_key: true|
|evaluation|references|null: false, foreign_key: true|
|status|references|null: false|
|seller|references|null: false, foreign_key: { to_table: :users }|
|buyer|references|foreign_key: { to_table: :users }|
|seller|references|null: false, foreign_key: { to_table: :users }|
|buyer|references|null: false, foreign_key: { to_table: :users }|
|dealing_stage|references|null: false, foreign_key: true|


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
- has_many :users, through: :goods
- has_many :images
- has_one :dealing_stage


## imagesテーブル
|Column|Type|Options|
|------|----|-------|
|item|references|null: false, foreign_key: true|
|image|string|null: false|

## Association
- belongs_to :item








