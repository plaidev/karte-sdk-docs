[KARTE Android SDK v1](index)

# `Variable`

> Class | v1.3.0 -

`Variable` クラスは、設定値配信に関連する機能で、設定値と配信元の接客サービスの情報を保持する機能を提供します。

[`Variables`](variables) クラスを経由して初期化されるため、個別で初期化して使用することはありません。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `getCampaignId()`

> Instance Method | v1.3.0 -

接客サービスのキャンペーン ID を返します。

### Declaration

```java
public String getCampaignId();
```

### Return Value

接客サービスのキャンペーン ID を返します。

## `getShortenId()`

> Instance Method | v1.3.0 -

接客アクションの短縮 ID。

### Declaration

```java
public String getShortenId();
```

### Return Value

接客アクションの短縮 ID を返します。

## `getString(String defaultValue)`

> Instance Method | v1.3.0 -

設定値を文字列値として返します。

### Declaration

```java
public String getString(String defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を文字列として返します。
接客サービス側で設定値が未設定の場合は、引数として指定したデフォルト値を返します。

## `getLong(long defaultValue)`

> Instance Method | v1.3.0 -

設定値を整数値として返します。

### Declaration

```java
public long getLong(long defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を整数値として返します。
値が浮動小数点数の場合、浮動小数点以下は切り捨てられます。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が数値として扱えない

## `getDouble(double defaultValue)`

> Instance Method | v1.3.0 -

設定値を浮動小数点数として返します。

### Declaration

```java
public double getDouble(double defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を浮動小数点値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が数値として扱えない

## `getBoolean(boolean defaultValue)`

> Instance Method | v1.3.0 -

設定値を真偽値として返します。

### Declaration

```java
public boolean getBoolean(boolean defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を真偽値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定

## `getJSONObject(JSONObject defaultValue)`

> Instance Method | v1.3.0 -

設定値を `JSONObject` 値として返します。

### Declaration

```java
public JSONObject getJSONObject(JSONObject defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を `JSONObject` 値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が `JSONObject` 値として扱えない

## `getJSONArray(JSONArray defaultValue)`

> Instance Method | v1.3.0 -

設定値を `JSONArray` 値として返します。

### Declaration

```java
public JSONArray getJSONArray(JSONArray defaultValue);
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を `JSONArray` 値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が `JSONArray` 値として扱えない
