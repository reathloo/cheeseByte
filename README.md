# cheeseByte

Dots and Boxes against a CPU opponent in a single **1,024-byte HTML file**.

## Play offline

Download [`index.html`](index.html) and open it in a browser. No installation, server, external assets, or network connection is needed.

Click an empty line between two `+` signs. Complete a box to score a point and take another turn. You are `X`; the CPU is `O`. Use **NEW GAME** to reset.

## How it fits

The game stores its 24 lines and 9 boxes in one 7 × 7 grid. The CPU closes available boxes, otherwise avoids setting up an immediate point for you when it can. HTML, CSS, and JavaScript are all inside `index.html`; the browser is the only runtime.
