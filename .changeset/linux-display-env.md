---
"@openfilm/desktop": patch
---

Desktop: started from a terminal on a Linux desktop, the app finds the session's display. Electron was given the OS identity variables but not DISPLAY, WAYLAND_DISPLAY or XAUTHORITY, which the display manager sets for every program it starts, so on X11 and Wayland it exited with "Missing Xserver or $DISPLAY". They are handed on now, with XDG_RUNTIME_DIR; an agent's own variables are still kept from it.
