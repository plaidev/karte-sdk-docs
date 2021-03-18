[KARTE Android SDK v1](index)

# `KRLog`

> Class | v1.0.0 -

`KRLog` クラスは、SDK 内部で発生するログメッセージのコンソールへの出力を制御するクラスです。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `VERBOSE`

> Static Variable | v1.0.0 -

ログレベルの定数表現です。
これを設定すると、`ERROR` より更に詳細な動作状況に関する情報をコンソールに出力します。

### Declaration

```java
public static final int VERBOSE;
```

## `DEBUG`

> Static Variable | v1.0.0 -

ログレベルの定数表現です。
これを設定すると、動作状況に関する詳細な情報をコンソールに出力します。

### Declaration

```java
public static final int DEBUG;
```

## `INFO`

> Static Variable | v1.0.0 -

ログレベルの定数表現です。
これを設定すると、実行時の注目すべき情報をコンソールに出力します。

### Declaration

```java
public static final int INFO;
```

## `WARN`

> Static Variable | v1.0.0 -

ログレベルの定数表現です。
これを設定すると、エラーではないイレギュラーな問題が発生した際の情報をコンソールに出力します。

### Declaration

```java
public static final int WARN;
```

## `ERROR`

> Static Variable | v1.0.0 -

ログレベルの定数表現です。
これを設定すると、予期せぬ実行時エラーが発生した際の情報をコンソールに出力します。

### Declaration

```java
public static final int ERROR;
```

## `setLevel(int minLevel)`

> Static Method | v1.0.0 -

ログレベルを設定します。

### Declaration

```java
public static void setLevel(int minLevel);
```

### Parameters

| Name     | Description |
| -------- | ----------- |
| minLevel | ログレベル  |
