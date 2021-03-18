[KARTE Android SDK v1](index)

# `Tracker`

> Abstract class | v1.0.0 -

`Tracker` クラスは、主にイベントのトラッキング機能を提供します。
KARTE にイベントを送信する場合、本クラスが提供する各種トラッキングメソッドを利用して行います。

`Tracker` クラスは内部的に複数のトラッカーオブジェクトを管理する仕組みになっています。
初期化されたトラッカーオブジェクトは、アプリケーションキーと紐付けて管理します。
そのためアプリケーションキーに対して生成されるオブジェクトの数は 1 つに制限されます。

またアプリケーション起動後、初回に生成されたトラッカーオブジェクトをデフォルトトラッカーとして特別な扱いをします。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `init(Context context, String key)`

> Static Method | v1.0.0 -

トラッカーの初期化を行います。

### Declaration

```java
public static void init(Context context, String key);
```

### Parameters

| Name    | Description          |
| ------- | -------------------- |
| context | `Context`            |
| key     | アプリケーションキー |

## `init(Context context, String key, TrackerConfig config)`

> Static Method | v1.2.0 -

設定を指定してトラッカーの初期化を行います。

### Declaration

```java
public static void init(Context context, String key, TrackerConfig config);
```

### Parameters

| Name    | Description          |
| ------- | -------------------- |
| context | `Context`            |
| key     | アプリケーションキー |
| config  | 設定                 |

## `getInstance(Context context, String key)`

> Static Method | v1.0.0 -

アプリケーションキーに紐付くトラッカーオブジェクトを返します。
キーに紐付くオブジェクトが存在しない場合は、オブジェクトを初期化して返します。

### Declaration

```java
public static Tracker getInstance(Context context, String key);
```

### Parameters

| Name    | Description          |
| ------- | -------------------- |
| context | `Context`            |
| key     | アプリケーションキー |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `getInstance(Context context)`

> Static Method | v1.2.0 -

デフォルトトラッカーのオブジェクトを返します。
オブジェクトが存在しない場合は、計測を行わない空のトラッカーオブジェクトを返します。

### Declaration

```java
public static Tracker getInstance(Context context);
```

### Parameters

| Name    | Description |
| ------- | ----------- |
| context | `Context`   |

### Return Value

初期化済みのデフォルトトラッカーオブジェクトを返します。

## `getInstance()`

> Static Method | v1.6.0 -

デフォルトトラッカーのオブジェクトを返します。
オブジェクトが存在しない場合は、計測を行わない空のトラッカーオブジェクトを返します。

### Declaration

```java
public static Tracker getInstance();
```

### Return Value

初期化済みのデフォルトトラッカーオブジェクトを返します。

## `getVisitorId()`

> Instance Method | v1.2.3 -

ビジター ID を返します。

### Declaration

```java
public abstract String getVisitorId();
```

### Return Value

ビジター ID を返します。

## `getAppKey()`

> Instance Method | v1.4.5 -

アプリケーションキーを返します。

### Declaration

```java
public abstract String getAppKey();
```

### Return Value

トラッカーの初期化時に指定したアプリケーションキーを返します。

## `getInAppMessagingManager()`

> Instance Method | v1.5.0 -

[`InAppMessagingManager`](inappmessagingmanager) のオブジェクトを返します。

### Declaration

```java
public abstract InAppMessagingManager getInAppMessagingManager();
```

### Return Value

`InAppMessagingManager` のオブジェクトを返します。

## `track(String eventName, JSONObject values)`

> Instance Method | v1.0.0 -

イベントを送信します。

### Declaration

```java
public abstract void track(String eventName, JSONObject values);
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |

> :warning: イベント名 (eventName) について
> イベント名には一部予約語があり使えない場合があります。
> [こちら](https://developers.karte.io/docs/predefined-event) をご確認下さい。

> :warning: カスタムオブジェクト (values) について
> values のフィールドには一部予約語があり、使えない場合があります。
> [こちら](https://developers.karte.io/docs/guide-event) をご確認下さい。

## `track(String eventName, JSONObject values, boolean withAppInfo)`

> Instance Method | v1.0.0 -

イベントを送信します。

### Declaration

```java
public abstract void track(String eventName, JSONObject values, boolean withAppInfo);
```

### Parameters

| Name        | Description                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------- |
| eventName   | イベント名                                                                                                      |
| values      | イベントに紐付けるカスタムオブジェクト                                                                          |
| withAppInfo | アプリケーション情報をイベントプロパティに付与するかどうかを表すフラグ<br>`true`: 付与する、`false`: 付与しない |

## `track(String eventName, Bundle values)`

> Instance Method | v1.3.5 -

イベントを送信します。

### Declaration

```java
public abstract void track(String eventName, Bundle values);
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |

> :warninig: トラッキングの注意事項
> SDK v1.5.3 未満で `Bundle` によるトラッキングを行なう場合、送信値に `null` が含まれていると `NullPointerException` が発生します。`Bundle` での送信を行う場合は v1.5.3 以上の SDK を使用してください。

## `track(String eventName, Bundle values, boolean withAppInfo)`

> Instance Method | v1.3.5 -

> :exclamation: このメソッドは廃止予定です。
> withAppInfo の値に関わらず、app_info はイベントに付与されます。
> `track(String eventName, Bundle values)`を利用してください。

イベントを送信します。

### Declaration

```java
public abstract void track(String eventName, Bundle values, boolean withAppInfo);
```

### Parameters

| Name        | Description                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------- |
| eventName   | イベント名                                                                                                      |
| values      | イベントに紐付けるカスタムオブジェクト                                                                          |
| withAppInfo | アプリケーション情報をイベントプロパティに付与するかどうかを表すフラグ<br>`true`: 付与する、`false`: 付与しない |

## `identify(JSONObject values)`

> Instance Method | v1.0.0 -

Identify イベント（ユーザー情報）を送信します。
KARTE ではユーザー情報もユーザー情報イベント
として、他のイベントと同じ形式で扱います。

### Declaration

```java
public abstract void identify(JSONObject values);
```

### Parameters

| Name   | Description                            |
| ------ | -------------------------------------- |
| values | ユーザーに紐付けるカスタムオブジェクト |

## `identify(Bundle values)`

> Instance Method | v1.3.5 -

Identify イベント（ユーザー情報）を送信します。
KARTE ではユーザー情報もユーザー情報イベント
として、他のイベントと同じ形式で扱います。

### Declaration

```java
public abstract void identify(Bundle values);
```

### Parameters

| Name   | Description                            |
| ------ | -------------------------------------- |
| values | ユーザーに紐付けるカスタムオブジェクト |

## `view(String viewName)`

> Instance Method | v1.0.0 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName);
```

### Parameters

| Name     | Description |
| -------- | ----------- |
| viewName | 画面名      |

## `view(String viewName, String title)`

> Instance Method | v1.3.0 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName, String title);
```

### Parameters

| Name     | Description  |
| -------- | ------------ |
| viewName | 画面名       |
| title    | 画面タイトル |

## `view(String viewName, String title, JSONObject values)`

> Instance Method | v1.3.0 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName, String title, JSONObject values);
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名                                 |
| title    | 画面タイトル                           |
| values   | イベントに紐付けるカスタムオブジェクト |

## `view(String viewName, JSONObject values)`

> Instance Method | v1.0.0 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName, JSONObject values);
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名                                 |
| values   | イベントに紐付けるカスタムオブジェクト |

## `view(String viewName, String title, Bundle values)`

> Instance Method | v1.3.5 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName, String title, Bundle values);
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名                                 |
| title    | 画面タイトル                           |
| values   | イベントに紐付けるカスタムオブジェクト |

## `view(String viewName, Bundle values)`

> Instance Method | v1.3.5 -

View イベントを送信します。

### Declaration

```java
public abstract void view(String viewName, Bundle values);
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名                                 |
| values   | イベントに紐付けるカスタムオブジェクト |

## `trackFcmToken(String token)`

> Instance Method | v1.0.0 -

FCM トークンを KARTE に登録します。
なお登録時に plugin_native_app_identify イベントを発行します。

### Declaration

```java
public abstract void trackFcmToken(String token);
```

### Parameters

| Name  | Description  |
| ----- | ------------ |
| token | FCM トークン |

## `logout(CompletionHandler completionHandler)`

> Instance Method | v1.5.2

> :exclamation: このメソッドは廃止予定です
> `renewVisitorId()` を利用してください。

ログアウト処理を行います。
処理が完了したら、第１引数に指定された [`CompletionHandler`](tracker_completionhandler) の `onCompleted` が呼び出されます。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (`false`) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け

### Declaration

```java
public abstract void logout(CompletionHandler completionHandler);
```

### Parameters

| Name              | Description                                                                                                                                                                                             |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| completionHandler | コールバック<br>コールバックの引数として、ログアウト処理の結果 isSuccessful が与えられます。<br>isSuccessful が `true` の場合は、ログアウト成功。<br>isSuccessful が `false` の場合は、ログアウト失敗。 |

## `logout()`

> Instance Method | v1.5.4 -

> :exclamation: このメソッドは廃止予定です
> `renewVisitorId()` を利用してください。

ログアウト処理を行います。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (false) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け

### Declaration

```java
public abstract void logout();
```

## `renewVisitorId()`

> Instance Method | v1.6.1 -

ビジター ID の再生成処理を行います。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (`false`) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け
- WebView の Cookie を削除(karte.io ドメインの Cookie のみ)

### Declaration

```java
public abstract void renewVisitorId();
```

## `optOut()`

> Instance Method | v1.6.0 -

オプトアウト処理を行います。
オプトアウト実行後、計測をはじめとした SDK の内部処理は全て無効化されます。
`optIn()` を実行することでオプトアウト状態を解除できます。

### Declaration

```java
public abstract void optOut();
```

## `optIn()`

> Instance Method | v1.6.0 -

オプトアウト状態を解除します。

### Declaration

```java
public abstract void optIn();
```
