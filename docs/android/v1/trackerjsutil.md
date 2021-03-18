[KARTE Android SDK v1](index)

# `TrackerJsUtil`

> Class | v1.2.0 -

`TrackerJsUtil` クラスは、ネイティブアプリケーションと `WebView` 内のユーザー行動を紐付ける際に必要となるヘルパーメソッドを提供します。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `QUERY_KEY_USER_SYNC`

> Static Variable | v1.2.0 -

付与されるクエリパラメータキーの定数表現です。

### Declaration

```java
public static final String QUERY_KEY_USER_SYNC;
```

## `appendUserSyncQueryParameter(Context context, String appKey, String url)`

> Static Method | v1.2.0 -

ネイティブアプリケーションと `WebView` 内のユーザー行動を紐付けるためのパラメータを URL に付与します。

### Declaration

```java
public static String appendUserSyncQueryParameter(Context context, String appKey, String url);
```

### Parameters

| Name    | Description                         |
| ------- | ----------------------------------- |
| context | `Context`                           |
| appKey  | アプリケーションキー                |
| url     | `WebView` で開くページの URL 文字列 |

### Return Value

紐付け用のパラメータを付与した URL 文字列を返します。

## `appendUserSyncQueryParameter(Context context, String appKey, Uri uri)`

> Static Method | v1.2.0 -

ネイティブアプリケーションと `WebView` 内のユーザー行動を紐付けるためのパラメータを URL に付与します。

### Declaration

```java
public static String appendUserSyncQueryParameter(Context context, String appKey, Uri uri);
```

### Parameters

| Name    | Description                               |
| ------- | ----------------------------------------- |
| context | `Context`                                 |
| appKey  | アプリケーションキー                      |
| uri     | `WebView` で開くページの Uri オブジェクト |

### Return Value

紐付け用のパラメータを付与した URL オブジェクトを返します。

## `buildUserSyncParameter(Context context, String appKey)`

> Static Method | v1.2.0 -

ネイティブアプリケーションと `WebView` 内のユーザー行動を紐付けるためのパラメータを返します。

### Declaration

```java
public static String buildUserSyncParameter(Context context, String appKey);
```

### Parameters

| Name    | Description          |
| ------- | -------------------- |
| context | `Context`            |
| appKey  | アプリケーションキー |

### Return Value

紐付け用のパラメータ文字列を返します。
