# Tab Context Menu - CSS Styling Reference

Zen 1.22.3b, generated 2026/10/01 from a devtools DOM dump of `#tabContextMenu` ([toolbar.html](./toolbar.html)).
DOM order as captured (classic layout, vertical tabs). The dump is a snapshot: `hidden` and `disabled` flip per tab, and labels reflect the tab that was right-clicked.

Legend:
- `[zen]` = injected by Zen's JS rather than Firefox markup. Present only while that Zen feature is enabled.
- `(runtime)` = generated when the popup opens (one per space / profile / device, or the lazily built share menu). Target these by class or attribute, never by label.
- `xN` = N identical sibling items collapsed into one line.
- `<...>` = personal labels (space, profile and device names) replaced with placeholders.
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
├── menuitem#context_openANewTab ("New Tab Below")
├── menuitem#context_moveTabToNewGroup ("Add Tab to New Group")
├── menuitem#context_moveSplitViewToNewGroup ("Add Split View to New Group")
├── menu#context_zenMoveToFolder ("Move to Folder")  [zen]
│   └── menupopup  [zen]
│       ├── menuseparator (no id)  [zen]
│       └── menuitem#zen-context-menu-new-folder ("New Folder")  [zen]
├── menu#context_moveTabToGroup
│   └── menupopup#context_moveTabToGroupPopupMenu
│       ├── menuitem#context_moveTabToGroupNewGroup ("New Group")
│       ├── menuseparator#open-tab-groups-separator-upper
│       ├── menuseparator#open-tab-groups-separator-lower
│       └── menu#context_moveTabToSavedGroup ("Closed Groups")
│           └── menupopup#context_moveTabToSavedGroupPopupMenu
├── menuitem#context_ungroupTab ("Remove from Group")
├── menuitem#context_ungroupSplitView ("Remove from Group")
├── menuitem#context_zenSplitTabs[command="cmd_zenSplitViewContextMenu"] ("Add Split View...")  [zen]
├── menuitem#context_zenShareSplitView[command="cmd_zenCtxShareSplitView"] ("Share Split View…")  [zen]
├── menuitem#context_moveTabToSplitView
├── menuitem#context_separateSplitView ("Separate Split View")
├── menuitem#context_reverseSplitView ("Reverse Tabs")
├── menuseparator#context_openAndOrganizeSeparator   <- end of open & organize section
├── menuitem#context_reloadTab ("Reload Tab")
├── menuitem#context_reloadSelectedTabs ("Reload Tabs")
├── menuitem#context_playTab ("Play Tab")
├── menuitem#context_playSelectedTabs ("Play Tabs")
├── menuitem#context_toggleMuteTab ("Mute Tab")
├── menuitem#context_toggleMuteSelectedTabs ("Mute Tabs")
├── menuitem#context_zen-add-essential[command="cmd_contextZenAddToEssentials"][badge] ("Add to Essentials")  [zen]
├── menuitem#context_zen-remove-essential[command="cmd_contextZenRemoveFromEssentials"] ("Remove from Essentials")  [zen]
├── menuseparator (no id)  [zen]
├── menuitem#context_zen-edit-tab-title ("Change Label…")  [zen]
├── menuitem#context_zen-edit-tab-icon ("Change Icon…")  [zen]
├── menuseparator (no id)  [zen]
├── menuitem#context_pinTab ("Pin Tab")
├── menuitem#context_unpinTab ("Unpin Tab")
├── menuitem#context_pinSelectedTabs ("Pin Tabs")
├── menuitem#context_unpinSelectedTabs ("Unpin Tabs")
├── menuitem#context_unloadTab ("Unload 0 Tabs")
├── menuitem#context_duplicateTab ("Duplicate Tab")
├── menuitem#context_duplicateTabs ("Duplicate Tabs")
├── menuseparator#context_tabStateSeparator   <- end of tab actions section
├── menu#context_askChat
├── menuitem#context_askChatSummarize
├── menuseparator#context_aiSeparator   <- end of AI section
├── menuitem#context_bookmarkSelectedTabs ("Bookmark Tabs…")
├── menuitem#context_bookmarkTab ("Bookmark Tab…")
├── menuitem#context_addNote ("Add Note")
├── menuitem#context_editNote ("Edit Note")
├── menu#context_moveTabOptions ("Move Tab")
│   └── menupopup#moveTabOptionsMenu
│       ├── menuitem.zen-workspace-context-menu-item[command="cmd_zenChangeWorkspaceTab"][zen-workspace-id] ("<space icon + name>")  x4  [zen]  (runtime)
│       ├── menuseparator.zen-workspace-context-menu-item  [zen]  (runtime)
│       ├── menuitem#context_moveToStart ("Move to Start")
│       ├── menuitem#context_moveToEnd ("Move to End")
│       ├── menuitem#context_openTabInWindow ("Move to New Window")
│       ├── menuseparator#moveTabSeparator
│       ├── menuitem[command="Profiles:MoveTabsToProfile"][profileid] ("Move to <profile name>")  x2  (runtime)
│       ├── menuseparator#context_moveTabToGroupSeparator
│       └── menuseparator#context_selectAllSeparator
├── menu.share-tab-url-item ("Share")  (runtime)
│   └── menupopup  (runtime)
│       ├── menuitem.menuitem-iconic.share-copy-link[image] ("Copy Link")  (runtime)
│       ├── menuitem.menuitem-iconic.share-qrcode-item[image] ("Generate QR Code…")  (runtime)
│       ├── menuseparator (no id)  (runtime)
│       └── menuitem.share-windows-item ("More Options")  (runtime)
├── menu#context_reopenInContainer ("Open in New Container Tab")
│   └── menupopup#context_reopenInContainerPopupMenu
├── menuitem#context_selectAllTabs ("Select All Tabs")
├── menuseparator#context_tabToolsSeparator   <- end of tab tools section
├── menuitem#context_shareSelectedTabs ("Create Shareable Link")
├── menuseparator#context_shareSelectedTabsSeparator
├── menu#context_sendTabToDevice.sync-ui-item ("Send to Device")
│   └── menupopup#context_sendTabToDevicePopupMenu.sync-ui-item
│       ├── menuitem.sync-menuitem.sendtab-target[clientType] ("<phone device name>")  (runtime)
│       ├── menuitem.sync-menuitem.sendtab-target[clientType] ("<desktop device name>")  x2  (runtime)
│       ├── menuseparator.sync-menuitem  (runtime)
│       ├── menuitem.sync-menuitem.sendtab-target[clientType] ("Send to All Devices")  (runtime)
│       └── menuitem.sync-menuitem.sendtab-target ("Manage Devices…")  (runtime)
├── menuseparator#context_sendTabToDeviceSeparator.sync-ui-item   <- end of sending section
├── menuitem#context_closeTab ("Close Tab")
├── menuitem#context_closeDuplicateTabs ("Close Duplicate Tabs")
├── menu#context_closeTabOptions ("Close Multiple Tabs")
│   └── menupopup#closeTabOptions
│       ├── menuitem#context_closeTabsToTheStart ("Close Tabs Above")
│       ├── menuitem#context_closeTabsToTheEnd ("Close Tabs Below")
│       └── menuitem#context_closeOtherTabs ("Close Other Tabs")
├── menuitem#context_undoCloseTab[command="History:UndoCloseTab"] ("Reopen Closed Tab")
├── menuseparator (no id)  [zen]
├── menuitem#context_zen-add-domain-to-routing ("Add Route for Domain")  [zen]
├── menuseparator#context_fullscreenSeparator[contexttype="fullscreen"]   <- end of close actions; starts the fullscreen section
├── menuitem#context_fullscreenAutohide.fullscreen-context-autohide[type="checkbox"][contexttype="fullscreen"] ("Hide Toolbars")
├── menuitem#context_fullscreenExit[contexttype="fullscreen"] ("Exit Full Screen Mode")
├── menuseparator#context_zen-pinned-tab-separator  [zen]
├── menu#context_zen-edit-pinned-page ("Edit Pinned URL")  [zen]
│   └── menupopup  [zen]
│       ├── menuitem#context_zen-replace-pinned-url-with-current[command="cmd_zenReplacePinnedUrlWithCurrent"] ("Replace with Current URL")  [zen]
│       └── menuitem#context_zen-edit-pinned-url[command="cmd_zenEditPinnedUrl"] ("Edit…")  [zen]
├── menuitem#context_zen-reset-pinned-tab[command="cmd_zenPinnedTabResetNoTab"] ("Reset Pinned Tab")  [zen]
└── (runtime) WebExtension menu items are appended here by ext-menus.js
```
