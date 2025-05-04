# Wasserstein Normalized AutoEncoder (WNAE)

## Installation

```bash
git clone git@github.com:fleble/wnae.git
```
The needed packages and versions can be found in `requirements.txt`.    

If you want to run the example in `example`, you will need more packages, refer to the documentation of the [SVJanalysis repo](https://github.com/eth-svj/SVJanalysis).    


## Usage

This repo provides:
* the WNAE implementation
* an example data loader
* an example encoder / decoder architecture
* an example training loop

The file `run_training.py` can be used to run trainings and shows how the different pieces talk to each other.    
Execute as:
```bash
cd example/
source setup_svj.sh  # need to be filled in with the path to the SVJanalysis repo
python run_training.py <output_path>
python make_plots.py <output_path>
```
where `<output_path>` must be replaced by the path where the output of the training will be written.

## To run on a cluster:
To test with a pod:
* Use the pod `nrp/wnae_pod.yaml` to make the pod 
* In the pod: `git clone https://github.com/ellisonscheuller/wnae_.git`
* `pip install -r requirements.txt`
* Then do testing as needed

To run the job:
`nrp/wnae_job.yaml`
