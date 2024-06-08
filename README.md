Slightly modified llyasviel/Omost to upload to Runpod. For my use only.

apt update && 
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O /opt/miniconda-installer.sh && 
bash /opt/miniconda-installer.sh -b && 
source /root/miniconda3/bin/activate && 
conda init && 
git clone https://github.com/1some1body1/OmPod.git && 
cd OmPod &&
conda create -n omost python=3.10 &&
conda activate omost &&
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121 &&
pip install -r requirements.txt &&
python gradio_app.py
