Generate screenshot: 

```
npx playwright screenshot --viewport-size=1072,1448 "file://$(PWD)/_site/doing/index.html" doing-raw.png
```

Convert to kindle-friendly

```
magick doing-raw.png -colorspace Gray -depth 8 -colors 16 -dither None -strip -interlace none -define png:color-type=0 assets/doing.png
```
