---
title: 'Physics-Informed Neural Networks for Anisotropic Cardiac Activation Mapping'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Sherif El-Gendy
  - Mazen Atlam
  - Ahmed Mohamed
# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'

date: '2025-11-01T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
#OR
# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: "In 35th International Conference on Computer Theory and Applications (ICCTA 2025)"
publication_short: "In ICCTA'25"

abstract: "Cardiac activation mapping is critical for guiding catheter ablation of arrhythmias but remains challenging due to the difficulty of reconstructing wavefront propagation from sparse intracardiac catheter scans. Existing methods often neglect the physical laws governing electrical signal propagation in cardiac tissues. Approaches that do incorporate physics rely on isotropic models, assuming constant conduction velocity in all directions, and thus fail to account for the influence of fiber orientation, leading to physiologically inconsistent activation maps. In contrast to previous physics-informed frameworks that assume isotropic conduction, this article introduces a Physics-Informed Neural Network (PINN) framework that integrates the anisotropic Eikonal equation to embed the underlying physics of cardiac conduction and explicitly model the effect of myocardial fiber orientation on wavefront propagation, enabling physio-logically consistent reconstruction of cardiac activation maps that reflect these directional effects. The framework employs a dual-network architecture: one network estimates activation time φ(x), and the other reconstructs the direction-dependent conduction velocity tensor D(x) from sparse intracardiac catheter data.Evaluated on a dataset with sharp conductivity transitions, the framework accurately reconstructed activation times (NRMSE:1.67%) and captured key features of conduction anisotropy. This physics-consistent approach represents a significant step toward clinically reliable cardiac activation maps for ablation planning."

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: ["Physics-Informed Neural Networks", "Deep Learning"]

# Display this page in the Featured widget?
# featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# image:
#   caption: ''
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
#   - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
