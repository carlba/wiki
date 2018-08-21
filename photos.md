# Usage

## Uploading folders to Google Photos

The tool [upload-gphotos](https://github.com/3846masa/upload-gphotos) can be used to upload photos
,like so:

```bash
upload-gphotos Fjällvandring_2013/* -u genzorg@gmail.com -a 'Fjällvandring 2013'
```

## Converting proprietary RAW formats such as .CR2 to .dng

[Adobe DNG Converter for Mac OS](http://www.adobe.com/go/dng_converter_mac/)

[Adobe DNG Converter for Windows](http://www.adobe.com/go/dng_converter_win/)


## Set the system modification time of a file to the EXIF time of the file
```
exiftool "-DateTimeOriginal>FileModifyDate" -ext .dng -r /storage/00data/pictures/albums/Sydamerika\ 2013/
```
-ext
:The changes will only be applied to files of this extension
-r
:Recursivly look for files in the specified folder

