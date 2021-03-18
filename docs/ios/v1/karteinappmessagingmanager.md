[KARTE iOS SDK v1](index)

# `KarteInAppMessagingManager`

> Class | v1.5.0 -

`KarteInAppMessagingManager` クラスは、アプリ内メッセージを管理するためのクラスです。

### Inherits From

`NSObject`

### Conforms To

None

## `sharedManager`

> Type Property | v1.5.0 -

初期化済みの `KarteInAppMessagingManager` オブジェクトを返します。

### Declaration

```objc
@property (class, nonatomic, strong, readonly) KarteInAppMessagingManager *sharedManager;
```

## `delegate`

> Instance Property | v1.5.1 -

アプリ内メッセージ内で発生したイベントの委譲先インスタンス。

### Declaration

```objc
@property (nonatomic, weak, nullable) id<KarteInAppMessagingManagerDelegate> delegate;
```

## `presenting`

> Instance Property | v1.5.0 -

アプリ内メッセージの表示有無。
アプリ内メッセージが表示中の場合に `true` を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isPresenting) BOOL presenting;
```

## `dismiss`

> Instance Method | v1.5.0 -

アプリ内メッセージを閉じます。

### Declaration

```objc
- (void)dismiss;
```

## `suppress`

> Instance Method | v1.6.2 -

アプリ内メッセージの表示を抑制します。

### Declaration

````objc
- (void)suppress;


## `unsuppress`

> Instance Method | v1.6.2 -


アプリ内メッセージの表示抑制を解除します。
### Declaration

```objc
- (void)unsuppress;
````
