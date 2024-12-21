# Pre-trained Models from NSDD

This repository provides checkpoints for ResNet-18 and ResNet-50 models, pre-trained on dermatological images from the National Skin Disease Database of Japan (NSDD).

## Usage

To load the checkpoint for ResNet-18, use the following code snippet:

```python
import torch
import torchvision

model = torchvision.models.resnet18()
unused_key = ('fc.weight', 'fc.bias')
state_dict = {k: v for k, v in torch.load('path_to_checkpoint.pth').items() if k not in unused_key}
model.load_state_dict(state_dict, strict=False)
```
For ResNet-50, replace `torchvision.models.resnet18()` with `torchvision.models.resnet50()`

## Checkpoints

| Model     | Pre-training Method                           | Image Data Used for Pre-training | Download                                                                                            |
| --------- | --------------------------------------------- | -------------------------------- | --------------------------------------------------------------------------------------------------- |
| ResNet-18 | Self-supervised method (SimCLR)               | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1GqGJPAddWPOxb32nzgv6QqIpeOmDv2Sy/view?usp=drive_link) |
| ResNet-18 | Self-supervised method (BYOL)                 | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1LOEGmtvJGueQc38kXRr7ZF190xPpazy2/view?usp=drive_link) |
| ResNet-18 | Self-supervised method (DINO)                 | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1dIbHrpBgmllX4ENqaQzStZRIUFCLu8C7/view?usp=drive_link) |
| ResNet-18 | Self-supervised method (SimCLR) + fine-tuning | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/11SLk180DNKCuskshfzNvM9SgnNm1lJzL/view?usp=drive_link) |
| ResNet-18 | Self-supervised method (BYOL) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/1pvSFAx5S2YsfnT5IvG7L8hEeJiSo0P-E/view?usp=drive_link) |
| ResNet-18 | Self-supervised method (DINO) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/18jxzY2fRRcrNkj3uphVTA566Q53kHrYw/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (SimCLR)               | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1q1IS_U85BbbPtEGwiw46yNISPpEvmXQP/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (BYOL)                 | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1KTHB-TOKo4fY-syfDkIHAGgdTSCNIQD7/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (DINO)                 | NSDD-unlabeled                   | [checkpoint](https://drive.google.com/file/d/1I6n-wJLHQF6Auzov2uHB7OlG-H5etMN4/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (SimCLR) + fine-tuning | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/1a4K_930bHKQbBdRtrOt-Kfsbd6CW8S2d/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (BYOL) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/1q4pcfBqmloTuTeY3xYhDR1hSRrCe3cuQ/view?usp=drive_link) |
| ResNet-50 | Self-supervised method (DINO) + fine-tuning   | NSDD-unlabeled + NSDD-labeled    | [checkpoint](https://drive.google.com/file/d/17c78v7y_kWepT-3bjZ9rBK89t9wiHNCH/view?usp=drive_link) |


## License

These checkpoints are freely available for **academic use only**. For commercial use and more detailed licensing information, please contact **shido1985 [AT] derma [DOT] med [DOT] tohoku [DOT] ac [DOT] jp**.

## Disclaimer

THESE CHECKPOINTS ARE PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THESE CHECKPOINTS OR THE USE OR OTHER DEALINGS IN THESE CHECKPOINTS.
