# Awesome Large Model (LM) System [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

This paper collects papers, repos, tools for large model system, including training, inference, serving and compression.

- [Awesome Large Model (LM) System ](#awesome-large-model-lm-system-)
  - [Papers](#papers)
    - [Training](#training)
    - [Inference](#inference)
    - [Benchmark](#benchmark)
    - [Survey](#survey)
  - [Frameworks](#frameworks)

## Papers

### Training

| Year |  Publisher   | Title                                                                                                                                                                                       |         Framework         |
|:----:|:------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------:|
| 2023 |              | [Understanding INT4 Quantization for Transformer Models: Latency Speedup, Composability, and Failure Cases](https://arxiv.org/abs/2301.12017)                                               |     [DeepSpeed](#ds)      |
| 2023 |     ICLR     | [DySR: Adaptive Super-Resolution via Algorithm and System Co-design](https://openreview.net/forum?id%253DPgtn4l6eKjv)                                                                       |     [DeepSpeed](#ds)      |
| 2023 |              | [Scaling Vision-Language Models with Sparse Mixture of Experts](https://arxiv.org/abs/2303.07226)                                                                                           |     [DeepSpeed](#ds)      |
| 2023 |    IPDPS     | [MCR-DL: Mix-and-Match Communication Runtime for Deep Learning](https://arxiv.org/abs/2303.08374)                                                                                           |     [DeepSpeed](#ds)      |
| 2023 |     ICS      | [A Hybrid Tensor-Expert-Data Parallelism Approach to Optimize Mixture-of-Experts Training](https://arxiv.org/abs/2303.06318)                                                                |     [DeepSpeed](#ds)      |
| 2023 |     OSDI     | [AlpaServe: Statistical Multiplexing with Model Parallelism for Deep Learning Serving](https://arxiv.org/abs/2302.11665)                                                                    |       [Alpa](#alpa)       |
| 2023 |    MLSys     | [On Optimizing the Communication of Model Parallelism](https://arxiv.org/abs/2211.05322)                                                                                                    |       [Alpa](#alpa)       |
| 2023 |              | [Colossal-Auto: Unified Automation of Parallelization and Activation Checkpoint for Large-scale Models](https://arxiv.org/abs/2302.02599)                                                   | [ColossalAI](#colossalai) |
| 2022 |     HiPC     | [1-bit LAMB: Communication Efficient Large-Scale Large-Batch Training with LAMB's Convergence Speed](https://ieeexplore.ieee.org/document/10106313)                                         |     [DeepSpeed](#ds)      |
| 2022 |   NeurIPS    | [The Stability-Efficiency Dilemma: Investigating Sequence Length Warmup for Training GPT Models](https://openreview.net/forum?id%253DJpZ5du_Kdh)                                            |     [DeepSpeed](#ds)      |
| 2022 |              | [Maximizing Communication Efficiency for Large-scale Training via 0/1 Adam](https://arxiv.org/abs/2202.06009)                                                                               |     [DeepSpeed](#ds)      |
| 2022 |     ICML     | [DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://proceedings.mlr.press/v162/rajbhandari22a.html)                              |     [DeepSpeed](#ds)      |
| 2022 |              | [Using DeepSpeed and Megatron to Train Megatron-Turing NLG 530B, A Large-Scale Generative Language Model](https://arxiv.org/abs/2201.11990)                                                 |     [DeepSpeed](#ds)      |
| 2022 |   NeuraIPS   | [Extreme Compression for Pre-trained Transformers Made Simple and Efficient](https://openreview.net/forum?id%253DxNeAhc2CNAl)                                                               |     [DeepSpeed](#ds)      |
| 2022 |   NeuraIPS   | [ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers](https://openreview.net/forum?id%253Df-fVCElZ-G1)                                              |     [DeepSpeed](#ds)      |
| 2022 |              | [Random-LTD: Random and Layerwise Token Dropping Brings Efficient Training for Large-scale Transformers](https://arxiv.org/abs/2211.11586)                                                  |     [DeepSpeed](#ds)      |
| 2022 |              | [DeepSpeed Data Efficiency: Improving Deep Learning Model Quality and Training Efficiency via Efficient Data Sampling and Routing](https://arxiv.org/abs/2212.03597)                        |     [DeepSpeed](#ds)      |
| 2022 |     OSDI     | [Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://www.usenix.org/conference/osdi22/presentation/zheng-lianmin)                                 |       [Alpa](#alpa)       |
| 2022 |     ICPP     | [Tesseract: Parallelize the Tensor Parallelism Efficiently](https://dl.acm.org/doi/abs/10.1145/3545008.3545087)                                                                             | [ColossalAI](#colossalai) |
| 2022 |              | [A Frequency-aware Software Cache for Large Recommendation System Embeddings](https://arxiv.org/abs/2208.05321)                                                                             | [ColossalAI](#colossalai) |
| 2022 |     TPDS     | [Parallel Training of Pre-Trained Models via Chunk-Based Dynamic Memory Management](https://www.computer.org/csdl/journal/td/2023/01/09940581/1I6O79tPnwc)                                  | [ColossalAI](#colossalai) |
| 2021 |      SC      | [ZeRO-Infinity: Breaking the GPU Memory Wall for Extreme Scale Deep Learning](https://dl.acm.org/doi/abs/10.1145/3458817.3476205)                                                           |     [DeepSpeed](#ds)      |
| 2021 |     ICML     | [1-bit Adam: Communication Efficient Large-Scale Training with Adam's Convergence Speed](http://proceedings.mlr.press/v139/tang21a.html)                                                    |     [DeepSpeed](#ds)      |
| 2021 |     ATC      | [ZeRO-Offload: Democratizing Billion-Scale Model Training.](https://www.usenix.org/conference/atc21/presentation/ren-jie)                                                                   |     [DeepSpeed](#ds)      |
| 2021 |    PPoPP     | [DAPPLE: a pipelined data parallel approach for training large models](https://dl.acm.org/doi/10.1145/3437801.3441593)                                                                      |                           |
| 2021 |     ICML     | [TeraPipe: Token-Level Pipeline Parallelism for Training Large](https://icml.cc/virtual/2021/poster/9181)                                                                                   |   [TeraPipe](#terapipe)   |
| 2021 |     ICML     | [Memory-Efficient Pipeline-Parallel DNN Training](https://icml.cc/virtual/2021/spotlight/10458)                                                                                             |  [PipeDream](#pipedream)  |
| 2021 |              | [An Efficient 2D Method for Training Super-Large Deep Learning Models](https://arxiv.org/abs/2104.05343)                                                                                    | [ColossalAI](#colossalai) |
| 2021 |              | [Maximizing Parallelism in Distributed Training for Huge Neural Networks](https://arxiv.org/abs/2105.14450)                                                                                 | [ColossalAI](#colossalai) |
| 2021 |              | [Sequence Parallelism: Long Sequence Training from System Perspective](https://arxiv.org/abs/2105.13120)                                                                                    | [ColossalAI](#colossalai) |
| 2021 |              | [Colossal-AI: A Unified Deep Learning System For Large-Scale Parallel Training](https://arxiv.org/abs/2110.14883)                                                                           | [ColossalAI](#colossalai) |
| 2020 | KDD Tutorial | [DeepSpeed: System Optimizations Enable Training Deep Learning Models with Over 100 Billion Parameters.](https://dl.acm.org/doi/10.1145/3394486.3406703)                                    |     [DeepSpeed](#ds)      |
| 2020 |      SC      | [ZeRO: memory optimizations toward training trillion parameter models.](https://dl.acm.org/doi/10.5555/3433701.3433727)                                                                     |     [DeepSpeed](#ds)      |
| 2020 |   NeuraIPS   | [Accelerating Training of Transformer-Based Language Models with Progressive Layer Dropping](https://proceedings.neurips.cc/paper/2020/hash/a1140a3d0df1c81e24ae954d935e8926-Abstract.html) |     [DeepSpeed](#ds)      |
| 2020 |              | [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053)                                                                   | [Megatron-LM](#megatron)  |
| 2020 |              | [torchgpipe: On-the-fly Pipeline Parallelism for Training Giant Models](https://arxiv.org/abs/2004.09910)                                                                                   |   [TorchGpipe](#gpipe)    |
| 2019 |   NeuraIPS   | [GPipe: efficient training of giant neural networks using pipeline parallelism](https://papers.nips.cc/paper_files/paper/2019/hash/093f65e080a295f8076b1c5722a46aa2-Abstract.html)          |   [TorchGpipe](#gpipe)    |
| 2019 |     SOSP     | [PipeDream: Generalized pipeline parallelism for DNN training](https://dl.acm.org/doi/10.1145/3341301.3359646 )                                                                             |  [PipeDream](#pipedream)  |





### Inference

| Year | Publisher | Title                                                                                                                                                          |       Framework       |
|:----:|:---------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------:|
| 2023 |           | [EnergonAI: An Inference System for 10-100 Billion Parameter Transformer Models](https://arxiv.org/abs/2209.02341)                                             | [EnergonAI](#energon) |
| 2022 |   ICML    | [DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://proceedings.mlr.press/v162/rajbhandari22a.html) |   [DeepSpeed](#ds)    |
| 2022 |    SC     | [DeepSpeed Inference: Enabling Efficient Inference of Transformer Models at Unprecedented Scale](https://dl.acm.org/doi/abs/10.5555/3571885.3571946)           |   [DeepSpeed](#ds)    |


### Benchmark

| Year  | Publisher | Title  | Framework |
| :---: | :-------: | :----- | :-------: |
| Year  |    Pub    | Title  | Framework |
| Year  |    Pub    | Title1 | Framework |

### Survey

| Year  | Publisher | Title  | Framework |
| :---: | :-------: | :----- | :-------: |
| Year  |    Pub    | Title  | Framework |
| Year  |    Pub    | Title1 | Framework |


## Frameworks

| Year |                                                Name                                                 | Training | Inference | Serving | Comments                                                                                |
|:----:|:---------------------------------------------------------------------------------------------------:|:---------|:---------:|:-------:|:----------------------------------------------------------------------------------------|
| 2023 |            <span id="energon"></span>[EnergonAI](https://github.com/hpcaitech/EnergonAI)            | ✗        |     ✔     |    ✗    |                                                                                         |
| 2022 |                <span id="alpa"></span>[Alpa](https://github.com/alpa-projects/alpa)                 | ✔        |     ✔     |    ✔    | Compilation based mixed parallelism                                                     |
| 2021 | <span id="megatron-ds"></span>[Megatron-DeepSpeed](https://github.com/microsoft/Megatron-DeepSpeed) | ✔        |     ✗     |    ✗    | Add  MoE model training, Curriculum Learning, 3D Parallelism from DeepSpeed to Megatron |
| 2021 |            <span id="terapipe"></span>[TeraPipe](https://github.com/zhuohan123/terapipe)            | ✔        |     ✗     |    ✗    |                                                                                         |
| 2021 |         <span id="colossalai"></span>[ColossalAI](https://github.com/hpcaitech/ColossalAI)          | ✔        |     ✔     |    ✔    |                                                                                         |
| 2021 |        <span id="ft"></span>[FasterTransformer](https://github.com/NVIDIA/FasterTransformer)        | ✗        |     ✔     |    ✗    |                                                                                         |
| 2020 |              <span id="ds"></span>[DeepSpeed](https://github.com/microsoft/DeepSpeed)               | ✔        |     ✔     |    ✗    | General Support of Transformers and MoE with 3d-parallelism                             |
| 2019 |           <span id="megatron"></span>[Megatron-LM](https://github.com/NVIDIA/Megatron-LM)           | ✔        |     ✗     |    ✗    |                                                                                         |
| 2019 |          <span id="pipedream"></span>[PipeDream](https://github.com/msr-fiddle/pipedream)           | ✔        |     ✗     |    ✗    |                                                                                         |
| 2019 |            <span id="gpipe"></span>[TorchGipe](https://github.com/kakaobrain/torchgpipe)            | ✔        |     ✗     |    ✗    | The `torchgipe` has been merged to PyTorch in 2020.                                     |
| 2019 |          <span id="pipedream"></span>[PipeDream](https://github.com/msr-fiddle/pipedream)           | ✔        |     ✗     |    ✗    |                                                                                         |
