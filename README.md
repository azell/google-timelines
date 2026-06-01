# Why does this project exist?

I needed a way to export all of the timeline data on my Android device into
a format that could be imported into [Google Maps](https://support.google.com/mymaps/answer/3024836).

## Getting started

[Export your Timeline data](https://support.google.com/maps/answer/6258979?co=GENIE.Platform%3DAndroid&oco=1)

## Install uv

Home page for **uv** is [here](https://docs.astral.sh/uv/)

```bash
brew install uv
```

## Create directories for personal data

```bash
mkdir data timelines
```

Copy your **Timeline.json** file into the `timelines` directory.

## Install Python dependencies

```bash
uv sync
```

## Cache the latest place metadata

Place IDs contained in the timeline file may be outdated. The Google Places API supports
refreshing stored place IDs [for free](https://developers.google.com/maps/documentation/places/web-service/place-id#refresh-id).
