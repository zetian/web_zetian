---
layout: publication
category: publications

authors: "Zetian Zhang, Raghvendra V. Cowlagi"
title: "Incremental Path Repair in Hierarchical Motion-Planning with Dynamical Feasibility Guarantees for Mobile Robotic Vehicles"
conference: "Control Conference (ECC), 2015 European. IEEE, 2015"
file: 2015-ecc-zhang-cowlagi-o.pdf
---

<a href="../2015-ecc-zhang-cowlagi-o.pdf"><i class="fa fa-file-pdf-o"></i> (paper)</a><br />

### Authors

Raghvendra V. Cowlagi, Zetian Zhang

### Abstract

New requirements of autonomous mobile vehicles necessitate hierarchical motion-planning techniques that not only find a plan to satisfy high-level specifications, but also guarantee that this plan is suitable for execution under vehicle dynamical constraints. In this context, the H-cost motion-planning technique has been reported in the recent literature. We propose an incremental motion-planning algorithm based on this technique. The proposed algorithm retains the benefits of the original technique, and also significantly reduces the associated computational cost. In particular, the proposed iterative algorithm presents during intermediate iterations feasible motion-planning solutions, with the guarantee that the algorithm eventually converges to an optimal solution. Furthermore, the costs of solutions at intermediate iterations are nonincreasing except, possibly, at a finite number of special iterations. Therefore, the proposed algorithm is suitable for real-time implementations, where hard bounds on the available computation time may be imposed, and where the original H-cost optimization algorithm may not have sufficient time to converge to any solution at all. We illustrate the proposed algorithm with numerical simulation examples.

### Bibtex

{% highlight html %}{% raw %}

@inproceedings{zhang2015incremental,
  title={Incremental path repair in hierarchical motion-planning with dynamical feasibility guarantees for mobile robotic vehicles},
  author={Zhang, Zetian and Cowlagi, Raghvendra V},
  booktitle={Control Conference (ECC), 2015 European},
  pages={2366--2371},
  year={2015},
  organization={IEEE}
}{% endraw %}
{% endhighlight %}