# screepsmod-dynamicmarket

[![NPM info](https://nodei.co/npm/screepsmod-dynamicmarket.png?downloads=true)](https://npmjs.org/package/screepsmod-dynamicmarket)

# Installation 

1. `npm install screepsmod-dynamicmarket` in your mods folder. / (Or use steam workshop)
2. Configure!

## Create NPC terminals

If there are no system (`null` user) terminals to trade with then at least one will need to be created. Access the server administrative prompt through the Steam GUI or using this console command:

```shell
npx screeps cli
```

Create a terminal, preferably in a permanent wall with the following command. Adjust the `room` and `x` and `y` as needed:

```js
storage.db["rooms.objects"].insert({type:'terminal',x:45,y:45,room:'W0N0',notifyWhenAttacked:false,user:null,store:{energy:0},storeCapacity:300000,hits:3000,hitsMax:3000})
```

# Features

- THIS NEEDS A LOT OF TESTING THAT I CANNOT DO ON A SOLO SERVER
- Dynamic simulated supply and demand. NPC terminals prices will fluctuate depending on how much of a resource is being bought or sold.
- Supports basic fixed/random pricing
- Random boost sales (Allow another way for players to get boosts)

# Upcoming Features

- Random market events (Effects pricing and supply)
- NPC Resell (NPC terminals will resell a portion of the resources it buys, competing with players)

# Config
Config is done via `example_dynamicMarketConfig.js`. Be sure to rename the file to `dynamicMarketConfig.js`. (Or don't, the defaults should work fine)

# Credits
Based off screepsmod-market by ags131 (https://github.com/ScreepsMods/screepsmod-market)

