[KARTE iOS SDK v1](index)

# `KarteTrackerConfigBuilder`

> Class | v1.3.0 -

`KarteTrackerConfigBuilder` クラスは、トラッカーに関する各種設定値を設定するためのクラスです。

### Inherits From

`NSObject`

### Conforms To

None

## `trackEndpoint`

> Instance Property | v1.3.0 -

トラッキング用の API エンドポイント URL。

> :warning: このプロパティについて
> 通常この設定を変更する必要はありません。

### Declaration

```objc
@property (nonatomic, copy, nonnull) NSString *trackEndpoint;
```

## `overlayEndpoint`

> Instance Property | v1.3.0 -

## `enabledTrackingAppLifecycle`

> Instance Property | v1.3.0 -

## `enabledTrackingAppOpen`

> Instance Property | v1.3.0 -

## `enabledTrackingIdfa`

> Instance Property | v1.3.0 - | (deprecated) v1.5.5 -

> :exclamation: このプロパティは廃止予定です
> IDFA の送信が必要な場合は、`IDFADelegate` を利用してください。

IDFA の送信有無。
`true` の場合に IDFA の送信が行われます。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingIdfa) BOOL enabledTrackingIdfa;
```

## `enabledTrackingCrashError`

> Instance Property | v1.3.0 -

アプリケーションのクラッシュイベントの送信有無。
`true` の場合にイベントの送信が行われます。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledTrackingCrashError) BOOL enabledTrackingCrashError;
```

## `enabledFCMTokenResend`

> Instance Property | v1.3.0 -

アプリケーションの起動時の FCM トークン送信有無。
`true` の場合に FCM トークンの送信が行われます。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isEnabledFCMTokenResend) BOOL enabledFCMTokenResend;
```

## `enabledVisualTracking`

> Instance Property | v1.6.0 -

ビジュアルトラッキング機能が有効かどうかを返します。

`true` の場合にビジュアルトラッキングが有効となります。

### Declaration

```objc
@property (nonatomic, assign, getter=isEnabledVisualTracking) BOOL enabledVisualTracking;
```

## `enabledOptOutDefault`

> Instance Property | v1.5.8 -

オプトアウトの有効化。
`true` の場合に SDK はデフォルトでオプトアウトされます。`optIn`実行時にオプトアウトが解除されます。

### Declaration

```objc
@property (nonatomic, assign, getter=isEnabledOptOutDefault) BOOL enabledOptOutDefault;
```

## `dryRun`

> Instance Property | v1.3.0 -

トラッカーのドライラン実行の有無。
`true` の場合にドライランで実行されます。

### Declaration

```objc
@property (nonatomic, assign, readonly, getter=isDryRun) BOOL dryRun;
```

## `IDFADelegate`

> Instance Property | v1.5.5 -

IDFA の取得処理の委譲先インスタンス。

### Declaration

```objc
@property (nonatomic, weak, nullable) id<KarteIDFADelegate> IDFADelegate;
```
