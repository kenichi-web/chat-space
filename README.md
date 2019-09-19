# README
# chat-space DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|name|string|null: false|
### association
- has_many :tweets


## tweetsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### association
- belongs_to :user
- has_many :comments


## groupテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### association
- belongs_to :group
- belongs_to :user
 