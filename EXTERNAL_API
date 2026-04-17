# PlayerStats External API

Base URL:

`http://YOUR_SERVER_IP:1339/api/v1`

Authentication:

- if `api.require-key: true`, send `X-API-Key: <key>`
- or pass `?api_key=<key>`
- single-profile public endpoint uses `api.profile-token`

CORS:

- configured by `api.cors-allow-origin`

Endpoints:

## `GET /api/v1/overview`

Returns plugin metadata and the full dashboard payload.

## `GET /api/v1/server`

Returns live server info and lifetime totals.

## `GET /api/v1/players`

Returns all player summaries.

## `GET /api/v1/player?name=<nick>`

Returns a player's summary plus top broken blocks, placed blocks, and mob kills.

Alternative:

`GET /api/v1/player?uuid=<uuid>`

## `GET /api/v1/compare?players=Steve,Alex`

Compares 2 or 3 players by returning full detail payloads for each.

## `GET /api/v1/public/player?name=<nick>&token=<profile-token>`

Returns one player profile only.

Alternative:

- send `X-Profile-Token: <profile-token>`
- use `uuid` instead of `name`



```bash
curl "http://127.0.0.1:1339/api/v1/player?name=Steve"
```
Example: "http://127.0.0.1:1339/api/v1/player?name=RaitXEVIL"
We getting this:
{
  "player": {
    "uuid": "be36e79d-6828-3847-8ed3-62216391e9ec",
    "name": "RaitXEVIL",
    "onlineSeconds": 815020,
    "totalMobKills": 18602,
    "totalBlocksPlaced": 125441,
    "totalBlocksBroken": 371886
  },
  "topBrokenBlocks": [
    {
      "key": "STONE",
      "count": 97047
    },
    {
      "key": "GRASS_BLOCK",
      "count": 57150
    },
    {
      "key": "NETHERRACK",
      "count": 57104
    },
    {
      "key": "SANDSTONE",
      "count": 41105
    },
    {
      "key": "DIRT",
      "count": 34287
    },
    {
      "key": "DARK_OAK_LOG",
      "count": 16374
    },
    {
      "key": "DIORITE",
      "count": 6842
    },
    {
      "key": "GRANITE",
      "count": 5749
    },
    {
      "key": "SAND",
      "count": 5057
    },
    {
      "key": "WHEAT",
      "count": 4528
    }
  ],
  "topMobKills": [
    {
      "key": "ENDERMAN",
      "count": 14402
    },
    {
      "key": "ZOMBIE",
      "count": 555
    },
    {
      "key": "SKELETON",
      "count": 335
    },
    {
      "key": "CREEPER",
      "count": 315
    },
    {
      "key": "SPIDER",
      "count": 255
    },
    {
      "key": "SHEEP",
      "count": 124
    },
    {
      "key": "COW",
      "count": 104
    },
    {
      "key": "MAGMA_CUBE",
      "count": 91
    },
    {
      "key": "WITHER_SKELETON",
      "count": 86
    },
    {
      "key": "SLIME",
      "count": 77
    }
  ],
  "topPlacedBlocks": [
    {
      "key": "DIRT",
      "count": 44276
    },
    {
      "key": "STONE_BRICKS",
      "count": 9489
    },
    {
      "key": "BAMBOO",
      "count": 8947
    },
    {
      "key": "POLISHED_GRANITE",
      "count": 7437
    },
    {
      "key": "POLISHED_DIORITE",
      "count": 7151
    },
    {
      "key": "TORCH",
      "count": 4703
    },
    {
      "key": "COBBLESTONE",
      "count": 3792
    },
    {
      "key": "STONE",
      "count": 2722
    },
    {
      "key": "TNT",
      "count": 2478
    },
    {
      "key": "SMOOTH_STONE",
      "count": 2351
    }
  ]
}

```bash
curl -H "X-API-Key: your-key" "http://127.0.0.1:1339/api/v1/compare?players=Steve,Alex,Notch"
```
Example: "http://127.0.0.1:1339/api/v1/compare?players=bot1,RaitXEVIL"
We getting this:
{
  "count": 2,
  "players": [
    {
      "player": {
        "uuid": "05f673da-66b5-37e3-b03b-09bbf434403e",
        "name": "bot1",
        "onlineSeconds": 595836,
        "totalMobKills": 0,
        "totalBlocksPlaced": 10,
        "totalBlocksBroken": 11
      },
      "topBrokenBlocks": [
        {
          "key": "COBBLESTONE",
          "count": 8
        },
        {
          "key": "DIRT",
          "count": 2
        },
        {
          "key": "REDSTONE_WIRE",
          "count": 1
        }
      ],
      "topPlacedBlocks": [
        {
          "key": "COBBLESTONE",
          "count": 8
        },
        {
          "key": "DIRT",
          "count": 2
        }
      ],
      "topMobKills": []
    },
    {
      "player": {
        "uuid": "be36e79d-6828-3847-8ed3-62216391e9ec",
        "name": "RaitXEVIL",
        "onlineSeconds": 815020,
        "totalMobKills": 18602,
        "totalBlocksPlaced": 125441,
        "totalBlocksBroken": 371886
      },
      "topBrokenBlocks": [
        {
          "key": "STONE",
          "count": 97047
        },
        {
          "key": "GRASS_BLOCK",
          "count": 57150
        },
        {
          "key": "NETHERRACK",
          "count": 57104
        },
        {
          "key": "SANDSTONE",
          "count": 41105
        },
        {
          "key": "DIRT",
          "count": 34287
        },
        {
          "key": "DARK_OAK_LOG",
          "count": 16374
        },
        {
          "key": "DIORITE",
          "count": 6842
        },
        {
          "key": "GRANITE",
          "count": 5749
        },
        {
          "key": "SAND",
          "count": 5057
        },
        {
          "key": "WHEAT",
          "count": 4528
        }
      ],
      "topPlacedBlocks": [
        {
          "key": "DIRT",
          "count": 44276
        },
        {
          "key": "STONE_BRICKS",
          "count": 9489
        },
        {
          "key": "BAMBOO",
          "count": 8947
        },
        {
          "key": "POLISHED_GRANITE",
          "count": 7437
        },
        {
          "key": "POLISHED_DIORITE",
          "count": 7151
        },
        {
          "key": "TORCH",
          "count": 4703
        },
        {
          "key": "COBBLESTONE",
          "count": 3792
        },
        {
          "key": "STONE",
          "count": 2722
        },
        {
          "key": "TNT",
          "count": 2478
        },
        {
          "key": "SMOOTH_STONE",
          "count": 2351
        }
      ],
      "topMobKills": [
        {
          "key": "ENDERMAN",
          "count": 14402
        },
        {
          "key": "ZOMBIE",
          "count": 555
        },
        {
          "key": "SKELETON",
          "count": 335
        },
        {
          "key": "CREEPER",
          "count": 315
        },
        {
          "key": "SPIDER",
          "count": 255
        },
        {
          "key": "SHEEP",
          "count": 124
        },
        {
          "key": "COW",
          "count": 104
        },
        {
          "key": "MAGMA_CUBE",
          "count": 91
        },
        {
          "key": "WITHER_SKELETON",
          "count": 86
        },
        {
          "key": "SLIME",
          "count": 77
        }
      ]
    }
  ]
}
