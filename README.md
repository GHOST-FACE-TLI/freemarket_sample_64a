## itemsテーブル
|Column|Type|Options|
|------|----|-------|

<!-- 枚数制限 -->
|image|string|null: false|
|name|string|null: false|
|description|text|null: false|
|category_id|integer|null: false, foreign_key: true|
|brand_id|integer|null: false, foreign_key: true|
|condition_id|integer|null: false, foreign_key: true|
|postage_id|integer|null: false, foreign_key: true|
<!-- 発送元・発送先住所 -->
|place_id|integer|null: false, foreign_key: true|
|shipping-days_id|integer|null: false, foreign_key: true|
|price|integer|null: false|
<!-- 中間テーブル？ -->
|good_id|integer|
|evaluation_id|integer|null: false|







<!-- 商品登録日(自動生成のため不要) -->
