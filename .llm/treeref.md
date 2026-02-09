# Tab Context Menu - CSS Styling Reference
```
menupopup#tabContextMenu
├── menuitem#context_openANewTab ("New Tab Below")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_moveTabToNewGroup ("Add Tab to New Group")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_moveSplitViewToNewGroup ("Add Split View to New Group")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#zen-context-menu-new-folder ("New Folder")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menu#context_moveTabToGroup
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-accel
│   └── menupopup#context_moveTabToGroupPopupMenu
│       ├── menuitem#context_moveTabToGroupNewGroup ("New Group")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuseparator#open-tab-groups-separator-upper
│       ├── menuseparator#open-tab-groups-separator-lower
│       └── menu#context_moveTabToSavedGroup ("Closed Groups")
│           ├── img.menu-icon
│           ├── label.menu-text
│           ├── label.menu-accel
│           └── menupopup#context_moveTabToSavedGroupPopupMenu
│
├── menuitem#context_ungroupTab ("Remove from Group")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_ungroupSplitView ("Remove from Group")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_moveTabToSplitView.badge-new
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   └── label.menu-accel
│
├── menuitem#context_separateSplitView.badge-new ("Separate Split View")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator
│
├── menuitem#context_reloadTab ("Reload Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_reloadSelectedTabs ("Reload Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_playTab ("Play Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_playSelectedTabs ("Play Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_toggleMuteTab ("Mute Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_toggleMuteSelectedTabs ("Mute Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_zen-add-essential ("Add to Essentials")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_zen-remove-essential ("Remove from Essentials")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator
│
├── menuitem#context_zen-edit-tab-title ("Change Label...")
│   ├── img.menu-icon
│   ├── label.menu-text
│   └── label.menu-highlightable-text
│
├── menuitem#context_zen-edit-tab-icon ("Change Icon...")
│   ├── img.menu-icon
│   ├── label.menu-text
│   └── label.menu-highlightable-text
│
├── menuseparator
│
├── menuitem#context_pinTab ("Pin Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_unpinTab ("Unpin Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_pinSelectedTabs ("Pin Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_unpinSelectedTabs ("Unpin Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_unloadTab ("Unload 0 Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_zenSplitTabs ("Split Tab (multiple selected tabs needed)")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_duplicateTab ("Duplicate Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_duplicateTabs ("Duplicate Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator
│
├── menu#context_askChat
│   ├── img.menu-icon
│   ├── label.menu-text
│   └── label.menu-accel
│
├── menuseparator
│
├── menuitem#context_bookmarkSelectedTabs ("Bookmark Tabs…")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_bookmarkTab ("Bookmark Tab…")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_addNote ("Add Note")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_editNote ("Edit Note")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menu#context_moveTabOptions ("Move Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-accel
│   └── menupopup#moveTabOptionsMenu
│       ├── menuitem.zen-workspace-context-menu-item ("Space 1")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuitem.zen-workspace-context-menu-item ("Space 2")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuitem.zen-workspace-context-menu-item ("Space 3")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuitem.zen-workspace-context-menu-item ("Space 4")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuitem.zen-workspace-context-menu-item ("Space 5")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuseparator.zen-workspace-context-menu-item
│       ├── menuitem#context_moveToStart ("Move to Start")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuitem#context_moveToEnd ("Move to End")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuitem#context_openTabInWindow ("Move to New Window")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       └── menuseparator#moveTabSeparator
│
├── menuitem.share-tab-url-item ("Share")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menu#context_reopenInContainer ("Open in New Container Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-accel
│   └── menupopup#context_reopenInContainerPopupMenu
│       ├── menuitem.identity-color-blue.identity-icon-fingerprint ("Personal")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuitem.identity-color-orange.identity-icon-briefcase ("Work")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuitem.identity-color-green.identity-icon-dollar ("Banking")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       └── menuitem.identity-color-pink.identity-icon-cart ("Shopping")
│           ├── img.menu-icon
│           ├── label.menu-text
│           ├── label.menu-highlightable-text
│           │   └── span.accesskey
│           └── label.menu-accel
│
├── menuitem#context_selectAllTabs ("Select All Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator
│
├── menu#context_sendTabToDevice.sync-ui-item ("Send to Device")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-accel
│   └── menupopup#context_sendTabToDevicePopupMenu.sync-ui-item
│       ├── menuitem.sync-menuitem.sendtab-target ("Device 1 (phone)")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuitem.sync-menuitem.sendtab-target ("Device 2 (desktop)")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       ├── menuseparator.sync-menuitem
│       ├── menuitem.sync-menuitem.sendtab-target ("Send to All Devices")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   └── label.menu-accel
│       └── menuitem.sync-menuitem.sendtab-target ("Manage Devices…")
│           ├── img.menu-icon
│           ├── label.menu-text
│           ├── label.menu-highlightable-text
│           └── label.menu-accel
│
├── menuseparator#context_sendTabToDeviceSeparator.sync-ui-item
│
├── menuitem#context_closeTab ("Close Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_closeDuplicateTabs ("Close Duplicate Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menu#context_closeTabOptions ("Close Multiple Tabs")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-accel
│   └── menupopup#closeTabOptions
│       ├── menuitem#context_closeTabsToTheStart ("Close Tabs Above")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       ├── menuitem#context_closeTabsToTheEnd ("Close Tabs Below")
│       │   ├── img.menu-icon
│       │   ├── label.menu-text
│       │   ├── label.menu-highlightable-text
│       │   │   └── span.accesskey
│       │   └── label.menu-accel
│       └── menuitem#context_closeOtherTabs ("Close Other Tabs")
│           ├── img.menu-icon
│           ├── label.menu-text
│           ├── label.menu-highlightable-text
│           │   └── span.accesskey
│           └── label.menu-accel
│
├── menuitem#context_undoCloseTab ("Reopen Closed Tab")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator
│
├── menuitem#context_fullscreenAutohide.fullscreen-context-autohide ("Hide Toolbars")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuitem#context_fullscreenExit ("Exit Full Screen Mode")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
├── menuseparator#context_zen-pinned-tab-separator
│
├── menuitem#context_zen-replace-pinned-url-with-current ("Replace Pinned URL with Current")
│   ├── img.menu-icon
│   ├── label.menu-text
│   ├── label.menu-highlightable-text
│   │   └── span.accesskey
│   └── label.menu-accel
│
└── menuitem#context_zen-reset-pinned-tab ("Reset Pinned Tab")
    ├── img.menu-icon
    ├── label.menu-text
    ├── label.menu-highlightable-text
    │   └── span.accesskey
    └── label.menu-accel
```
