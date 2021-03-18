[KARTE iOS SDK v1](index)

# `KarteTrackerJsUtil`

> Class | v1.2.0 -

`KarteTrackerJsUtil` クラスは、ネイティブアプリケーションと WebView 内のユーザー行動を紐付ける際に必要となるヘルパーメソッドを提供します。

### Inherits From

`NSObject`

### Conforms To

None

## `stringByAppendingUserSyncQueryParameter:withURLString:`

> Type Method | v1.2.0 -

ネイティブアプリケーションと WebView 内のユーザー行動を紐付けるためのパラメータを URL に付与します。

### Declaration

```objc
+ (nonnull NSString *)stringByAppendingUserSyncQueryParameter:(nonnull NSString *)appKey withURLString:(nonnull NSString *)url;
```

### Parameters

| Name   | Description                       |
| ------ | --------------------------------- |
| appKey | アプリケーションキー              |
| url    | WebView で開くページの URL 文字列 |

### Return Value

紐付け用のパラメータを付与した URL 文字列を返します。

## `URLByAppendingUserSyncQueryParameter:withURL:`

> Type Method | v1.2.0 -

ネイティブアプリケーションと WebView 内のユーザー行動を紐付けるためのパラメータを URL に付与します。

### Declaration

```objc
+ (nonnull NSURL *)URLByAppendingUserSyncQueryParameter:(nonnull NSString *)appKey withURL:(nonnull NSURL *)url;
```

### Parameters

| Name   | Description                             |
| ------ | --------------------------------------- |
| appKey | アプリケーションキー                    |
| url    | WebView で開くページの URL オブジェクト |

### Return Value

紐付け用のパラメータを付与した URL オブジェクトを返します。

## `userSyncQueryParameter:`

> Type Method | v1.2.0 -

ネイティブアプリケーションと WebView 内のユーザー行動を紐付けるためのパラメータを返します。

### Declaration

```objc
+ (nullable NSString *)userSyncQueryParameter:(nonnull NSString *)appKey;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |

### Return Value

紐付け用のパラメータ文字列を返します。
