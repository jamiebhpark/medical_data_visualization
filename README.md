## 데이터 시각화 도구

### 1. 프로젝트 소개

**프로젝트 이름**: 데이터 시각화 도구

**목적**: 생성된 데이터를 시각화하여 사용자가 유용한 정보를 얻을 수 있도록 하는 간단한 도구를 개발합니다.

**주요 기능**:

- 데이터를 CSV 파일로 불러오기
- 데이터 전처리 및 필터링
- 다양한 형태의 그래프 및 차트 생성 (예: 라인 차트, 히스토그램)
- 시각화된 데이터를 이미지 파일로 저장

**기술 스택**: Python, Pandas, Matplotlib, Seaborn

---

### 2. 디렉토리 구조 설정

```bash
medical_data_visualization/
│
├── data/
│   └── medical_data.csv  # 예제 데이터 파일
│
├── src/
│   └── visualize.py  # 데이터 시각화 코드
│
└── venv/  # 가상 환경 디렉토리

```

1. **CSV 파일 생성**:
    - `data` 디렉토리를 우클릭하고, `New` -> `File`을 선택하여 `medical_data.csv` 파일을 생성합니다.
    - 다음 데이터를 `medical_data.csv` 파일에 추가합니다:
        
        ```
        csv코드 복사
        time,value
        0,1.1
        1,2.3
        2,2.9
        3,3.5
        4,4.1
        5,4.8
        6,5.3
        7,5.9
        8,6.2
        9,6.8
        
        ```
        
2. **Python 파일 생성**:
    - `src` 디렉토리를 우클릭하고, `New` -> `Python File`을 선택하여 `visualize.py` 파일을 생성합니다.

---

### 4. 코드 작성

**visualize.py**:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

def load_data(file_path):
    """
    Load medical data from a CSV file.
    """
    return pd.read_csv(file_path)

def visualize_data(data):
    """
    Visualize medical data using line plot.
    """
    plt.figure(figsize=(10, 6))
    sns.lineplot(data=data, x='time', y='value')
    plt.title('Medical Data Over Time')
    plt.xlabel('Time')
    plt.ylabel('Value')
    plt.savefig('data_visualization.png')
    plt.show()

if __name__ == "__main__":
    # Load the data
    data = load_data('../data/medical_data.csv')

    # Visualize the data
    visualize_data(data)

```

---

### 5. 라이브러리 설치

1. **PyCharm 터미널 열기**:
    - PyCharm의 하단에 있는 `Terminal` 탭을 클릭합니다.
2. **라이브러리 설치**:
    - 터미널에서 다음 명령어를 입력하여 필요한 라이브러리를 설치합니다:
        
        ```bash
        pip install pandas matplotlib seaborn
        ```
        

---

### 6. 코드 실행

1. **코드 실행**:
    - `visualize.py` 파일을 열고, PyCharm의 상단에 있는 `Run` 버튼을 클릭하여 코드를 실행합니다.
    - 또는, `visualize.py` 파일을 우클릭하고, `Run 'visualize'`를 선택합니다.

---

### 7. 결과 확인

1. **결과 이미지 확인**:
    - 코드 실행 후, 프로젝트 루트 디렉토리에 `data_visualization.png` 파일이 생성되었는지 확인합니다.
    - `data_visualization.png` 파일을 열어 시각화된 그래프를 확인합니다.
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/f9f35de7-0091-4a79-819a-501ef9435828/7e7fc5e2-f655-4a48-97b7-e95f10ed0ecc/Untitled.png)
    

---

### 8. 프로젝트 요약 및 결론

**프로젝트 요약**:
이 프로젝트는 기기에 생성된 데이터를 시각화하여 사용자가 유용한 정보를 얻을 수 있도록 하는 간단한 도구를 개발하였습니다. Pandas를 사용하여 데이터를 로드하고, Matplotlib과 Seaborn을 사용하여 데이터를 시각화하였습니다.

**결론**:
이 프로젝트를 통해 데이터 전처리 및 시각화 기술 기본기를 향상시킬 수 있었으며, 데이터의 패턴을 시각적으로 분석하는 데 도움을 줄 수 있는 간단한 도구를 구현하였습니다.
