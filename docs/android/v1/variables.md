[KARTE Android SDK v1](index)

# `Variables`

> Class | v1.3.0 -

`Variables` クラスは、設定値配信に関連するクラスで、以下の機能を提供します。

- 設定値の取得
- 設定値の保持・管理
- 効果測定用のイベントの送信

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `getInstance(Context context)`

> Static Method | v1.3.0 -

初期化済みの `Variables` オブジェクトを返します。

> 🚧 このメソッドの呼び出しについて
> 初期化にはデフォルトトラッカーのアプリケーションキーが利用されます。
> そのため本プロパティを呼び出す前にトラッカーの初期化が必要です。

### Declaration

```java
public static Variables getInstance(Context context);
```

### Parameters

| Name    | Description |
| ------- | ----------- |
| context | `Context`   |

### Return Value

初期化済みの `Variables` オブジェクトを返します。

## `getInstance(Context context, String appKey)`

> Static Method | v1.3.0 -

初期化済みの `Variables` オブジェクトを返します。

### Declaration

```java
public static Variables getInstance(Context context, String appKey);
```

### Parameters

| Name    | Description          |
| ------- | -------------------- |
| context | `Context`            |
| appKey  | アプリケーションキー |

### Return Value

初期化済みの `Variables` オブジェクトを返します。

## `fetch()`

> Instance Method | v1.3.0 -

設定値を取得します。
取得は非同期で行われるため、設定値の取得完了をトリガーに処理を行いたい場合は、`fetch(final CompletionHandler completionHandler)` を利用してください。

### Declaration

```java
public void fetch();
```

## `fetch(final CompletionHandler completionHandler)`

> Instance Method | v1.3.0 -

設定値を取得します。
設定値の取得が完了したタイミングで、引数に指定したハンドラにコールバックされます。

### Declaration

```java
public void fetch(final CompletionHandler completionHandler);
```

### Parameters

| Name              | Description          |
| ----------------- | -------------------- |
| completionHandler | 取得完了通知ハンドラ |

## `getVariable(String key)`

> Instance Method | v1.3.0 -

キーに紐付く [`Variable`](variable) オブジェクトを返します。
接客サービス側で設定値を設定していない場合であってもオブジェクトは返ります。

### Declaration

```java
public Variable getVariable(String key);
```

### Parameters

| Name | Description |
| ---- | ----------- |
| key  | 設定値キー  |

### Return Value

`Variable` オブジェクトを返します。

## `track(Iterable<Variable> variables, String eventName)`

> Instance Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```java
public void track(Iterable<Variable> variables, String eventName);
```

### Parameters

| Name      | Description                   |
| --------- | ----------------------------- |
| variables | `Variable` オブジェクトの配列 |
| eventName | イベント名                    |

## `track(Iterable<Variable> variables, String eventName, JSONObject values)`

> Instance Method | v1.3.0 -

効果測定用のイベントを送信します。

### Declaration

```java
public void track(Iterable<Variable> variables, String eventName, JSONObject values);
```

### Parameters

| Name      | Description                            |
| --------- | -------------------------------------- |
| variables | `Variable` オブジェクトの配列          |
| eventName | イベント名                             |
| values    | イベントに紐付けるカスタムオブジェクト |
