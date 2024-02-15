 # batchImg-rembg 
[Rembg](https://github.com/danielgatis/rembg)(Remove background) of Plural Images for [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
</br></br>

<img src = 'https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/d3e05963-b047-4900-aa58-10f1e1b0980c' width="400" height="400"></img>
<img src = 'https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/bef5f8b4-3976-4c59-848f-7e77df6bd5a3' width="400" height="400"></img>


## Installation 

1. Clone to your `custom_nodes` folder in ComfyUI:

```
git clone https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes.git
```

2. Install `rembg[gpu]` (recommended) or `rembg`, depending on GPU support, to your ComfyUI virtual environment. E.g.:

```
pip install rembg[gpu]
pip install tqdm
```


### [batchImg-rembg](https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes) workflows will often make use of these helpful node packs:
---
</br>

- > [ComfyUI-AnimateDiff-Evolved](https://github.com/Kosinkadink/ComfyUI-AnimateDiff-Evolved) for img2vid.
- > [ComfyUI-VideoHelperSuite](https://github.com/Kosinkadink/ComfyUI-VideoHelperSuite) for loading videos, combining images into videos.
- > [comfyui_controlnet_aux](https://github.com/Fannovel16/comfy_controlnet_preprocessors) for preprocessing original images to depth, lineart, openpose images. 
</br>
    
## Workflow 
> for example,
<img src= 'https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/a516f83b-f149-45be-9dba-31c35c719f3b'>

</br>
</br>
</br>
<img src = 'https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/17966afa-0b8a-4774-95d0-2c57b3846694'>


### Optional Models(Choose according to your work, downloaded automatically)
---

All models are downloaded and saved in the user home folder in the `.u2net` directory.

The available models are:

<details open>
<summary>Rembg Model Name </summary>

  | Name            | Description                                                                  | Link |
  |--------|-------------------------------------------------------------------------------------|------------------------------------|
  | u2net(default) | A pre-trained model for general use cases.                                          | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/u2net.onnx), [source](https://github.com/xuebinqin/U-2-Net) |
  | u2netp | A lightweight version of u2net model.   | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/u2netp.onnx), [source](https://github.com/xuebinqin/U-2-Net)        |
  | u2net_human_seg |  A pre-trained model for human segmentation.   | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/u2net_human_seg.onnx), [source](https://github.com/xuebinqin/U-2-Net)        |
  | u2net_cloth_seg | A pre-trained model for Cloths Parsing from human portrait. Here clothes are parsed into 3 category: Upper body, Lower body and Full body.   | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/u2net_cloth_seg.onnx), [source](https://github.com/levindabhi/cloth-segmentation)        |
  | silueta | Same as u2net but the size is reduced to 43Mb.   | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/silueta.onnx), [source](https://github.com/xuebinqin/U-2-Net/issues/295)        |
  | isnet-general-use | A new pre-trained model for general use cases. |[download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/isnet-general-use.onnx), [source](https://github.com/xuebinqin/DIS)        |
  | isnet-anime | A high-accuracy segmentation for anime character.   | [download](https://github.com/danielgatis/rembg/releases/download/v0.0.0/isnet-anime.onnx), [source](https://github.com/SkyTNT/anime-segmentation)        |
  | sam(not recommended, not easy to use) | A pre-trained model for any use cases. | [download encoder](https://github.com/danielgatis/rembg/releases/download/v0.0.0/vit_b-encoder-quant.onnx), [download decoder](https://github.com/danielgatis/rembg/releases/download/v0.0.0/vit_b-decoder-quant.onnx), [source](https://github.com/facebookresearch/segment-anything)        |
</details>

</br>
</br>

## Example 
<table class="center">
    <tr style="line-height: 0">
    <td width=34% style="border: none; text-align: center">Original Image</td>
    <td width=33% style="border: none; text-align: center">LineArt before Rembg</td>
    <td width=33% style="border: none; text-align: center">LineArt after Rembg</td>
    </tr>
    <tr>
    <td width=34% style="border: none"><img src="https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/ef065506-e844-4b92-a282-d20198267f8e" style="width:100%"></td>
    <td width=33% style="border: none"><img src="https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/e4440bec-d6dd-4726-8200-c38facbd1130" style="width:100%"></td>
    <td width=33% style="border: none"><img src="https://github.com/Mamaaaamooooo/batchImg-rembg-ComfyUI-nodes/assets/135937372/0d828694-1440-464b-9c68-7f646b73886f" style="width:100%"></td>
    </tr>
</table>

</br>

## Acknowledgements

Thanks to [rembg-comfyui-node](https://github.com/Jcd1230/rembg-comfyui-node) for insight.</br>
Thanks to [rembg-comfyui-node-better](https://github.com/Loewen-Hob/rembg-comfyui-node-better/tree/main) for modifying repo.
