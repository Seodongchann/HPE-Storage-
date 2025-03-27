# HPE GreenLake for Block Storage 사전 등록 작업 **(인터넷 연결 필수)**

## DSCC 계정 등록 작업

### 1. [HPE Cloud](https://common.cloud.hpe.com) 에 접속 후 "Sign up"을 눌러 정보를 입력하여 계정을 생성합니다.  
###   이메일을 통해 검증 메일을 받습니다.

   ![image](https://github.com/user-attachments/assets/bbabc6ce-3b30-4036-a7c5-49339d36cb4c)

### 2. 메일을 확인 후 계정 활성화를 누르고 만든 계정으로 접속합니다.

   ![image](https://github.com/user-attachments/assets/6a235230-fce0-4f6f-85fd-8295baf77edf)

### 3. 처음 로그인 후 "WorkSpace"가 보이지 않으면 장비 등록 및 DSCC를 사용하기 위해서 **WorkSpace**를 생성합니다.

   ![image](https://github.com/user-attachments/assets/373b48fa-d86f-4f5d-9c7f-49e8f8e24e4a)  
###   정보 입력 후 "Create WorkSpace"를 클릭하면 WorkSpace가 만들어지고 DashBoard 화면이 나타납니다.

   ![image](https://github.com/user-attachments/assets/a5605bd1-a328-4dd0-bf0a-00d7eef1eb69)

### 4. Role 부여 순서: ① → ② → ③ → ④

   ![image](https://github.com/user-attachments/assets/4a127106-3a77-4389-9cb6-85e19a3a35ec)

### 5. 이메일을 확인하여 **Subscription을 Activation**하고 Key값을 받아 둡니다.  
###   영업(HPE 혹은 파트너사)에게 확인.  
###   **※ Subscription Key를 찾기 어려운 경우, Setup Wizard를 실행하여 마지막까지 진행하면 인터넷을 통해 받을 수 있습니다.**

   ![image](https://github.com/user-attachments/assets/5c9d78cb-64da-486b-9363-1debe21adab7)

---

## 장비 등록 작업 (계정이 있는 경우 여기서부터)

### 1. **GreenLake portal**에 접속 후 "Go to Workspace"를 클릭

   ![image](https://github.com/user-attachments/assets/34f2b115-3e37-4bac-8e2e-22472e488297)

### 2. **Add Device** 

   ![image](https://github.com/user-attachments/assets/53c4efb4-20bf-4d5a-b9da-4a626c1f2738)

### 3. **Add Device** 

   ![image](https://github.com/user-attachments/assets/c99a85b6-d1e6-44f4-9db8-d4c1aee012ea)  
   ![image](https://github.com/user-attachments/assets/45b8a9d5-c1e5-4bd4-9fd8-cf8c91d79d5d)

### 4. **Add Device Subscription** 

   ![image](https://github.com/user-attachments/assets/cec11b49-a5e3-4526-9229-55d0c7bca8fa)

### 5. **Assign to Service Manager** 

   ![image](https://github.com/user-attachments/assets/33526acb-201b-4786-8889-88f2389efaa1)

### 6. **Apply Subscription** 

   ![image](https://github.com/user-attachments/assets/c259c3df-a395-4aa4-8268-a12c416c9de1)  
   ![image](https://github.com/user-attachments/assets/7668b489-a287-4f1a-b155-e06360f20183)

### 7. 문제가 발생하면 **Case Open** 방법

   ![image](https://github.com/user-attachments/assets/9a3215ee-13db-43c6-8fc8-286aaf9b3fa5)  
   ![image](https://github.com/user-attachments/assets/4f7d2583-9c27-4eb2-8617-4528276dd42d)

---

# Rack Mount 방법

- **Controller 샤시 (E01)**는 20-21U에 장착  
- **Drive 샤시 (E41, E42, E43)**는 19U를 띄고 18U부터 아래로 장착  
- Controller 샤시와 Drive 샤시가 있다면, Cabling Guid를 확인 후 케이블 연결

   ![image](https://github.com/user-attachments/assets/b0d58a78-b7ad-4515-bc3b-03f6fa0b7ab2)
