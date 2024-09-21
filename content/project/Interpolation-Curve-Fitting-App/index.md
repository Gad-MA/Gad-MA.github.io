---
title: Interpolation-Curve-Fitting-App
summary: Curve fitting and interpolation are among the most useful tool in signal processing and data science! this desktop app opens the door to engineers to easily visualize how the process is done using one chunk or multiple chunks, Also the error map shows us how our model is far from the original data and what is the percentage error.
tags:
  - DSP

date: '2022-04-27T00:00:00Z'

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
url_code: 'https://github.com/Yasien99/Interpolation-Curve-Fitting-App'
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
# Interpolation-Curve-Fitting-App

## About

>Curve fitting and interpolation are among the most useful tool in signal processing and data science! this desktop app opens the door to engineers to easily visualize how the process is done using one chunk or multiple chunks, Also the error map shows us how our model is far from the original data and what is the percentage error.

## Features
- The user can open and display any arbitrary signal
- The user can choose if the fitting to be done as one chunk or multiple ones.
- The user can choose the order of the fitting polynomial (either for the big chunk or the multiple ones).
- The user can generate an error map for the fitting process.
- The user can clip the curve fitting process into only portion of the open signal. so the last portion is practically extrapolated.


### Running

1. **_Clone the repository_**

```sh
$ git clone https://github.com/Yasien99/Interpolation-Curve-Fitting-App.git
```
2. **_Navigate to repository directory_**
```sh
$ cd Interpolation-Curve-Fitting-App\src

```
3. **_install project dependencies_**
```sh
pip install -r dependencies.txt
```
4. **_Run the application_**
```sh
python main.py
```

<div align="center">
  <img src="docs/shot.gif" />
</div>




