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
|name|string|null: false, index: true|
|e-mail|string|null: false, index: true| 
### Association
- has_many :groups
- has_many :messages

### groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false|
|group_id|integer|null: false|
### Association
- has_many :messages
- belongs_to :user


### messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
### Association
- belongs_to :user
- belongs_to :group