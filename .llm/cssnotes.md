## Key CSS Selectors

Zen 1.22.3b, 2026/10/01, checked against a devtools DOM dump. Items marked [zen] are injected by Zen's JS and only exist while that feature is enabled.
See [treeref.md](./treeref.md) for the DOM order and [toolbar.html](./toolbar.html) for the markup.

### Primary Container
- `#tabContextMenu` - Main tab context menu popup

### Open & Organize (top section, ends at `#context_openAndOrganizeSeparator`)
- `#context_openANewTab` - New tab below / to the right
- `#context_moveTabToNewGroup` / `#context_moveSplitViewToNewGroup` - Add tab / split view to a new group
- `#context_zenMoveToFolder` [zen] - "Move to Folder" submenu; its unnamed `menupopup` gets one item per folder plus `#zen-context-menu-new-folder`
- `#context_moveTabToGroup` - "Add Tab to Group" submenu
- `#context_moveTabToGroupPopupMenu` - its popup: `#context_moveTabToGroupNewGroup`, one `menuitem[tab-group-id]` per open group between `#open-tab-groups-separator-upper` / `-lower`, and `#context_moveTabToSavedGroup` ("Closed Groups") with `#context_moveTabToSavedGroupPopupMenu`
- `#context_ungroupTab` / `#context_ungroupSplitView` - Remove from group
- `#context_zenSplitTabs` [zen] - Add split view / split out / join tabs
- `#context_zenShareSplitView` [zen] - Share split view
- `#context_moveTabToSplitView` / `#context_separateSplitView` / `#context_reverseSplitView` - Firefox split view items (no `.badge-new` any more)

### Tab Actions (ends at `#context_tabStateSeparator`)
- `#context_reloadTab` / `#context_reloadSelectedTabs`
- `#context_playTab` / `#context_playSelectedTabs`
- `#context_toggleMuteTab` / `#context_toggleMuteSelectedTabs`
- `#context_pinTab` / `#context_unpinTab` / `#context_pinSelectedTabs` / `#context_unpinSelectedTabs`
- `#context_unloadTab`
- `#context_duplicateTab` / `#context_duplicateTabs`

### Essentials & Tab Customization [zen] (inserted just before `#context_pinTab`)
- `#context_zen-add-essential` / `#context_zen-remove-essential` - add-essential carries a `badge` attribute with the slot count (e.g. "0 / 12")
- `#context_zen-edit-tab-title` ("Change Label…") / `#context_zen-edit-tab-icon` ("Change Icon…")
- Two unnamed separators wrap the edit items: `#context_zen-remove-essential + menuseparator` and `#context_zen-edit-tab-icon + menuseparator`

### AI (ends at `#context_aiSeparator`)
- `#context_askChat` - "Ask <chatbot>" submenu, popup built lazily
- `#context_askChatSummarize` - "Summarize Page" (hidden in the classic layout)

### Tab Tools (ends at `#context_tabToolsSeparator`)
- `#context_bookmarkTab` / `#context_bookmarkSelectedTabs`
- `#context_addNote` / `#context_editNote`
- `#context_moveTabOptions` - "Move Tab" submenu
- `#moveTabOptionsMenu` - its popup: `#context_moveToStart`, `#context_moveToEnd`, `#context_openTabInWindow`, `#moveTabSeparator`, plus `#context_moveTabToGroupSeparator` and `#context_selectAllSeparator` (both hidden in the classic layout)
- `.zen-workspace-context-menu-item` - one per other space (and a separator with the same class), prepended to `#moveTabOptionsMenu` on open; `[zen-workspace-id]` carries the space id
- `menuitem[profileid]` - per-profile entries inserted after `#moveTabSeparator`
- `.share-tab-url-item` - lazily created share submenu, placed right after `#context_moveTabOptions`. Its unnamed popup holds `.share-copy-link`, `.share-qrcode-item` (both `.menuitem-iconic` with an `image` attribute), an unnamed separator, and `.share-windows-item` ("More Options")
- `#context_reopenInContainer` / `#context_reopenInContainerPopupMenu` - container submenu; entries are `.menuitem-iconic.identity-color-<color>.identity-icon-<icon>`
- `#context_selectAllTabs`

### Sending (ends at `#context_sendTabToDeviceSeparator`)
- `#context_shareSelectedTabs` ("Create Shareable Link") / `#context_shareSelectedTabsSeparator`
- `#context_sendTabToDevice.sync-ui-item` / `#context_sendTabToDevicePopupMenu` - device entries are `.sync-menuitem.sendtab-target[clientType]` (`phone` / `desktop`); "Send to All Devices" and "Manage Devices…" share the same classes

### Close Actions
- `#context_closeTab`
- `#context_closeDuplicateTabs`
- `#context_closeTabOptions` / `#closeTabOptions` - "Close Multiple Tabs" submenu: `#context_closeTabsToTheStart`, `#context_closeTabsToTheEnd`, `#context_closeOtherTabs`
- `#context_undoCloseTab`
- `#context_zen-add-domain-to-routing` [zen] - "Add Route for Domain", after `#context_undoCloseTab`, preceded by an unnamed separator (`#context_undoCloseTab + menuseparator`)

### Fullscreen (starts at `#context_fullscreenSeparator`)
- `#context_fullscreenAutohide.fullscreen-context-autohide` / `#context_fullscreenExit`

### Pinned / Essential Tab Tail [zen] (appended at the very end of the menu)
- `#context_zen-pinned-tab-separator`
- `#context_zen-edit-pinned-page` - "Edit Pinned URL" submenu holding `#context_zen-replace-pinned-url-with-current` and `#context_zen-edit-pinned-url`
- `#context_zen-reset-pinned-tab`

### Common Element Classes (inside every item)
- `.menu-icon`, `.menu-text`, `.menu-highlightable-text`, `.accesskey`, `.menu-accel`

### Separators
- Named, top level: `#context_openAndOrganizeSeparator`, `#context_tabStateSeparator`, `#context_aiSeparator`, `#context_tabToolsSeparator`, `#context_shareSelectedTabsSeparator`, `#context_sendTabToDeviceSeparator.sync-ui-item`, `#context_fullscreenSeparator`, `#context_zen-pinned-tab-separator`
- Named, inside submenus: `#open-tab-groups-separator-upper` / `-lower`, `#moveTabSeparator`, `#context_moveTabToGroupSeparator`, `#context_selectAllSeparator`
- Unnamed (Zen injections), target positionally: `#context_zen-remove-essential + menuseparator`, `#context_zen-edit-tab-icon + menuseparator`, `#context_undoCloseTab + menuseparator`, `#context_zenMoveToFolder menuseparator`

### Notes
- Ids used in chrome.css that no longer exist anywhere in 1.22.3b, with no successor (removed features): `context-pocket`, `context-savelinktopocket` (Firefox dropped Pocket), `context_zenDeleteWebPanel`, `context_zenOpenNewTabWebPanel`, `context_zenToggleMuteWebPanel`, `context_zenWebPanelContextInContainer`, `zen-sidebar-web-panel-pinned` (Zen dropped web panels), `context_zenOpenWorkspace`, `context_zenOpenWorkspacePanel` (removed from the space menu). Rules targeting them are harmless no-ops.
- Renamed in 1.22 and already applied to chrome.css: `.menu-iconic-left` / `.menu-iconic-icon` -> `.menu-icon` (icons are set with `content`, not `list-style-image`), `.menu-iconic-text` -> `.menu-text`, `[checked='true']` -> `[checked]` (checked is presence-only; unchecked items drop the attribute, never `checked='false'`), `#context-zen-change-workspace-tab` -> `#context_moveTabOptions` (spaces now live in the Move Tab submenu as `.zen-workspace-context-menu-item`). Removed as duplicates: the `#context_selectedAllTabs` typo and `#context_zenTabActions`.
- Don't target tab menu items by position (`:nth-child`). Counts shift with spaces, devices and enabled Zen features, and nested `:nth-child` inside `#tabContextMenu { }` matches inside submenus too. Use the named section separators, or Zen's unnamed ones via their neighbour (`#context_zen-edit-tab-icon + menuseparator`, `#context_undoCloseTab + menuseparator`).
- Preference names that don't match between chrome.css and preferences.json:
  - chrome.css reads `uc.hidecontext.closemultiple`, but the Settings toggle writes `uc.hidecontext.closetabmultiple`, so "Hide Close Multiple Tabs" has no effect.
  - chrome.css reads `uc.hidecontext.newtab`, which has no toggle in preferences.json.
  - `uc.hidecontext.unloadactions` ("Hide Unload Tabs") has a toggle but no rule in chrome.css.
  - `widget.macos.native-context-menus` is also declared but not read by chrome.css. That is intended, because it is a Firefox pref the toggle flips directly.
- `#ContentSelectDropdown` is not in the tab menu tree but is still live. The toolkit creates it at runtime (`SelectParent.sys.mjs`) as the menulist for web page `<select>` dropdowns. chrome.css uses it in `:not(...)` to keep the icon-padding rules off those dropdowns, so keep it.
- New since 1.18.5b: `#context_zenMoveToFolder`, `#context_zenShareSplitView`, `#context_reverseSplitView`, `#context_askChatSummarize`, `#context_shareSelectedTabs`, `#context_zen-edit-pinned-page` / `#context_zen-edit-pinned-url`, `#context_zen-add-domain-to-routing`, and the named section separators.
- Firefox's MenuSectionLayout (tab-context-menu.js) would reorder the menu on first open, but in Zen 1.22.3b it throws and leaves the DOM untouched because Zen's injected items are not declared in its layout. DOM order is therefore the authored order plus the injection points above. If Zen adds its items to that layout in a later release, the order will change.
