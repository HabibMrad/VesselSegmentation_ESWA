# Retinal vessel segmentation based on Fully Convolutional Neural Networks

This repository contains materials supporting the paper: Oliveira, Américo, et al., "Retinal vessel segmentation based on Fully Convolutional Neural Networks", Expert Systems with Applications, Volume 112, 1 December 2018, Pages 229-242. <br />

([Google Scholar](https://scholar.google.com/citations?user=shL_8g0AAAAJ&hl=en#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DshL_8g0AAAAJ%26citation_for_view%3DshL_8g0AAAAJ%3A9yKSN-GCB0IC%26tzom%3D0) | [Journal version](https://doi.org/10.1016/j.eswa.2018.06.034) | [ArXiv preprint version](https://arxiv.org/abs/1812.07110))

## Abstract

The retinal vascular condition is a reliable biomarker of several ophthalmologic and cardiovascular diseases, so automatic vessel segmentation may be crucial to diagnose and monitor them. In this paper, we propose a novel method that combines the multiscale analysis provided by the Stationary Wavelet Transform (SWT) with a multiscale Fully Convolutional Neural Network (FCN) to cope with the varying width and direction of the vessel structure in the retina. Our proposal uses rotation operations as the basis of a joint strategy for both data augmentation and prediction, which allows us to explore the information learned during training to refine the segmentation. The method was evaluated on three publicly available databases, achieving an average accuracy of 0.9576, 0.9694, and 0.9653, and average area under the ROC curve of 0.9821, 0.9905, and 0.9855 on the DRIVE, STARE, and CHASE_DB1 databases, respectively. It also appears to be robust to the training set and to the inter-rater variability, which shows its potential for real-world applications.

## Overview

![Pipeline](https://github.com/americofmoliveira/VesselSegmentation_ESWA/blob/master/resources/architecture/1a.png)

![Architecture](https://github.com/americofmoliveira/VesselSegmentation_ESWA/blob/master/resources/architecture/1b.png)

## Results

The proposed method was evaluated in three databases: [DRIVE](https://www.isi.uu.nl/Research/Databases/DRIVE/), [STARE](http://cecas.clemson.edu/~ahoover/stare/), and [CHASE_DB1](https://blogs.kingston.ac.uk/retinal/chasedb1/). Below you can find a brief comparison between our method and other state of the art works. For a more detailed analysis, please refer to the manuscript.

<p align="center">

<table class="tg">
  <tr>
    <th class="tg-lm6i" col width="220" rowspan="2"><br>Method </th>
    <th class="tg-lm6i" colspan="4">DRIVE</th>
  </tr>
  <tr>
    <td class="tg-lm6i"><div align="center">Sn</td>
    <td class="tg-lm6i"><div align="center">Sp</td>
    <td class="tg-lm6i"><div align="center">Acc</td>
    <td class="tg-lm6i"><div align="center">AUC</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Soares et al. [1]</td>
    <td class="tg-akyt">.7332</td>
    <td class="tg-akyt">.9782</td>
    <td class="tg-akyt">.9466</td>
    <td class="tg-akyt">.9614</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Fraz et al. [2]</td>
    <td class="tg-akyt">.7406</td>
    <td class="tg-akyt">.9807</td>
    <td class="tg-akyt">.9480</td>
    <td class="tg-akyt">.9747</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Roychowdhury et al. [3]</td>
    <td class="tg-akyt">.7249</td>
    <td class="tg-qpkk"><b>.9830</b></td>
    <td class="tg-akyt">.9519</td>
    <td class="tg-akyt">.9620</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Li et al. [4]</td>
    <td class="tg-akyt">.7569</td>
    <td class="tg-akyt">.9816</td>
    <td class="tg-akyt">.9527</td>
    <td class="tg-akyt">.9738</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Liskowski and Krawiec [5]</td>
    <td class="tg-akyt">.7520</td>
    <td class="tg-akyt">.9806</td>
    <td class="tg-akyt">.9515</td>
    <td class="tg-akyt">.9710</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">This work</td>
    <td class="tg-qpkk"><b>.8039</td>
    <td class="tg-akyt">.9804</td>
    <td class="tg-qpkk"><b>.9576</td>
    <td class="tg-qpkk"><b>.9821</td>
  </tr>
</table>


<table class="tg">
  <tr>
    <th class="tg-lm6i" col width="220" rowspan="2"><br>Method </th>
    <th class="tg-lm6i" colspan="4">STARE</th>
  </tr>
  <tr>
    <td class="tg-lm6i"><div align="center">Sn</td>
    <td class="tg-lm6i"><div align="center">Sp</td>
    <td class="tg-lm6i"><div align="center">Acc</td>
    <td class="tg-lm6i"><div align="center">AUC</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Soares et al. [1]</td>
    <td class="tg-akyt">.7207</td>
    <td class="tg-akyt">.9747</td>
    <td class="tg-akyt">.9480</td>
    <td class="tg-akyt">.9671</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Fraz et al. [2]</td>
    <td class="tg-akyt">.7548</td>
    <td class="tg-akyt">.9763</td>
    <td class="tg-akyt">.9534</td>
    <td class="tg-akyt">.9768</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Roychowdhury et al. [3]</td>
    <td class="tg-akyt">.7719</td>
    <td class="tg-qpkk">.9726</td>
    <td class="tg-akyt">.9515</td>
    <td class="tg-akyt">.9688</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Li et al. [4]</td>
    <td class="tg-akyt">.7726</td>
    <td class="tg-akyt">.9844</td>
    <td class="tg-akyt">.9628</td>
    <td class="tg-akyt">.9879</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Liskowski and Krawiec [5]</td>
    <td class="tg-akyt">.8145</td>
    <td class="tg-akyt"><b>.9866</td>
    <td class="tg-akyt"><b>.9696</td>
    <td class="tg-akyt">.9880</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">This work</td>
    <td class="tg-qpkk"><b>.8315</td>
    <td class="tg-akyt">.9858</td>
    <td class="tg-qpkk">.9694</td>
    <td class="tg-qpkk"><b>.9905</td>
  </tr>
</table>


<table class="tg">
  <tr>
    <th class="tg-lm6i" col width="220" rowspan="2"><br>Method </th>
    <th class="tg-lm6i" colspan="4">CHASE_DB1</th>
  </tr>
  <tr>
    <td class="tg-lm6i"><div align="center">Sn</td>
    <td class="tg-lm6i"><div align="center">Sp</td>
    <td class="tg-lm6i"><div align="center">Acc</td>
    <td class="tg-lm6i"><div align="center">AUC</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Fraz et al. [2]</td>
    <td class="tg-akyt">.7224</td>
    <td class="tg-akyt">.9711</td>
    <td class="tg-akyt">.9469</td>
    <td class="tg-akyt">.9712</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Roychowdhury et al. [3]    </td>
    <td class="tg-akyt">.7201</td>
    <td class="tg-akyt">.9824</td>
    <td class="tg-akyt">.9530</td>
    <td class="tg-akyt">.9532</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Li et al. [4]</td>
    <td class="tg-akyt">.7507</td>
    <td class="tg-qpkk">.9793</td>
    <td class="tg-akyt">.9581</td>
    <td class="tg-akyt">.9716</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">Zhang et al. [6]</td>
    <td class="tg-akyt">.7644</td>
    <td class="tg-akyt">.9716</td>
    <td class="tg-akyt">.9502</td>
    <td class="tg-akyt">.9706</td>
  </tr>
  <tr>
    <td class="tg-7x02"><div align="left">This work</td>
    <td class="tg-qpkk"><b>.7779</td>
    <td class="tg-akyt"><b>.9864</td>
    <td class="tg-qpkk"><b>.9653</td>
    <td class="tg-qpkk"><b>.9855</td>
  </tr>
</table>
</p>


## Contents

The materials in this repository are organized as follows:

- `code`: Code required to test our model, including calibration files -- files containing the statistical parameters (mean and standard deviation) to perform standardization on each dataset.

- `folds_constitution`: Since there is no explicit division between training and test sets for the STARE and CHASE_DB1 databases, we used *5*-fold and *4*-fold cross-validation, respectively, to evaluate the results in these cases. Here we show the constitution of the folds, so that future works can replicate our evaluation conditions.

- `image_level_results`: Evaluation metrics for each image in terms of Sensitivity, Specificity, Accuracy, Area under the ROC curve (AUC), and Matthews correlation coefficient (MCC). For STARE, in particular, we also provide the performance of our model in the set of pathological images.

- `resources`: Mask, probability map outputted by the model, and final binary segmentation for each image. 

- `statistical_comparison`: Statistical comparison between our method and other state-of-the-art works that have made their segmentations publicly available.

- `supplementary_materials`: Quotable document summarizing the metrics obtained by image and dataset.

## Citation

If you find this work useful, please, cite our paper:

Oliveira, A. F. M., Pereira, S. R. M., & Silva, C. A. B. (2018). Retinal Vessel Segmentation based on Fully Convolutional Neural Networks. Expert Systems with Applications.

## Contact

For information related with the paper, please feel free to contact me (americofmoliveira@gmail.com) or Prof. Carlos A. Silva (csilva@dei.uminho.pt).

## Bibliography

[1] Soares, J. V., Leandro, J. J., Cesar, R. M., Jelinek, H. F., & Cree, M. J. (2006). Retinal vessel segmentation using the 2-D Gabor wavelet and supervised classification. IEEE Transactions on medical Imaging, 25(9), 1214-1222.

[2] Fraz, M. M., Remagnino, P., Hoppe, A., Uyyanonvara, B., Rudnicka, A. R., Owen, C. G., & Barman, S. A. (2012). An ensemble classification-based approach applied to retinal blood vessel segmentation. IEEE Transactions on Biomedical Engineering, 59(9), 2538-2548.

[3] Roychowdhury, S., Koozekanani, D. D., & Parhi, K. K. (2015). Blood vessel segmentation of fundus images by major vessel extraction and subimage classification. IEEE journal of biomedical and health informatics, 19(3), 1118-1128.

[4] Li, Q., Feng, B., Xie, L., Liang, P., Zhang, H., & Wang, T. (2016). A Cross-Modality Learning Approach for Vessel Segmentation in Retinal Images. IEEE Trans. Med. Imaging, 35(1), 109-118.

[5] Liskowski, P., & Krawiec, K. (2016). Segmenting retinal blood vessels with deep neural networks. IEEE transactions on medical imaging, 35(11), 2369-2380.

[6] Zhang, J., Chen, Y., Bekkers, E., Wang, M., Dashtbozorg, B., & ter Haar Romeny, B. M. (2017). Retinal vessel delineation using a brain-inspired wavelet transform and random forest. Pattern Recognition, 69, 107-123.
