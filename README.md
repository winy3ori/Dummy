# Dummy


### 🧪 Dummy Text to JSON Converter


 간단한 탭 구문 텍스트 데이터를 JSON 형태로 변환하는 Python 스크립트

```python
import json

data = """
A001	테스트코드	123	1
A002	샘플코드	456	2
A003	임시코드	789	3
"""

lines = [line.strip() for line in data.strip().split('\n') if line.strip()]

result = []
for line in lines:
    parts = line.split('\t')
    if len(parts) == 4:
        result.append({
            "text1": parts[0],
            "text2": parts[1],
            "text3": parts[2],
            "text4": parts[3]
        })

print(json.dumps(result, ensure_ascii=False, indent=4))
