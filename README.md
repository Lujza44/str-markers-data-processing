# STR markers data processing

This repository contains the code for my bachelor's thesis on the processing and visualization of STR markers population data. The repository includes SQL, Python and Shell scripts for downloading a necessary VCF file, transforming the data format, and visualizing the results.

## Installation

To run the scripts, you need to clone this GitHub repository. Note that the original data is not included in this repository due to privacy concerns.

```bash
git clone https://github.com/Lujza44/str-markers-data-processing.git
cd str-markers-data-processing
```

### Dependencies

To run the scripts, you need the following dependencies:

- Python 3: Ensure Python 3 is installed. You can download it from [python.org](https://www.python.org/).
- Python packages: Install the required Python packages by running:

```shell
pip install -r requirements.txt
```

- Command-line tools: You need to have the following tools installed:
  - wget: For downloading files from the internet.
  - gzip: For decompressing .gz files. 
  - tabix: For compressing and indexing VCF files.
  - bcftools: For processing VCF files.

  You can install these tools on Ubuntu using:

```shell
sudo apt-get update
sudo apt-get install -y wget gzip tabix bcftools
```

## Usage

### Downloading the VCF file

Before transforming and visualizing the data, you need to download the VCF file containing the rs numbers. This can be done by running the `get_vcf.sh` script:

```bash
./code/get_vcf.sh
```

### Transforming the Data

To transform the data format, you can run the `transform_data.sh` script, which executes four Python scripts in the necessary order:

```bash
./code/transform_data.sh
```

### Visualizing the Data

For data visualization, you can run the `visualize.sh` script, which executes three Python scripts in the necessary order:

```bash
./code/visualize.sh
```

These scripts also handle the deletion of any existing output files before running the Python scripts.

## Output Files

The output files generated by the scripts are stored in the `data/output` directory. The files include:
- `transformed_data.json` - The transformed data in JSON format.
- `Tables.xlsx` - The tables in XLSX format.