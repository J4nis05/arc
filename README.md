# arc
Something Something Arc Raiders

---

Some Testing with the Public API from [MetaForge](https://metaforge.app/arc-raiders)

---

Base-URL: `https://metaforge.app/api/arc-raiders`

Endpoints

* `/api/arc-raiders/items       `: Item Data, Component Relationships
* `/api/arc-raiders/arcs        `: Arc Data, Loot Data
* `/api/arc-raiders/quests      `: Quests with required Items and Rewards
* `/api/arc-raiders/event-timers`: Timers for Map Events
* `/api/arc-raiders/traders     `: Trader Inventories
* `/api/game-map-data           `: Data for specific Maps

---

#### items - Parameters

| Name              | Type    | Required | Default | Description                                   |
| ----------------- | ------- | -------- | ------- | --------------------------------------------- |
| page              | number  | No       | 1       | Page number for pagination                    |
| limit             | number  | No       | 50      | Items per page (max 100)                      |
| id                | string  | No       | -       | Specific item ID to fetch                     |
| item_type         | string  | No       | -       | Filter by item type (e.g., Weapon, Armor)     |
| rarity            | string  | No       | -       | Filter by rarity (e.g., Common, Rare, Epic)   |
| search            | string  | No       | -       | Search items by name (max 100 chars)          |
| loadout_slot      | string  | No       | -       | Filter by loadout slot                        |
| workbench         | string  | No       | -       | Filter by workbench requirement               |
| subcategory       | string  | No       | -       | Filter by subcategory                         |
| shield_type       | string  | No       | -       | Filter by shield type                         |
| includeComponents | boolean | No       | false   | Include crafting components and relationships |
| sortBy            | string  | No       | name    | Sort field                                    |
| sortOrder         | string  | No       | asc     | Sort order (asc/desc)                         |
| minimal           | boolean | No       | false   | Return minimal item data only                 |


#### arcs - Parameters

| Name        | Type    | Required | Default | Description                            |
| ----------- | ------- | -------- | ------- | -------------------------------------- |
| page        | number  | No       | 1       | Page number for pagination             |
| limit       | number  | No       | 50      | Arcs per page (max 100)                |
| id          | string  | No       | -       | Specific arc ID to fetch               |
| search      | string  | No       | -       | Search arcs by name (max 100 chars)    |
| includeLoot | boolean | No       | false   | Include loot items dropped by this arc |
| sortBy      | string  | No       | name    | Sort field                             |
| sortOrder   | string  | No       | asc     | Sort order (asc/desc)                  |


#### quests - Parameters

| Name      | Type   | Required | Default | Description                           |
| --------- | ------ | -------- | ------- | ------------------------------------- |
| id        | string | No       | -       | Specific quest ID to fetch            |
| page      | number | No       | 1       | Page number for pagination            |
| limit     | number | No       | 40      | Quests per page (max 100)             |
| search    | string | No       | -       | Search quests by name (max 100 chars) |
| sortBy    | string | No       | name    | Sort field                            |
| sortOrder | string | No       | asc     | Sort order (asc/desc)                 |


#### event-timers - Parameters

| Name | Type   | Required | Default | Description                 |
| ---- | ------ | -------- | ------- | --------------------------- |
| map  | string | No       | -       | Filter events by map name   |
| name | string | No       | -       | Filter events by event name |


#### game-map-data - Parameters

| Name    | Type   | Required | Default | Description                            |
| ------- | ------ | -------- | ------- | -------------------------------------- |
| tableID | string | Yes      | -       | arc_map_data                           |
| mapID   | string | Yes      | -       | dam, spaceport, buried-city, blue-gate |
