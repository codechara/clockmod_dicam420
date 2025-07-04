# Digma DiCam 420
Digma DiCam 420 - Экшен камера от компании Digma построенная на чипе от [Allwinner V3](https://linux-sunxi.org/V3). Оригинальная прошивка названа как "Camdroid" и построенная на частях Android. (если посмотреть на его файлы и на файлы android-recovery, то они похожи). Прошивка поднимает adbd и консоль поднимает от рута.

## Основные компоненты на плате
- **25Q128FVFG** - SPI флеш-память на 16мб.
- **NT5CB128M16FP-DI** - Оперативная память DDR3 на 256mb.
- **XR819** - Wi-Fi чип.
- **AXP209** - Контроллер питания.
- **Экран на чипе ST7789** - *Дополнительный экран?*
- **Экран на чипе ILI9225G** - *Основной экран?*
- ***imx179s???*** - Матрица камеры.
- Так-же, есть распаенный усилитель звука для встроенного динамика.
- На дополнительной плате распаяно 2 кнопки, 3 светодиода и 1 микрофон.

## Инфа
Логи U-Boot и ядра пишутся в UART.

В целом, его родную флешку можно отпаять или замкнуть DI+CLK потому что проц умеет грузить SPL с сдхи и прекрасно грузит.

В [FEL](https://linux-sunxi.org/FEL) можно попасть двумя тремя:
- Слать цифру 2 в UART пины
- При подключении к питанию, зажать кнопку рядом с microUSB разьёмом.
- Зажать DI+CLK на флеш памяти, что бы он не смог с неё прочитать данные.

## Благодарности
**[Xp14](https://t.me/xp14rs)** - Спасибо за то что отдал мне эту экшен камеру и помог с u-boot. \
**[Автору этой статьи на Habr](https://habr.com/ru/articles/865146/)** - Спасибо ему за его интересную статью, и дополнительную информацию \
**[ktkd](https://github.com/ktkd)** - Спасибо ему за патчи для мейнлайн u-boot \
**[linux-sunxi](https://linux-sunxi.org)** - Спасибо сообществу linux-sunxi за их тяжёлый труд в разработке открытого программного обеспечения для Allwinner!
