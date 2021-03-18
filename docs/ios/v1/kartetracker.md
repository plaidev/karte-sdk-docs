[KARTE iOS SDK v1](index)

# `KarteTracker`

> Class | v1.0.0 -

`KarteTracker` クラスは、主にイベントのトラッキング機能を提供します。
KARTE にイベントを送信する場合、本クラスが提供する各種トラッキングメソッドを利用して行います。

`KarteTracker` クラスは内部的に複数のトラッカーオブジェクトを管理する仕組みになっています。
初期化されたトラッカーオブジェクトは、アプリケーションキーと紐付けて管理します。
そのためアプリケーションキーに対して生成されるオブジェクトの数は 1 つに制限されます。

またアプリケーション起動後、初回に生成されたトラッカーオブジェクトをデフォルトトラッカーとして特別な扱いをします。

### Inherits From

`NSObject`

### Conforms To

None

## `sharedTracker`

> Type Property | v1.3.0 -

デフォルトトラッカーのオブジェクトを返します。
初期化処理が行われていない場合は、例外を発生させます。

### Declaration

```objc
@property (nonatomic, class, strong, readonly, nonnull) KarteTracker *sharedTracker;
```

## `appKey`

> Instance Property | v1.3.0 -

トラッカーの初期化時に指定したアプリケーションキーを返します。

### Declaration

```objc
@property (nonatomic, copy, readonly) NSString *appKey;
```

## `config`

> Instance Property | v1.3.0 -

トラッカーの初期化時に指定した設定情報を管理している [`KarteTrackerConfig`](kartetrackerconfig)オブジェクトを返します。

### Declaration

```objc
@property (nonatomic, strong, readonly) KarteTrackerConfig *config;
```

## `visitorId`

> Instance Property | v1.2.1 -

UUID で構成された、ビジター ID を返します。
（例：E621E1F8-C36C-495A-93FC-0C247A3E6E5F）

### Declaration

```objc
@property (nonatomic, copy, readonly, nonnull) NSString *visitorId;
```

## `sharedTrackerWithAppKey:`

> Type Method | v1.0.0 -

アプリケーションキーに紐付くトラッカーオブジェクトを返します。
初期化処理が行われていない（アプリケーションキーに紐付くトラッカーオブジェクトが存在しない）場合は、例外を発生させます。

### Declaration

```objc
+ (nonnull instancetype)sharedTrackerWithAppKey:(nonnull NSString *)appKey;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `setupWithAppKey:`

> Type Method | v1.0.0 -

トラッカーの初期化を行います。
アプリケーションキーが空文字列の場合は、例外を発生させます。

### Declaration

```objc
+ (nonnull instancetype)setupWithAppKey:(nonnull NSString *)appKey;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `setupWithAppKey:withConfig:`

> Type Method | v1.3.0 -

設定を指定してトラッカーの初期化を行います。
アプリケーションキーが空文字列の場合は、例外を発生させます。

### Declaration

```objc
+ (nonnull instancetype)setupWithAppKey:(nonnull NSString *)appKey withConfig:(nonnull KarteTrackerConfig *)config;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |
| config | 設定                 |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `initWithAppKey:`

> Instance Method | v1.0.0 -

トラッカーの初期化を行います。
アプリケーションキーが空文字列の場合は、例外を発生させます。

### Declaration

```objc
- (nonnull instancetype)initWithAppKey:(nonnull NSString *)appKey;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `initWithAppKey:withConfig:`

> Instance Method | v1.3.0 -

設定を指定してトラッカーの初期化を行います。
アプリケーションキーが空文字列の場合は、例外を発生させます。

### Declaration

```objc
- (nonnull instancetype)initWithAppKey:(nonnull NSString *)appKey withConfig:(nonnull KarteTrackerConfig *)config;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |
| config | 設定                 |

### Return Value

初期化済みのトラッカーオブジェクトを返します。

## `track:values:`

> Instance Method | v1.0.0 -

イベントを送信します。

### Declaration

```objc
- (void)track:(nonnull NSString *)eventName values:(nullable NSDictionary *)values;
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |

> :warning: イベント名 (eventName) について
> イベント名には一部予約語があり、使えない場合があります。
> [こちら](https://developers.karte.io/docs/predefined-event) をご確認下さい。

> :warning: カスタムオブジェクト (values) について
> values のフィールドには一部予約語があり、使えない場合があります。
> [こちら](https://developers.karte.io/docs/guide-event) をご確認下さい。

## `track:values:view:`

> Instance Method | v1.7.2 -

イベントを送信します。
iPad OS のマルチウインドウに対応しています。
このメソッドで発生するイベントに対応して接客が表示される場合、view パラメタで渡した `UIView` が属するシーン(`UIScene`)で接客が表示されます。
このメソッドは iOS13 以降で使用できます。

### Declaration

```objc
- (void)track:(NSString *)eventName values:(nullable NSDictionary *)values view:(nullable UIView *)view API_AVAILABLE(ios(13.0));
```

### Parameters

| Name      | Description                                                                                                                              |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| eventName | イベント名                                                                                                                               |
| values    | イベントに紐付けるカスタムオブジェクト                                                                                                   |
| view      | イベントに紐付ける `UIView`<br>このイベントに対応して接客が表示される場合、この `UIView` が属するシーン(`UIScene`)で接客が表示されます。 |

> :warning: イベント名 (eventName) について
> イベント名には一部予約語があり、使えない場合があります。
> [こちら](https://developers.karte.io/docs/predefined-event) をご確認下さい。

> :warning: カスタムオブジェクト (values) について
> values のフィールドには一部予約語があり、使えない場合があります。
> [こちら](https://developers.karte.io/docs/guide-event) をご確認下さい。

## `trackNotification:`

> Instance Method | v1.0.0 -

プッシュ通知の開封イベントを送信します。

### Declaration

```objc
- (void)trackNotification:(nonnull NSDictionary *)userInfo;
```

### Parameters

| Name     | Description    |
| -------- | -------------- |
| userInfo | 通知メッセージ |

## `identify:`

> Instance Method | v1.0.0 -

Identify イベント（ユーザー情報）を送信します。
KARTE ではユーザー情報もユーザー情報イベントとして、他のイベントと同じ形式で扱います。

### Declaration

```objc
- (void)identify:(nonnull NSDictionary *)values;
```

### Parameters

| Name   | Description                            |
| ------ | -------------------------------------- |
| values | ユーザーに紐付けるカスタムオブジェクト |

## `identify:view:`

> Instance Method | v1.7.2 -

Identify イベント（ユーザー情報）を送信します。
KARTE ではユーザー情報もユーザー情報イベントとして、他のイベントと同じ形式で扱います。

iPad OS のマルチウインドウに対応しています。
このメソッドで発生するイベントに対応して接客が表示される場合、view パラメタで渡した `UIView` が属するシーン(`UIScene`)で接客が表示されます。
このメソッドは iOS13 以降で使用できます。

### Declaration

```objc
- (void)identify:(NSDictionary *)values view:(nullable UIView *)view API_AVAILABLE(ios(13.0));
```

### Parameters

| Name   | Description                                                                                                                              |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| values | ユーザーに紐付けるカスタムオブジェクト                                                                                                   |
| view   | イベントに紐付ける `UIView`<br>このイベントに対応して接客が表示される場合、この `UIView` が属するシーン(`UIScene`)で接客が表示されます。 |

## `view:`

> Instance Method | v1.0.0 -

View イベントを送信します。

### Declaration

```objc
- (void)view:(nonnull NSString *)viewName;
```

### Parameters

| Name     | Description              |
| -------- | ------------------------ |
| viewName | 画面名（view.view_name） |

## `view:title:`

> Instance Method | v1.3.0 -

View イベントを送信します。

### Declaration

```objc
- (void)view:(nonnull NSString *)viewName title:(nonnull NSString *)title;
```

### Parameters

| Name     | Description                |
| -------- | -------------------------- |
| viewName | 画面名（view.view_name）   |
| title    | 画面タイトル（view.title） |

## `view:title:values:`

> Instance Method | v1.3.0 -

View イベントを送信します。

### Declaration

```objc
- (void)view:(nonnull NSString *)viewName title:(nonnull NSString *)title values:(nullable NSDictionary *)values;
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名（view.view_name）               |
| title    | 画面タイトル（view.title）             |
| values   | イベントに紐付けるカスタムオブジェクト |

## `view:title:values:view:`

> Instance Method | v1.7.2 -

View イベントを送信します。
iPad OS のマルチウインドウに対応しています。
このメソッドで発生するイベントに対応して接客が表示される場合、view パラメタで渡した `UIView` が属するシーン(`UIScene`)で接客が表示されます。
このメソッドは iOS13 以降で使用できます。

### Declaration

```objc
- (void)view:(NSString *)viewName title:(NSString *)title values:(nullable NSDictionary *)values view:(nullable UIView *)view API_AVAILABLE(ios(13.0));
```

### Parameters

| Name     | Description                                                                                                                              |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| viewName | 画面名（view.view_name）                                                                                                                 |
| title    | 画面タイトル（view.title）                                                                                                               |
| values   | イベントに紐付けるカスタムオブジェクト                                                                                                   |
| view     | イベントに紐付ける `UIView`<br>このイベントに対応して接客が表示される場合、この `UIView` が属するシーン(`UIScene`)で接客が表示されます。 |

## `view:values:`

> Instance Method | v1.0.0 -

View イベントを送信します。

### Declaration

```objc
- (void)view:(nonnull NSString *)viewName values:(nullable NSDictionary *)values;
```

### Parameters

| Name     | Description                            |
| -------- | -------------------------------------- |
| viewName | 画面名（view.view_name）               |
| values   | イベントに紐付けるカスタムオブジェクト |

## `registerFCMToken:`

> Instance Method | v1.0.0 -

FCM トークンを KARTE に登録します。
なお登録時に plugin_native_app_identify イベントを発行します。

### Declaration

```objc
- (void)registerFCMToken:(nonnull NSString *)token;
```

### Parameters

| Name  | Description  |
| ----- | ------------ |
| token | FCM トークン |

## `logoutWithCompletionBlock:`

> Instance Method | v1.5.2 - | (deprecated) v1.5.3 -

> :exclamation: このメソッドは廃止予定です
> `renewVisitorId` を利用してください。

ログアウト処理を行います。
処理が完了したら、第１引数に指定されたブロックが呼び出されます。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (`false`) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け

### Declaration

```objc
- (void)logoutWithCompletionBlock:(nonnull void (^)(BOOL isSuccessful))completion;
```

### Parameters

| Name       | Description                                                                                                                                   |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| completion | ブロック<br>ブロックの引数として、ログアウト処理の結果が与えられます。<br>`YES` の場合は、ログアウト成功。<br>`NO` の場合は、ログアウト失敗。 |

## `logout`

> Instance Method | v1.5.3 - | (deprecated) v1.5.9 -

> :exclamation: このメソッドは廃止予定です
> `renewVisitorId` を利用してください。

ログアウト処理を行います。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (`false`) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け

### Declaration

```objc
- (void)logout;
```

## `renewVisitorId`

> Instance Method | v1.5.9 -

ビジター ID の再生成処理を行います。

なお内部では、以下の処理が行われます。

- プッシュ通知の配信許可フラグ (plugin_native_app_identity.subscribe) を 非許可 (`false`) に変更
- 端末に保存されている設定値の削除
- visitor_id の再発行
- 新たに生成された visitor に対して FCM トークンを紐付け
- `WKWebView` の Cookie を削除(karte.io ドメインの Cookie のみ)

### Declaration

```objc
- (void)renewVisitorId;
```

## `optOut`

> Instance Method | v1.5.8 -

オプトアウト処理を行います。
オプトアウト実行後、計測をはじめとした SDK の内部処理は全て無効化されます。
`optIn` を実行することでオプトアウト状態を解除できます。

### Declaration

```objc
- (void)optOut;
```

## `optIn`

> Instance Method | v1.5.8 -

オプトアウト状態を解除します。

### Declaration

```objc
- (void)optIn;
```
