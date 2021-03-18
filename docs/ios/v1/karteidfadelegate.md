[KARTE iOS SDK v1](index)

# `KarteIDFADelegate`

> Protocol | v1.5.5 -

`KarteIDFADelegate` プロトコルは、IDFA 取得処理の委譲先インスタンスが実装すべきインターフェースです。

### Inherits From

`NSObject`

### Conforming Types

None

## `advertisingIdentifierString`

> Instance Method | v1.5.5 -

IDFA の送信が必要な場合に、IDFA の取得処理を委譲します。

### Declaration

```objc
- (nullable NSString *)advertisingIdentifierString;
```

### Return Value

取得した IDFA を戻り値として指定します。

## `isAdvertisingTrackingEnabled`

> Instance Method | v1.5.5 -

IDFA の取得が必要な場合に、IDFA の取得を行うか委譲先インスタンスに尋ねます。

### Declaration

```objc
- (BOOL)isAdvertisingTrackingEnabled;
```

### Return Value

IDFA の取得を行うかどうかを戻り値として指定します。
`YES` の場合は、IDFA の取得を行います。
`NO` の場合は、IDFA の取得は行いません。
