# E27_Medical_Unet

# 결론: Encoder-Decoder 모델, U-Net 모델, Pretrained U-Net 모델 비교 분석

## (1) 총 파라미터 수
- Unet Model이 Vgg16 Unet Model과 Encoder_Decoder Model 보다 파라미터 수가 많다. 
    1. Encoder_Decoder Model: 7,047,969
    2. Unet Model:  61,240,193
    3. Vgg16 Unet Model: 58,723,265

## (2) 학습 결과
### : Vgg16 Unet Model >> Unet Model >> Encoder_Decoder Model

### 1. Encoder_Decoder Model
- loss: 0.0680, dice_loss: 0.0491, val_loss: 0.0882, ***val_dice_loss: 0.0641***

![ed_model](https://user-images.githubusercontent.com/39249809/99675734-ec334a00-2aba-11eb-94d0-9dc53b25a4f1.png)

### 2. Unet Model
- loss: 0.0531, dice_loss: 0.0381, val_loss: 0.0536, ***val_dice_loss: 0.0393***

![unet_model](https://user-images.githubusercontent.com/39249809/99675736-eccbe080-2aba-11eb-9b0b-6791298fae7a.png)

### 3. Vgg16 Unet Model
- loss: 0.0342, dice_loss: 0.0189, val_loss: 0.0487, ***val_dice_loss: 0.0285***

![vgg16unet_model](https://user-images.githubusercontent.com/39249809/99675738-ed647700-2aba-11eb-88e3-02c0c400a7e8.png)

## (2) mean IoU
### :  Vgg16 Unet Model이 Unet Model보다 0.154 높았고, Unet Model이 Encoder_Decoder Model 보다 0.253 높았다.
    1. Encoder_Decoder Model: ***0.9190***
    2. Unet Model: ***0.9443***
    3. Vgg16 Unet Model: ***0.9597***

### (3) 테스트 이미지 결과 분석

### 1. Encoder_Decoder Model
- 용종의 가장자리를 정확하게 세그멘테이션 하지 못했다. 

![ed_model_image](https://user-images.githubusercontent.com/39249809/99675724-e9385980-2aba-11eb-9262-d61e2a5e752c.png)

### 2. Unet Model
- 대부분 세그멘테이션 결과가 나아졌지만, 일부는 용종의 가장자리를 정확하게 세그멘테이션 하지 못했다. 

![unet_model_image](https://user-images.githubusercontent.com/39249809/99675729-eb021d00-2aba-11eb-8662-eecf935ff064.png)

### 3. Vgg16 Unet Model
- 전체적으로 세그멘테이션 결과가 매우 정확해졌다. 

![vgg16unet_model_image](https://user-images.githubusercontent.com/39249809/99675732-eb9ab380-2aba-11eb-8dbe-4ebef0da361d.png)
