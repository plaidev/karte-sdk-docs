[KARTE Android SDK v1](index)

# `InAppMessagingManager.OnOpenURLListener`

> Interface | v1.5.2 -

`InAppMessagingManager.OnOpenUrlListener` クラスは、アプリ内メッセージのリンククリック時の制御を行なうためのハンドラを提供します。

### Package

`io.karte.android.tracker.inappmessaging`

### Inherits From

None

### Conforms To

None

## `shouldOverrideOpenURL(Uri uri)`

> Instance Method | v1.5.2 -

アプリ内メッセージでリンクがタップされたことを Listener に通知し、そのリンクを SDK 側で自動的に開くかどうかを、Listener に尋ねます。

### Declaration

```java
boolean shouldOverrideOpenURL(Uri url);
```

### Return Value

リンクを自動的に開くかどうかを指定します。
`false` の場合は、SDK により自動的にリンクが開かれます。
`true` の場合は、SDK では何も行いません。
