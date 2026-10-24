# cheeseByte

**Dots and Boxes against a CPU, packed into one 1,024-byte HTML file.**

## Play

Download [`cheeseByte.html`](cheeseByte.html) and open it in any modern browser. No server, install, assets, or internet connection is needed.

Click an empty line between two dots. Close a box to score and play again. Your boxes turn **green**; the CPU's turn **red**. The player with more boxes wins. **NEW** starts a new game.

## The 1 KiB challenge

The 5 × 5 board has **25 boxes and 60 drawable lines**. One 11 × 11 array holds both the occupied lines and the owners of completed boxes, so there is no separate board or score map. A single four-neighbor check detects a completed box for either player, including moves that close two boxes at once.

The CPU checks every free line, favoring captures and avoiding moves that offer you an immediate box. A random bonus changes its choice: openings vary, and it sometimes misses a capture or gives you a chance. It remains a small rule-based opponent, not a perfect solver.

The file contains the entire interface, game rules, CPU, scoring, result display, and reset button. A 356 × 356 pixel canvas draws white dots and teal lines at fixed coordinates. Captured boxes are 60 × 60 pixel rectangles that meet the inside edges of the lines without covering them. Short score labels and the compact button make room for the canvas drawing code. The shipped file is **1,024 bytes uncompressed**, exactly at the 1 KiB limit. The README and browser are outside that count; there is no build step or runtime dependency beyond the browser.
