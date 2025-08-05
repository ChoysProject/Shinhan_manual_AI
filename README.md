# Shinhan_manual_AI


<img width="579" height="845" alt="image" src="https://github.com/user-attachments/assets/8383dc4b-3b12-4946-b8b0-57c917911b27" />
<img width="859" height="564" alt="image" src="https://github.com/user-attachments/assets/f200b791-abb4-4b54-8a31-4ce76ca9049f" />
<img width="1155" height="730" alt="image" src="https://github.com/user-attachments/assets/a2cc2b80-d28c-4552-ad46-19264349c0f2" />
<img width="940" height="583" alt="image" src="https://github.com/user-attachments/assets/3a127f32-0fdf-42b1-88e4-0b4c409c2475" />


// frontend
  1. 언어 및 프레임워크 : next.js and typescript
  2. 설치 가이드 :
                      # 1. 프로젝트 폴더로 이동
                      cd frontend
                      
                      # 2. next.js + TypeScript 프로젝트 생성
                      npx create-next-app@latest . --typescript --eslint --src-dir --app --import-alias "@/*" --use-npm
                      
                      # 3. UI 라이브러리 설치 (Material UI 예시)
                      npm install @mui/material @emotion/react @emotion/styled @mui/icons-material
                      
                      # 4. 기타 필요한 라이브러리(예: axios 등)
                      npm install axios
                      

// backend
  1. python and fastAPI
  2. 설치 가이드 : 
                   /backend 경로 이동
                   경로에서 파이썬 설치 pip install fastapi uvicorn openai faiss-cpu "pdfplumber<0.11.0" python-pptx python-docx python-multipart
  3. 백엔드 구조 backend/
                    ├─ main.py              # FastAPI 진입점
                    ├─ requirements.txt     # 의존성 목록
                    ├─ vector_store.py      # FAISS 벡터DB 관리
                    ├─ file_utils.py        # 파일/텍스트 추출 유틸
                    └─ (data/, uploads/)    # 업로드/임베딩 데이터


  4. 백엔드 준비 (실행 코드 uvicorn main:app --reload)
        1) 필요한 패키지 설치
                  아래 패키지들이 필요합니다:
                  fastapi
                  uvicorn
                  openai
                  faiss-cpu
                  numpy
                  pdfplumber
                      => 명령어 pip install --upgrade pip (pip 구버전이라서)
                                pip install fastapi uvicorn openai faiss-cpu numpy pdfplumber

           pip install python-pptx python-docx -> 파이썬에서 각 문서들 읽기 패키지


           DB : Pinecone -> pcsk_BaUYA_Hb3cpxNJFhw6Z9WCUVPs9Ukzckf948ttTsAGBfzeNXPLvtrpWsS7k3qqUhrJoTt
           backend에서 설치 : pip install pinecone-client
           GPT : 비밀
           Pinecone : 비밀
           replica : key 및 임베딩 모델
           벡터DB : 모드 GPT 

            FLOW
            파일 업로드 시 텍스트 추출 → 임베딩 생성 → Pinecone(벡터DB)에 저장
            질문 시 임베딩 생성 → Pinecone에서 유사 문서 검색 → GPT에 문서+질문 전달 → 답변 생성

5. 단체 대화방
   매뉴얼 AI방 (60%) -> 유사도 조절필요
   위키 링크방 
   점메추방
   엑셀 AI 
   일반 GPT (100%) 


   
