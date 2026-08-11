Generate screenshot: 

```
npx playwright screenshot --viewport-size=1448,1072 "file://$(PWD)/_site/doing/index.html" doing-raw.png
```

Convert to kindle-friendly and remove raw

```
magick doing-raw.png -rotate 90 -colorspace Gray -depth 8 -colors 16 -dither None -strip -interlace none -define png:color-type=0 assets/doing.png && rm doing-raw.png
```
