# BrightPath — exactly 4 intentional UI alignment/layout issues

Open `index.html` in a browser. All four issues are deliberately introduced in `styles.css`. No other bugs are intentionally added.

| # | Element / selector | Where to change | Existing broken rule | Exact fix | Why |
|---|---|---|---|---|---|
| 1 | Header “Get Started” button / `.header-cta` | `styles.css`, find `/* ISSUE 1 */` | `transform:translateY(16px)` | Delete `transform:translateY(16px)` (or use transform:none`) | Lets the flex header's `align-items:center` vertically center the button. |
| 2 | Hero illustration / `.hero-art` | `styles.css`, find `/* ISSUE 2 */` | `transform:translateX(55px)` | Delete `transform:translateX(55px)` (or use `transform:none`) | Aligns artwork inside its grid column and avoids right-side overflow. |
| 3 | Middle service card / `.featured-card` | `styles.css`, find `/* ISSUE 3 */` | `margin-top:42px` | Change to `margin-top:0` | Restores a consistent top edge across all three service cards. |
| 4 | Contact form / `.contact-form` | `styles.css`, find `/* ISSUE 4 */` | `transform:translateX(48px)` | Delete `transform:translateX(48px)` (or use `transform:none`) | Aligns form to its grid column and prevents right-side overflow. |

## How to verify
1. Open `index.html` in Chrome or Edge.
2. Observe the displaced header button, hero artwork, middle service card, and contact form.
3. Open `styles.css` and search for `ISSUE 1` through `ISSUE 4`.
4. Apply each exact change above, save, and refresh the browser.
5. Test at 1440px desktop and 375px mobile widths.

The form is a demonstration only; it displays a local message instead of sending data.
