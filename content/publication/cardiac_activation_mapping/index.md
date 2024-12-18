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
# Team Members
# References
[1] “Correction to: Heart Disease and Stroke Statistics—
2018 Update: A Report From the American
Heart Association”. In: Circulation 137.12 (2018),
e493–e493. url: https://www.ahajournals.org/
doi/abs/10.1161/CIR.0000000000000573.

[2] Steven E Williams et al. “Local activation time
sampling density for atrial tachycardia contact
mapping: how much is enough?” In: EP Europace
20.2 (Apr. 2017), e11–e20. issn: 1099-5129. doi:
10.1093/europace/eux037.

[3] Sam Coveney et al. “Probabilistic Interpolation
of Uncertain Local Activation Times on Human
Atrial Manifolds”. In: IEEE Transactions on
Biomedical Engineering 67.1 (2020), pp. 99–109.
doi: 10.1109/TBME.2019.2908486.

[4] M. Mas`e and F. Ravelli. “Automatic reconstruction
of activation and velocity maps from electroanatomic
data by radial basis functions”. In: 2010
Annual International Conference of the IEEE Engineering
in Medicine and Biology. 2010, pp. 2608–
2611. doi: 10.1109/IEMBS.2010.5626616.

[5] Vincent Jacquemet. “An eikonal-diffusion solver
and its application to the interpolation and the
simulation of reentrant cardiac activations”. In:
Computer Methods and Programs in Biomedicine
108.2 (2012), pp. 548–558. issn: 0169-2607. doi:
https://doi.org/10.1016/j.cmpb.2011.05.
003. url: https : / / www . sciencedirect . com /
science/article/pii/S0169260711001180.

[6] Simone Pezzuto et al. “Evaluation of a Rapid
Anisotropic Model for ECG Simulation”. English.
In: Frontiers in physiology 8.MAY (May 2017).
issn: 1664-042X. doi: 10 . 3389 / fphys . 2017 .
00265.

[7] P. Colli Franzone, L. Guerri, and S. Rovida.
“Wavefront propagation in an activation model of
the anisotropic cardiac tissue: asymptotic analysis
and numerical simulations”. In: Journal of Mathematical
Biology 28.2 (Feb. 1990), pp. 121–176.
issn: 1432-1416. doi: 10.1007/BF00163143. url:
https://doi.org/10.1007/BF00163143.

[8] Piero Colli Franzone and Luciano Guerri. “Spreading
of excitation in 3-d models of the anisotropic
cardiac tissue. I. validation of the eikonal
model”. In: Mathematical Biosciences 113.2
(1993), pp. 145–209. issn: 0025-5564. doi: https:
/ / doi . org / 10 . 1016 / 0025 - 5564(93 ) 90001 -
Q. url: https : / / www . sciencedirect . com /
science/article/pii/002555649390001Q.

[9] Hubert Baty and L´eo Baty. “Solving differential
equations using physics informed deep learning: a
hand-on tutorial with benchmark tests”. working
paper or preprint. Apr. 2023. url: https://hal.
science/hal-04002928.

[10] M. Raissi, P. Perdikaris, and G.E. Karniadakis.
“Physics-informed neural networks: A deep learning
framework for solving forward and inverse
problems involving nonlinear partial differential
equations”. In: Journal of Computational Physics
378 (2019), pp. 686–707. issn: 0021-9991. doi:
https://doi.org/10.1016/j.jcp.2018.10.
045. url: https : / / www . sciencedirect . com /
science/article/pii/S0021999118307125.

[11] Mart´ın Abadi et al. TensorFlow: A system for
large-scale machine learning. 2016. arXiv: 1605.
08695 [cs.DC]. url: https://arxiv.org/abs/
1605.08695.

[12] Diederik P. Kingma and Jimmy Ba. Adam: A
Method for Stochastic Optimization. 2017. arXiv:
1412.6980 [cs.LG]. url: https://arxiv.org/
abs/1412.6980.

[13] Michael Stein. “Large Sample Properties of Simulations
Using Latin Hypercube Sampling”. In:
Technometrics 29.2 (1987), pp. 143–151. doi: 10.
1080/00401706.1987.10488205. eprint: https:
//www.tandfonline.com/doi/pdf/10.1080/
00401706.1987.10488205. url: https://www.
tandfonline.com/doi/abs/10.1080/00401706.
1987.10488205.

[14] Carl Edward Rasmussen and Christopher K. I.
Williams. Gaussian Processes for Machine
Learning. The MIT Press, Nov. 2005. isbn:
9780262256834. doi: 10.7551/mitpress/3206.
001 . 0001. url: https : / / doi . org / 10 . 7551 /
mitpress/3206.001.0001.

[15] P. Perdikaris. Gaussian Processes: A Hands-on Tutorial.
Available online at: https://github.com/
paraklas/GPTutorial. 2017.

[16] Francisco Sahli Costabal, Daniel E. Hurtado, and
Ellen Kuhl. “Generating Purkinje networks in the
human heart”. In: Journal of Biomechanics 49.12
(2016). Cardiovascular Biomechanics in Health
and Disease, pp. 2455–2465. issn: 0021-9290. doi:
https://doi.org/10.1016/j.jbiomech.2015.
12.025. url: https://www.sciencedirect.com/
science/article/pii/S0021929015007332.
6