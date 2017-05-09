# rofigen - Generates rofi application

## Getting Started

To start, download `rofigen` to your computer.
You can run `rofigen` with
```./rofigen ~/kawaiifaces```

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

![Menu-kawaii](images/example1-1.png)

### Example #2 - Printscreen

```bash
#!/bin/bash

title="Printscreen:"
widthpercent=15

typeset -A menu
menu=(
  [Selection | clipboard]="~/sh_printscreen 4"
  [Selection | folder]="~/sh_printscreen 3"
  [Fullscreen | clipboard]="~/sh_printscreen 2"
  [Fullscreen | folder]="~/sh_printscreen 1"
  [Cancel]=""
)
menu_nrows=${#menu[@]}
```

#### Output

![Menu-print](images/example2-1.png)
