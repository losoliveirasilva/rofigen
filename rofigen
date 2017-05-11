#!/bin/bash

source $1

# Window title
ROFI_TEXT=$title

# Optional window size
if [ -z ${widthpercent+x} ]; then
    ROFI_OPTIONS=(-location 0 -hide-scrollbar -bw 2)
else
    ROFI_OPTIONS=(-width $widthpercent -location 0 -hide-scrollbar -bw 2)
fi

# Optional window color
if ((${#colors[@]})); then
    for i in "${!colors[@]}"; do
        ROFI_COLORS+=($i "${colors[$i]}")
    done
else
    ROFI_COLORS=()
fi

launcher_options=(-dmenu -i -lines "${#menu[@]}" -p "${ROFI_TEXT}" \
         "${ROFI_COLORS[@]}" "${ROFI_OPTIONS[@]}") 

launcher=(rofi "${launcher_options[@]}")

selection="$(printf '%s\n' "${!menu[@]}" | sort | "${launcher[@]}")"

if [[ -n $selection ]]
then
    exec ${menu[${selection}]}
fi

