---
title: Docs - Item Snippets and Examples
permalink: /docs/items/
---

Get some Item Snippets and start making your own server!

##### Table of Contents  
[Currency Example](#currency)  
[Mob Example](#mob)  
[Block Example](#block)  
[Shop Inventory Example](#shop)   

<a name="currency"/>

## Currency Examples

```
{
	"foreign_ids": [
	],
	"mod_desc": {
		"author": "1004158810",
		"filename": "1525797788",
		"uuid": "90b4c879-b9a8-443d-860d-6e6aad5f3e83",
		"version": "1" 
	},
	"property": {
		"copyid": 10100,
		"describe": "#cFFFFFF You can get it in# #c00ff00 events# #cFFFFFF or# #c00ff00 killing monsters.",
			"esn_describe": "#cFFFFFF Puedes conseguirla en# #c00ff00 eventos# #cFFFFFF o# #c00ff00 matando monstruos.",
		"icon": "*12059",
		"id": 100004,
		"model": "*12059",
		"name": "#c00ff00 Hello World Coin",
			"esn_name": "#c00ff00 Moneda Hola Mundo",
		"stack_max": 10000
	} 
} 
```

From there you should edit ``name`` and ``describe`` with your own information, you can remove the lines ``esn_describe``
and ``esn_name``.

<a name="mob"/>
## Mob Example

<p class="text-danger">This plugin is a Default Mob, not a new one.</p>
```
{
	"foreign_ids": [
		{
			"id": 100004,
			"key": "1004158810667f325c-1ff1-11e7-93ae-92361f0026711525797788" 
		} 
	],
	"mod_desc": {
		"author": "1004158810",
		"filename": "Savage",
		"uuid": "90b4c879-b9a8-443d-860d-6e6aad5f3e83",
		"version": "1" 
	},
	"property": {
		"attack": 50,
		"attack_distance": 2,
		"attack_type": 0,
		"buff_id": 0,
		"desc": "",
		"drop_exp": 13,
		"drop_exp_prob": 100,
		"drop_item1": 12526,
		"drop_item2": 312,
		"drop_item3": 100004,
		"drop_item_prob1": 100,
		"drop_item_prob2": 100,
		"drop_item_prob3": 100,
		"height": 195,
		"hit_height": 220,
		"hit_thickness": 110,
		"hit_width": 110,
		"icon": "3101",
		"id": 3101,
		"life": 200,
		"model": "100026",
		"model_scale": 1,
		"name": "Savage",
		"speed": 200,
		"team_id": 0,
		"type": 0,
		"view_distance": 24,
		"width": 95 
	},
	"set_ai": [
		{
			"dist": 3000,
			"monster_id": 3407,
			"name": "ride",
			"priority": 0 
		},
		{
			"name": "follow_direction",
			"priority": 1,
			"speed": 1.1 
		},
		{
			"name": "break_door",
			"priority": 1 
		},
		{
			"name": "move_towards_restriction",
			"priority": 4,
			"speed": 1 
		},
		{
			"name": "wander",
			"priority": 6,
			"speed": 1 
		},
		{
			"name": "look_idle",
			"priority": 7 
		},
		{
			"name": "swimming",
			"priority": 1 
		},
		{
			"attack_type": 0,
			"move_speed": 1,
			"name": "attack",
			"priority": 2,
			"will_trace": false 
		},
		{
			"brightness": 0,
			"chance": 0,
			"check_sight": true,
			"minhp": 0,
			"name": "target_nearest",
			"priority": 2 
		},
		{
			"name": "sun_hurt" 
		},
		{
			"maxhp": 0.0001,
			"name": "panic",
			"priority": 1,
			"speed": 3.25 
		},
		{
			"dist": 800,
			"name": "watch_closest",
			"priority": 7 
		} 
	] 
} 
```

To make the mob drops Coins you should edit ``drop_item1``, ``drop_item2`` and ``drop_item3`` with your Coin ID.

<a name="block"/>
## Block Example

<p class="text-danger">This plugin is an example of how to make an Air Block that can't collide to players but it collides with projectils and bullets.</p>

```
{
	"foreign_ids": [
	],
	"item_property": {
		"desc": "Colócalo para entrar en el modo Supervivencia. Puede ocultarse con otros cubos alrededor. Se usa para conseguir que una zona será inquebrantable.",
		"describe": "Colócalo para entrar en el modo Supervivencia. Puede ocultarse con otros cubos alrededor. Se usa para conseguir que una zona será inquebrantable.",
		"icon": "",
		"id": 1001,
		"model": "",
		"name": "Muro de aire" 
	},
	"mod_desc": {
		"author": "1004863995",
		"filename": "Airwallcube",
		"uuid": "90b4c879-b9a8-443d-860d-6e6aad5f3e83",
		"version": "1" 
	},
	"property": {
		"anti_explode": 1000,
		"breakable": false,
		"burn_speed": 0,
		"catch_fire": 0,
		"english_name": "Airwallcube",
		"hardness": 1000,
		"id": 1001,
		"light_src": 15,
		"move_collide": 4,
		"slipperiness": 1,
		"tool_mine_drop1": 0 
	} 
} 
```

<a name="shop"/>
## Shop Inventory Example

<p class="text-danger">This plugin will make a new crafting recipe simulating a shop in the inventory.</p>
<p class="text-danger">Do not delete the other craftings from the inventory shop, they are needed for just to show the listed items.</p>
<p class="text-danger">You can delete the ones that have ``"is_followme": true,``</p>

```
{
	"foreign_ids": [
	],
	"mod_desc": {
		"author": "1000872134",
		"filename": "1527439615",
		"uuid": "90b4c879-b9a8-443d-860d-6e6aad5f3e83",
		"version": "1" 
	},
	"property": {
		"copyid": 1000,
		"id": 1007,
		"is_followme": true,
		"material_count1": 120,
		"material_count2": 0,
		"material_count3": 0,
		"material_count4": 0,
		"material_count5": 0,
		"material_count6": 0,
		"material_count7": 0,
		"material_count8": 0,
		"material_count9": 0,
		"material_id1": 4097,
		"material_id2": 0,
		"material_id3": 0,
		"material_id4": 0,
		"material_id5": 0,
		"material_id6": 0,
		"material_id7": 0,
		"material_id8": 0,
		"material_id9": 0,
		"result_count": 1,
		"result_id": 845,
		"type": 0 
	} 
} 
```

To add the resulting item edit ``result_id`` with the ID of your item.
To add the price edit ``material_count1``.
To add your coin as the currency edit ``material_id1`` with your Coin ID.
