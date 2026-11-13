# Kaggle Learn 학습 기록

[Kaggle Learn](https://www.kaggle.com/learn) 마이크로코스를 들으며 실습한 코드를 모아 두는 저장소입니다.
레슨 내용은 Kaggle에서 읽고, 실습은 **Google Colab**에서 진행한 뒤 노트북을 이 저장소에 저장합니다.
개념 정리는 Notion "Kaggle Learn 개념정리" 페이지의 **개념 노트**에 따로 기록합니다.

## 학습 흐름

1. Kaggle Learn에서 레슨(Tutorial)을 읽는다.
2. 해당 코스 폴더의 노트북을 Colab으로 연다. (노트북 맨 위 **Open in Colab** 배지 클릭)
3. 튜토리얼 코드를 따라 치고, 연습문제(Exercise)를 풀면서 내 메모를 덧붙인다.
4. Colab 메뉴 **파일 → GitHub에 사본 저장**으로 이 저장소의 같은 경로에 저장한다.
5. 아래 진도표의 체크박스를 채우고, 배운 개념은 Notion 개념 노트에 정리한다.

## 폴더 구조

```
kaggle/
├── README.md                 # 이 문서 (전체 진도표)
├── requirements.txt          # 로컬/Colab에서 필요한 패키지
├── templates/
│   └── lesson_template.ipynb # 새 레슨 노트북을 만들 때 복사해서 쓰는 틀
├── courses/
│   ├── 01_python/
│   ├── 02_pandas/
│   ├── 03_data-visualization/
│   ├── 04_data-cleaning/
│   ├── 05_intro-to-sql/
│   ├── 06_intro-to-machine-learning/
│   ├── 07_intermediate-machine-learning/
│   └── 08_feature-engineering/
└── data/                     # 실습용 데이터 (용량이 큰 파일은 커밋하지 않음)
```

각 코스 폴더 안에는 레슨 목록과 진도 체크가 담긴 `README.md`가 있고,
노트북은 `레슨번호_레슨이름.ipynb` 형식으로 저장합니다. (예: `courses/01_python/01_hello_python.ipynb`)

## 진도표

| 순서 | 코스 | 폴더 | 상태 |
|---|---|---|---|
| 1 | Python | [01_python](courses/01_python) | 🟡 진행 중 |
| 2 | Pandas | [02_pandas](courses/02_pandas) | ⚪ 예정 |
| 3 | Data Visualization | [03_data-visualization](courses/03_data-visualization) | ⚪ 예정 |
| 4 | Data Cleaning | [04_data-cleaning](courses/04_data-cleaning) | ⚪ 예정 |
| 5 | Intro to SQL | [05_intro-to-sql](courses/05_intro-to-sql) | ⚪ 예정 |
| 6 | Intro to Machine Learning | [06_intro-to-machine-learning](courses/06_intro-to-machine-learning) | ⚪ 예정 |
| 7 | Intermediate Machine Learning | [07_intermediate-machine-learning](courses/07_intermediate-machine-learning) | ⚪ 예정 |
| 8 | Feature Engineering | [08_feature-engineering](courses/08_feature-engineering) | ⚪ 예정 |

상태 표시: ⚪ 예정 · 🟡 진행 중 · 🟢 완료

## Colab에서 실습할 때 참고

- Kaggle 연습문제의 정답 확인 코드(`q1.check()` 등)는 Kaggle이 만든 `learntools` 패키지와
  Kaggle 노트북에 연결된 데이터셋을 전제로 합니다. Colab에서는 둘 다 기본으로 없으므로,
  정답 확인까지 하고 싶다면 Kaggle 노트북에서 풀고, Colab에는 직접 작성한 코드와 메모를 정리하는 방식을 추천합니다.
- 데이터가 필요한 코스(Pandas 이후)는 Kaggle 데이터셋을 내려받아 `data/` 폴더에 두거나
  `kagglehub`로 불러옵니다. 자세한 내용은 [data/README.md](data/README.md)를 참고하세요.
- `kaggle.json`(Kaggle API 키)은 절대 커밋하지 않습니다. `.gitignore`에 등록되어 있습니다.

## 커밋 메시지 규칙

```
[코스] 레슨명 - 한 일
예) [Python] Hello, Python - 튜토리얼 실습 및 연습문제 풀이
예) [Pandas] Grouping and Sorting - 연습문제 3~5번 풀이
```
