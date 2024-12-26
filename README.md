DLCV Final Project ( Multiple Concept Personalization )

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
conda create -n dlcv_final python=3.9.21 -y
conda activate dlcv_final
```
Install the environment with pip and requirements.txt, note that the version of pytorch should match your CUDA version.
```bash 
pip install -r requirements.txt
```
Get the dataset with
```bash
bash get_dataset.sh
```
# Training
We wrote the bash script that can train the concepts for the tasks, by simply run 
```bash
bash training_all.sh
```
The tuned parameters for the concept will be store in the specific folder assign in the .sh

# Inference
As our inference need a layout and the model need to know the specific trained embedding for the concept, we assign the json and the layout image for the prompt individualy
```bash 
bash inference_all.sh
```
When the inference information and the path to the layout image are written in the output(1~4).json