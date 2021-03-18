[KARTE iOS SDK v1](index)

# `KarteInAppMessagingManagerDelegate`

> Protocol | v1.5.1 -

`KarteInAppMessagingManagerDelegate` プロトコルは、アプリ内メッセージで発生したイベントの委譲先インスタンスが実装すべきインターフェースです。

### Inherits From

`NSObject`

### Conforming Types

None

## `inAppMessagingManager:shouldOpenURL:`

> Instance Method | v1.5.1 -

アプリ内メッセージでリンクがタップされた場合に、そのリンクを SDK 側で自動的に開くかどうかを、委譲先のインスタンスに尋ねます。

本メソッドの実装は必須ではありません。

### Declaration

```objc
- (BOOL)inAppMessagingManager:(nonnull KarteInAppMessagingManager *)manager shouldOpenURL:(nullable NSURL *)url;
```

### Parameters

| Name    | Description                                  |
| ------- | -------------------------------------------- |
| manager | `InAppMessagingManager` クラスのインスタンス |
| url     | 開こうとしているリンクの URL                 |

### Return Value

リンクを自動的に開くかどうかを指定します。
`YES` の場合は、SDK により自動的にリンクが開かれます。
`NO` の場合は、SDK では何も行いません。
