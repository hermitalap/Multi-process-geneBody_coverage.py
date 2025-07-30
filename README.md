# 多进程 geneBody_coverage.py for RSeQC

## 英文版 (English)

### Introduction

This repository contains a modified version of the `geneBody_coverage.py` script from RSeQC, with added support for multiprocessing. RSeQC is a toolkit for quality control of RNA-seq data, and the original script is used to plot gene body coverage to assess the uniformity of read coverage across genes. This version enhances performance by utilizing multiple CPU cores through Python's `concurrent.futures.ProcessPoolExecutor` module, making it particularly suitable for processing large BAM files, while achieving faster processing times.

### License

This project is licensed under the **GNU General Public License version 3 (GPLv3)**, in compliance with the original RSeQC package. For the full license text, see the [LICENSE](LICENSE) file.

### Attribution

This work is based on the original RSeQC package developed by Liguo Wang, Shengqin Wang, and Wei Li. The original RSeQC package can be found at [RSeQC Official Website](https://rseqc.sourceforge.net/).

### Modifications

The primary modification in this version is the addition of multiprocessing support using Python's `concurrent.futures.ProcessPoolExecutor` module. This allows the script to process multiple genes or regions in parallel, significantly reducing the processing time for large datasets. The number of processes can be specified using the `-p` or `--processes` option.

### Usage

Run the script using the following command:

```bash
genebody_coverage.py -p 32 -i input.bam -r RedSeq.bed -o output_geneBody_coverage
```

#### Options

- `-p, --processes`: Number of processes to use (default: 32)
- Other options remain the same as in the original RSeQC script. For details on other options, please refer to the [RSeQC Documentation](https://rseqc.sourceforge.net/#gene-body-coverage).


## 中文版

### 介绍

本存储库包含 RSeQC 的 `geneBody_coverage.py` 脚本的修改版本，增加了多进程支持。RSeQC 是一个用于 RNA-seq 数据质量控制的工具包，原始脚本用于绘制基因体覆盖图，以评估读数在基因上的覆盖均匀性。本版本通过利用 Python 的 `concurrent.futures.ProcessPoolExecutor` 模块进行多核 CPU 并行处理，显著提高了处理大型 BAM 文件的效率。

### 许可证

本项目采用 **GNU 通用公共许可证第 3 版（GPLv3）** 进行许可，符合原始 RSeQC 包的要求。有关许可证的完整文本，请参见 [LICENSE](LICENSE) 文件。

### 归属

本工作基于由 Liguo Wang、Shengqin Wang 和 Wei Li 开发的原始 RSeQC 包。原始 RSeQC 包可在 [RSeQC 官方网站](https://rseqc.sourceforge.net/) 找到。

### 修改内容

本版本的主要修改是使用 Python 的 `concurrent.futures.ProcessPoolExecutor` 模块添加了多进程支持。这允许脚本同时处理多个基因或区域，显著减少大型数据集的处理时间。用户可以通过 `-p` 或 `--processes` 选项指定进程数。

### 使用方法

使用以下命令运行脚本：

```bash
genebody_coverage.py -p 32 -i input.bam -r RedSeq.bed -o output_geneBody_coverage
```

#### 选项

- `-p, --processes`：使用的进程数（默认：32）
- 其他选项与原始 RSeQC 脚本相同。有关原始选项的详细信息，请参阅 [RSeQC 文档](https://rseqc.sourceforge.net/#gene-body-coverage)。

