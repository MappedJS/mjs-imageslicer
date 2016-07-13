# MappedJS image-slicer

Python application for slicing large images into small tiles. mjs-imageslicer is part of [MappedJS](http://mappedjs.de/) application

## usage examples
```sh
# smallest usage example
$ python imageslicer.py -i image/foo-1.png -o image/dist/
```

```
# slicing multiple images at once
$ python imageslicer.py -i image/foo-1.png image/bar/foo-2.png -o image/dist/
```

```
# slicing with options
$ python imageslicer.py -i image/foo-1.png -o image/dist/ -p img/ -t 512 -s 512 -m 256 -e png
```

## options
### -i or --input (required)
    * type: string
    * arguments: 1+
    * description: path of source files(s)
### -o or --output (required)
    * type: string
    * arguments: 1
    * description: path of destination
### -s or --size (optional)
    * type: integer
    * default: 512
    * arguments: 1
    * description: size of one tile
### -m or --minsize (optional)
    * type: integer
    * default: 128
    * arguments: 1
    * description: minimum size of one tile
### -z or --zoom (optional)
    * type: float
    * default: [0.8, 1.2]
    * arguments: 2
    * description: minimum zoom of smallest image and maximum zoom of largest image
### -t or --thumbSize (optional)
    * type: integer
    * default: 10
    * arguments: 1
    * description: maximum width or height of thumbnail in percentage relative to original size
### -p or --path (optional)
    * type: string
    * default: ""
    * arguments: 1
    * description: path information for image paths in JSON output
### -c or --clearfolder (optional)
    * type: boolean
    * default: False
    * arguments: 1
    * description: use with care: deletes all contents of output-folder
### -e or --extension (optional)
    * type: string
    * default: jpg
    * arguments: 1
    * description: extension of output

## requirements
mjs-imageslicer requires [python](http://python.org/) to run.

## license
See [bsd-2-clause-license](./LICENSE) for details
