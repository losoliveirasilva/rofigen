# rofigen - Generates rofi application

## Getting Started

To start, download `rofigen` to your computer. Next, follow along with a couple
of examples which you can find in the repository:

### Example #1 - Kawaii Faces

```bash
#!/bin/bash

title="Kawaii faces:"
widthpercent=10

typeset -A menu
menu=(
  [( ͡° ͜ʖ ͡°)]="~/sh_kawaiifaces 2"
  [¯\_(ツ)_/¯]="~/sh_kawaiifaces 1"
  [Cancel]=""
)
menu_nrows=${#menu[@]}
```

#### Output

![Menu](images/example1-1.png)

- `title` title displayed
- `widthpercent` set width of menu, is specified in percentage
- `menu` menu items: `[text]="command_to_execute"`
