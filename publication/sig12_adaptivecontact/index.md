---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Adaptive Image-based Intersection Volume"
authors: [Bin Wang, François Faure, Dinesh K. Pai]
date: 2012-05-16T00:11:24+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-05-16T00:11:24+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "ACM Transactions on Graphics (Proceedings of SIGGRAPH 2012)"
publication_short: ""

abstract: "A method for image-based contact detection and modeling, with guaranteed precision on the intersection volume, is presented. Unlike previous image-based methods, our method optimizes a non-uniform ray sampling resolution and allows precise control of the volume error. By cumulatively projecting all mesh edges into a generalized 2D texture, we construct a novel data structure, the Error Bound Polynomial Image (EBPI), which allows efficient computation of the maximum volume error as a function of ray density. Based on a precision criterion, EBPI pixels are subdivided or clustered. The rays are then cast in the projection direction according to the non-uniform resolution. The EBPI data, combined with ray-surface intersection points and normals, is also used to detect transient edges at surface intersections. This allows us to model intersection volumes at arbitrary resolution, while avoiding the geometric computation of mesh intersections. Moreover, the ray casting acceleration data structures can be reused for the generation of high quality images."

# Summary. An optional shortened abstract.
summary: "The accuracy of intersection volume is important for plausible collision response. In this paper we have presented the first imagebased collision detection method that provides the controllability of intersection volume without explicit geometrical computation, and demonstrated its relevance for precise contact modeling. Its computation combines rasterization at moderate resolution with adaptive ray casting, which allows more precise contact modeling where needed and a reduced memory footprint"

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
url_video: "https://www.youtube.com/watch?v=qRqJmX-bAoA"

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
