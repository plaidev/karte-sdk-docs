[KARTE iOS SDK v1](index)

# `KarteTrackerConfig`

> Class | v1.3.0 -

`KarteTrackerConfig` クラスは、トラッカーに関する各種設定値を管理するクラスです。
本クラスはイミュータブルなオブジェクトとなっているため、設定値を変更する場合は新たにオブジェクトを生成する必要があります。

### Inherits From

`NSObject`

### Conforms To

None

## `configure`

> Type Property | v1.3.0 -

デフォルト設定のオブジェクトを返します。
デフォルト設定については、初期化オプション一覧を確認してください。

### Declaration

```objc
@property (nonatomic, class, strong, readonly, nonnull) KarteTrackerConfig *configure;
```

## `trackEndpoint`

> Instance Property | v1.3.0 -

トラッキング用の API エンドポイント URL を返します。

### Declaration

```objc
@property (nonatomic, copy, readonly, nonnull) NSString *trackEndpoint;
```

## `overlayEndpoint`

> Instance Property | v1.3.0 -

アプリ内メッセージ表示用ページのエンドポイント URL を返します。

### Declaration

```objc
@property (nonatomic, copy, readonly, nonnull) NSString *overlayEndpoint;
```

## `enabledTrackingAppLifecycle`

> Instance Property | v1.3.0 -

アプリケーションのライフサイクルイベント（初回起動 / アップデート）の送信有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingAppLifecycle) BOOL enabledTrackingAppLifecycle;
```

## `enabledTrackingAppOpen`

> Instance Property | v1.3.0 -

アプリケーションの起動イベントの送信有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingAppOpen) BOOL enabledTrackingAppOpen;
```

## `enabledTrackingIdfa`

> Instance Property | v1.3.0 - | (deprecated) v1.5.5 -

> ❗️ このプロパティは廃止予定です
> IDFA の送信が必要な場合は、`IDFADelegate` を利用してください。

IDFA の送信有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingIdfa) BOOL enabledTrackingIdfa;
```

## `enabledTrackingCrashError`

> Instance Property | v1.3.0 -

アプリケーションのクラッシュイベントの送信有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingCrashError) BOOL enabledTrackingCrashError;
```

## `enabledFCMTokenResend`

> Instance Property | v1.3.0 -

アプリケーションの起動時の FCM トークン送信有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledFCMTokenResend) BOOL enabledFCMTokenResend;
```

## `enabledVisualTracking`

> Instance Property | v1.6.0 -

ビジュアルトラッキング機能が有効かどうかを返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledVisualTracking) BOOL enabledVisualTracking NS_SWIFT_NAME(isEnabledVisualTracking);
```

## `enabledOptOutDefault`

> Instance Property | v1.5.8 -

オプトアウトの有効化の有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledOptOutDefault) BOOL enabledOptOutDefault;
```

## `dryRun`

> Instance Property | v1.3.0 -

トラッカーのドライラン実行の有無を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isDryRun) BOOL dryRun;
```

## `IDFADelegate`

> Instance Property | v1.5.5 -

IDFA の取得処理の委譲先インスタンスを返します。

### Declaration

```objc
@property (nonatomic, weak, readonly, nullable) id<KarteIDFADelegate> IDFADelegate;
```

## `initWithBuilder:`

> Instance Method | v1.3.0 -

`KarteTrackerConfig` オブジェクトの初期化を行います。


### Declaration

```objc
- (nonnull instancetype)initWithBuilder:(KarteTrackerConfigBuilder *)builder;
```

### Parameters

| Name    | Description  |
| ------- | ------------ |
| builder | 設定ビルダー |

### Return Value

初期化済みの `KarteTrackerConfig` オブジェクトを返します。

## `configureWithBuilder:`

> Type Method | v1.3.0 -

`KarteTrackerConfig` オブジェクトの初期化を行います。

### Declaration

```objc
+ (nonnull instancetype)configureWithBuilder:(void (^)(KarteTrackerConfigBuilder *_Nonnull builder))closure;
```

### Parameters

| Name    | Description                                                |
| ------- | ---------------------------------------------------------- |
| builder | ブロック<br>ブロックの引数として設定ビルダーが渡されます。 |

### Return Value

初期化済みの `KarteTrackerConfig` オブジェクトを返します。
