## Key CSS Selectors

### Primary Container
- `#tabContextMenu` - Main context menu popup container

### Tab Management Items
- `#context_openANewTab` - New tab below action
- `#zen-context-menu-new-folder` - New folder action
- `#context_moveTabToGroup` - Move tab to group submenu
- `#context_moveTabToGroupPopupMenu` - Group submenu popup
- `#context_moveTabToNewGroup` - New group creation
- `#context_moveTabToSavedGroup` - Closed groups submenu

### Split View & Groups
- `#context_moveTabToSplitView` - Move to split view (has `.badge-new`)
- `#context_separateSplitView` - Separate split view (has `.badge-new`)
- `#context_moveSplitViewToNewGroup` - Add split view to group
- `#context_ungroupTab` - Remove tab from group
- `#context_ungroupSplitView` - Remove split view from group

### Zen-specific Features
- `#context_zen-add-essential` - Add to essentials
- `#context_zen-remove-essential` - Remove from essentials
- `#context_zen-edit-tab-title` - Edit tab title
- `#context_zen-edit-tab-icon` - Edit tab icon
- `#context_zen-replace-pinned-url-with-current` - Replace pinned URL
- `#context_zen-reset-pinned-tab` - Reset pinned tab

### Workspace Selectors
- `.zen-workspace-context-menu-item` - Workspace menu items in Move Tab submenu

### Tab Actions
- `#context_reloadTab` / `#context_reloadSelectedTabs` - Reload actions
- `#context_playTab` / `#context_playSelectedTabs` - Play media actions
- `#context_toggleMuteTab` / `#context_toggleMuteSelectedTabs` - Mute actions
- `#context_pinTab` / `#context_unpinTab` - Pin/unpin actions
- `#context_pinSelectedTabs` / `#context_unpinSelectedTabs` - Batch pin actions
- `#context_duplicateTab` / `#context_duplicateTabs` - Duplicate actions
- `#context_zenSplitTabs` - Split tabs action
- `#context_unloadTab` - Unload tabs action

### Bookmarks & Notes
- `#context_bookmarkTab` / `#context_bookmarkSelectedTabs` - Bookmark actions
- `#context_addNote` / `#context_editNote` - Note actions

### Move Tab Options
- `#context_moveTabOptions` - Move tab submenu container
- `#moveTabOptionsMenu` - Move tab popup menu
- `#context_moveToStart` / `#context_moveToEnd` - Position movement
- `#context_openTabInWindow` - Move to new window

### Container Tabs
- `#context_reopenInContainer` - Container tab menu
- `#context_reopenInContainerPopupMenu` - Container submenu
- `.identity-color-blue` / `.identity-color-orange` / `.identity-color-green` / `.identity-color-pink` - Container colors
- `.identity-icon-fingerprint` / `.identity-icon-briefcase` / `.identity-icon-dollar` / `.identity-icon-cart` - Container icons

### Send to Device (Sync)
- `#context_sendTabToDevice` - Send to device menu
- `#context_sendTabToDevicePopupMenu` - Device list popup
- `.sync-ui-item` - Sync-related items
- `.sync-menuitem` - Individual sync menu items
- `.sendtab-target` - Send target devices

### Close Actions
- `#context_closeTab` - Close single tab
- `#context_closeDuplicateTabs` - Close duplicate tabs
- `#context_closeTabOptions` - Close multiple tabs submenu
- `#closeTabOptions` - Close options popup
- `#context_closeTabsToTheStart` / `#context_closeTabsToTheEnd` - Directional close
- `#context_closeOtherTabs` - Close all other tabs
- `#context_undoCloseTab` - Reopen closed tab

### Fullscreen Context
- `#context_fullscreenAutohide` - Auto-hide toolbars toggle
- `#context_fullscreenExit` - Exit fullscreen
- `.fullscreen-context-autohide` - Fullscreen-specific styling

### Other Actions
- `.share-tab-url-item` - Share tab action
- `#context_selectAllTabs` - Select all tabs
- `#context_askChat` - AI chat integration (when visible)

### Common Element Classes (within menu items)
- `.menu-icon` - Icon images
- `.menu-text` - Text labels
- `.menu-highlightable-text` - Highlighted text with accesskeys
- `.menu-accel` - Keyboard accelerator display
- `.accesskey` - Accesskey character highlighting
- `.badge-new` - "New" badge indicator

### Separators
- `menuseparator` - Visual dividers between menu sections
- `#open-tab-groups-separator-upper` / `#open-tab-groups-separator-lower` - Group section dividers
- `#context_sendTabToDeviceSeparator` - Sync section divider
- `#context_zen-pinned-tab-separator` - Pinned tab section divider
- `#moveTabSeparator` - Move tab section divider
