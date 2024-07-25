# Better Call SAL: Towards Learning to Segment Anything in Lidar

Accepted to European Conference on Computer Vision (ECCV), 2024

[Project page](https://research.nvidia.com/labs/dvl/projects/sal/)

Code coming soon!

Authors: [Aljosa Osep](https://aljosaosep.github.io/)* [Tim Meinhardt](https://research.nvidia.com/labs/dvl/author/tim-meinhardt/)* [Francesco Ferroni](https://www.francescoferroni.com/),[Neehar Peri](https://www.neeharperi.com/), [Deva Ramanan](https://www.cs.cmu.edu/~deva/) and [Laura Leal-Taixe](https://research.nvidia.com/labs/dvl/author/laura-leal-taixe/) (* Equal Contribution) 



**Summary:** Our SAL (Segment Anything in Lidar) method consists of a text-promptable zero-shot model for segmenting and classifying any object in Lidar, and a pseudo-labeling engine that facilitates model training without manual supervision. Our pseudo-labels consist of instance masks and corresponding CLIP tokens, which we lift to Lidar using calibrated multi-modal data. By training our model on these labels, we distill the 2D foundation models into our Lidar SAL model. Even without manual labels, our model achieves 91% in terms of class-agnostic segmentation and 44% in terms of zero-shot LPS of the fully supervised state-of-the-art. Moreover, we show that SAL supports arbitrary class prompts, can be easily extended to new datasets, and shows significant potential to improve with increasing amounts of self-labeled data.

![Screenshot 2024-07-25 at 5 06 05 PM](https://github.com/user-attachments/assets/6c325d47-c48e-42be-bd1f-ad2ceb1b4481)
**Segment Anything in Lidar (SAL):** The SAL model performs class-agnostic instance segmentation (i) and zero-shot classification via text prompting. This allows us to not only predict semantic/panoptic segmentation (ii) for fixed class vocabularies but segment any object (iii and iv) in a given Lidar scan.


![Screenshot 2024-07-25 at 5 06 17 PM](https://github.com/user-attachments/assets/cd4a5e3d-9e19-4a67-8334-67757de93df7)
**SAL overview:** Given a Lidar scan and a class vocabulary prompt, specified as a list of per-class free-form text descriptions (left), SAL segments and classifies objects (thing and stuff classes). As labeled data for training such a model does not exist, we supervise SAL by distilling off-the-shelf vision foundation models to Lidar (right).

