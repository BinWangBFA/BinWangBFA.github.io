---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Example-driven Virtual Cinematography by Learning Camera Behaviors"
authors: ["Hongda Jiang", "Bin Wang", "Xi Wang", "Marc Christie", "Baoquan Chen"]
date: 2020-05-13T19:11:48+08:00
doi: "10.1145/3386569.3392427"

# Schedule page publish date (NOT publication's date).
spublishDate: 2020-05-13T19:11:48+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "ACM Transactions on Graphics (Proceedings of SIGGRAPH 2020)"
publication_short: ""

abstract: "Designing a camera motion controller that has the capacity to move a virtual camera automatically in relation with contents of a 3D animation, in a cinematographic and principled way, is a complex and challenging task. Many cinematographic rules exist, yet practice shows there are significant stylistic variations in how these can be applied. 
In this paper, we propose an example-driven camera controller which can extract camera behaviors from an example film clip and re-apply the extracted behaviors to a 3D animation, through learning from a collection of camera motions."

# Summary. An optional shortened abstract.
summary: "In this paper, we propose an example-driven camera controller which can extract camera behaviors from an example film clip and re-apply the extracted behaviors to a 3D animation, through learning from a collection of camera motions."

tags: [Camera control, Animation]
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
url_video: https://www.youtube.com/watch?v=QbphVbdiTTk

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "We propose the design of a camera motion controller which has the ability to automatically extract camera behaviors from different film clips (on the left) and re-apply these behaviors to a 3D animation (center). "
  focal_point: "Bottom"
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

### Demo
{{< youtube QbphVbdiTTk >}}

### Method
{{< figure src="overview.png" title="Our proposed framework for learning camera behaviors composed of a Cinematic Feature Estimator which extracts high-level features from movie clips, a Gating network which estimates the type of camera behavior from the high-level features, and a Prediction network which applies the estimated behavior on a 3D animation." numbered="true" lightbox="true">}}

{{< figure src="extractorPipeline.jpg" title="To estimate cinematic features from film clips, each frame should pass through the following steps: (i) extracting 2D skeletons with LCR-Net, (ii) pose association, filling missing joints and smoothing, and (iii) estimating features through a neural network."  numbered="true" lightbox="true">}}

{{< figure src="estimation_model.jpg" title="Learning stage of the Cinematic Feature Estimator. Input data is gathered over on a sliding window of $t_c=8$ frames to increase robustness during the learning and testing phases. The output data gathers cinematic features such as the camera pose estimation in Toric space and character features."  numbered="true" lightbox="true">}}

{{< figure src="gatingPipeline.jpg" title="Structure of our Mixture of Experts (MoE) training network. The network takes as input the result of the Cinematic Feature Estimator applied on reference clips and the 3D animation. It outputs a sequence of camera parameters for each frame of the animation that can be used to render the animation." numbered="true" lightbox="true">}}

{{< figure src="sideTrack.jpg" title="Side track with different main character. In side track mode, the camera will always look from one side of the main character no matter his/her facing orientation. Green arrow indicates the main character in each sequence." numbered="true" lightbox="true">}}

{{< figure src="a_relative_b_direct.jpg" title="Relative vs direct track with same main character. Relative track (top) puts more emphasis on the male character; while the feeling conveyed by direct track (bottom) is more objective. Green arrow indicates the main character in each sequence." numbered="true" lightbox="true">}}


{{< figure src="zombie_seq_overview.jpg" title="Snapshots taken from two distinct camera motions computed on the zombie sequence using two distinct sequences of input. The green arrow represents the main character. As viewed in the snapshots, there are changes in the main character throughout the sequence. This enables the designer, through selected clips, to emphasize one character over another at different moments." numbered="true" lightbox="true">}}

### Bibtex

TBD

### Acknowledgement

This work was supported in part by the National Key R&D Program of China (2018YFB1403900, 2019YFF0302902). We also thank Anthony Mirabile and Ludovic Burg from University Rennes, Inria, CNRS, IRISA and Di Zhang from AICFVE, Beijing Film Academy for their help in animation generation and rendering.