---
title: Image Processing in Frequency and Spatial domains
summary: Image Processing GUI using Python.Implemented some image processing algorithms applicable on both RGB and grayscale Images with the ability to modify the kernel size (filter strength). Filters implemented and applied Histogram Equalisation, Mean Filter, Median Filter, Low Pass Filter, High Pass Filter, Gaussian Filter, Sobel Filter, and Laplacbian Filter.
tags:
  - Computer Vision
date: '2022-01-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: ""
  focal_point: Smart

links:
  # - icon: github
  #   icon_pack: fab
  #   name: Follow
  #   url: https://github.com/Yasien99/GI-Tract-Image-Segmentation
url_code: 'https://github.com/Yasien99/Img-Filter'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---
# Img-Filter

## About

>simple GUI was made for computer vision course, it has 2 tabs, one for filters and the other one for histogram equalization.

## Features
- The user can open and display any arbitrary image
- The user can choose between 4 filters.
- The user can see the filtered image alongside the original one.
- The user can see the histogram equalization of his image.


### Running

1. **_Clone the repository_**

```sh
$ git clone https://github.com/Yasien99/Img-Filter.git
```
2. **_Navigate to repository directory_**
```sh
$ cd Img-Filter\src

```
3. **_install project dependencies_**
```sh
pip install -r requirements.txt
```
4. **_Run the application_**
```sh
python main.py
```

<div align="center">
  <img src="docs/img-filter.gif" />
</div>



