# data

실습용 데이터를 두는 폴더입니다. 이 README를 제외한 파일은 `.gitignore`로 커밋에서 빠집니다.
(데이터셋 용량이 커서 저장소가 무거워지는 것을 막기 위해서입니다.)

## Colab에서 Kaggle 데이터셋 불러오기

### 방법 1. kagglehub (간단)

```python
import kagglehub

# 예: Melbourne 집값 데이터 (Intro to Machine Learning 코스에서 사용)
path = kagglehub.dataset_download("dansbecker/melbourne-housing-snapshot")
print(path)  # 내려받은 폴더 경로
```

공개 데이터셋은 로그인 없이 받을 수 있는 경우가 많고, 로그인이 필요하면 아래 방법 2의 API 키를 설정합니다.

### 방법 2. Kaggle API 키 사용

1. Kaggle → Settings → API → **Create New Token**을 눌러 `kaggle.json`을 내려받습니다.
2. Colab 왼쪽 🔑(보안 비밀) 메뉴에 `KAGGLE_USERNAME`, `KAGGLE_KEY`를 등록합니다.
3. 노트북에서 다음과 같이 불러옵니다.

```python
import os
from google.colab import userdata

os.environ["KAGGLE_USERNAME"] = userdata.get("KAGGLE_USERNAME")
os.environ["KAGGLE_KEY"] = userdata.get("KAGGLE_KEY")

!kaggle datasets download -d dansbecker/melbourne-housing-snapshot -p data --unzip
```

`kaggle.json` 파일이나 키 값을 노트북 코드에 직접 적어서 커밋하지 마세요.
