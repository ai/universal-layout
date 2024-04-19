# Универсальная раскладка Ситника

## Установка

```sh
mkdir -p ~/.config/xkb/symbols/ ~/.config/xkb/rules/
curl -o ~/.config/xkb/symbols/universal_en https://raw.githubusercontent.com/ai/universal-layout/main/universal_en.xkb
curl -o ~/.config/xkb/symbols/universal_ru https://raw.githubusercontent.com/ai/universal-layout/main/universal_ru.xkb
curl -o ~/.config/xkb/rules/evdev.xml https://raw.githubusercontent.com/ai/universal-layout/main/evdev.xml
```

Перезапустите систему.

Выберите `Russian Universal` и `English/Spanish Universal` в настройках клавиатуры.

Мы также рекомендуем выставить немодальное переключение раскладки — <kbd>CapsLock</kbd> всегда на английский, <kbd>CapsLock</kbd>+<kbd>Shift</kbd> всегда на русский.

```sh
dconf write /org/gnome/desktop/input-sources/xkb-options "['grp_led:caps', 'lv3:ralt_switch', 'grp:shift_caps_switch']"
```

## Альтернативы

Проект вдохновлялся проектами — вы можете взять их? если они подходят вам лучше:
* [Раскладка Никиты Широкова](https://github.com/braindefender/universal-layout)
* [Раскладка Никиты Прокопова](https://github.com/tonsky/Universal-Layout)
* Встроенная в Линукс раскладка `misc:typo`, копия [Раскладки Бирмана](https://ilyabirman.ru/typography-layout/)