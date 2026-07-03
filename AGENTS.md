# Why This Fork Exists

This is a personal fork of [shell-ninja/hyprconf-v2](https://github.com/shell-ninja/hyprconf-v2) with a single local modification to improve window management behavior.

## Local Changes

### Commit: `ae15d2a` - "feat: prevent window focus/workspace stealing"

Modified `config/hypr/confs/windowrules.conf` to:

1. **Add `silent` flags to workspace rules** - Prevents applications from forcing workspace switches when they open. Apps will open in their assigned workspaces but won't steal focus or switch you away from your current workspace.

2. **Add global `noinitialfocus` rule** - Prevents new windows from stealing keyboard focus when they appear. This keeps your current workflow uninterrupted when new windows spawn.

## Rationale

The default Hyprland behavior of auto-switching workspaces and stealing focus on new windows was disruptive to workflow. These changes provide a more predictable window management experience where:
- Apps open in their designated workspaces without interrupting current work
- New windows don't steal keyboard focus
- You maintain control over workspace switching and focus management

## Upstream

This fork tracks the upstream `shell-ninja/hyprconf-v2` repository. The local change is minimal and should be rebased or merged appropriately when updating from upstream.
