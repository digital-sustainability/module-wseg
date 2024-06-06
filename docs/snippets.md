# Snippets

## git pull all

```
find . -type d -depth 1 -exec git --git-dir={}/.git --work-tree=$PWD/{} pull origin --verbose \;
```

## render git activity with [gource](https://gource.io)

```
rm -rf gource/ \
  && mkdir gource \
  && for d in $(ls -d *); do \
       cd $d && gource --key -a 1 --max-file-lag 0.1 --seconds-per-day 1 -1920x1080 -o - \
       | ffmpeg -y -r 60 -f image2pipe -vcodec ppm -i - -vcodec libx264 -preset ultrafast -pix_fmt yuv420p -crf 1 -threads 0 -bf 0 ../gource/$d.mp4 \
       & cd .. ; \
  done
```
