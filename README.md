# Full Body Fix for ComfyUI Nodes Based on Yoloworld

Q: Why do this?  
A: Because the midjourney-generated characters have a kind of oil painting texture, and they need to be fixed with sd every time. So I developed a workflow to fix them directly.

Q: Why isn't finger repair good?  
A: Because this process only focuses on realism, it doesn't handle making unreasonable things reasonable. In other words, it can't fix a distorted finger back to normal, it can only add blood vessels to the original hand.

- Recommended big model: [majic V7](https://www.liblib.art/modelinfo/bced6d7ec1460ac7b923fc5bc95c4540)

- Recommended Vae: [Realistic difConsistency Negative (Pack)](https://www.liblib.art/modelinfo/232ff495f7c14381910dc6f4df78a7ab)

- lora: [YFilter_PortraitEnhance recommended](https://www.liblib.art/modelinfo/ec6239d3fcdc46beb8aefbd587e291b7)

- Recommended high-definition repair node. If you want the image to be more realistic, even including pore details, please use this scaling node. [Link](https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx)

My nodes use G-DinoSAM to recognize objects, not just redraw faces and such. You can freely copy and paste, freely combine them.

1. If the whole head is recognized when identifying hair, please adjust the threshold parameters in G-DinoSAM.

2. After all, it's automation. Please don't expect too much. I can only try to replicate manual operations, and post-processing in Photoshop is unavoidable.

3. If there is anything that is not user-friendly or any suggestions, please leave a comment actively.

# Sample Images:

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/e8c35b5a-07d3-4a5c-8776-7ca876e7195a" width="800" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/3e39dc7d-b68b-43c8-8951-9f3b94a38c41" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/1d18d7e2-02ae-49a9-b40f-089981ccd778" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/4a27640b-79d5-4613-8641-81972f5d7113" width="400" alt="Image Description">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/360d8fb3-a6e0-4c2e-b29c-b3312a45251a" width="400" alt="Image Description">
okok
# Release Notes

### Version v2.0.2
- Optimization of update parameters.

### Version v2.0.1
- Optimization of update parameters.

### Version v2.0.0
- Change: Updated Yoloworld ESAM to G-DinoSAM.
- Update: Brand new layout.
- Update: Brand new parameters for smoother and softer results.
- Addition: Added mask softening feature.
- Addition: Added DA deep preprocessor, anyline preprocessor, and openpose preprocessor.

### Version v1.0.8
- Fix: Previous approach was incorrect; cutting through masks did not improve results and slowed down performance. Changed method to expand mask range.
- Fix: It seems that tile is not necessary for HD restoration, and using tile can cause skin darkening issues.
- Fix: Adjusted cropping size and mask blur, removed mask overlay for facial restoration.

### Version v1.0.7
- Addition: Quick switch to directly close unnecessary node groups.
- Fix: After modifying parameters, characters turned black but had more details, not sure why.

### Version v1.0.6
- Known issues: Cannot correctly identify arms and thighs.
- Fix: Previous nodes failed to detect the neck effectively, causing neck errors. Mask inter-cutting now meets neck scene requirements, and all 30 tested images worked normally.
- Fix: Previous nodes were ineffective for clothing, possibly detecting pants, etc. Mask cutting only meets clothing detection scenes, and 30 tested images worked normally.
- Fix: Changed keywords and settings for more accurate pants recognition.
- Deprecated: High-frequency and low-frequency nodes officially deprecated.

### Version v1.0.5
- Fix: Seemingly fixed the issue of face darkening.
- Fix: High-frequency and low-frequency modules are apparently unnecessary, so images can be obtained in one step.
- Bug: I was wrong; component transfer should not be used as it reduces image quality.

### Version v1.0.4
- Known issues: With increased amplitude of repainting and facial detail, the face darkens.
- Fix: Third node connection error.
- Addition: Added a type of image node to avoid restarting the demo due to subsequent step errors.
- Addition: Multi-person judgment: false for multiple people, true for a single person.
- Addition: High-frequency and low-frequency facial restoration nodes. If you don't want to adjust Sharpen's parameters, you can place two images in PS and use the mask to erase.

### Version v1.0.2
- Bug fix: Image transfer did not proceed sequentially but all at once.

### Version v1.0.1
- Modified facial parameters to make the face look less like a mask.

Author Pages:  
[liblib](https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image)
[civitai](https://civitai.com/user/1637083533489)
[小红书](https://www.xiaohongshu.com/user/profile/5fc2948e0000000001000b4e?xhsshare=CopyLink&appuid=5fc2948e0000000001000b4e&apptime=1714843011)
[抖音](https://v.douyin.com/i2ky4oxf/)
[openart](https://openart.ai/workflows/profile/flamingo_sudden_15?tab=workflows&sort=latest)

Please adhere to the open source license, redistribution is allowed, but please credit the author and commercial sales are prohibited.
