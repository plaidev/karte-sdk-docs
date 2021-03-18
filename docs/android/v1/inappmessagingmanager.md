[KARTE Android SDK v1](index)

# `InAppMessagingManager`

> Class | v1.5.0 -

`InAppMessagingManager` クラスは、アプリ内メッセージに関連する機能を提供します。

### Package

`io.karte.android.tracker.inappmessaging`

### Inherits From

None

### Conforms To

None

## `dismiss()`

> Instance Method | v1.5.0 -

表示中のアプリ内メッセージをリセットします。

### Declaration

```java
public void dismiss();
```

## `isPresenting()`

> Instance Method | v1.5.0 -

接客が表示中であるか判定します。

### Declaration

```java
public boolean isPresenting();
```

### Return Value

判定結果を返します。アプリ内メッセージを表示中の場合は `true`、そうでない場合は `false` を返します。

## `setOnOpenURLListener(OnOpenURLListener listener)`

> Instance Method | v1.5.2 -

[`OnOpenURLListener`](inappmessagingmanager_onopenurllistener) をセットします。

### Declaration

```java
public void setOnOpenURLListener(OnOpenURLListener listener);
```

### Parameters

| Name     | Description         |
| -------- | ------------------- |
| listener | `OnOpenURLListener` |

## `removeOnOpenURLListener()`

> Instance Method | v1.5.2 -

OnOpenURLListener リスナーを解除します。

### Declaration

```java
public void removeOnOpenURLListener();
```

## `registerPopupWindow(PopupWindow popupWindow)`

> Instance Method | v1.6.6 -

アプリ内で保持している `PopupWindow` を渡します。SDK はアプリ内メッセージ表示中に、渡された `PopupWindow` の状態に応じてタップの透過等を行ないます。

### Declaration

```java
public void registerPopupWindow(PopupWindow popupWindow);
```

### Parameters

| Name        | Description   |
| ----------- | ------------- |
| popupWindow | `PopupWindow` |

## `registerWindow(Window window)`

> Instance Method | v1.6.6 -

アプリ内で保持している `TYPE_APPLICATION_PANEL` タイプの `Window` を渡します。SDK はアプリ内メッセージ表示中に、渡された `Window` の状態に応じてタップの透過等を行ないます。

### Declaration

```java
public void registerWindow(Window window);
```

### Parameters

| Name   | Description |
| ------ | ----------- |
| window | `Window`    |
