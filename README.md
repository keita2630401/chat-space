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
|name|string|null: false, unique: true, index: true|
|e-mail|string|null: false, unique: true, index: true| 
### Association
- has_many :groups,through: :group_users
- has_many :groups_users
- has_many :messages

### groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false, unique: true, index: true|
|user_id|integer|null: false|
|group_id|integer|null: false|
### Association
- has_many :users,through: :group_users
- has_many :group_users
- has_many :messages

### messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string||
### Association
- belongs_to :user
- belongs_to :group