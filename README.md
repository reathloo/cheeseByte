# cheeseByte

**Dots and Boxes against a CPU, packed into one 970-byte HTML file.**

## Play

Download [`cheeseByte.html`](cheeseByte.html) and open it in any modern browser. No server, install, assets, or internet connection is needed.

Click an empty line between two dots. Close a box to score and play again. Your boxes turn **green**; the CPU's turn **red**. The player with more boxes wins. **RESTART** resets the board.

## The 1 KiB challenge

The 5 × 5 board has **25 boxes and 60 drawable lines**. One 11 × 11 array holds both the occupied lines and the owners of completed boxes, so there is no separate board or score map. A single four-neighbor check detects a completed box for either player, including moves that close two boxes at once.

The CPU checks every free line, favoring captures and avoiding moves that offer you an immediate box. A random bonus changes its choice: openings vary, and it sometimes misses a capture or gives you a chance. It remains a small rule-based opponent, not a perfect solver.

The file contains the entire interface, game rules, CPU, scoring, result display, and reset button. Text characters draw the grid; a few HTML color values mark captured boxes. The shipped file is **970 bytes uncompressed**, 54 bytes below the 1,024-byte limit. The README and browser are outside that count; there is no build step or runtime dependency beyond the browser.
