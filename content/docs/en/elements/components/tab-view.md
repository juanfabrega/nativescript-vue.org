---
title: TabView
apiRef: https://docs.nativescript.org/api-reference/classes/_ui_tab_view_.tabview
contributors: [MisterBrownRSA, rigor789, eddyverbruggen, ikoevska, kharysharpe]
---

`<TabView>` is a navigation component that shows content grouped into tabs and lets users switch between tabs.

---

```html
<TabView :selectedIndex="selectedIndex">
  <TabViewItem title="Tab 1">
    <Label text="Content for Tab 1" />
  </TabViewItem>
  <TabViewItem title="Tab 2">
    <Label text="Content for Tab 2" />
  </TabViewItem>
</TabView>
```
**Note:** `TabViewItem` currently expects a single child element, in most cases you will want to wrap your content in a layout.

[> screenshots for=TabView <]

#### Adding icons to tabs

```html
<TabView :selectedIndex="selectedIndex" iosIconRenderingMode="alwaysOriginal">
  <TabViewItem title="Tab 1" iconSource="~/images/icon.png">
    <Label text="Content for Tab 1" />
  </TabViewItem>
  <TabViewItem title="Tab 2" iconSource="~/images/icon.png">
    <Label text="Content for Tab 2" />
  </TabViewItem>
</TabView>
```
**Note:** icon fonts may work in some cases, but generally it is recommended to use images as tab icons.

## Props

| Name | Type | Description |
|------|------|-------------|
| `selectedIndex` | `Number` | Gets or sets the currently selected tab. Default is `0`.
| `tabTextColor` | `Color` | (Style property) Gets or sets the text color of the tabs titles.
| `tabBackgroundColor` | `Color` | (Style property) Gets or sets the background color of the tabs.
| `selectedTabTextColor` | `Color` | (Style property) Gets or sets the text color of the selected tab title.

## Events

| Name | Description |
|------|-------------|
| `selectedIndexChanged` | Emitted when one of the `<TabViewItem>` components is tapped.

## Native component

| Android | iOS |
|---------|-----|
| [`android.support.v4.view.ViewPager`](https://developer.android.com/reference/android/support/v4/view/ViewPager.html) | [`UITabBarController`](https://developer.apple.com/documentation/uikit/uitabbarcontroller)
