[KARTE Android SDK v1](index)

# `TrackerConfig.Builder`

> Class | v1.2.0 -

`TrackerConfig.Builder` クラスは、トラッカーに関する各種設定値の設定を行うためのクラスです。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `Builder()`

> Constructor | v1.2.0 -

ビルダーオブジェクトの初期化を行います。

### Declaration

```java
public Builder();
```

### Return Value

初期化済みのビルダーオブジェクトを返します。

## `build()`

> Instance Method | v1.2.0 -

本クラスで設定した設定値を元に、[`TrackerConfig`](trackerconfig) オブジェクトを生成します。

### Declaration

```java
public TrackerConfig build();
```

### Return Value

`TrackerConfig` オブジェクトを返します。

## `setTrackEndpoint(String trackEndpoint)`

> Instance Method | v1.2.0 -

トラッキング用の API エンドポイント URL を設定します。

> :warning: このメソッドについて
> 通常この設定を変更する必要はありません。

### Declaration

```java
public Builder setTrackEndpoint(String trackEndpoint);
```

### Parameters

| Name          | Description                             |
| ------------- | --------------------------------------- |
| trackEndpoint | トラッキング用の API エンドポイント URL |

### Return Value

ビルダーオブジェクトを返します。

### `setOverlayEndpoint(String overlayEndpoint)`

> Instance Method | v1.2.0 -

アプリ内メッセージ表示用ページのエンドポイント URL を設定します。

> :waring: このメソッドについて
> 通常この設定を変更する必要はありません。

### Declaration

```java
public Builder setOverlayEndpoint(String overlayEndpoint);
```

### Parameters

| Name            | Description                                        |
| --------------- | -------------------------------------------------- |
| overlayEndpoint | アプリ内メッセージ表示用ページのエンドポイント URL |

### Return Value

ビルダーオブジェクトを返します。

## `setEnableTrackingCrashError(boolean enableTrackingCrashError)`

> Instance Method | v1.2.0 -

アプリケーションのクラッシュイベントの送信有無を設定します。
`true` の場合にイベントの送信が行われます。

### Declaration

```java
public Builder setEnableTrackingCrashError(boolean enableTrackingCrashError);
```

### Parameters

| Name                     | Description                  |
| ------------------------ | ---------------------------- |
| enableTrackingCrashError | クラッシュイベントの送信有無 |

### Return Value

ビルダーオブジェクトを返します。

## `setEnableFCMTokenResend(boolean enableFCMTokenResend)`

> Instance Method | v1.2.0 -

アプリケーションの起動時の FCM トークン送信有無を設定します。
`true` の場合に FCM トークンの送信が行われます。

### Declaration

```java
public Builder setEnableFCMTokenResend(boolean enableFCMTokenResend);
```

### Parameters

| Name                 | Description          |
| -------------------- | -------------------- |
| enableFCMTokenResend | FCM トークン送信有無 |

### Return Value

ビルダーオブジェクトを返します。

## `setEnableTrackingAaid(boolean enableTrackingAaid)`

> Instance Method | v1.2.7 -

AAID の送信有無を設定します。
`true` の場合に AAID の送信が行われます。

### Declaration

```java
public Builder setEnableTrackingAaid(boolean enableTrackingAaid);
```

### Parameters

| Name               | Description     |
| ------------------ | --------------- |
| enableTrackingAaid | AAID の送信有無 |

### Return Value

ビルダーオブジェクトを返します。

## `setDryRun(boolean dryRun)`

> Instance Method | v1.3.0 -

トラッカーのドライラン実行の有無を設定します。
`true` の場合にドライランで実行されます。

### Declaration

```java
public Builder setDryRun(boolean dryRun);
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| dryRun | ドライラン実行の有無 |

### Return Value

ビルダーオブジェクトを返します。

## `setAutoControlSoftInputAdjust(boolean autoControlSoftInputAdjust)`

> Instance Method | v1.3.1 -

> :exclamation: このメソッドは廃止予定です。
> SDK v1.6.0 から、このオプションの値は無視されます。

キーボードが画面要素に被らないように `Activity` のサイズを自動調節する機能の有無を設定します。

### Declaration

```java
public Builder setAutoControlSoftInputAdjust(boolean autoControlSoftInputAdjust);
```

### Parameters

| Name                       | Description                                 |
| -------------------------- | ------------------------------------------- |
| autoControlSoftInputAdjust | `Activity` のサイズを自動調節する機能の有無 |

### Return Value

ビルダーオブジェクトを返します。

## `setEnableTrackerOptOut(boolean enableTrackerOptOut)`

> Instance Method | v1.6.0 -

初期化時のオプトアウトの有効化の有無を設定します。

### Declaration

```java
public Builder setEnableTrackerOptOut(boolean enableTrackerOptOut);
```

### Parameters

| Name                | Description                          |
| ------------------- | ------------------------------------ |
| enableTrackerOptOut | 初期化時のオプトアウトの有効化の有無 |

### Return Value

ビルダーオブジェクトを返します。
