
# Changelog

### 1.4.3
- Fix face detection freezes on few Xiaomi devices.
- Fix occasional crash on face detection start due to race condition.

### 1.4.2
- Fix occasional crashes

### 1.4.1
- Fix crash on few Xiaomi devices due to bug in MIUI.

### 1.4.0
- interaction messages can be customized same way like error messages. Interaction events can be intercepted via `CameraOverlayDelegateOut.receive`.
- interaction can be enabled for every bestshot detection session via `LunaID.showCamera()` (instead of `LunaID.init()`)
- (minor) `LunaID.showCamera()` from now on accepts `ShowCameraParams` with all available params.

### v1.3.3
- add optional logging to file

### v1.3.2
- explicitly forbid to call `LunaID.init()` twice during Application's life-cycle.


### v1.3.1
- fix recorded video aspect ratio

### v1.3.0
- опциональная запись видео процедуры получения бестшота 
- возможность добавлять произвольные заголовки (статические и динамические) в запросы к Platform API  
- уменьшили minApi до 21

### v1.2.4
* фикс краша в некоторых случаях, если приложение собирается из консоли

### v1.2.3
* минорный фикс WebAPI
* рефакторинг работы с камерой, чтобы сделать ее независимой от жизненного цикла вызывающего кода

### v1.2.2
* фикс для опциональной проверки online-liveness во время получения бестшота

### 1.2.1
* фикс для просроченной лицензии


### 1.2.0
* минорные фиксы WebAPI
* новое WebApi, более точно совпадающее с Platform API
* новый пример как использовать WebAPI
* поддержка опциональной генерации дескрипторов на девайсе
* поддержка опциональной интеракции (моргнуть)
