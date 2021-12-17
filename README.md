# CLIP Upscaler and Enhancer
Using OpenAI's CLIP to upscale and enhance images

[![GitHub Repo stars](https://img.shields.io/github/stars/tripplyons/clip-upscaler-and-enhancer?style=social)](https://github.com/tripplyons/clip-upscaler-and-enhancer)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tripplyons/clip-upscaler-and-enhancer/blob/main/clip-upscaler-and-enhancer.ipynb)

Based on [nshepperd's JAX CLIP Guided Diffusion v2.4](https://colab.research.google.com/drive/10YWuTxtBI7PS0xBJCLAUjhR5cB0UUXe-)

## Sample Results

<table>
<tr>
<th>
Viewport
</th>
<th>
Original Image (512x512)
</th>
<th>
Using This Repo (scaled to 1024x1024 in 45 minutes)
</th>
<th>
Using Waifu2x (scaled to 1024x1024 in a few seconds)
</th>
</tr>
<tr>
<td>
Full Image
</td>
<td>
<img width="512" src="img/original.png">
</td>
<td>
<img width="512" src="img/this-repo.png">
</td>
<td>
<img width="512" src="img/waifu2x.png">
</td>
</tr>
<tr>
<td>
Zoomed In
</td>
<td>
<img width="512" src="img/original-details.png">
</td>
<td>
<img width="512" src="img/this-repo-details.png">
</td>
<td>
<img width="512" src="img/waifu2x-details.png">
</td>
</tr>
</table>

## How it works

1. Start with any image.
2. Find CLIP's embeddings of the image.
3. Resize the image to the desired resolution and add some noise.
4. **Optimize the resized image for the original image's embeddings** (using nshepperd's JAX CLIP Guided Diffusion v2.4).
