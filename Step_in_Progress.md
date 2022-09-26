o 본 프로그램의 흐름 설명

 1. 사용자가 의심가거나 검증이 필요한 .exe 파일 업로드
 
 2. 프로그램 내부에서 해당 .exe 파일에 대한 .text Section Opcode 추출 및 항목별 빈도수 .csv 파일 출력
 
 3. 서버(리눅스)에 해당 .exe 파일이 업로드 되고 Cuckoo Sandbox 동적 분석 수행, 프로그램 내부에서는 서버에서 .json 파일을 가져와 항목별 빈도수 .csv 파일 출력

 4. 앞서 2, 3번에서 출력한 각 .csv 파일을 하나의 .csv 파일로 병합

 5. 4번에서 병합한 하나의 .csv 파일을 본 프로젝트에서 구축한 탐지모델에 검증하는 데이터로 사용 (testset)

 6. 5번의 결과인 탐지모델의 검증치 및 파일의 세부 분석정보 등을 사용자에게 결과보고서 형태로 출력 -> 사용자가 해당 결과보고서를 확인 후 대처