# XIVCrossBarUpdate  
Credit goes to https://github.com/AliekberFFXI/xivcrossbar  
  
  
FIXED:  
HideActionCost now hides MP/TP costs but still displays the "greyed out" box if MP/TP is too low.  
Dancer/Wards now load properly.  
HideActionName now hides the action name from the icon.  


ADDED:  
GearSwap Macros.
  
To add a gearswap macro, go to your Gearswap set and add the set: sets.gsmacro1 through sets.gsmacro8.  
```
	   sets.gsmacro1 = {ring1 = "Facility Ring"}
```

Then go to XIVCrossBar's "Crossbar_abilities.lua" and set the icons.  
```
    ["gsmacro1"] = { id = 1550, en = "gsmacro1", res_key = "macros", type = "gs", category = "ready", element = "Light", default_icon = "/images/icons/weapons/katana.png", custom_icon = "weaponskills/katana/zesho-meppo.png", mp_cost = 0, tp_cost = 0},
    ...
    ["gsmacro8"] = { id = 1557, en = "gsmacro8", res_key = "macros", type = "gs", category = "ready", element = "Light", default_icon = "/images/icons/weapons/katana.png", custom_icon = "weaponskills/katana/zesho-meppo.png", mp_cost = 0, tp_cost = 0},
```

Finally open "XIVCrossBar\data\hotbar\SERVER\CHARACTER\Job-Subjob.Lua"
To set Slot4 to gsmacro 1, adjust it as follows.  
```xml
            <slot_4>  
                <target>me</target>  
                <type>gs</type>  
                <action>gsmacro1</action>  
                <alias>gsmacro1</alias>  
            </slot_4>
```
