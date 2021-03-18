[KARTE Android SDK v1](index)

# `TrackerConfig`

> Class | v1.2.0 -

`TrackerConfig` クラスは、トラッカーに関する各種設定値を管理するクラスです。
インスタンスを生成する場合は、`TrackerConfig.Builder` クラスを利用してください。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `getTrackEndpoint()`

> Instance Method | v1.2.0 -

トラッキング用の API エンドポイント URL を返します。

### Declaration

```java
public String getTrackEndpoint();
```

### Return Value

トラッキング用の API エンドポイント URL を返します。

## `getOverlayEndpoint()`

> Instance Method | v1.2.0 -

アプリ内メッセージ表示用ページのエンドポイント URL を返します。

### Declaration

```java
public String getOverlayEndpoint();
```

### Return Value

アプリ内メッセージ表示用ページのエンドポイント URL を返します。

## `enabledTrackingCrashError()`

> Instance Method | v1.2.0 -

アプリケーションのクラッシュイベントの送信有無を返します。

### Declaration

```java
public boolean enabledTrackingCrashError();
```

### Return Value

クラッシュイベントの送信有無を返します。

## `enabledFCMTokenResend()`

> Instance Method | v1.2.0 -

アプリケーションの起動時の FCM トークン送信有無を返します。

### Declaration

```java
public boolean enabledFCMTokenResend();
```

### Return Value

アプリケーションの起動時の FCM トークン送信有無を返します。

## `enabledTrackingAaid()`

> Instance Method | v1.2.7 -

AAID の送信有無を返します。

### Declaration

```java
public boolean enabledTrackingAaid();
```

### Return Value

AAID の送信有無を返します。

## `isDryRun()`

> Instance Method | v1.3.0 -

トラッカーのドライラン実行の有無を返します。

### Declaration

```java
public boolean isDryRun();
```

### Return Value

トラッカーのドライラン実行の有無を返します。

## `autoControlSoftInputAdjust()`

> Instance Method | v1.3.1 -

キーボードが画面要素に被らないように `Activity` のサイズを自動調節する機能の有無を返します。

> ❗️ このメソッドは廃止予定です
> SDK v1.6.0 から、このオプションの値は無視されます。

> 📘 このオプションについて
> アプリ内メッセージが表示されている間でのみ有効なオプションです。

### Declaration

```java
public boolean autoControlSoftInputAdjust();
```

### Return Value

`Activity` のサイズを自動調節する機能の有無を返します。

## `enabledTrackerOptOut()`

> Instance Method | v1.6.0 -

オプトアウトの有効化の有無を返します。

### Declaration

```java
public boolean enabledTrackerOptOut();
```

### Return Value

オプトアウトの有効化の有無を返します。
