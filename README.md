# Imgur Album Downloader

`imgur_download` is a small python script to download all images from an Imgur album.

# Requirements
 * Registrating with the Imgur API due to their [requirments](https://api.imgur.com/#authentication 'The Imgur API - General Information') (no unauthenticated requests are accepted)
 * Python 2.7 or greater
 * pip to install Imgur's [python wrapper](https://github.com/Imgur/imgurpython 'Imgur/imgurpython: The official Imgur python client library')

# Installation

 1. Copy [example.config.yaml](./example.config.yaml) to `~/.config/imgur_downloader/config.yaml` or any other location
 2. Register for an Imgur API application [here](http://api.imgur.com/#registerapp 'The Imgur API - General Information') (Remember the Client ID and Client Secret!)
 3. Fill in  `imgur_client_id` and `imgur_client_secret` in `config.yaml`

# Usage
```
$ ./imgur_downloader -h
usage: imgur_downloader [-h] [-c CONFIG] -a ALBUM [-d DIRECTORY]

Download an Imgur album/gallery into a folder.

optional arguments:
  -h, --help            show this help message and exit
  -c CONFIG, --config CONFIG
                        config file to load settings from
  -a ALBUM, --album ALBUM
                        album ID to download from Imgur (can be specified
                        multiple times)
  -d DIRECTORY, --directory DIRECTORY
                        directory to save images into
```

Get your Imgur album ID (`https://imgur.com/a/<album ID>/`) and pass it to the script!

If your Imgur URL is http://imgur.com/a/3sHNB your album ID is `3sHNB `

```
$ ./imgur_downloader -a 3sHNB
```

Download multiple albums at once by specifying multiple ID's

```
$ ./imgur_downloader -a 3sHNB -a 5jBc45
```

By default the script will download the images into the current working directory, otherwise you can specify a directory by passing `-d` to the script

```
$ ./imgur_downloader -a 3sHNB -a 5jBc45 -d ~/Wallpapers
```

# License
See [LICENSE](./LICENSE)

# Credit
Written by [James Loh](https://jloh.co/l/blog) ([@itsjloh](https://twitter.com/itsjloh))
