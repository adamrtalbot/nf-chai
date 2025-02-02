# nf-chai

[![GitHub Actions CI Status](https://github.com/seqeralabs/nf-chai/actions/workflows/ci.yml/badge.svg)](https://github.com/seqeralabs/nf-chai/actions/workflows/ci.yml)
[![GitHub Actions Linting Status](https://github.com/seqeralabs/nf-chai/actions/workflows/linting.yml/badge.svg)](https://github.com/seqeralabs/nf-chai/actions/workflows/linting.yml)
[![nf-test](https://img.shields.io/badge/unit_tests-nf--test-337ab7.svg)](https://www.nf-test.com)

[![Nextflow](https://img.shields.io/badge/nextflow%20DSL2-%E2%89%A524.04.2-23aa62.svg)](https://www.nextflow.io/)
[![run with docker](https://img.shields.io/badge/run%20with-docker-0db7ed?labelColor=000000&logo=docker)](https://www.docker.com/)
[![run with singularity](https://img.shields.io/badge/run%20with-singularity-1d355c.svg?labelColor=000000)](https://sylabs.io/docs/)
[![Launch on Seqera Platform](https://img.shields.io/badge/Launch%20%F0%9F%9A%80-Seqera%20Platform-%234256e7)](https://cloud.seqera.io/launch?pipeline=https://github.com/seqeralabs/nf-chai)

## Introduction

**nf-chai** is a bioinformatics pipeline for running the [Chai-1](https://github.com/chaidiscovery/chai-lab) protein prediction algorithm on an input set of protein sequences in FASTA format. The pipeline has been written in Nextflow to generate results for downstream analysis in a reproducible, scalable and portable way.

## Usage

> [!NOTE]
> If you are new to Nextflow, please refer to [this page](https://nf-co.re/docs/usage/installation) on how to set-up Nextflow. Make sure to [test your setup](https://nf-co.re/docs/usage/introduction#how-to-run-a-pipeline) with `-profile test` before running the workflow on actual data.

First, prepare a FASTA file with your protein sequence(s) that looks as follows:

`protein_sequences.fa`:

```txt
>protein|name=short-protein-example
AIQRTPKIQVYSRHPAENGKSNFLNCYVSGFHPS
```

Now, you can run the pipeline using:

```bash
nextflow run seqeralabs/nf-chai \
   -profile <docker/singularity> \
   --input protein_sequences.fa \
   --outdir <OUTDIR>
```

## Credits

seqeralabs/nf-chai was originally written by the Seqera Team.

We thank the following people for their extensive assistance in the development of this pipeline:

## Contributions and Support

If you would like to contribute to this pipeline, please see the [contributing guidelines](.github/CONTRIBUTING.md).

## Citations

An extensive list of references for the tools used by the pipeline can be found in the [`CITATIONS.md`](CITATIONS.md) file.

This pipeline uses code and infrastructure developed and maintained by the [nf-core](https://nf-co.re) community, reused here under the [MIT license](https://github.com/nf-core/tools/blob/main/LICENSE).

> **The nf-core framework for community-curated bioinformatics pipelines.**
>
> Philip Ewels, Alexander Peltzer, Sven Fillinger, Harshil Patel, Johannes Alneberg, Andreas Wilm, Maxime Ulysse Garcia, Paolo Di Tommaso & Sven Nahnsen.
>
> _Nat Biotechnol._ 2020 Feb 13. doi: [10.1038/s41587-020-0439-x](https://dx.doi.org/10.1038/s41587-020-0439-x).
