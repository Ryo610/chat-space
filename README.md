# DB設計

## users table

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|

### Association
- has_many :groups, through: users_groupes
- has_many :messages
- has_many :users_groupes

## groupes table

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|string|null: false|

### Association
- has_many :users, through: users_groupes
- has_many :messages
- has_many :users_groupes

## messages table

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|images|string|null: false|
|group_id|integur|null: false|
|user_id|integur|null: false|

### Association
- has_many :groups
- has_many :users

## users_groupes table

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|string|null: false|

### Association
- has_many :groups
- has_many :users