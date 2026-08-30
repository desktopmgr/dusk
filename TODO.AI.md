# TODO

## etc/bspwmrc and etc/bspwm-sxhkdrc issues (found incidentally, out of scope for keybinding standardization)

- [ ] `etc/bspwmrc:19` (`sleep 60 && sxhkd -c ~/.config/bspwm/bspwm-sxhkdrc &`)
      points at bspwm's config path, not dusk's own
      (`~/.config/dusk/bspwm-sxhkdrc`), and is redundant with
      `etc/autostart.sh:103-105` which kills any running sxhkd and
      restarts it via `run_sxhkd` anyway. Confirm intent and fix the
      path or remove the line.
- [ ] `super + o` is bound twice in `etc/bspwm-sxhkdrc`: line 97
      (`bspc node -g sticky={on,off}`) and line 104-105
      (`super + {i,o}` -> `bspc node -f {prev,next}.local`). Only one
      can actually fire; decide which binding is intended.
