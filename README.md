# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
# freemarket_sample_64a

# large_categoryテーブル

|Column|Type|Options|
|------|----|------|
|largecategory_id|reference|foreign_key: true, null: false|
|item_id|reference|foreign_key: true, null: false|

### Association
- belongs_to :item


## medium_categoryテーブル

|Column|Type|Options|
|------|----|------|
|mediumcategory_id|reference|foreign_key: true, null: false|
|item_id|reference|foreign_key: true, null: false|

### Association
- belongs_to :item


## small_categoryテーブル

|Column|Type|Options|
|------|----|-------|
|smallcategory_id|reference|foreign_key: true, null: false|
|item_id|reference|foreign_key: true, null: false|

### Association
- belongs_to :item


## brandテーブル

|Column|Type|Options|
|------|----|-------|
|brand_id|reference|foreign_key: true, null: false|
|item_id|reference|foreign_key: true, null: false|
|name|string|

### Association
- has_many :items

## placeテーブル

|Column|Type|Option|
|------|----|------|
|user_id|reference|foreign_key: true, null: false|
|place_id|reference|forign_key: true, null: false|
|postalcodes|integer|
|Prefectures|string|
|Municipalities|string|
|numbers|string|
|buildings|string|
|emergency contact|integer|

### Association
- belongs_to :user

## goodテーブル

|Column|Type|Option|
|------|----|------|
|good_id|reference|foreign_key: true, null: false|
|user_id|reference|foreign_key: true, null: false|
|item_id|reference|foreign_key: true, null: false|

### Association
- belongs_to :user
- belongs_to :item
