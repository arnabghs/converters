To convert a single image from PNG to WEBP,


For Mac M1 ARM64, run the following commands in your terminal:
```
cd ARM/image
./libwebp-1.6.0-mac-arm64/bin/cwebp ~/Downloads/web.png -o ~/Downloads/DSL0082-web.webp
```

For intel x86_64, run the following commands in your terminal:
```
cd x86/image
./libwebp-1.5.0-mac-x86-64 ~/Downloads/web.png -o ~/Downloads/DSL0082-web.webp
```

To Convert a zip of folder containing PNG images:
```
./png2webp ARM ~/Downloads/BES0001-20250913T131615Z-1-001.zip
```

It will create a new folder, convert all the images to WEBP and organize them in Regular and Oversize dir.

=============================================

To reduce JPG image size, use built-in library

```
sips --setProperty formatOptions 50 ~/Downloads/IMG_5133.JPG --out ~/Downloads/output.jpg
```