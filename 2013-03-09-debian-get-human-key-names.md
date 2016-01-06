  - Uncategorized
---
in cli

<pre>xev | grep -A2 --line-buffered '^KeyRelease' | sed -n '/keycode /s/^.*keycode \([0-9]*\).* (.*, \(.*\)).*$/\1 \2/p'
</pre>

then start pressing things.

<pre>133 Super_L
134 Super_R
135 Menu
105 Control_R
108 ISO_Level3_Shift
37 Control_L
133 Super_L
64 Alt_L
</pre>