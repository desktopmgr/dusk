## Key Bindings

Source: cross-desktop app/media/lock/screenshot/logout bindings come
from the shared `run_sxhkd` (dfmgr/sxhkd `etc/sxhkdrc`), started by
`etc/autostart.sh`. `etc/bspwm-sxhkdrc` holds only dusk's own
bspwm-specific window-management bindings (see TODO.AI.md for a
pre-existing config issue found while auditing this).

### Cross-desktop canonical bindings (via dfmgr/sxhkd)

```text
super + Return                   # Open terminal
super + alt + b                  # Open browser
alt + r                          # Open file manager
super + alt + l                  # Lock screen (loginctl lock-session)
Print                            # Screenshot menu
shift + Print                    # Screenshot of a selected region
XF86Audio{RaiseVolume,LowerVolume} # Volume up/down
XF86AudioMute                    # Mute toggle
XF86MonBrightness{Up,Down}       # Brightness down/up
super + alt + ctrl + l           # Logout menu
```

### dusk-specific bindings (etc/bspwm-sxhkdrc)

```text
super + {_,shift + }q            # Close/kill window
super + {_,shift + }f            # Toggle monocle/fullscreen
super + y                        # Rotate current node 90 degrees
super + space                    # Swap with biggest local node
super + shift + space            # Toggle floating
super + {_,shift + }{h,j,k,l}    # Focus/swap node in direction
super + {p,b,comma,period}       # Focus node by path jump
super + {g,semicolon}            # Focus prev/next occupied desktop
super + {Prior,Next}             # Focus prev/next occupied desktop
super + {Tab,backslash}          # Focus last desktop
super + {_,shift + }c            # Focus/swap next local node
super + {_,shift + }{1-9,0}      # Focus/send to desktop
super + ctrl + {1-9}             # Preselect ratio
super + ctrl + space             # Cancel preselection
super + shift + {y,u,i,o}        # Expand window side
super + {Left,Down,Up,Right}     # Move floating window
super + shift + d                # Toggle gaps
super {_,+ shift} + z            # Increase/decrease gap size
super + u                        # Restore dropdown window
super + o                        # Toggle sticky (see TODO.AI.md conflict)
super + {i,o}                    # Focus prev/next local node
super + shift + n                # Float + hover right
super + shift + b                # Float + hover left
```
