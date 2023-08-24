# Pre-trained models from NSDD

This repository contains checkpoints of ResNet-18 model pre-trained by using dermatological images in National Skin Disease Database of Japan (NSDD).

## Usage

To load the pre-trained model, use the following code snippet:

```python
import torch
import torchvision

model = torchvision.models.resnet18()
model.load_state_dict(torch.load('path_to_checkpoint.pth'), strict=False)
```

## Checkpoints

| Pre-training method                           | Image data used for pre-training | Download                                             |
| --------------------------------------------- | -------------------------------- | ---------------------------------------------------- |
| Self-supervised method (SimCLR)               | NSDD-unlabeled                   | [checkpoint](./checkpoints/SimCLR_pretrained.pth)    |
| Self-supervised method (BYOL)                 | NSDD-unlabeled                   | [checkpoint](./checkpoints/BYOL_pretrained.pth)      |
| Self-supervised method (DINO)                 | NSDD-unlabeled                   | [checkpoint](./checkpoints/DINO_pretrained.pth)      |
| Self-supervised method (SimCLR) + fine-tuning | NSDD-unlabeled + NSDD-labeled    | [checkpoint](./checkpoints/SimCLR_SL_pretrained.pth) |
| Self-supervised method (BYOL) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](./checkpoints/BYOL_SL_pretrained.pth)   |
| Self-supervised method (DINO) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](./checkpoints/DINO_SL_pretrained.pth)   |

## License

These checkpoints are freely available for academic use. For commercial use and more detailed licensing information, please contact shido1985 [AT] derma [DOT] med [DOT] tohoku [DOT] ac [DOT] jp.

## Disclaimer

THESE CHECKPOINTS ARE PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THESE CHECKPOINTS OR THE USE OR OTHER DEALINGS IN THESE CHECKPOINTS.
