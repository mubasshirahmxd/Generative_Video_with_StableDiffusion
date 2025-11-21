# 🎥✨ Generative Video with Stable Diffusion

Create AI-Generated Videos from Text Prompts Using HuggingFace Diffusers

<p align="center">
  <img src="https://img.shields.io/badge/StableDiffusion-Text2Video-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/HuggingFace-Diffusers-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Colab-Ready-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-Video%20Generation-purple?style=for-the-badge" />
</p>

---

# 🚀 Project Overview

This project demonstrates **Text-to-Video Generation** using **Stable Diffusion (Zeroscope)** via the **HuggingFace Diffusers** library.
You simply provide a text prompt and the system generates a full **AI-generated video sequence** along with individual frames.

Perfect for:

✔️ AI content creation
✔️ Motion design experiments
✔️ Stable diffusion learning
✔️ Multimodal generative AI workflows

---

# 📁 Folder Structure

```
03_Generative_Video_with_StableDiffusion/
├─ notebooks/
│   └─ 01_StableDiffusion_text2video.ipynb
└─ output/
    ├─ output_frames/
    │   ├─ frame_000.png
    │   ├─ frame_001.png
    │   ├─ ...
    │   └─ frame_035.png
    └─ Sample_output.mp4
```

---

# 🧠 Model Used

### **📌 Zeroscope v2 — Text-to-Video Stable Diffusion Model**

HuggingFace Model:
`cerspense/zeroscope_v2_576w`

---

# 🔥 Features

- 🎞️ Generate videos from **any text prompt**
- 🖼️ Save every generated **frame**
- 🎬 Export video as `.mp4`
- ⚡ GPU optimized
- 🧪 Clean notebook
- 🧩 Customizable

---


## ⚙️ Installation

### 1. Install Dependencies

Ensure you have a GPU-enabled environment (local or Google Colab).

```
pip install git+[https://github.com/huggingface/diffusers.git](https://github.com/huggingface/diffusers.git)
pip install transformers accelerate torch imageio
```

### 2. Authentication

You need a Hugging Face Access Token to download the model weights.

**Option A: Via Python Script**

```
from huggingface_hub import login
login(token="YOUR_HF_TOKEN")
```

**Option B: Environment Variable**

```
export HUGGINGFACE_TOKEN="hf_xxxxx"
```

---

🧪 Example Prompts

Try these prompts inside the notebook to generate different styles of video:

| **Style**     | **Prompt**                                                      |
| ------------------- | --------------------------------------------------------------------- |
| **Playful**   | `A cat playing with a red ball in a sunny garden`                   |
| **Cyberpunk** | `Futuristic neon-lit Tokyo street with flying cars, cinematic shot` |
| **Humorous**  | `A robot cooking biryani in a kitchen, humorous style`              |
| **Sci-Fi**    | `An astronaut walking on Mars during sunset, ultra-realistic`       |
| **Nature**    | `Beautiful waterfall flowing in slow motion, 4K nature shot`        |

---

## 🧩 How It Works (Pipeline Flow)

1. **Load Model:** The script initializes the `cerspense/zeroscope_v2_576w` pipeline.
2. **Inference:** You pass a text prompt.
3. **Generation:** The model produces a tensor of 36 (or more) frames.
4. **Post-Processing:** Frames are extracted and saved as PNGs.
5. **Encoding:** `imageio` stitches the frames into a standard `.mp4` file.

---

## 💡 Future Enhancements

* [ ] Add audio generation for full video creation.
* [ ] Build a Streamlit UI for easier interaction.
* [ ] Add camera-motion effects (pan, zoom).
* [ ] Extend to long-video generation.
* [ ] Integrate with ControlNet for precise style control.

---

## ⭐ Author

**Mubasshir Ahmed** *Full Stack Data Science — Generative AI | LangChain | Diffusers*

💛 **If you found this repository helpful, please give it a ⭐ Star!**
