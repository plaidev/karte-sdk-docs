[KARTE iOS SDK v1](index)

# `KarteVariables`

> Class | v1.3.0 -

`KarteVariables` クラスは、設定値配信に関連するクラスで、以下の機能を提供します。

- 設定値の取得
- 設定値の保持・管理
- 効果測定用のイベントの送信

なお `KarteVariables` クラスを利用するためには、事前に [`KarteTracker`](kartetracker) の初期化が必要です。
初期化が行われていない場合、例外が発生する可能性があります。

### Inherits From

`NSObject`

### Conforms To

None

## `variables`

> Type Property | v1.3.0 -

初期化済みの `KarteVariables` オブジェクトを返します。

### Declaration

```objc
@property (class, strong, readonly) KarteVariables *variables;
```

## `initWithAppKey:`

> Instance Method | v1.3.0 -

`KarteVariables` オブジェクトを初期化します。

### Declaration

```objc
- (nonnull instancetype)initWithAppKey:(nonnull NSString *)appKey;
```

### Parameters

| Name   | Description          |
| ------ | -------------------- |
| appKey | アプリケーションキー |

### Return Value

初期化済みのオブジェクトを返します。

## `variablesWithAppKey:`

> Type Method | v1.3.0 -

## `fetch`

> Instance Method | v1.3.0 -

## `fetch`

> Type Method | v1.3.0 -

設定値を取得します。
取得は非同期で行われるため、設定値の取得完了をトリガーに処理を行いたい場合は、`fetchWithCompletionBlock:` を利用してください。

> 🚧 事前にトラッカーの初期化が必要です。
> 初期化にはデフォルトトラッカーのアプリケーションキーが利用されます。
> そのためトラッカーの初期化が行われていない場合は、例外が発生します。

### Declaration

```objc
+ (void)fetch;
```

## `fetchWithCompletionBlock:`

> Instance Method | v1.3.0 -

設定値を取得します。
設定値の取得が完了したタイミングで、引数に指定したブロックにコールバックされます。

> 🚧 事前にトラッカーの初期化が必要です。
> 初期化時に指定したアプリケーションキーに対応するトラッカーの初期化が行われていない場合は、例外が発生します。

### Declaration

```objc
- (void)fetchWithCompletionBlock:(nonnull void (^)(BOOL isSuccessful))completion;
```

### Parameters

| Name       | Description          |
| ---------- | -------------------- |
| completion | 取得完了通知ブロック |

## `fetchWithCompletionBlock:`

> Type Method | v1.3.0 -

デフォルトのトラッカーを利用して設定値を取得します。
設定値の取得が完了したタイミングで、引数に指定したブロックにコールバックされます。

> 🚧 事前にトラッカーの初期化が必要です。
> 初期化にはデフォルトトラッカーのアプリケーションキーが利用されます。
> そのためトラッカーの初期化が行われていない場合は、例外が発生します。

### Declaration

```objc
+ (void)fetchWitchCompletionBlock:(nonnull void (^)(BOOL isSuccessful))completion;
```

### Parameters

| Name       | Description |
| ---------- | ----------- |
| completion | 設定        |

### Return Value

初期化済みの設定オブジェクトを返します。

## `variableForKey:`

> Instance Method | v1.3.0 -

キーに紐付く [`KarteVariable`](kartevariable) オブジェクトを返します。
接客サービス側で設定値を設定していない場合であってもオブジェクトは返ります。
設定値の設定有無は `KarteVariable` クラスの `isDefined` プロパティを使って判定します。

### Declaration

```objc
- (nonnull KarteVariable *)variableForKey:(nonnull NSString *)key;
```

### Parameters

| Name | Description |
| ---- | ----------- |
| key  | 設定値キー  |

### Return Value

`KarteVariable` オブジェクトを返します。

## `variableForKey:`

> Type Method | v1.3.0 -

キーに紐付く `KarteVariable` オブジェクトを返します。
接客サービス側で設定値を設定していない場合であってもオブジェクトは返ります。
設定値の設定有無は `KarteVariable` クラスの `isDefined` プロパティを使って判定します。

> 🚧 事前にトラッカーの初期化が必要です。
> 初期化にはデフォルトトラッカーのアプリケーションキーが利用されます。
> そのためトラッカーの初期化が行われていない場合は、例外が発生します。

### Declaration

```objc
+ (nonnull KarteVariable *)variableForKey:(nonnull NSString *)key;
```

### Parameters

| Name | Description |
| ---- | ----------- |
| key  | 設定値キー  |

### Return Value

`KarteVariable` オブジェクトを返します。

## `trackWithVariables:withEventName:`

> Instance Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```objc
- (void)trackWithVariables:(NSArray *)variables withEventName:(NSString *)eventName;
```

### Parameters

| Name      | Description                 |
| --------- | --------------------------- |
| variables | Variable オブジェクトの配列 |
| eventName | イベント名                  |

## `trackWithVariables:withEventName:withValues:`

> Instance Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```objc
- (void)trackWithVariables:(NSArray *)variables withEventName:(NSString *)eventName withValues:(nullable NSDictionary *)values;
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| variables | `KarteVariable` オブジェクトの配列     |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |

## `trackWithVariables:withEventName:`

> Type Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```objc
+ (void)trackWithVariables:(NSArray *)variables withEventName:(NSString *)eventName;
```

### Parameters

| Name      | Description                        |
| --------- | ---------------------------------- |
| variables | `KarteVariable` オブジェクトの配列 |
| eventName | イベント名                         |

## `trackWithVariables:withEventName:withValues:`

> Type Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```objc
+ (void)trackWithVariables:(NSArray *)variables withEventName:(NSString *)eventName withValues:(nullable NSDictionary *)values;
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| variables | `KarteVariable` オブジェクトの配列     |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |
