---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Deformation Capture and Modeling of Soft Objects"
authors: [Bin Wang , Longhua Wu , KangKang Yin, Uri Ascher, Libin Liu, Hui Huang]
date: 2015-05-16T00:11:09+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-05-16T00:11:09+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "ACM Transactions on Graphics (Proceedings of SIGGRAPH 2020)"
publication_short: ""

abstract: "We present a data-driven method for deformation capture and modeling of general soft objects. We adopt an iterative framework that consists of one component for physics-based deformation tracking and another for spacetime optimization of deformation parameters. Low cost depth sensors are used for the deformation capture, and we do not require any force-displacement measurements, thus making the data capture a cheap and convenient process. We augment a state-of-the-art probabilistic tracking method to robustly handle noise, occlusions, fast movements and large deformations. The spacetime optimization aims to match the simulated trajectories with the tracked ones. The optimized deformation model is then use to boost the accuracy of the tracking results, which can in turn improve the deformation parameter estimation itself in later iterations. Numerical experiments demonstrate that the tracking and parameter optimization components complement each other nicely. 

Our spacetime optimization of the deformation model includes not only the material elasticity parameters and dynamic damping coefficients, but also the reference shape which can differ significantly from the static shape for soft objects. The resulting optimization problem is highly nonlinear in high dimensions, and challenging to solve with previous methods. We propose a novel splitting algorithm that alternates between reference shape optimization and deformation parameter estimation, and thus enables tailoring the optimization of each subproblem more efficiently and robustly.

Our system enables realistic motion reconstruction as well as synthesis of virtual soft objects in response to user stimulation. Validation experiments show that our method not only is accurate, but also compares favorably to existing techniques. We also showcase the ability of our system with high quality animations generated from optimized deformation parameters for a variety of soft objects, such as live plants and fabricated models.
"

# Summary. An optional shortened abstract.
summary: "We present a data-driven method that can capture deformation of generic soft objects in high fidelity with low-cost depth sensors; and estimate plausible deformation parameters from these pure kinematic motion trajectories, without requiring any force-displacement measurements as is common in traditional methods. Using the learned deformation models, new motion and deformation can be synthesized at interactive rates to respond to dynamic perturbations or satisfy user-specified constraints. "

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video: https://www.youtube.com/watch?v=1gRa8KCxR08

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---


### Acknowledgement

We thank the anonymous reviewers for their constructive comments. We are grateful to the authors of [Chen et al. 2014] for sharing their data and fabricated models for our validation and comparison experiments. We also thank Jiacheng Ren, Jiangtao Shen, Keng Hua Sing, Francois Faure and Matthieu Nesme for their help and thoughtful discussions at the various stages of developing this project. This work is supported in part by Singapore Ministry of Education Academic Research Fund Tier 2 (MOE2011-T2-2-152); Microsoft Research Asia Collaborative Research Program (FY14-RES-OPP-002); NSFC (61402459, 61379090, 61331018); National 973 Program (2014CB360503); Shenzhen Innovation Program (CXB201104220029A, JCYJ20140901003939034, JCYJ20130401170306810); NSERC Discovery Grant (84306).