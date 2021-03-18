[KARTE Android SDK v1](index)

# `Tracker.CompletionHandler`

> Interface | v1.5.2 -

`Tracker.CompletionHandler` クラスは、ログアウト等の非同期処理完了を検知するためのハンドラを提供します。

### Package

`io.karte.android.tracker`

### Inherits From

None

### Conforms To

None

## `onCompleted(boolean isSuccessful)`

> Instance Method | v1.5.2 -

非同期処理の完了時に呼び出されます。

### Declaration

```java
void onCompleted(boolean isSuccessful);
```

### Parameters

| Name         | Description    |
| ------------ | -------------- |
| isSuccessful | 処理の成功可否 |
