# Heide Park Resort API

> **Disclaimer:** The following information has been reverse-engineered from the Heide Park Resort app. This project is not affiliated with Heide Park Resort or attractions.io.

Hardcoded API endpoint, sourced from the Heide Park Resort app ([Google Play](https://play.google.com/store/apps/details?id=de.heide_park.heidepark)).

Returns a JSON file containing opening hours, attraction wait times, etc. Check out [`data/response.json`](https://github.com/theme-park/heide-park-api) for a sample.

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