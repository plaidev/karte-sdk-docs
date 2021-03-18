[KARTE iOS SDK v1](index)

# `KarteUrlSchemeHandler`

> Class | v1.6.0 -

`KarteUrlSchemeHandler` クラスは Karte に関連する URL スキームを処理する機能を提供します。

### Inherits From

`NSObject`

### Conforms To

None

## `handle:`

> Type Method | v1.6.0 -

Karte に関連する URL スキームを処理して結果を返します。

### Declaration

```objc
+ (BOOL)handle:(nullable NSURL *)url;
```

### Parameters

| Name | Description    |
| ---- | -------------- |
| url  | 処理対象の URL |

### Return Value

URL スキームのハンドルに成功したかどうかを返します。
