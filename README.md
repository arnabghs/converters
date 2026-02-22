# Image Conversion
To convert a single image from PNG to WEBP

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

# Video Conversion

Install ffmpeg using Homebrew:
```
brew install ffmpeg
``` 

To convert a single video from MKV to WEBM:
```
ffmpeg -i ~/Downloads/original_files/H_AOT_0001.mkv -c:v libvpx-vp9 -crf 18 -b:v 0 -c:a libopus ~/Downloads/transformed_files/H_AOT_0001.webm
```

To convert an entire folder of MKV videos to WEBM,

1. Make sure all the `.mkv` files are in `~/Downloads/original_files`

```
./mkv2webm
```

New files will be stored in `~/Downloads/transformed_files`