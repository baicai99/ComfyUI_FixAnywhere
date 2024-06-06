# 基于Yoloworld的ComfyUI节点全身修复

### 问答：

**Q：为什么要这样做？**  
**A：** 因为MidJourney生成的人物具有油画质感，每次都需要用sd进行修复。所以我开发了一个工作流程来直接修复这些人物。

**Q：为什么手指修复效果不好？**  
**A：** 因为这个过程只关注逼真度，而不会处理不合理的情况。换句话说，它无法将扭曲的手指修复为正常状态，只能在原来的手上添加血管。

- 推荐的大模型：[majic V7](https://www.liblib.art/modelinfo/bced6d7ec1460ac7b923fc5bc95c4540)

- 推荐的Vae：[Realistic difConsistency Negative (Pack)](https://www.liblib.art/modelinfo/232ff495f7c14381910dc6f4df78a7ab)

- lora：[YFilter_PortraitEnhance 推荐](https://www.liblib.art/modelinfo/ec6239d3fcdc46beb8aefbd587e291b7)

- 推荐的高清修复节点。如果你希望图像更逼真，甚至包括毛孔细节，请使用此缩放节点。[链接](https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx)

我的节点使用G-DinoSAM识别对象，不只是重绘面部等。你可以自由复制粘贴，自由组合。

1. 如果在识别头发时识别到了整个头部，请调整G-DinoSAM中的阈值参数。

2. 毕竟这是自动化。请不要期望过高。我只能尽量复制手动操作，在Photoshop中的后期处理是不可避免的。

3. 如果有任何不便或建议，请积极留言。

### 示例图片：

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/e8c35b5a-07d3-4a5c-8776-7ca876e7195a" width="800" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/3e39dc7d-b68b-43c8-8951-9f3b94a38c41" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/1d18d7e2-02ae-49a9-b40f-089981ccd778" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/4a27640b-79d5-4613-8641-81972f5d7113" width="400" alt="图片描述">

<img src="https://github.com/baicai99/ComfyUI_Yoloworld_based_full_body_fix_for_ComfyUI_nodes/assets/101706274/360d8fb3-a6e0-4c2e-b29c-b3312a45251a" width="400" alt="图片描述">

# 更新日志

### 版本号 v2.0.2
- 优化更新参数。

### 版本号 v2.0.1
- 优化更新参数。

### 版本号 v2.0.0
- 更改：把Yoloworld ESAM更改为G-DinoSAM。
- 更新：全新的排版。
- 更新：全新的参数，更丝滑，更柔和。
- 新增：蒙版柔和。
- 新增：DA深度预处理器、anyline预处理器，openpose预处理器。

### 版本号 v1.0.8
- 修复：之前思路错了，通过蒙版裁切并不能取得更好的效果，反而会拖慢运行速度。更改方式改为扩大蒙版范围。
- 修复：似乎不需要tile也能很好的高清修复，并且tile还会伴随着皮肤变黑的问题。
- 修复：调整了裁剪尺寸以及蒙版模糊，面部修复去除蒙版叠加。

### 版本号 v1.0.7
- 新增：快捷开关，直接关闭不需要的节点组。
- 修复：修改参数后，字符会变黑，但细节更多了，不知道为什么。

### 版本号 v1.0.6
- 已知问题：无法正确识别手臂。无法正确识别大腿。
- 修复：之前的节点无法有效检测到颈部，导致颈部错误，通过蒙版之间的相互裁剪可以满足颈部的场景，测试中的所有30张图像都可以正常使用。
- 修复：之前的节点对服装无效，可能会检测到裤子等，通过蒙版裁剪只能满足检测服装的场景，测试30张图片可以正常使用。
- 修复：更改关键字和设置，使裤子识别更准确。
- 废弃：高频和低频节点正式废弃。

### 版本号 v1.0.5
- 修复：似乎修复了脸变黑的问题。
- 修复：高频和低频模块似乎不是必需的，因此可以一步获得图像。
- Bug：我错了，不应该使用组件传输，它会降低图像质量。

### 版本号 v1.0.4
- 已知问题：随着重绘的振幅和面部细节增加，脸部会变暗。
- 修复：第三个节点连接错误。
- 新增：添加了一种图像节点类型，避免由于后续步骤中的错误而需要重新启动演示。
- 新增：多人判断：多个人为假，单个人为真。
- 新增：高频和低频面部修复节点。如果你懒得调整过Sharpen的参数，可以在PS中放两张图像，并使用蒙版擦除。

### 版本号 v1.0.2
- 修复bug：图像传输没有按顺序进行，而是一次性全部进行。

### 版本号 v1.0.1
- 修改面部参数，使面部更不像假面。

作者主页：
[liblib](https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image)
[civitai](https://civitai.com/user/1637083533489)
[小红书](https://www.xiaohongshu.com/user/profile/5fc2948e0000000001000b4e?xhsshare=CopyLink&appuid=5fc2948e0000000001000b4e&apptime=1714843011)
[抖音](https://v.douyin.com/i2ky4oxf/)
[openart](https://openart.ai/workflows/profile/flamingo_sudden_15?tab=workflows&sort=latest)

请遵循开源协议，允许转发但请注明作者，并且禁止售卖。