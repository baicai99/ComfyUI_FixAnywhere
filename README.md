# Full Body Fix for ComfyUI Nodes Based on Yoloworld

### Very important, please be sure to read.

- Recommended nodes are used for high-definition repairs. If you want more realistic images, even including pore details, please use this scale node. [Link here](https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx)

My node uses Yoloworld to recognize objects, not just to repaint faces and hair. You can combine them as needed.

1. If there are many people, turn on the nodes for multiple people; if there are many people, split the mask and repaint each character separately, otherwise repaint them all together.

2. If the whole head is recognized when identifying hair, adjust the first parameter in Yoloworld ESAM.

# Sample Images:

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/3e9c774c-bc6f-4ed2-b70a-c02423bed245" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/cf0814ee-863e-498a-b9ec-7d6a03f2eaad" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8cbd0b6e-64a3-4bdf-a228-b502bfbcb16e" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8183c713-5456-42ce-9d6b-c848a1328e30" width="400" alt="Image Description">

# Update Log

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
