# Comfy_workflows

## IP adapter face

```bash
git clone https://github.com/cubiq/ComfyUI_IPAdapter_plus ./ComfyUI/custom_nodes/ComfyUI_IPAdapter_plus

# clipvison vit-h encoder
wget -P ComfyUI/models/clip_vision/ https://huggingface.co/h94/IP-Adapter/resolve/main/models/image_encoder/model.safetensors

# create folder for ipadapter if not exist
mkdir ComfyUI/models/ipadapter

# sdxl plus face
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter/resolve/main/sdxl_models/ip-adapter-plus-face_sdxl_vit-h.safetensors

# sd1.5 plus face
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter/resolve/main/models/ip-adapter-plus-face_sd15.safetensors

# sd1.5 full face
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter/resolve/main/models/ip-adapter-full-face_sd15.safetensors

# sdXL ipa vit-h
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter/resolve/main/sdxl_models/ip-adapter_sdxl_vit-h.safetensors

# sd ipa vit-h
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter/resolve/main/models/ip-adapter-plus_sd15.safetensors

# ----- faceID ----

# sd1.5 faceid plus v2
wget -p ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter-FaceID/resolve/main/ip-adapter-faceid-plusv2_sd15.bin
wget -P ComfyUI/models/loras/ https://huggingface.co/h94/IP-Adapter-FaceID/resolve/main/ip-adapter-faceid-plusv2_sd15_lora.safetensors

# sdxl faceid plus v2
wget -P ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter-FaceID/resolve/main/ip-adapter-faceid-plusv2_sdxl.bin
wget -P ComfyUI/models/loras/ https://huggingface.co/h94/IP-Adapter-FaceID/resolve/main/ip-adapter-faceid-plusv2_sdxl_lora.safetensors


# sd1.5 portrait
wget -P ComfyUI/models/ipadapter https://huggingface.co/h94/IP-Adapter-FaceID/resolve/main/ip-adapter-faceid-portrait_sd15.bin


# insightface
apt-get update
apt-get install -y build-essential
pip install onnxruntime onnxruntime-gpu insightface

pip install insightface



# SAM
git clone https://github.com/storyicon/comfyui_segment_anything ./ComfyUI/custom_nodes/comfyui_segment_anything
mkdir ComfyUI/models/grounding-dino
wget -P ComfyUI/models/grounding-dino https://huggingface.co/ShilongLiu/GroundingDINO/resolve/main/groundingdino_swinb_cogcoor.pth
wget -P ComfyUI/models/grounding-dino https://huggingface.co/ShilongLiu/GroundingDINO/resolve/main/GroundingDINO_SwinB.cfg.py
mkdir ComfyUI/models/sams
wget -P ComfyUI/models/sams https://huggingface.co/lkeab/hq-sam/resolve/main/sam_hq_vit_h.pth



# UPSCALE
git clone https://github.com/ssitu/ComfyUI_UltimateSDUpscale --recursive ./ComfyUI/custom_nodes/ComfyUI_UltimateSDUpscale
apt update && apt install git-lfs
git lfs install
git clone https://huggingface.co/lllyasviel/control_v11f1e_sd15_tile ComfyUI/models/controlnet/control_v11f1e_sd15_tile
wget -P ComfyUI/models/upscale_models https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth

```
