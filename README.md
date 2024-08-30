# Cosmological Generative Model Evaluation Suite

This repository provides tools for evaluating generative models in cosmology, focusing on generating and analyzing images using various statistical measures. The provided scripts allow you to generate pixel intensity histograms, power spectra, and Minkowski functionals from real and generated sample images.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Scripts Overview](#scripts-overview)
- [Acknowledgments](#acknowledgments)
- [Contributing](#contributing)
- [License](#license)

## Installation

To install the required packages and set up your environment, use Conda with the provided `environment.yml` file:

```bash
conda env create -f environment.yml
conda activate cosmo_eval_env
```

## Usage
### Command-Line Interface
The main script allows you to generate pixel intensity histograms, power spectra, and Minkowski functionals from sample images.

python evalstats.py --real_samples <path_to_real_samples> \
                    --gen_samples <path_to_generated_samples> \
                    --num_samples <number_of_samples> \
                    --save_path <output_directory> \
                    --pixel_min <minimum_pixel_value> \
                    --pixel_max <maximum_pixel_value>


### Parameters
- real_samples: Directory containing the real sample images.
- gen_samples: Directory containing the generated sample images.
- num_samples: Number of samples to process from each directory (default: 100).
- save_path: Directory where the output images and statistics will be saved.
- pixel_min: Minimum pixel intensity value for histogram and Minkowski functionals.
- pixel_max: Maximum pixel intensity value for histogram and Minkowski functionals.

## Scripts Overview
evalstats.py: Main script for generating statistics and visualizations of sample images.
Functions:
- gen_samplelist(): Generates a list of real and generated samples.
- get_pixel_histogram_for_samples(): Computes and plots pixel intensity histograms.
- plot_ps_samples(): Plots power spectra for the samples.
- get_powspec_for_samples(): Calculates the power spectrum for a list of samples.
- calc_1dps_img2d(): Calculates 1D power spectra from 2D images.
- plot_mink_functionals(): Plots Minkowski functionals for the samples.
- generate_PIH(): Wrapper function for generating pixel intensity histograms.
- generate_ps(): Wrapper function for generating power spectra.
- mink_funcs(): Wrapper function for generating Minkowski functionals.


## Acknowledgments
This repository is a separate evaluation codebase derived from the excellent work done in the [diffusion-models-astrophysical-fields-mlps repository](https://github.com/nmudur/diffusion-models-astrophysical-fields-mlps)

I would like to express my gratitude to the original authors for their contributions to this area of research and for making their code available. The evaluation scripts in this repository are heavily based on their work, and I recommend checking out their repository for more comprehensive implementations and insights.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue for discussion.

## Licence
This project is licensed under the MIT License.

