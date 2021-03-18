[KARTE Android SDK v1](index)

# `KarteAttributes`

> Class | v1.5.2 -

`KarteAttributes` クラスは、KARTE が自動で処理するプッシュ通知のデータを取り扱うクラスです。

### Package

`io.karte.android.tracker.firebase`

### Inherits From

None

### Conforms To

None

## `getBody()`

> Instance Method | v1.5.2 -

プッシュ通知の本文を返します。これはプッシュ通知アクションに指定した静的変数の `body` に対応しています。

### Declaration

```java
public String getBody();
```

### Return Value

プッシュ通知の本文を返します。

## `getBigImage()`

> Instance Method | v1.5.2 -

プッシュ通知の画像を返します。これはプッシュ通知アクションに指定した静的変数の `attachment_url` に対応しています。

### Declaration

```java
public Bitmap getBigImage();
```

### Return Value

プッシュ通知の画像を返します。

## `getLink()`

> Instance Method | v1.5.2 -

プッシュ通知のクリックリンクを返します。これはプッシュ通知アクションに指定した静的変数の `url` に対応しています。

### Declaration

```java
public String getLink();
```

### Return Value

プッシュ通知のクリックリンクを返します。

## `getChannel()`

> Instance Method | v1.5.2 -

プッシュ通知のチャンネル ID を返します。これはプッシュ通知アクションに指定した静的変数の `android_channel_id` に対応しています。

### Declaration

```java
public String getChannel();
```

### Return Value

プッシュ通知のチャンネル ID を返します。

## `getSound()`

> Instance Method | v1.5.2 -

プッシュ通知の通知音可否を返します。これはプッシュ通知アクションに指定した静的変数の `sound_for_android` に対応しています。

### Declaration

```java
public boolean getSound();
```

### Return Value

プッシュ通知の通知音可否を返します。

## `getTitle()`

> Instance Method | v1.5.2 -

プッシュ通知のタイトルを返します。これはプッシュ通知アクションに指定した静的変数の `title` に対応しています。

### Declaration

```java
public String getTitle();
```

### Return Value

プッシュ通知のタイトルを返します。
