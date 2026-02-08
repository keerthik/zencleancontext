[local zen-themes css file]("file:///C:/Users/<user-folder>/AppData/Roaming/zen/Profiles/<profile-folder>/chrome/zen-themes.css")

# Inspected HTML Analysis
## Zen Browser 1.18.5b - Tab Context Menu

### Visual Tree Structure

**Tab Context Menu (XUL)**

```
menuitem#context_openANewTab ("New Tab Below")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#context_moveTabToNewGroup ("Add Tab to New Group")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#context_moveSplitViewToNewGroup ("Add Split View to New Group")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#zen-context-menu-new-folder ("New Folder")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menu#context_moveTabToGroup
├── img.menu-icon
├── label.menu-text
├── label.menu-accel
└── menupopup#context_moveTabToGroupPopupMenu
    ├── menuitem#context_moveTabToGroupNewGroup ("New Group")
    │   ├── img.menu-icon
    │   ├── label.menu-text
    │   ├── label.menu-highlightable-text
    │   │   └── span.accesskey
    │   └── label.menu-accel
    ├── menuseparator#open-tab-groups-separator-upper
    ├── menuseparator#open-tab-groups-separator-lower
    └── menu#context_moveTabToSavedGroup ("Closed Groups")
        ├── img.menu-icon
        ├── label.menu-text
        ├── label.menu-accel
        └── menupopup#context_moveTabToSavedGroupPopupMenu

menuitem#context_ungroupTab ("Remove from Group")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#context_ungroupSplitView ("Remove from Group")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#context_moveTabToSplitView.badge-new
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
└── label.menu-accel

menuitem#context_separateSplitView.badge-new ("Separate Split View")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuseparator

menuitem#context_reloadTab ("Reload Tab")
menuitem#context_reloadSelectedTabs ("Reload Tabs")
menuitem#context_playTab ("Play Tab")
menuitem#context_playSelectedTabs ("Play Tabs")
menuitem#context_toggleMuteTab ("Mute Tab")
menuitem#context_toggleMuteSelectedTabs ("Mute Tabs")

menuitem#context_zen-add-essential ("Add to Essentials")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuitem#context_zen-remove-essential ("Remove from Essentials")
├── img.menu-icon
├── label.menu-text
├── label.menu-highlightable-text
│   └── span.accesskey
└── label.menu-accel

menuseparator

menuitem#context_zen-edit-tab-title ("Change Label...")
menuitem#context_zen-edit-tab-icon ("Change Icon...")

menuseparator

menuitem#context_pinTab ("Pin Tab")
menuitem#context_unpinTab ("Unpin Tab")
menuitem#context_pinSelectedTabs ("Pin Tabs")
menuitem#context_unpinSelectedTabs ("Unpin Tabs")
menuitem#context_unloadTab ("Unload 0 Tabs")
menuitem#context_zenSplitTabs ("Split Tab (multiple selected tabs needed)")
menuitem#context_duplicateTab ("Duplicate Tab")
menuitem#context_duplicateTabs ("Duplicate Tabs")

menuseparator

menu#context_askChat
menuitem#context_bookmarkSelectedTabs ("Bookmark Tabs…")
menuitem#context_bookmarkTab ("Bookmark Tab…")
menuitem#context_addNote ("Add Note")
menuitem#context_editNote ("Edit Note")

menu#context_moveTabOptions ("Move Tab")
├── img.menu-icon
├── label.menu-text
├── label.menu-accel
└── menupopup#moveTabOptionsMenu
    ├── menuitem.zen-workspace-context-menu-item ("Space 1")
    ├── menuitem.zen-workspace-context-menu-item ("Space 2")
    ├── menuitem.zen-workspace-context-menu-item ("Space 3")
    ├── menuitem.zen-workspace-context-menu-item ("Space 4")
    ├── menuitem.zen-workspace-context-menu-item ("Space 5")
    ├── menuseparator.zen-workspace-context-menu-item
    ├── menuitem#context_moveToStart ("Move to Start")
    ├── menuitem#context_moveToEnd ("Move to End")
    ├── menuitem#context_openTabInWindow ("Move to New Window")
    ├── menuseparator#moveTabSeparator
    ├── menuitem ("Move to Profile 1")
    └── menuitem ("Move to Profile 2")

menuitem.share-tab-url-item ("Share")

menu#context_reopenInContainer ("Open in New Container Tab")
├── img.menu-icon
├── label.menu-text
├── label.menu-accel
└── menupopup#context_reopenInContainerPopupMenu

menuitem#context_selectAllTabs ("Select All Tabs")

menuseparator

menu#context_sendTabToDevice.sync-ui-item ("Send to Device")
├── img.menu-icon
├── label.menu-text
├── label.menu-accel
└── menupopup#context_sendTabToDevicePopupMenu.sync-ui-item

menuseparator#context_sendTabToDeviceSeparator.sync-ui-item

menuitem#context_closeTab ("Close Tab")
menuitem#context_closeDuplicateTabs ("Close Duplicate Tabs")

menu#context_closeTabOptions ("Close Multiple Tabs")
├── img.menu-icon
├── label.menu-text
├── label.menu-accel
└── menupopup#closeTabOptions
    ├── menuitem#context_closeTabsToTheStart ("Close Tabs Above")
    ├── menuitem#context_closeTabsToTheEnd ("Close Tabs Below")
    └── menuitem#context_closeOtherTabs ("Close Other Tabs")

menuitem#context_undoCloseTab ("Reopen Closed Tab")

menuseparator

menuitem#context_fullscreenAutohide.fullscreen-context-autohide ("Hide Toolbars")
menuitem#context_fullscreenExit ("Exit Full Screen Mode")

menuseparator#context_zen-pinned-tab-separator

menuitem#context_zen-replace-pinned-url-with-current ("Replace Pinned URL with Current")
menuitem#context_zen-reset-pinned-tab ("Reset Pinned Tab")
```

---

### Key CSS Selectors

#### Menu Structure
- `menuitem` - All menu items
- `menu` - Submenus with nested options
- `menupopup` - Popup menu containers
- `menuseparator` - Menu dividers

#### Icon & Text Components
- `.menu-icon` - Icons for menu items
- `.menu-text` - Main text label
- `.menu-highlightable-text` - Text with keyboard shortcuts
- `.menu-accel` - Accelerator/shortcut display
- `.accesskey` - Underlined access key character

#### Special Classes
- `.badge-new` - Items with "New" badge
- `.zen-workspace-context-menu-item` - Workspace-specific items
- `.share-tab-url-item` - Share menu item
- `.sync-ui-item` - Sync-related items
- `.fullscreen-context-autohide` - Fullscreen menu items

#### Important IDs
- `#context_openANewTab` - New tab option
- `#zen-context-menu-new-folder` - New folder
- `#context_moveTabToGroup` - Tab grouping menu
- `#context_zen-add-essential` - Add to essentials
- `#context_zen-edit-tab-title` - Edit tab title
- `#context_zen-edit-tab-icon` - Edit tab icon
- `#context_pinTab` / `#context_unpinTab` - Pin/unpin tabs
- `#context_moveTabOptions` - Move tab submenu
- `#moveTabOptionsMenu` - Workspace/profile destinations
- `#context_closeTabOptions` - Close options submenu
- `#closeTabOptions` - Close multiple tabs options
- `#context_zen-replace-pinned-url-with-current` - Replace pinned URL
- `#context_zen-reset-pinned-tab` - Reset pinned tab

#### State Attributes (for CSS selectors)
- `[hidden]` - Hidden items
- `[disabled]` - Disabled items
- `[checked]` - Checked items (checkbox type)

---

### Notes for CSS Styling
- All menu items follow consistent structure with icon, text, highlightable text, and accel labels
- Workspace menu items are dynamically generated with custom emojis
- Badge items (`.badge-new`) indicate new features
- Menu separators divide logical sections
- Hidden items can be targeted with `[hidden]` attribute selector
