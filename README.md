# Rounded Corners Overlay (Screen-anchored)

Simpler alternative to per-window tracking: since a maximized window is
always flush with its monitor's work area, this pins four small
click-through, topmost, layered "corner mask" windows to the work-area
corners of every monitor -- once, at startup, plus whenever display
configuration changes (resolution, monitor added/removed, taskbar
moved/resized).

Whatever window happens to be maximized underneath a corner automatically
appears to have that corner clipped round. Works instantly for any app,
any process, with no window enumeration loop at all.

Trade-off vs. per-window tracking: this only rounds corners that touch a
monitor's work-area edge. A maximized window on a single monitor gets all
four corners rounded (since it fills the whole work area). If you ever use
a window that's large but not technically maximized, or an edge-snapped
half-screen window, only the corners that land on the monitor's own
corners will be rounded -- snapped windows won't get their inner corners
touched by this mod, which is usually what you want anyway (only the
screen-facing outer corners are visually squared off by DWM to begin
with).
