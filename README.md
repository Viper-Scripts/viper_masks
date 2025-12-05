# viper_masks
FiveM Mask and Hat Script - Credit to LucidKniight

## Dependencies
- [ox_inventory](https://github.com/overextended/ox_inventory)
- [ox_lib](https://github.com/overextended/ox_lib)

# Installation

## Step 1
* Drag `viper_masks` into your resources folder or any subfolder
* Make sure that the folder is named `viper_masks` and NOT `viper_masks-main`

## Step 2
* Add the following line to your **qb-core/shared/items.lua**
```lua
    ['mask'] = {
        label = 'Mask',
        weight = 100,
        price = 10,
        stack = false,
        client = {
            image = 'mask.png',
            export = 'viper_masks.mask'
        }
    },

    ['hat'] = {
        label = 'Hat',
        price = 10,
        weight = 100,
        stack = false,
        client = {
            image = 'hat.png',
            export = 'viper_masks.hat'
        }
    },
```
* Drag all images into your **inventory/web/images**

## Step 3
* Find the following line in your **qb-radialmenu/config.lua** or **qbx_radialmenu/config.lua**
```lua
    id = 'Mask',
    title = 'Mask',
    icon = 'masks-theater',
    type = 'client',
    event = 'qb-radialmenu:ToggleProps',
    shouldClose = true
```

* and replace it with :

```lua
    id = 'Mask',
    title = 'Mask',
    icon = 'masks-theater',
    type = 'client',
    event = 'viper_masks:client:ToggleMask',
    shouldClose = true
```

## Step 4
* Find the following line to your **qb-radialmenu/config.lua** or **qbx_radialmenu/config.lua**
```lua
    ["mask"] = {
        Func = function() ToggleClothing("Mask") end,
        Sprite = "mask",
        Desc = "Take your mask off/on",
        Button = 6,
        Name = "Mask"
    }
```

* and comment it out :

```lua
    --["mask"] = {
    --    Func = function() ToggleClothing("Mask") end,
    --    Sprite = "mask",
    --    Desc = "Take your mask off/on",
    --    Button = 6,
    --    Name = "Mask"
    --}
```

## Credits
- [mckleansscripts](https://github.com/McKleans-Scripts/mk-items) For the mask image
- [Lucidkniight](https://github.com/Lucidkniight/lucid-masks) For the original repo for Masks
