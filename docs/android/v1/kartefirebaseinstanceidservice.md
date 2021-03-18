[KARTE Android SDK v1](index)

# `KarteFirebaseInstanceIdService`

> Abstract class | v1.0.0 - | (deprecated) v1.5.2 -

> ❗️ このクラスは非推奨です
> 代わりに `Tracker.trackFcmToken()` を使いアプリからトークンを送信してください。

`KarteFirebaseInstanceIdService` クラスは、FCM トークンの更新イベントをハンドルし、KARTE へ FCM トークンの送信する機能を提供します。

### Package

`io.karte.android.tracker.firebase`

### Inherits From

`com.google.firebase.iid.FirebaseInstanceIdService`

### Conforms To

None

## `getToken()`

> Static Method | v1.0.0 -

FCM トークンを返します。

### Declaration

```java
public static String getToken();
```

### Return Value

FCM トークンを返します。

## `onTokenRefresh()`

> Instance Method | v1.0.0 -

FCM トークンの更新を受け取ります。

`KarteFirebaseInstanceIdService` クラスでは、このメソッドをオーバーライドして最新の FCM トークンを KARTE に送信するようになっています。
このメソッドを更にオーバーライドする場合は、上位クラスの `onTokenRefresh()` の呼び出しを行なってください。

### Declaration

```java
public void onTokenRefresh();
```

## `getTracker()`

> Abstract Method | v1.0.0 -

KARTE にトークンを送信する際に、利用するトラッカーオブジェクトを返してください。

### Declaration

```java
protected abstract Tracker getTracker();
```

### Return Value

トラッカーオブジェクトを返します。
