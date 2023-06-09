# DataprocessingProject

## Description
This pipeline was developed using Snakemake, a workflow management system that helps to create reproducible and scalable data analyses. The pipeline is designed to perform SNP calling from genotyping-by-sequencing data.

## Requirements
To run this pipeline, you'll need to have the following software installed:

- Snakemake 7.30.1
- R 4.3
- Conda 23.5.0 **or the following tools**
- Samtools 1.17
- cutadpt 4.4
- bwa 0.7.17
- bcftools 1.17

# Usage

To run the entire pipeline, navigate to the Dataprocessing folder and execute **(requires all tools)**:  
`snakemake --cores [NUMBER_OF_CORES]`

Alternatively, the pipeline can manage the required tools for you if you have conda installed. Simply run the following command:  
`snakemake --cores [NUMBER_OF_CORES] --use-conda`


## Preperation
The pipeline requires you to have your input .fastq(.gz) files, referencegenome.fasta and GeneralFeatureFormat.gff in directories set in the configuration file config/parameters.yaml. It contains the parameters used by the pipeline. Edit this file to customize the pipeline's behavior.


# Workflow
The workflow of the pipeline is described in the workflow/Snakefile. Each rule specifies a task and its dependencies. The rules are connected to each other as seen in the DAG.png, where each node represents a rule and each edge represents a dependency.

## Output File
The output file generated by the pipeline is located in the results/ directory. The file is a visualisation of the information obtained from the vcf file generaated by the pipeline.

# License
This pipeline is distributed under the MIT license. See the LICENSE file for details.

# Author
Made by Jorick Baron for any questios please contact me at j.baron@st.hanze.nl
