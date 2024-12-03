n# DLCV Final Project ( Multiple Concept Personalization )

# How to run your code?
* TODO: Please provide the scripts for TAs to reproduce your results, including training and inference. For example, 

```shell script=
bash train.sh <Path to gt image folder> <Path to annot file>
bash inference.sh <Path to gt image folder> <Path to annot file> <Path to output image folder>
```

# Usage
To start working on this final project, you should clone this repository into your local machine by the following command:

    git clone https://github.com/DLCV-Fall-2024/DLCV-Fall-2024-Final-2-<team name>.git
  
Note that you should replace `<team_name>` with your own team name.

For more details, please click [this link](https://docs.google.com/presentation/d/1eeXx_dL0OgkDn9_lhXnimTHrE6OYvAiiVOBwo2CTVOQ/edit?usp=sharing) to view the slides of Final Project - Multiple Concept Personalization. **The introduction video for final project can be accessed in the slides.**

# Submission Rules
### Deadline
113/12/26 (Thur.) 23:59 (GMT+8)
    
# Q&A
If you have any problems related to Final Project, you may
- Use TA hours
- Contact TAs by e-mail ([ntudlcv@gmail.com](mailto:ntudlcv@gmail.com))
- Post your question under `[Final challenge 2] Discussion` section in NTU Cool Discussion

# Environment Setup
This work should be completed using Python 3.8.5. Create a environment under conda
```bash
conda create -n dlcv_final python=3.8.5 -y
conda activate dlcv_final
```
Install the environment with pip and requirements.txt, note that the version of pytorch should match your CUDA version.
```bash 
pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install -r requirements.txt
cd stable-diffusion
pip install -e .
```
Get the dataset with
```bash
bash get_dataset.sh
```
To install the stable-diffusion v1.4. You can download the sd-v1-4.ckpt file from hugging face link or use wget
```bash
wget https://huggingface.co/CompVis/stable-diffusion-v-1-4-original/resolve/main/sd-v1-4.ckpt
```
place the model checkpoint in the following path:
```
stable-diffusion/models/ldm/stable-diffusion-v1/model.ckpt
```
or just simply input
```bash
cd stable-diffusion
mkdir -p ldm/models/stable-diffusion-v1/
mv sd-v1-4.ckpt ldm/models/stable-diffusion-v1/model.ckpt
```

