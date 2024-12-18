---
title: "Cardiac Activation Mapping using Physics-Informed Neural Networks"
authors:
- admin
date: "2024-12-18T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
# publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Atrial fibrillation (AF) is the most common heart arrhythmia, affecting millions worldwide. Diagnosis and treatment of AF often involves creating electro-anatomic activation maps, which represent the timing of tissue activation across the heart’s atria. Current mapping methods use interpolation techniques like linear or Gaussian process regression based on sparse electrode data collected within the atria. However, these techniques suffer from noise from electrode positioning and lack of prior physical knowledge of cardiac wave propagation, leading to suboptimal diagnostic accuracy. To address these challenges, we propose a physics-informed neural network (PINN) for cardiac activation mapping that incorporates the underlying wave propagation dynamics of cardiac electrical activity. Benchmarking against traditional interpolation and Gaussian process regression, the PINN model demonstrated improved diagnostic accuracy, paving the way for improved procedural efficiency and patient outcomes in atrial fibrillation diagnostics.

# Summary. An optional shortened abstract.
summary:

tags:
# - Source Themes
featured: false

links:
# - name: Custom Link
#   url: http://example.org
url_pdf: uploads/cardiac_activation_mapping/cardiac_activation_mapping.pdf
# url_code: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_dataset: '#'
url_poster: '#'
url_project: ''
# url_slides: ''
# url_source: '#'
# url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: "Electrical Activation of The Heart. SOURCE: https://ccl.medunigraz.at/ep_modeling.html"
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
# - internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
