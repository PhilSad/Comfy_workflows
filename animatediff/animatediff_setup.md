```bash
cd ComfyUI
git pull
# Custom nodes
git clone https://github.com/Kosinkadink/ComfyUI-Advanced-ControlNet custom_nodes/ComfyUI-Advanced-ControlNet
git clone https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite custom_nodes/ComfyUI-VideoHelperSuite
git clone https://github.com/Fannovel16/comfyui_controlnet_aux custom_nodes/comfyui_controlnet_aux
git clone https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved custom_nodes/ComfyUI-AnimateDiff-Evolved
pip install -r custom_nodes/ComfyUI-VideoHelperSuite/requirements.txt
pip install -r custom_nodes/comfyui_controlnet_aux/requirements.txt
pip install -r custom_nodes/ComfyUI-AnimateDiff-Evolved/requirements.txt

apt update && apt install -y ffmpeg

# models
wget https://huggingface.co/lllyasviel/control_v11p_sd15_inpaint/resolve/main/config.json -P models/controlnet
wget https://huggingface.co/lllyasviel/control_v11p_sd15_inpaint/resolve/main/diffusion_pytorch_model.fp16.safetensors -P models/controlnet


wget https://huggingface.co/guoyww/animatediff/resolve/cd71ae134a27ec6008b968d6419952b0c0494cf2/v3_sd15_mm.ckpt -P custom_nodes/ComfyUI-AnimateDiff-Evolved/models
