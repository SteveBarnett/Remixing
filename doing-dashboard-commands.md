Short version:

```
npx playwright screenshot --viewport-size=1072,1448 "file://$(PWD)/_site/doing-dashboard/index.html" doing.png && magick doing.png -rotate 180 doing.png
```

Long version:

```
npx playwright screenshot --viewport-size=1072,1448 "file://$(PWD)/_site/doing-dashboard/index.html" doing-raw.png
```

Convert to kindle-friendly and remove raw

```
magick doing-raw.png -colorspace Gray -depth 8 -colors 16 -dither None -strip -interlace none -define png:color-type=0 assets/doing.png && rm doing-raw.png
```
