## Intro
hexo-tag-flickr-extended is a Hexo plugin for inserting image from Flickr in Hexo posts.This plugin is based on [plugin](https://github.com/visioncan/hexo-tag-flickr).And add http proxy support.


## Installation
Run command in the hexo root directory :

```npm install hexo-tag-flickr-extended --save```


## Usage
In _config.yml of hexo :

```yaml
# Flickr API key
flickr_ext_api_key: your_flickr_api_key

# Http proxy host & port,e.g. http://127.0.0.1:1080
flickr_ext_proxy_config: your_http_server

# Cache file path & expiry time in milliseconds
flickr_ext_cache_file_path: flickr_img_cache.json
flickr_ext_cache_expires: 2592000000
```

Then,you can insert hexo tag in markdown file like this :

```markdown
{% flickrExt flickr_image_id size_suffix %} 
```

Available size suffixes :


* **`s`**   small square 75x75
* **`q`**	large square 150x150
* **`t`**	thumbnail, 100 on longest side
* **`m`**	small, 240 on longest side
* **`n`**	small, 320 on longest side
* **`-`**	medium, 500 on longest side
* **`z`**	medium 640, 640 on longest side
* **`c`**	medium 800, 800 on longest side†
* **`b`**	large, 1024 on longest side*
* **`h`**	large 1600, 1600 on longest side†
* **`k`**	large 2048, 2048 on longest side†
* **`o`**	original image, either a jpg, gif or png, depending on source format

## License
MIT
