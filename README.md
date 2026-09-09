# cod-for-liquid-boton-option-
prompt:

The top edge of this bottom nav is a liquid surface. The selected tab is a bead lying on it — and the surface dips beneath it, then smears as it moves.

The notch is NOT a stack of welded pseudo-element curves. It's one SVG path whose socket is solved for tangency: a convex shoulder turning the flat edge down, a concave bowl wrapping the bead exactly, a second shoulder back up. Because it's computed instead of assembled, it can change shape mid-flight — the trailing shoulder draws out long, the leading one tightens, and the bead squashes along its direction of travel. That asymmetry is the whole illusion.

What you're seeing:
• Tap a tab, or grab the bead and drag it along the bar
• Icons are picked up as it passes — each rises on its own proximity curve, dips in, gets set back down
• Release and it snaps to the nearest tab
• The accent is a live ramp (lime → amber → coral → rose) lerped from whatever sits under the bead, and the room's ambient wash follows it

Built as a real APG tab list, not a decoration: roving tabindex, arrow + Home/End keys, one panel at a time, visible focus ring, and two tones of every accent — the bright one fills the bead, the dark one prints the 11px label, because the bright tone only measures 3:1 against the bar and is unreadable at that size.

One rAF loop, one spring, and it parks itself when nothing is moving. With JavaScript off it degrades to a plain rounded bar that still works.

Stack: vanilla HTML + CSS + JavaScript. Zero dependencies. No framework, no canvas, no animation library.

Which component should I build next? Drop it in the comments.
