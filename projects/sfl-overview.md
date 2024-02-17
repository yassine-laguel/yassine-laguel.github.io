---
author_profile: true
redirect_from:
  - /sfl-overview
  - /sfl-overview.html
---

Federated Learning with Superquantile Aggregation for Heterogeneous Data
=========================================================================

<div style="text-align: center">
    <table align=center>
        <tr>
            <h4 style="font-weight:normal, text-align: center">
                <a href="https://krishnap25.github.io">Krishna Pillutla</a><sup>1*</sup>,
                <a href="https://yassine-laguel.github.io/">Yassine Laguel</a><sup>2*</sup>,
                <a href="https://membres-ljk.imag.fr/Jerome.Malick/cv.html">Jérôme Malick</a><sup>3</sup>,
                <a href="http://faculty.washington.edu/zaid/">Zaid Harchaoui</a><sup>4</sup>
            </h4>
        </tr>
        <tr>
              <h5 style="font-weight:normal">
                <sup>1</sup>Google Research,
                <sup>2</sup>Université Côte d’Azur,
                <sup>3</sup>CNRS,
                <sup>4</sup>University of Washington, <br>
                <sup>*</sup>Equal Contribution
              </h5>
        </tr>
        <tr>
              <h4 style="font-weight:normal">
                Machine Learning Journal (2023). <br>
                Preliminary versions in IEEE CISS 2021 and
                DistShift-NeurIPS 2022 (Spotlight).
              </h4>
        </tr>
        <tr>
              <h4 style="font-weight:normal">
                <a href="https://link.springer.com/article/10.1007/s10994-023-06332-x">
                  [Paper]
                </a>  &nbsp;
                <a href="https://arxiv.org/pdf/2112.09429.pdf">
                  [ArXiv]
                </a>  &nbsp;
                <a href="https://github.com/krishnap25/sqwash">
                  [Software]
                </a>  &nbsp;
                <a href="https://github.com/krishnap25/simplicial-fl">
                  [Code]
                </a>  &nbsp;
              </h4>
        </tr>
    </table>
</div>


<img src="/images/sfl-illustration.png" alt="alternate text" width="900" style="display: block; margin: 0 auto;">

We present a federated learning framework that is designed to robustly deliver good predictive performance across individual clients with heterogeneous data. The proposed approach hinges upon a superquantile/CVaR learning objective that captures the tail statistics of the error distribution over heterogeneous clients. We present a stochastic training algorithm that interleaves differentially private client filtering with federated averaging steps. We prove finite time convergence guarantees for the in the nonconvex case in T communication rounds and the strongly convex case. Experimental results on benchmark datasets for federated learning demonstrate that our approach is competitive with classical ones in terms of average error and outperforms them in terms of tail statistics of the error.

Empirical Results
------------------

We show results on the EMNIST dataset:

(a) the left plot shows the misclassification errors
(b) the right plot shows the mean and 90th percentile error of our approach compared to baselines.

These results show that our approach has a much better performance on the tail while being competitive on the average performance.

<img src="/images/sfl-results1.png" alt="alternate text" width="700" style="display: block; margin: 0 auto;">

The next plot shows that this conclusion is true across a wide range of differential privacy parameters.

<img src="/images/sfl-results2.png" alt="alternate text" width="700" style="display: block; margin: 0 auto;">

References
------------
[1] Pillutla, K., Laguel, Y., Malick J. and Harchaoui, Z., 2023.
**Federated learning with superquantile aggregation for heterogeneous data**. Machine Learning, pp.1-68.

[2] Laguel, Y., Pillutla, K., Malick J. and Harchaoui, Z., 2021.
**A Superquantile Approach to Federated Learning with Heterogeneous Devices**. In the 55th Annual Conference on Information Sciences and Systems (CISS) (pp. 1-6). IEEE.

Acknowledgments
----------------
This work has been partially supported by by NSF DMS 2023166, DMS 1839371, CCF 2019844, the CIFAR program "Learning in Machines and Brains", faculty research awards, a JP Morgan Ph.D. fellowship, and MIAI – Grenoble Alpes (ANR-19-P3IA-0003). The work was mainly performed while Krishna Pillutla was at the University of Washington, and Yassine Laguel was at the Université Grenoble Alpes.
