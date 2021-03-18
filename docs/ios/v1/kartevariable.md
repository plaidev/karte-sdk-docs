[KARTE iOS SDK v1](index)

# `KarteVariable`

> Class | v1.3.0 -

`KarteVariable` クラスは、設定値配信に関連する機能で、設定値と配信元の接客サービスの情報を保持する機能を提供します。

[`KarteVariables`](kartevariables) クラスを経由して初期化されるため、個別で初期化して使用することはありません。

### Inherits From

`NSObject`

### Conforms To

None

## `campaignId`

> Instance Property | v1.3.0 -

接客サービスのキャンペーン ID。

### Declaration

```objc
@property (nonatomic, copy, nullable, readonly) NSString *campaignId;
```

## `shortenId`

> Instance Property | v1.3.0 -

接客アクションの短縮 ID。

### Declaration

```objc
@property (nonatomic, copy, nullable, readonly) NSString *shortenId;
```

## `isDefined`

> Instance Property | v1.3.0 -

接客サービス側で定義済みの設定値かどうかを返します。
定義済みの場合は `true`、未定義の場合は `false` を返します。

### Declaration

```objc
@property (nonatomic, assign, readonly) BOOL isDefined;
```

## `string`

> Instance Property | v1.3.0 -

設定値を文字列値として返します。
接客サービス側で設定値が未設定の場合は、`nil` を返します。

### Declaration

```objc
@property (nonatomic, copy, readonly, nullable) NSString *string;
```

## `array`

> Instance Property | v1.3.0 -

設定値を配列値として返します。

なお以下の場合は、`nil` を返します。

- 接客サービス側で設定値が未設定
- 設定値を配列として扱えない

### Declaration

```objc
@property (nonatomic, copy, readonly, nullable) NSArray *array;
```

## `dictionary`

> Instance Property | v1.3.0 -

設定値を辞書値として返します。

なお以下の場合は、`nil` を返します。

- 接客サービス側で設定値が未設定
- 設定値を辞書として扱えない

### Declaration

```objc
@property (nonatomic, copy, readonly, nullable) NSDictionary *dictionary;
```

## `stringWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を文字列値として返します。

### Declaration

```objc
- (nonnull NSString *)stringWithDefaultValue:(nonnull NSString *)defaultValue;
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を文字列として返します。
接客サービス側で設定値が未設定の場合は、引数として指定したデフォルト値を返します。

## `integerWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を整数値として返します。

### Declaration

```objc
- (NSInteger)integerWithDefaultValue:(NSInteger)defaultValue;
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を整数値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が数値として扱えない

## `doubleWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を浮動小数点数として返します。

### Declaration

```objc
- (double)doubleWithDefaultValue:(double)defaultValue;
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

## `boolWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を真偽値として返します。

### Declaration

```objc
- (BOOL)boolWithDefaultValue:(BOOL)defaultValue;
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を真偽値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が真偽値として扱えない

## `arrayWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を配列値として返します。

### Declaration

```objc
- (nonnull NSArray *)arrayWithDefaultValue:(nonnull NSArray *)defaultValue;
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を配列値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が配列として扱えない

## `dictionaryWithDefaultValue:`

> Instance Method | v1.3.0 -

設定値を辞書値として返します。

### Declaration

```objc
- (nonnull NSDictionary *)dictionaryWithDefaultValue:(nonnull NSDictionary *)defaultValue;
```

### Parameters

| Name         | Description                      |
| ------------ | -------------------------------- |
| defaultValue | 設定値が未設定の場合に利用する値 |

### Return Value

設定値を辞書値として返します。

なお以下の場合は、デフォルト値を返します。

- 接客サービス側で設定値が未設定
- 設定値が辞書値として扱えない
