[KARTE Android SDK v1](index)

# `KarteMessageHandler`

> Class | v1.0.0 - | (deprecated) v1.1.0 -

> :exclamation: このクラスは廃止予定です
> [`MessageHandler`](messagehandler) クラスを利用してください。

`KarteMessageHandler` クラスは、KARTE から送信された通知メッセージを処理する機能を提供します。

### Package

`io.karte.android.tracker.firebase`

### Inherits From

None

### Conforms To

None

## `EXTRA_PUSH_FLAG`

> Static Variable | v1.0.0 -

プッシュ通知メッセージキーの定数表現です。
KARTE 経由のプッシュ通知であるか判定するために用いられます。

### Declaration

```java
public static final String EXTRA_PUSH_FLAG;
```

## `EXTRA_CAMPAIGN_ID`

> Static Variable | v1.0.0 -

プッシュ通知メッセージキーの定数表現です。
キャンペーン ID を取得する際に用いられます。

### Declaration

```java
public static final String EXTRA_CAMPAIGN_ID;
```

## `EXTRA_SHORTEN_ID`

> Static Variable | v1.0.0 -

プッシュ通知メッセージキーの定数表現です。
短縮 ID を取得する際に用いられます。

### Declaration

```java
public static final String EXTRA_SHORTEN_ID;
```

## `copyInfoToIntent(Map<String, String> data, Intent intent)`

> Static Method | v1.0.0 -

プッシュ通知の開封イベントの送信に必要なパラメータを `Intent` にコピーします。

### Declaration

```java
public static void copyInfoToIntent(Map<String, String> data, Intent intent);
```

### Parameters

| Name   | Description                                                              |
| ------ | ------------------------------------------------------------------------ |
| data   | 通知データ                                                               |
| intent | Intent <br> 通知メッセージをクリックした際に開始するアクティビティの情報 |
