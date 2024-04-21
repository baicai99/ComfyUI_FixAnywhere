# 基于Yoloworld的ComfyUI节点的全身修复

### 非常重要，请务必阅读。

- 推荐的节点用于高清修复，如果您想要更真实的图像，甚至包括毛孔细节，请使用此缩放节点。[此处链接](https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx)

我的这个节点使用Yoloworld来识别物体，而不仅仅是重绘脸部和头发，您可以根据需要组合它们。

1. 如果有很多人，将许多人的节点打开，如果有很多人，则分割掩码并单独重绘每个角色，否则将它们全部一起重绘。

2. 如果识别出头发时识别出整个头部，请调整Yoloworld ESAM中的第一个参数。

# 样张：

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/3e9c774c-bc6f-4ed2-b70a-c02423bed245" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/cf0814ee-863e-498a-b9ec-7d6a03f2eaad" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8cbd0b6e-64a3-4bdf-a228-b502bfbcb16e" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/8183c713-5456-42ce-9d6b-c848a1328e30" width="400" alt="图片描述">

# 更新日志

### 版本号 v1.0.5
- 修复：似乎修复了脸部变黑的问题。
- 修复：似乎不需要高低频率模块，因此可以一步获取图片。
- bug：我错了，不应该使用组件传递，它会损失图像质量。

### 版本 v1.0.4
- 已知问题：随着重绘振幅和面部细节增加，面部会变暗。
- 修复：第三个节点连接错误。
- 新增：节点类型添加图片，避免了后续步骤错误导致需要重新开始演示的问题。
- 新增：多人判断：False为多人，True为单人。
- 新增：面部修复高低频节点。如果您太懒得调整过锐化的参数，请将两张图片放入PS并使用蒙版擦除。

### 版本 v1.0.2
- 修复bug，图片传递不是按顺序进行，而是全部并行进行。

### 版本 v1.0.1
- 更改了脸部参数，使脸部更少像假脸。

作者主页：  
[liblib](https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image)  
[civitai](https://civitai.com/user/1637083533489)  

请遵守开源协议，允许重新分发，但请标明作者，并且禁止销售。
