# cheeseByte

**Dots and Boxes against a CPU, in exactly 1 KiB of HTML.** One file contains the game, its opponent, and the entire visual interface.

[Download the game](https://github.com/reathloo/cheeseByte/releases/latest/download/cheeseByte.html) · [View the source](cheeseByte.html)

## Play

Download `cheeseByte.html` and open it in a browser. No installation or server is needed; it also works offline.

Click between two adjacent dots to draw a line. Complete a box to score a point and take another turn. Your boxes are **green**, the CPU's are **red**. The higher score wins; **NEW** starts another game.

## How it fits

- **One board array:** An 11 × 11 grid maps all 36 dots, 60 possible lines, and 25 boxes. Its occupied-line and box-owner entries also serve as the game state.
- **One move routine:** It checks the boxes on both sides of a new line, awards up to two points, and handles the extra turn after a capture.
- **A compact CPU:** It evaluates the remaining lines for captures and risky setups. Randomness varies its choices and leaves room for mistakes; it is a heuristic opponent, not a perfect solver.
- **Drawn in code:** A 356 × 356 canvas renders the dots, lines, and colored boxes. The fills stay inside the lines. There are no image or style assets.

The complete HTML, JavaScript, canvas drawing, scoring, result display, and reset control are **1,024 bytes uncompressed**. Verify the limit with `wc -c cheeseByte.html`. The README is separate from the game file; there is no build step or runtime dependency beyond a browser.
