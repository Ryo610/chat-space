#　DB設計

## users_table

|Column|Type|Options|
|------|----|-------|
|name|string|index: true, null: false, unique: true|
|mail|string|null: false|

### Association
_ has_many :groups, through: memberes
_ has_many :messages
_ has_many :members