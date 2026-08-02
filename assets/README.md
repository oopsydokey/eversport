# Eversport logo assets (option 2E)

## What's here
| File | Use |
| --- | --- |
| eversport-logo-light.png / -dark.png | primary lockup (bar + wordmark), 4x |
| eversport-logo-full-light.png / -dark.png | lockup + GAME ON tagline, 4x |
| eversport-mark-green.svg / -ink.svg (+ .png) | square mark — avatar, app icon |
| eversport-favicon.svg / -ink.svg (+ -256.png) | favicon |
| eversport-tally-bar.svg | the bar alone, reusable UI element |

The marks, favicon and bar are pure vector geometry — no font needed, safe in
`<img>`, `background-image` and `<link rel="icon">`.

The wordmark ships as PNG (4x, transparent on the light versions) because it is
set in Archivo Black; an SVG with live text would fall back to the wrong
typeface when loaded through `<img>`. For the website, build the lockup in
HTML instead — it stays crisp, selectable and themeable:

    <link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=JetBrains+Mono:wght@700&display=swap" rel="stylesheet">

    <a href="/" style="display:inline-flex;flex-direction:column;gap:9px;width:196px;text-decoration:none">
      <span style="display:flex;gap:3px;height:7px">
        <span style="flex:7;background:#3fbf4f"></span>
        <span style="flex:3;background:#dcdedb"></span>
      </span>
      <span style="font:400 29px/0.98 'Archivo Black',sans-serif;letter-spacing:0.005em;color:#2b322c">EVERSPORT</span>
    </a>

    <link rel="icon" href="/assets/eversport-favicon.svg">

On dark backgrounds swap #3fbf4f -> #5fe05a, #dcdedb -> #4a504a, #2b322c -> #f6f7f4.
If you need a true vector wordmark for print, open a PNG-free copy in Figma,
set EVERSPORT in Archivo Black and outline it.

## Colors
PITCH  #3fbf4f   primary green (light backgrounds)
FLOOD  #5fe05a   green on dark backgrounds
INK    #2b322c   text / dark background
DEEP   #16241a   marks on green
TRACK  #dcdedb   empty portion of the bar
PAPER  #f6f7f4   text on dark

## Type
Archivo Black (wordmark) · JetBrains Mono Bold (tagline, tally copy) — Google Fonts.

## Rules
Minimum width 120px. Clear space on all sides = 3x the bar height.
Never stretch, never recolor outside the palette, and never fill the bar to
100% — the empty portion is the point.
