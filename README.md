# Heide Park Resort API

> **Disclaimer:** The following information has been reverse-engineered from the Heide Park Resort app. This project is not affiliated with Heide Park Resort or attractions.io.

Hardcoded API endpoint, sourced from the Heide Park Resort app ([Google Play](https://play.google.com/store/apps/details?id=de.heide_park.heidepark)).

Returns a JSON file containing opening hours, attraction wait times, etc. Check out [`data/response.json`](https://github.com/theme-park-research/heide-park-api/blob/main/data/response.json) for a sample.

For mapping an item's `_id` to its name, check out [`data/mappings.json`](https://github.com/theme-park-research/heide-park-api/blob/main/data/mappings.json).

## Request

```sh
curl --request GET \
  --url https://live-data.attractions.io/3d67a479-3b8b-4cac-ab17-1218a1aec37e.json \
  --header 'accept-encoding: gzip' \
  --header 'connection: Keep-Alive' \
  --header 'host: live-data.attractions.io' \
  --header 'user-agent: okhttp/3.14.9'
```

[View this request on Hoppscotch](https://hopp.sh/r/6AR5Q2veLG9j)

---

The above code snippet should produce the exact same request as the Android app, no headers have been omitted.

Since the API is not official, it may be subject to change.

## Further investigation

If you want, you can investigate the API further:

- Use `mitmproxy` or a similar tool to intercept the Android app's traffic
- Use `apktool` or a similar tool to extract UUIDs, URLs, etc.

The [`data/mappings.json`](https://github.com/theme-park-research/heide-park-api/blob/main/data/mappings.json) file is based on [`data/records.json`](https://github.com/theme-park-research/heide-park-api/blob/main/data/records.json), which can be extracted from this [zip](https://attractions-io-app-bundled-data-prod.s3.amazonaws.com/deltas/heide-park/2022-05-10T09:00:46Z_2022-05-22T10:21:00Z.zip) containing application data. An up-to-date version of the zip can be acquired by intercepting the application's traffic.