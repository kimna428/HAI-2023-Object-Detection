# HAI-2023-Object-Detection

## 초기 세팅
코드 구현 환경 : wsl ubuntu-22.04 && Windows 10, miniconda 가상환경 사용

필요한 패키지 설치 방법 : ```pip install -r requirements.txt```

혹여 누락된 패키지가 있다면, 해당 패키지는 ```pip install (package)```를 통해 설치하시면 됩니다.


## 실행방법
trian : ```bash ./scripts/train.sh```

eval : ```bash ./scripts/eval.sh```

draw(bbox 그려진 이미지 그리기) : ```bash ./scripts/draw.sh```

use_model(모델을 사용해 image를 image with bbox와 식재료 리스트로 변경) : ```bash ./scripts/use_model.sh```


인자를 직접 설정하고자 할 때는, python main.py --help를 통해 인자에 대한 설명을 볼 수 있습니다.


## 모델 사용 관련
input_image 폴더 내의 마지막 이미지를 model에 넣어 bbox를 그린 이미지와 식재료 리스트(집합)을 저장합니다.

bbox를 그린 이미지는 "bbox_(model에 넣은 이미지 이름)"으로 저장되고, 식재료 리스트는 "ingredients_(model에 넣은 이미지 이름)"으로 저장됩니다.

현재 구현한 코드는 한번에 하나의 쿼리만 처리합니다.

즉, 한 명의 유저가 하나의 사진을 input_image 폴더로 보낸 후 Object Detection하는 상황을 가정하여 코드를 작성했습니다.
