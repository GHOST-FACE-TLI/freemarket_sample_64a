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
|largecategory_id|integer|foreign_key: true|
|item_id|integer|foreign_key: true|

## medium_categoryテーブル

|Column|Type|Options|
|------|----|------|
|mediumcategory_id|integer|foreign_key: true|
|item_id|integer|foreign_key: true|

## small_categoryテーブル

|Column|Type|Options|
|------|----|-------|
|smallcategory_id|integer|foreign_key: true|
|item_id|integer|foreign_key: true|


## brandテーブル

|Column|Type|Options|
|------|----|-------|
|brand_id|integer|foreign_key: true|
|item_id|integer|foreign_key: true|
|name|string|


## placeテーブル

|Column|Type|Option|
|------|----|------|
|user_id|integer|foreign_key: true|
|place_id|integer|forign_key: true|
|postalcodes|integer|
|Prefectures|string|
|Municipalities|string|
|numbers|string|
|buildings|string|
|emergency contact|integer|

## goodテーブル

|Column|Type|Option|
|------|----|------|
|good_id|integer|foreign_key: true|
|user_id|integer|foreign_key: true|
|item_id|integer|foreign_key: true|