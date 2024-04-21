# Универсальная раскладка Ситника

* **Немодальное переключение языка.** <kbd>CapsLock</kbd> — всегда
  на английский. <kbd>Shift</kbd>+<kbd>CapsLock</kbd> — всегда на русский.
  Светодиод CapsLock указывает на текущий язык.
* **Знаки препинания на одном и том же месте.** `,` `.` `?` совпадают во всех
  раскладках.
* **Английская раскладка без изменений.** В русской раскладке сдвинуты только 2 
  буквы — <kbd>Б</kbd> и <kbd>Ю</kbd>.
* Можно быстро вводить «правильные кавычки», длинное тире, градус (10°C),
  стрелки (↓↑←→) и многие другие спец. символы (м², ⅓, ≠).
* Можно вводить **испанский** и **каталонский** текст на английской
  ANSI-клавиатуре (с длинным <kbd>↵</kbd> и без лишней клавиши). Включая ¿, ¡,
  l·l.

## Установка

Установка не меняет глобальные файлы. Всё ставиться в `~/.config/` в директории
пользователя. 

```sh
mkdir -p ~/.config/xkb/symbols/ ~/.config/xkb/rules/
curl -o ~/.config/xkb/symbols/universal_en https://raw.githubusercontent.com/ai/universal-layout/main/universal_en.xkb
curl -o ~/.config/xkb/symbols/universal_ru https://raw.githubusercontent.com/ai/universal-layout/main/universal_ru.xkb
curl -o ~/.config/xkb/rules/evdev.xml https://raw.githubusercontent.com/ai/universal-layout/main/evdev.xml
```

Перезапустите систему.

Выберите `Russian Universal` и `English/Spanish/Catalan Universal` в настройках клавиатуры.

Мы также рекомендуем выставить немодальное переключение раскладки — <kbd>CapsLock</kbd> всегда на английский, <kbd>CapsLock</kbd>+<kbd>Shift</kbd> всегда на русский.

```sh
dconf write /org/gnome/desktop/input-sources/xkb-options "['grp_led:caps', 'lv3:ralt_switch', 'grp:shift_caps_switch']"
```

## Альтернативы

Проект вдохновлялся проектами — вы можете взять их? если они подходят вам лучше:
* [Раскладка Никиты Широкова](https://github.com/braindefender/universal-layout)
* [Раскладка Никиты Прокопова](https://github.com/tonsky/Universal-Layout)
* Встроенная в Линукс раскладка `misc:typo`, копия [Раскладки Бирмана](https://ilyabirman.ru/typography-layout/)