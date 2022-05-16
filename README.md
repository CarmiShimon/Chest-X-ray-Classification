# Chest-X-Ray-Classification.
Pytorch implementation of Chest-X-ray-Classification  

## Dataset  
[Covid-19 Chest X-Ray](https://github.com/ieee8023/covid-chestxray-dataset)  
[Chest X-Ray images](https://www.kaggle.com/datasets/tolgadincer/labeled-chest-xray-images)  
**Clasess:**    
- Normal
- Bacteria
- Covid-19  

Set | #Normal | #Bacteria | #Covid-19 |
--- | --- | --- | --- |
#images | 1349 | 2538 | 156 |  

**Installations**  
```pip install torch, torchvision, tensorflow, sklearn```  
## Imbalanced Data (Under sampling, Over sampling, Class weights):  

## Data Augmentation ('noise', 'RandomRotation', 'RandomHorizontalFlip', 'brightness', 'contrast', 'RandomResizedCrop'):  
 
**'Noise'**
```transforms.Compose([transforms.ToTensor(), AddGaussianNoise(0.1, 0.08)])```  
![noiseAug](./images/noise.png)  
**'RandomRotation', 5%**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomRotation(degrees=5)])```  
![RandomRotationAug](./images/random_rotation.png)  
**'RandomHorizontalFlip', 90% probability**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomHorizontalFlip(p=0.9)])```
![RandomHorizontalFlip](./images/random_horizontal_flip.png)  
**'brightness', 50%**  
```transforms.Compose([transforms.ToTensor(), transforms.ColorJitter(brightness=0.5)])```  
![Brightness](./images/brightness.png)  
**'contrast', 50%**  
```transforms.Compose([transforms.ToTensor(), transforms.ColorJitter(contrast=0.5)])```  
![Contrast](./images/contrast.png)   
**'RandomResizedCrop', original size=28X28 pixels**  
```transforms.Compose([transforms.ToTensor(), transforms.RandomResizedCrop(size=(28, 28))])```  
![RandomResizedCrop](./images/random_resized_crop.png)   


