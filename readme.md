- based on `jpeg-9d` from https://ijg.org/
- adds a couple of modifications to mess with the encoding process in order to produce glitchy images

## build

```
./configure
make -j4
```

## run

```
./cjpeg -grayscale -baseline \
  -qtables "tables.txt" \
  -huffTableMultiplier 0.8 \
  -dctNoise 1000 \
  -quantMultiplier 30 \
  -outfile glitch.jpg
  input.tga
```
