conda create -n sam3 python=3.12
conda deactivate
conda activate sam3

pip install torch==2.10.0 torchvision --index-url https://download.pytorch.org/whl/cu128

git clone https://github.com/facebookresearch/sam3.git
cd sam3
pip install -e .

# For running example notebooks
pip install -e ".[notebooks]"

# For development
pip install -e ".[train,dev]"