# Tab Context Menu - CSS Styling Reference

Zen 1.22.3b (zen-browser/desktop @ ca522d44), generated 2026/10/01 from [toolbar.html](./toolbar.html).
DOM order of `#tabContextMenu` in the classic layout (`browser.tabs.contextmenu.altstructure.enabled` = false).

Legend:
- `[zen]` = injected at runtime by Zen's JS (see the comments in toolbar.html for the source file). Present only when that feature is enabled.
- `(runtime)` = items generated when the popup opens (one per space / group / container / device); only their classes and attributes are stable.
- Labels in quotes are en-US; `A / B` means the label depends on state (single vs multiple tabs, pinned vs essential, vertical vs horizontal tabs).
- Every `menuitem` and `menu` renders the same internal anatomy, omitted below. Target it with descendant selectors (e.g. `#context_closeTab .menu-text`):

```
menuitem#any-item
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel
```

```
menupopup#tabContextMenu
├── menuitem#context_openANewTab ("New Tab Below (vertical tabs) / New Tab to Right")
├── menuitem#context_moveTabToNewGroup ("Add Tab to New Group")
├── menuitem#context_moveSplitViewToNewGroup ("Add Split View to New Group")
├── menu#context_zenMoveToFolder ("Move to Folder")  [zen]
│   └── menupopup  [zen]
│       ├── menuseparator (no id)  [zen]
│       └── menuitem#zen-context-menu-new-folder ("New Folder")  [zen]
├── menu#context_moveTabToGroup ("Add Tab to Group / Add Tabs to Group")
│   └── menupopup#context_moveTabToGroupPopupMenu
│       ├── menuitem#context_moveTabToGroupNewGroup ("New Group")
│       ├── menuseparator#open-tab-groups-separator-upper
│       ├── menuseparator#open-tab-groups-separator-lower
│       ├── menu#context_moveTabToSavedGroup ("Closed Groups")
│       │   └── menupopup#context_moveTabToSavedGroupPopupMenu
│       │       └── (runtime) one menuitem[tab-group-id] per saved group (tab-context-menu.js)
│       └── (runtime) one menuitem[tab-group-id] per open tab group, inserted between the two separators (tab-context-menu.js)
├── menuitem#context_ungroupTab ("Remove from Group")
├── menuitem#context_ungroupSplitView ("Remove from Group")
├── menuitem#context_zenSplitTabs ("Add Split View... / Split Out Tab / Join N Tabs")  [zen]
├── menuitem#context_zenShareSplitView ("Share Split View…")  [zen]
├── menuitem#context_moveTabToSplitView ("Add Split View / Open in Split View")
├── menuitem#context_separateSplitView ("Separate Split View")
├── menuitem#context_reverseSplitView ("Reverse Tabs")
├── menuseparator#context_openAndOrganizeSeparator   <- end of open & organize section
├── menuitem#context_reloadTab ("Reload Tab")
├── menuitem#context_reloadSelectedTabs ("Reload Tabs")
├── menuitem#context_playTab ("Play Tab")
├── menuitem#context_playSelectedTabs ("Play Tabs")
├── menuitem#context_toggleMuteTab ("Mute Tab / Unmute Tab")
├── menuitem#context_toggleMuteSelectedTabs ("Mute Tabs / Unmute Tabs")
├── menuitem#context_zen-add-essential ("Add to Essentials")  [zen]
├── menuitem#context_zen-remove-essential ("Remove from Essentials")  [zen]
├── menuseparator (no id)  [zen]
├── menuitem#context_zen-edit-tab-title ("Change Label…")  [zen]
├── menuitem#context_zen-edit-tab-icon ("Change Icon…")  [zen]
├── menuseparator (no id)  [zen]
├── menuitem#context_pinTab ("Pin Tab")
├── menuitem#context_unpinTab ("Unpin Tab")
├── menuitem#context_pinSelectedTabs ("Pin Tabs")
├── menuitem#context_unpinSelectedTabs ("Unpin Tabs")
├── menuitem#context_unloadTab ("Unload Tab / Unload N Tabs")
├── menuitem#context_duplicateTab ("Duplicate Tab")
├── menuitem#context_duplicateTabs ("Duplicate Tabs")
├── menuseparator#context_tabStateSeparator   <- end of tab actions section
├── menu#context_askChat ("Ask <chatbot name> (set at runtime)")
│   └── (runtime) menupopup built lazily by TabContextMenu.GenAI.buildTabMenu(); label set at runtime (AI chatbot name)
├── menuitem#context_askChatSummarize ("Summarize Page")
├── menuseparator#context_aiSeparator   <- end of AI section
├── menuitem#context_bookmarkSelectedTabs ("Bookmark Tabs…")
├── menuitem#context_bookmarkTab ("Bookmark Tab…")
├── menuitem#context_addNote ("Add Note")
├── menuitem#context_editNote ("Edit Note")
├── menu#context_moveTabOptions ("Move Tab / Move Tabs")
│   └── menupopup#moveTabOptionsMenu
│       ├── menuitem#context_moveToStart ("Move to Start")
│       ├── menuitem#context_moveToEnd ("Move to End")
│       ├── menuitem#context_openTabInWindow ("Move to New Window")
│       ├── menuseparator#moveTabSeparator
│       ├── menuseparator#context_moveTabToGroupSeparator
│       ├── menuseparator#context_selectAllSeparator
│       └── (runtime) prepended on popupshowing: menuseparator.zen-workspace-context-menu-item + one menuitem.zen-workspace-context-menu-item[zen-workspace-id] per other space (ZenSpaceManager.mjs); after #moveTabSeparator: one menuitem[profileid] per profile (gProfiles.populateMoveTabMenu)
├── (runtime) menu.share-tab-url-item, created lazily right after #context_moveTabOptions when sharing is available (SharingUtils.ensureShareMenu)
├── menu#context_reopenInContainer ("Open in New Container Tab")
│   └── menupopup#context_reopenInContainerPopupMenu
│       └── (runtime) one menuitem.menuitem-iconic.identity-color-<color>.identity-icon-<icon> per container
├── menuitem#context_selectAllTabs ("Select All Tabs")
├── menuseparator#context_tabToolsSeparator   <- end of tab tools section
├── menuitem#context_shareSelectedTabs ("Create Shareable Link")
├── menuseparator#context_shareSelectedTabsSeparator
├── menu#context_sendTabToDevice.sync-ui-item ("Send to Device")
│   └── menupopup#context_sendTabToDevicePopupMenu.sync-ui-item
│       └── (runtime) menuitem.sync-menuitem.sendtab-target per device, plus menuseparator.sync-menuitem and the 'Send to All Devices' / 'Manage Devices...' items
├── menuseparator#context_sendTabToDeviceSeparator.sync-ui-item   <- end of sending section
├── menuitem#context_closeTab ("Close Tab / Close N Tabs")
├── menuitem#context_closeDuplicateTabs ("Close Duplicate Tabs")
├── menu#context_closeTabOptions ("Close Multiple Tabs")
│   └── menupopup#closeTabOptions
│       ├── menuitem#context_closeTabsToTheStart ("Close Tabs Above (vertical) / Close Tabs to Left")
│       ├── menuitem#context_closeTabsToTheEnd ("Close Tabs Below (vertical) / Close Tabs to Right")
│       └── menuitem#context_closeOtherTabs ("Close Other Tabs")
├── menuitem#context_undoCloseTab ("Reopen Closed Tab")
├── menuseparator (no id)  [zen]
├── menuitem#context_zen-add-domain-to-routing ("Add Route for Domain")  [zen]
├── menuseparator#context_fullscreenSeparator   <- end of close actions; starts the fullscreen section
├── menuitem#context_fullscreenAutohide.fullscreen-context-autohide ("Hide Toolbars")
├── menuitem#context_fullscreenExit ("Exit Full Screen Mode")
├── menuseparator#context_zen-pinned-tab-separator  [zen]
├── menu#context_zen-edit-pinned-page ("Edit Pinned URL / Edit Essential URL")  [zen]
│   └── menupopup  [zen]
│       ├── menuitem#context_zen-replace-pinned-url-with-current ("Replace with Current URL")  [zen]
│       └── menuitem#context_zen-edit-pinned-url ("Edit…")  [zen]
├── menuitem#context_zen-reset-pinned-tab ("Reset Pinned Tab / Reset Essential Tab")  [zen]
└── (runtime) WebExtension menu items appended here by ext-menus.js
```
