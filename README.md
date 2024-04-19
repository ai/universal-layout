# Универсальная раскладка Ситника

## Установка

```sh
mkdir -p ~/.config/xkb/symbols/ ~/.config/xkb/rules/
wget -O ~/.config/xkb/symbols/universal_en https://raw.githubusercontent.com/ai/universal-layout/main/universal_en.xkb
wget -O ~/.config/xkb/symbols/universal_ru https://raw.githubusercontent.com/ai/universal-layout/main/universal_ru.xkb
wget -O ~/.config/xkb/rules/evdev.xml https://raw.githubusercontent.com/ai/universal-layout/main/evdev.xml
```

Перезапустите систему.

Выберите `Russian Universal` и `English/Spanish Universal` в настройках клавиатуры.

Мы также рекомендуем выставить немодальное переключение раскладки — <kbd>CapsLock</kbd> всегда на английский, <kbd>CapsLock</kbd>+<kbd>Shift</kbd> всегда на русский.

```sh
dconf write /org/gnome/desktop/input-sources/xkb-options "['grp_led:caps', 'lv3:ralt_switch', 'grp:shift_caps_switch']"
```