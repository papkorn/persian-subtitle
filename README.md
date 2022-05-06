# Persian Subtitle - Open API

## This is a __FREE__ API Endpoint for downloading Persian APIs

For PapkornBot, we need to use Persian subtitles. However, there was not sufficient API to fulfill our needs. As a result, we implement a powerful crawler to gather Persian subtitles from various resources and manage them. 

---
## Endpoints

All of the Subtitles are accessible through IMDB_ID info! You need to know IMDB_ID to get the appropiate subtitles.

Main URL: https://api.pkdirectdl.xyz

### Get Movie Subtitle List

**URL** : `/movie​/{imdb_id}​/subtitle/`

**Method** : `GET`

**Auth required** : NO


#### Success Response

**Code** : `200 OK`

**Content example**

```json
[
  {
    "id": 30471,
    "uri": "https://subtitle.pkdirectdl.xyz/subtitles/1375666/Inception.Making.of.2010.BluRay.720p.AC3.x264-for.HD-bits.ro%20fa.srt",
    "file_name": "Inception.Making.of.2010.BluRay.720p.AC3.x264-for.HD-bits.ro fa.srt",
    "quality": "BluRay",
    "resolution": "720p",
    "encoder": null,
    "x265": false,
    "size": "66.2 kB",
    "author": null,
    "is_deleted": false,
    "extra_info": null,
    "created_at": "2022-04-18T14:51:46.624761+04:30"
  },
  ...
]
```

#### Error Response

**Condition** : If IMDB_ID is not valid

**Code** : `500 BAD REQUEST`

---
### Get Series Subtitle List

**URL** : `/series/{imdb_id}​/subtitle/?episode_no={EPISODE_NUMBER}&season_no={SEASON_NUMBER}`

**Method** : `GET`

**Auth required** : NO


#### Success Response

**Code** : `200 OK`

**Content example**

```json
[
  {
    "id": 5024,
    "uri": "https://subtitle.pkdirectdl.xyz/subtitles/4370596/Better.Things.S05E02.1080p.WEB.h264-GOSSIP-%5BFarsi%5D.srt",
    "file_name": "Better.Things.S05E02.1080p.WEB.h264-GOSSIP-[Farsi].srt",
    "quality": "WEBRip",
    "resolution": "1080p",
    "encoder": null,
    "x265": false,
    "size": "47.9 kB",
    "author": null,
    "is_deleted": false,
    "extra_info": null,
    "created_at": "2022-04-13T10:11:08.561745+04:30"
  },
  ...
]
```

#### Error Response

**Condition** : If IMDB_ID is not valid or episode_no or season_no are not defiened

**Code** : `500 BAD REQUEST` | `404 Not Found`

