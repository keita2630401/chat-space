### groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user



### usersテーブル
|column|Type|Options|
|------|----|-------|
|name|string|null: false, index|
|e-mail|string|null: false, index| 
### Association
-
-


### groupsテーブル
|Column|Type|Options|
|------|----|-------|
||||
||||
### Association




### messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|string|null:false|
|image|string|null:false|
### Association
- belongs_to :user
- belongs_to :group