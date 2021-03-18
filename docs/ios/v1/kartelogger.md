[KARTE iOS SDK v1](index)

# `KarteLogger`

> Class | v1.3.0 -

`KarteLogger` クラスは、SDK 内部で発生するログメッセージのコンソールへの出力を制御するクラスです。

### Inherits From

`NSObject`

### Conforms To

`NSCopying`

## `sharedLogger`

> Type Property | v1.3.0 -

共有のロガーオブジェクト。

### Declaration

```objc
@property (class, strong, readonly, nonnull) KarteLogger *sharedLogger;
```

## `logLevel`

> Instance Property | v1.3.0 -

ログレベル。

### Declaration

```objc
@property (nonatomic, assign) KarteLogLevel logLevel;
```
