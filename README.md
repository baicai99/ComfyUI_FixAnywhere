# Yoloworld-based-full-body-fix-for-ComfyUI-nodes

[English](/README.md) | [中文](/README.zh.md)

### Very important, must read.

- Recommended node for HD restoration, use this zoom node if you want a more realistic image, even including pore detail. https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx

This node of mine uses Yoloworld to recognize objects, not just just redraw faces and hair, you can combine them as you like.

1. the many / many prople node turns on if there are many people, if there are many people then split the mask and redraw each character individually, otherwise redraw them all together. 2. if the hair is recognized when the hair is recognized then use this zoom node.

2. If you recognize the whole head when you recognize the hair, please adjust the first parameter in Yoloworld ESAM.

3. I use RemapImageRange to pass the image, if you don't want to pass you can disable the node.

How to use high and low frequency: measured high CFG and high noise reduction can greatly increase the details of the screen, but the character face will become black, low frequency is the same reason, if you know PS, you can use the mask to scrape to get a very good picture effect.

# UPDATE LOG

### Version number v1.0.5
- Fix: Seems to fix the problem that the face will turn black.
- Fix: It seems that there is no need for high and low frequency modules, so you can get a picture in one step.
- bug: I was wrong, I shouldn't use components to pass, it will lose image quality.

### Version v1.0.4
- Known issue: Face will become darker as the redraw amplitude and facial details increase.
- Fixed, third node connection error.
- New: node type adding pictures, avoiding the subsequent step errors that lead to the need to start over for the demo.
- New: Multi-Person Judgment: False is multi-person, true is single person.
- New: Facial repair high and low frequency nodes. If you are too lazy to adjust the parameters of oversharpening, put two pictures into PS and erase them with mask.

### Version v1.0.2
- Bug fix, picture passing is not in order, but all in parallel.

### Version v1.0.1
- Changed the face parameter to make the face less like a fake face.

Author's homepage:  
[liblib](https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image)  
[civitai](https://civitai.com/user/1637083533489)  

Please follow the open source agreement, redistribution is allowed but please credit the author, and selling is prohibited.
