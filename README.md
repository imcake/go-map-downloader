# go-map-downloader

![build_badge](https://github.com/Icemap/go-map-downloader/workflows/Go/badge.svg)

English | [中文](README_ch.md)

Map downloader for golang. It supports multiple map type:

- google satellite
- google image
- google terrain
- amap satellite
- amap cover
- amap image

## Feature

- Download map tile picture
- Combine tile to a big map

## Install

```bash
$ go get -u github.com/Icemap/go-map-downloader
```

## Example

### google satellite
```bash
$ ./go-map-downloader -l 139.278433 -t 35.968355 -r 140.506452 -b 35.427143 -min 11 -max 11 -type GoogleSatellite
```
![google satellite](pic/google_satellite_level_11.jpg)

### amap image
```bash
$ ./go-map-downloader -l 139.278433 -t 35.968355 -r 140.506452 -b 35.427143 -min 11 -max 11 -type AMapImage
```
![amap_image](pic/amap_image_level_11.jpg)

### help
```bash
$ ./go-map-downloader -h
Usage of ./go-map-downloader:
  -b float
        bottom latitude
  -c    combine same level map together (default true)
  -g int
        goroutine nums (default 50)
  -l float
        left longitude
  -max int
        map max level (default 3)
  -min int
        map min level (default 1)
  -p string
        map save path (default "/tmp")
  -q int
        query file per second number (default 500)
  -r float
        right longitude
  -retry int
        max retry num (default 3)
  -t float
        top latitude
  -type string
        map type (GoogleSatellite/GoogleImage/GoogleTerrain/AMapSatellite/AMapCover/AMapImage) (default "GoogleSatellite")
```
