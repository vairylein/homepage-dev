---
layout: post

author: Peter Flach

title: "Precision-Recall-Gain Curves: PR Analysis Done Right"
tldr: Don't use Precision-Recall curves -- use PRG curves instead! Selected for spotlight presentation at NIPS'15, has clocked up around 100 citations on Google Scholar in 4.5 years, comes with code (Python/R/Matlab), video, poster and slides.
paper-authors: Peter A. Flach and Meelis Kull

hero-image: http://people.cs.bris.ac.uk/~flach/PRGcurves/curves.jpg

venue: NIPS 2015
venue-url: http://papers.nips.cc/paper/5867-precision-recall-gain-curves-pr-analysis-done-right

scholar: https://scholar.google.com/citations?user=o9ggd4sAAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3Do9ggd4sAAAAJ%26cstart%3D20%26pagesize%3D80%26citation_for_view%3Do9ggd4sAAAAJ%3ARc-B-9qnGaUC%26tzom%3D-60

manuscript: https://research-information.bris.ac.uk/ws/portalfiles/portal/72164009/5867_precision_recall_gain_curves_pr_analysis_done_right.pdf
supplement: http://people.cs.bris.ac.uk/~flach/PRGcurves/PRcurves_supplementary.pdf

slides: http://people.cs.bris.ac.uk/~flach/PRGcurves/PRcurves_ISL.pdf
poster: http://people.cs.bris.ac.uk/~flach/PRGcurves/2015_12_07_nips_prg_poster.pdf
video: http://people.cs.bris.ac.uk/~flach/PRGcurves/259653_clipped.mp4
code: https://github.com/meeliskull/prg

theme: ROC
tags: Fscore Precision-Recall

categories:
  - ROC/Fscore Precision-Recall
---

Precision-Recall analysis abounds in applications of binary classification where true negatives do not add value and hence should not affect assessment of the classifier's performance. Perhaps inspired by the many advantages of receiver operating characteristic (ROC) curves and the area under such curves for accuracy-based performance assessment, many researchers have taken to report Precision-Recall (PR) curves and associated areas as performance metric. We demonstrate in this paper that this practice is fraught with difficulties, mainly because of incoherent scale assumptions -- e.g., the area under a PR curve takes the arithmetic mean of precision values whereas the $F_{\beta}$ score applies the harmonic mean. We show how to fix this by plotting PR curves in a different coordinate system, and demonstrate that the new Precision-Recall-Gain curves inherit all key advantages of ROC curves. In particular, the area under Precision-Recall-Gain curves conveys an expected $F_1$ score on a harmonic scale, and the convex hull of a Precision-Recall-Gain curve allows us to calibrate the classifier's scores so as to determine, for each operating point on the convex hull, the interval of $\beta$ values for which the point optimises $F_{\beta}$. We demonstrate experimentally that the area under traditional PR curves can easily favour models with lower expected $F_1$ score than others, and so the use of Precision-Recall-Gain curves will result in better model selection.
