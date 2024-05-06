# Full Body Fix for ComfyUI Nodes Based on Yoloworld

### Very important, must read.

- Recommended large model: [majic V7](https://www.liblib.art/modelinfo/bced6d7ec1460ac7b923fc5bc95c4540)

- Recommended vae: [Realistic difConsistency Negative (Pack)](https://www.liblib.art/modelinfo/232ff495f7c14381910dc6f4df78a7ab)

- lora: [YFilter_PortraitEnhance recommended](https://www.liblib.art/modelinfo/ec6239d3fcdc46beb8aefbd587e291b7)

- Recommended HD repair node, use this zoom node if you want the image to be more realistic, even including pore details. [Link](https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx)

My node uses Yoloworld to recognize objects, not just redraw faces and hair, you can combine them at will.

1. If the whole head is recognized when identifying hair, please adjust the parameter of the first item in Yoloworld ESAM.

2. After all, it is automation, please do not have too much hope, I can only try to copy manual operation, post-PS is inevitable.

# Sample Images:

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/597c0558-4aea-41a3-a10f-07b26975df2d" width="800" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/3e9c774c-bc6f-4ed2-b70a-c02423bed245" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/cf0814ee-863e-498a-b9ec-7d6a03f2eaad" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8cbd0b6e-64a3-4bdf-a228-b502bfbcb16e" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8183c713-5456-42ce-9d6b-c848a1328e30" width="400" alt="Image Description">

# Update Log

### Version number v1.0.7
- Added: Shortcut switch to directly shut down unwanted node groups.
- Fix: Change the parameters, the character will turn black, but the details are much more, I don't know why.

### Version number v1.0.6
- Known problem: Arm cannot be identified correctly. The thigh cannot be correctly identified.
- Repair: The previous node could not effectively detect the neck, resulting in neck fault. The scene of the neck can be met by cutting each other between masks, and all 30 images in the test can be used normally.
- Fix: the previous node is not valid for clothes, may detect pants and the like, through the mask cutting to meet the detection of clothes only scenario, the test 30 pictures can be used normally.
- Fix: Change keywords and Settings to make pants more accurate.
- Abandoned: The high and low frequency node is officially abandoned.

### Version No. v1.0.6
- Known issues: Arms cannot be recognized correctly. Thighs can not be recognized correctly.
- Repair: the previous node can not effectively detect the neck, resulting in neck fault, through the mutual crop between the mask can meet the neck of the scene, test 30 pictures can be used normally.
- Fix: The previous node can't detect clothes effectively, it may detect pants and so on, through the mask crop to meet the scene of only detecting clothes, test 30 pictures can be used normally.
- Fix: Change the keywords and settings, pants recognition is more accurate.
- Abandonment: The high and low frequency nodes are officially abandoned.

### Version v1.0.5
- Fix: Appears to have fixed the issue of faces turning black.
- Fix: It seems that high and low frequency modules are not necessary, thus images can be obtained in one step.
- Bug: I was wrong, should not use component transmission, it degrades image quality.

### Version v1.0.4
- Known Issue: As the amplitude and facial details of the repaint increase, the face darkens.
- Fix: The third node connection was incorrect.
- New: Added a node type for images to avoid the need to restart the demonstration due to errors in subsequent steps.
- New: Multiple-person judgement: False for multiple people, True for a single person.
- New: High and low frequency facial repair node. If you're too lazy to adjust over-sharpened parameters, put two images in PS and use a mask to erase.

### Version v1.0.2
- Fix bug: Image transmission is not done in sequence, but all at once.

### Version v1.0.1
- Changed facial parameters to make the face less like a fake face.

Author Pages:  
[liblib](https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image)  
[civitai](https://civitai.com/user/1637083533489)  

Please adhere to the open source license, redistribution is allowed, but please credit the author and commercial sales are prohibited.
