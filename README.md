# Yoloworld-based-full-body-fix-for-ComfyUI-nodes

# Version number v1.0.2
- Bug fix, image delivery is not in order, but all in parallel.
# Version number v1.0.1
- Changed the facial parameters to make the face less of a masquerade.

This is the HD Restoration node, use this zoom node if you want the image to be more realistic, even including pore detail. https://openart.ai/workflows/seven947/1minute-8k-upscale/1IPTks1gL7v0EPmvsMcx

This node uses Yoloworld to recognize objects, you can use any combination of nodes.

If you use the HD zoom node I provided you with, and then fix it, the face is too large and may cause problems such as bursting video memory, and the fixing process will be slow, taking 30 minutes for just the face and hair 4080.
  
If you recognize the whole head when recognizing the hair, please adjust the first parameter in Yoloworld ESAM.

Yoloworld recommended parameters:
Hair: Use 0.2 for half body photos
Face: 0.1 for half body photo

Author's homepage:
liblib: https://www.liblib.art/userpage/c0e1c819d36c4bce9b077e04f9eaf693/publish/image
civitai: https://civitai.com/user/1637083533489

Please follow the open source agreement, redistribution is allowed with attribution, and selling is prohibited.
