[KARTE iOS SDK v1](index)

# `KarteRemoteNotificationHandler`

> Class | v1.1.0 -

`KarteRemoteNotificationHandler` クラスは、KARTE から送信された通知メッセージを処理する機能を提供します。

### Inherits From

`NSObject`

### Conforms To

None

## `canHandleRemoteNotification:`

> Type Method | v1.2.2 -

KARTE 経由で送信された通知メッセージであるか判定します。

### Declaration

```objc
+ (BOOL)canHandleRemoteNotification:(nullable NSDictionary *)userInfo;
```

### Parameters

| Name     | Description    |
| -------- | -------------- |
| userInfo | 通知メッセージ |

### Return Value

判定結果を返します。
KARTE 経由で送信された通知メッセージの場合は `true`、KARTE 以外から送信された通知メッセージの場合は、`false`を返します。

## `handleRemoteNotification:`

> Type Method | v1.1.0 -

KARTE 経由で送信された通知メッセージに含まれるディープリンク URL を開きます。

### Declaration

```objc
+ (BOOL)handleRemoteNotification:(nullable NSDictionary *)userInfo;
```

### Parameters

| Name     | Description    |
| -------- | -------------- |
| userInfo | 通知メッセージ |

### Return Value

処理結果を返します。
ディープリンクが開けた場合は `true`、開けなかった場合は `false`を返します。

## `retrieveURLFromUserInfo:`

> Type Method | v1.5.1 -

KARTE 経由で送信された通知メッセージに含まれるディープリンク URL を返します。

### Declaration

```objc
+ (nullable NSURL *)retrieveURLFromUserInfo:(nullable NSDictionary *)userInfo;
```

### Parameters

| Name     | Description    |
| -------- | -------------- |
| userInfo | 通知メッセージ |

### Return Value

ディープリンク URL を返します。
