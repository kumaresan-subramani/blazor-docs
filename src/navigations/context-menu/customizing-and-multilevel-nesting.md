# Customizing Items and Multilevel Nesting

## Customizing Context Menu Items

The Context Menu items can be customized by using the `CssClass` property. In the following sample, the menu items is customized by adding new styles.

```csharp

@using Syncfusion.Blazor.Navigations

<div id="target">Right click/Touch hold to open the ContextMenu </div>
<SfContextMenu Target="#target" TValue="MenuItem" CssClass="custom">
    <MenuItems>
        <MenuItem Text="Cut"></MenuItem>
        <MenuItem Text="Copy"></MenuItem>
        <MenuItem Text="Paste"></MenuItem>
    </MenuItems>
</SfContextMenu>

<style>
    #target {
        border: 1px dashed;
        height: 150px;
        padding: 10px;
        position: relative;
        text-align: justify;
        color: gray;
        user-select: none;
    }
    .custom.e-contextmenu-container .e-menu-item {
        display: inline-block;
        font-size: 10px;
        font-style: oblique;
    }
</style>

```

Output be like

![Context Menu Sample](./images/cm-template.png)

## Multilevel nesting

The Multiple level nesting supports in Context Menu. It can be achieved by mapping the [`MenuItems`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Navigations.MenuItems.html)
property inside the parent [`MenuItem`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Navigations.MenuItem.html). In the below sample, three level nesting of Context Menu is provided.

```csharp
@using Syncfusion.Blazor.Navigations

<div id="target">Right click/Touch hold to open the ContextMenu </div>
<SfContextMenu Target="#target" TValue="MenuItem">
    <MenuItems>
        <MenuItem Text="Show All Bookmarks"></MenuItem>
        <MenuItem Text="Bookmarks Toolbar">
            <MenuItems>
                <MenuItem Text="Most Visited">
                    <MenuItems>
                        <MenuItem Text="Google"></MenuItem>
                        <MenuItem Text="Gmail"></MenuItem>
                    </MenuItems>
                </MenuItem>
            </MenuItems>
        </MenuItem>
        <MenuItem Text="Recently Added"></MenuItem>
    </MenuItems>
</SfContextMenu>

<style>
    #target {
        border: 1px dashed;
        height: 150px;
        padding: 10px;
        position: relative;
        text-align: justify;
        color: gray;
        user-select: none;
    }
</style>

```

Output be like

![Context Menu Sample](./images/cm-multilevel.png)