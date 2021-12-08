# Instructions for Bias Neutralization

## Introduction

Claims from Snopes and PolitiFact were neutralized using a validated model published by <a href="https://arxiv.org/abs/1911.09709" title="Paper">Pryzant et al.</a> at Stanford in 2020. The Stanford model neutralizes subjective bias by single-word substitution in text. We applied the CONCURRENT variant of the Stanford model on claims only as it was validated only for single sentences. The original <a href="https://github.com/rpryzant/neutralizing-bias" title="Code">code</a> is incompatible with our claims data. We extensively modified the original code and wrote a custom interface to enable the model to process our data.


## Download this Repository
* This repository contains the required code

## Load Claims Data

* Download and extract the ZIP <a href="https://www.dropbox.com/s/3v5oy3eddg3506j/multi_fc_publicdata.zip?dl=0" title="file">file</a>
* Copy the Snopes claims as snes.tsv from /multi_fc_publicdata/snes to /data/hansen_data/snes
* Copy PolitiFact claims as pomt.tsv from /multi_fc_publicdata/pomt to /data/hansen_data/pomt

## Load Trained Model

* Download the <a href="https://bit.ly/bias-model" title="model">model</a> and rename to neutralization_model.ckpt
* Copy neutralization_model.ckpt to /model

## Running the Model
* Run the Jupyter notebook named ac295_project_neutralization.ipynb for each set of data.
* The neutralized claims data will be output to /data as ac295_snes_main_neutralized.tsv and ac295_pomt_main_neutralized.tsv
* Rename the files to snes.tsv and pomt.tsv respectively before use in the next step
* Each of the two files are formatted as direct substitutes for snes.tsv and pomt.tsv in the <a href="https://github.com/casperhansen/fake-news-reasoning" title="model">model</a> for <a href="https://arxiv.org/abs/2105.07698" title="paper">Automatic Fake News Detection</a>
# ac295_project
