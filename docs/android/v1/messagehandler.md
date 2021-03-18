[KARTE Android SDK v1](index)

# `MessageHandler`

> Class | v1.1.0 -

`MessageHandler` クラスは、KARTE から送信された通知メッセージを処理する機能を提供します。

### Package

`io.karte.android.tracker.firebase`

### Inherits From

None

### Conforms To

None

## `KARTE_PUSH_NOTIFICATION_FLAG`

> Static Variable | v1.2.2 -

プッシュ通知メッセージキーの定数表現です。
KARTE 経由のプッシュ通知であるか判定するために用いられます。

### Declaration

```java
public static final String KARTE_PUSH_NOTIFICATION_FLAG;
```

## `KARTE_MASS_PUSH_NOTIFICATION_FLAG`

> Static Variable | v1.3.0 -

プッシュ通知メッセージキーの定数表現です。
KARTE Mass Push 経由のプッシュ通知であるか判定するために用いられます。

### Declaration

```java
public static final String KARTE_MASS_PUSH_NOTIFICATION_FLAG;
```

## `EXTRA_CAMPAIGN_ID`

> Static Variable | v1.2.5 -

プッシュ通知メッセージキーの定数表現です。
キャンペーン ID を取得する際に用いられます。

### Declaration

```java
public static final String EXTRA_CAMPAIGN_ID;
```

## `EXTRA_SHORTEN_ID`

> Static Variable | v1.2.5 -

プッシュ通知メッセージキーの定数表現です。
短縮 ID を取得する際に用いられます。

### Declaration

```java
public static final String EXTRA_SHORTEN_ID;
```

## `EXTRA_MASS_PUSH_ID`

> Static Variable | v1.3.0 -

プッシュ通知メッセージキーの定数表現です。
KARTE Mass Push 経由のプッシュ通知 ID を取得する際に用いられます。

### Declaration

```java
public static final String EXTRA_MASS_PUSH_ID;
```

## `canHandleMessage(RemoteMessage message)`

> Static Method | v1.2.6 -

KARTE 経由で送信された通知メッセージであるか判定します。

### Declaration

```java
public static boolean canHandleMessage(RemoteMessage message);
```

### Parameters

| Name    | Description     |
| ------- | --------------- |
| message | `RemoteMessage` |

### Return Value

判定結果を返します。
KARTE 経由で送信された通知メッセージの場合は `true`、KARTE 以外から送信された通知メッセージの場合は、`false`を返します。

## `handleMessage(Context context, RemoteMessage message)`

> Static Method | v1.1.0 -

KARTE 経由で送信された通知メッセージから、通知を作成します。

### Declaration

```java
public static boolean handleMessage(Context context, RemoteMessage message);
```

### Parameters

| Name    | Description     |
| ------- | --------------- |
| context | `Context`       |
| message | `RemoteMessage` |

### Return Value

判定結果を返します。
KARTE 経由で送信された通知メッセージの場合は `true`、KARTE 以外から送信された通知メッセージの場合は、`false`を返します。

## `handleMessage(Context context, RemoteMessage message, Intent defaultIntent)`

> Static Method | v1.3.1 -

KARTE 経由で送信された通知メッセージから、通知を作成します。

### Declaration

```java
public static boolean handleMessage(Context context, RemoteMessage message, Intent defaultIntent);
```

### Parameters

| Name          | Description                                                                                                                          |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| context       | `Context`                                                                                                                            |
| message       | `RemoteMessage`                                                                                                                      |
| defaultIntent | `Intent`<br>ディープリンクが未指定の場合や、ディープリンクに対応するアクティビティが存在しない場合に、開始するアクティビティの情報。 |

### Return Value

判定結果を返します。
KARTE 経由で送信された通知メッセージの場合は `true`、KARTE 以外から送信された通知メッセージの場合は、`false`を返します。

## `copyInfoToIntent(Map<String, String> data, Intent intent)`

> Static Method | v1.1.0 -

プッシュ通知の開封イベントの送信に必要なパラメータを `Intent` にコピーします。

### Declaration

```java
public static void copyInfoToIntent(Map<String, String> data, Intent intent);
```

### Parameters

| Name   | Description                                                              |
| ------ | ------------------------------------------------------------------------ |
| data   | 通知データ                                                               |
| intent | `Intent`<br>通知メッセージをクリックした際に開始するアクティビティの情報 |

## `extractKarteAttributes(Context context, RemoteMessage message)`

> Instance Method | v1.5.2 -

`RemoteMessage` から SDK が自動で処理するデータを取り出し、[`KarteAttributes`](karteattributes) インスタンスを返します。

### Declaration

```java
public static KarteAttributes extractKarteAttributes(Context context, RemoteMessage message);
```

### Return Value

`KarteAttributes` インスタンスを返します。
