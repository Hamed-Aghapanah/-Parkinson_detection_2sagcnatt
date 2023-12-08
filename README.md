<div align="center">
  <img src="https://github.com/Hamed-Aghapanah/2sagcnatt/blob/main/3.png" width="600"/>
  <div>&nbsp;</div>
  <div align="center">
    <b><font size="5">Hamed Aghapanah </font></b>
    <sup>
      <a href="https://HamedAghapanah.com">
        <i><font size="4">HOT</font></i>
      </a>
    </sup>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <b><font size="5">HamedAghapanah platform</font></b>
    <sup>
      <a href="https://HamedAghapanah.com">
        <i><font size="4">TRY IT OUT</font></i>
      </a>
    </sup>
  </div>


 
[![Documentation](https://readthedocs.org/projects/mmaction2/badge/?version=latest)](https://mmaction2.readthedocs.io/en/latest/)
[![actions](https://github.com/open-mmlab/mmaction2/workflows/build/badge.svg)](https://github.com/open-mmlab/mmaction2/actions)
[![codecov](https://codecov.io/gh/open-mmlab/mmaction2/branch/master/graph/badge.svg)](https://codecov.io/gh/open-mmlab/mmaction2)
[![PyPI](https://img.shields.io/pypi/v/mmaction2)](https://pypi.org/project/mmaction2/)
[![LICENSE](https://img.shields.io/github/license/open-mmlab/mmaction2.svg)](https://github.com/open-mmlab/mmaction2/blob/master/LICENSE)
[![Average time to resolve an issue](https://isitmaintained.com/badge/resolution/open-mmlab/mmaction2.svg)](https://github.com/open-mmlab/mmaction2/issues)
[![Percentage of issues still open](https://isitmaintained.com/badge/open/open-mmlab/mmaction2.svg)](https://github.com/open-mmlab/mmaction2/issues)

%[📘Documentation](https://mmaction2.readthedocs.io/en/latest/) |
#[🛠️Installation](https://mmaction2.readthedocs.io/en/latest/install.html) |
[👀Model Zoo](https://mmaction2.readthedocs.io/en/latest/modelzoo.html) |
[🆕Update News](https://mmaction2.readthedocs.io/en/latest/changelog.html) |
[🚀Ongoing Projects](https://github.com/open-mmlab/mmaction2/projects) |
[🤔Reporting Issues](https://github.com/open-mmlab/mmaction2/issues/new/choose)

</div>

English | [简体中文](/README_zh-CN.md)

## Introduction

MMAction2 is an open-source toolbox for video understanding based on PyTorch.
It is a part of the [HamedAghapanah](http://HamedAghapanah.org/) project.

The master branch works with **PyTorch 1.5+**.

<div align="center">
  <div style="float:left;margin-right:10px;">
  <img src="https://github.com/open-mmlab/mmaction2/raw/master/resources/mmaction2_overview.gif" width="380px"><br>
    <p style="font-size:1.5vw;">Action Recognition Results on Kinetics-400</p>
  </div>
  <div style="float:right;margin-right:0px;">
  <img src="https://github.com/Hamed-Aghapanah/2sagcnatt/blob/main/0.1/211_18_3_1_1_stand.txt.gif" width="380px"><br>
    <p style="font-size:1.5vw;">Skeleton-base Action Recognition Results on NTU-RGB+D-120</p>
  </div>
</div>
<div align="center">
  <img src="https://user-images.githubusercontent.com/30782254/155710881-bb26863e-fcb4-458e-b0c4-33cd79f96901.gif" width="580px"/><br>
    <p style="font-size:1.5vw;">Skeleton-based Spatio-Temporal Action Detection and Action Recognition Results on Kinetics-400</p>
</div>
<div align="center">
  <img src="https://github.com/open-mmlab/mmaction2/raw/master/resources/spatio-temporal-det.gif" width="800px"/><br>
    <p style="font-size:1.5vw;">Spatio-Temporal Action Detection Results on AVA-2.1</p>
</div>

## Major Features

- **Modular design**: We decompose a video understanding framework into different components. One can easily construct a customized video understanding framework by combining different modules.

- **Support four major video understanding tasks**: MMAction2 implements various algorithms for multiple video understanding tasks, including action recognition, action localization, spatio-temporal action detection, and skeleton-based action detection. We support **27** different algorithms and **20** different datasets for the four major tasks.

- **Well tested and documented**: We provide detailed documentation and API reference, as well as unit tests.
 
## Installation

MMAction2 depends on [PyTorch](https://pytorch.org/), [MMCV](https://github.com/open-mmlab/mmcv), [MMDetection](https://github.com/open-mmlab/mmdetection) (optional), and [MMPose](https://github.com/open-mmlab/mmdetection)(optional).
Below are quick steps for installation.
Please refer to [install.md](docs/install.md) for more detailed instruction.

```shell
conda create -n open-mmlab python=3.8 pytorch=1.10 cudatoolkit=11.3 torchvision -c pytorch -y
conda activate open-mmlab
pip3 install openmim
mim install mmcv-full
mim install mmdet  # optional
mim install mmpose  # optional
git clone https://github.com/open-mmlab/mmaction2.git
cd mmaction2
pip3 install -e .
```

## Get Started

Please see [getting_started.md](docs/getting_started.md) for the basic usage of MMAction2.
There are also tutorials:

- [learn about configs](docs/tutorials/1_config.md)
- [finetuning models](docs/tutorials/2_finetune.md)
- [adding new dataset](docs/tutorials/3_new_dataset.md)
- [designing data pipeline](docs/tutorials/4_data_pipeline.md)
- [adding new modules](docs/tutorials/5_new_modules.md)
- [exporting model to onnx](docs/tutorials/6_export_model.md)
- [customizing runtime settings](docs/tutorials/7_customize_runtime.md)

A Colab tutorial is also provided. You may preview the notebook [here](demo/mmaction2_tutorial.ipynb) or directly [run](https://colab.research.google.com/github/open-mmlab/mmaction2/blob/master/demo/mmaction2_tutorial.ipynb) on Colab.
 
## Supported Datasets

<table style="margin-left:auto;margin-right:auto;font-size:1.3vw;padding:3px 5px;text-align:center;vertical-align:center;">
  <tr>
    <td colspan="4" style="font-weight:bold;">Action Recognition</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/hmdb51/README.md">HMDB51</a> (<a href="https://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/">Homepage</a>) (ICCV'2011)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/ucf101/README.md">UCF101</a> (<a href="https://www.crcv.ucf.edu/research/data-sets/ucf101/">Homepage</a>) (CRCV-IR-12-01)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/activitynet/README.md">ActivityNet</a> (<a href="http://activity-net.org/">Homepage</a>) (CVPR'2015)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/kinetics/README.md">Kinetics-[400/600/700]</a> (<a href="https://deepmind.com/research/open-source/kinetics/">Homepage</a>) (CVPR'2017)</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/sthv1/README.md">SthV1</a> (<a href="https://20bn.com/datasets/something-something/v1/">Homepage</a>) (ICCV'2017)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/sthv2/README.md">SthV2</a> (<a href="https://20bn.com/datasets/something-something/">Homepage</a>) (ICCV'2017)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/diving48/README.md">Diving48</a> (<a href="http://www.svcl.ucsd.edu/projects/resound/dataset.html">Homepage</a>) (ECCV'2018)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/jester/README.md">Jester</a> (<a href="https://20bn.com/datasets/jester/v1">Homepage</a>) (ICCV'2019)</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/mit/README.md">Moments in Time</a> (<a href="http://moments.csail.mit.edu/">Homepage</a>) (TPAMI'2019)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/mmit/README.md">Multi-Moments in Time</a> (<a href="http://moments.csail.mit.edu/challenge_iccv_2019.html">Homepage</a>) (ArXiv'2019)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/hvu/README.md">HVU</a> (<a href="https://github.com/holistic-video-understanding/HVU-Dataset">Homepage</a>) (ECCV'2020)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/omnisource/README.md">OmniSource</a> (<a href="https://kennymckormick.github.io/omnisource/">Homepage</a>) (ECCV'2020)</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/gym/README.md">FineGYM</a> (<a href="https://sdolivia.github.io/FineGym/">Homepage</a>) (CVPR'2020)</td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td colspan="4" style="font-weight:bold;">Action Localization</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/thumos14/README.md">THUMOS14</a> (<a href="https://www.crcv.ucf.edu/THUMOS14/download.html">Homepage</a>) (THUMOS Challenge 2014)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/activitynet/README.md">ActivityNet</a> (<a href="http://activity-net.org/">Homepage</a>) (CVPR'2015)</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td colspan="4" style="font-weight:bold;">Spatio-Temporal Action Detection</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/ucf101_24/README.md">UCF101-24*</a> (<a href="http://www.thumos.info/download.html">Homepage</a>) (CRCV-IR-12-01)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/jhmdb/README.md">JHMDB*</a> (<a href="http://jhmdb.is.tue.mpg.de/">Homepage</a>) (ICCV'2015)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/ava/README.md">AVA</a> (<a href="https://research.google.com/ava/index.html">Homepage</a>) (CVPR'2018)</td>
    <td></td>
  </tr>
  <tr>
    <td colspan="4" style="font-weight:bold;">Skeleton-based Action Recognition</td>
  </tr>
  <tr>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/skeleton/README.md">PoseC3D-FineGYM</a> (<a href="https://kennymckormick.github.io/posec3d/">Homepage</a>) (ArXiv'2021)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/skeleton/README.md">PoseC3D-NTURGB+D</a> (<a href="https://kennymckormick.github.io/posec3d/">Homepage</a>) (ArXiv'2021)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/skeleton/README.md">PoseC3D-UCF101</a> (<a href="https://kennymckormick.github.io/posec3d/">Homepage</a>) (ArXiv'2021)</td>
    <td><a href="https://github.com/open-mmlab/mmaction2/blob/master/tools/data/skeleton/README.md">PoseC3D-HMDB51</a> (<a href="https://kennymckormick.github.io/posec3d/">Homepage</a>) (ArXiv'2021)</td>
  </tr>
</table>

Datasets marked with * are not fully supported yet, but related dataset preparation steps are provided. A summary can be found on the [**Supported Datasets**](https://mmaction2.readthedocs.io/en/latest/supported_datasets.html) page.

## Benchmark

To demonstrate the efficacy and efficiency of our framework, we compare MMAction2 with some other popular frameworks and official releases in terms of speed. Details can be found in [benchmark](docs/benchmark.md).

## Data Preparation

Please refer to [data_preparation.md](docs/data_preparation.md) for a general knowledge of data preparation.
The supported datasets are listed in [supported_datasets.md](docs/supported_datasets.md)

## FAQ

Please refer to [FAQ](docs/faq.md) for frequently asked questions.

## Projects built on MMAction2

Currently, there are many research works and projects built on MMAction2 by users from community, such as:

- Video Swin Transformer. [\[paper\]](https://arxiv.org/abs/2106.13230)[\[github\]](https://github.com/SwinTransformer/Video-Swin-Transformer)
- Evidential Deep Learning for Open Set Action Recognition, ICCV 2021 **Oral**. [\[paper\]](https://arxiv.org/abs/2107.10161)[\[github\]](https://github.com/Cogito2012/DEAR)
- Rethinking Self-supervised Correspondence Learning: A Video Frame-level Similarity Perspective, ICCV 2021 **Oral**. [\[paper\]](https://arxiv.org/abs/2103.17263)[\[github\]](https://github.com/xvjiarui/VFS)

etc., check [projects.md](docs/projects.md) to see all related projects.

## Contributing

We appreciate all contributions to improve MMAction2. Please refer to [CONTRIBUTING.md](https://github.com/open-mmlab/mmcv/blob/master/CONTRIBUTING.md) in MMCV for more details about the contributing guideline.

## Acknowledgement

MMAction2 is an open-source project that is contributed by researchers and engineers from various colleges and companies.
We appreciate all the contributors who implement their methods or add new features and users who give valuable feedback.
We wish that the toolbox and benchmark could serve the growing research community by providing a flexible toolkit to reimplement existing methods and develop their new models.

## Citation

If you find this project useful in your research, please consider cite:

```BibTeX
@misc{  paper sss
}
```

## License

This project is released under the [Apache 2.0 license](LICENSE).
 
