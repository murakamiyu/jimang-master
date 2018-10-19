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

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false, unique: true|
|introduction|string|
|image|string|
|native|string|null: false|
|present|string|null: false|

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|area|string|null: false|

## user_groupテーブル

|Column|Type|Options|
|------|-----|------|
|user_id|integer|foregin_key: true|
|group_id|integer|forgin_key: true|

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|
|user_id|integer|foregin_key: true|
|group_id|integer|foregin_key: true|

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|comment|string|null: false|
|user_id|integer|foregin_key: true|
|group_id|integer|foregin_key: true|
|message_id|integer|foregin_key: true|
|image|image|

