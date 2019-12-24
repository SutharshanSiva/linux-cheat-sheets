# convert

[Back](README.md) to Linux Cheatsheets by Ireaneus

To resize an image to a fixed width and proportional height:

```bash
[user@server1]$ convert original-image.jpg -resize 100x converted-image.jpg
```

To resize an image to a fixed height and proportional width

```bash
[user@server1]$ convert original-image.jpg -resize x100 converted-image.jpg
```

To resize an image to a fixed width and height

```bash
[user@server1]$ convert original-image.jpg -resize 100x100 converted-image.jpg
```

To resize an image and simultaneously change its file type

```bash
[user@server1]$ convert original-image.jpg -resize 100x converted-image.png
```

To resize all of the images within a directory and implement a for loop

```bash
for file in `ls original/image/path/`;
    do new_path=${file%.*};
    new_file=`basename $new_path`;
    convert $file -resize 150 conerted/image/path/$new_file.png;
done
```
