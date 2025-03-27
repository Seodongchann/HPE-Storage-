# 🚀 HPE GreenLake for Block Storage UI 

## Dashboard - Overview, alerts, and tasks 
![image](https://github.com/user-attachments/assets/75dcf54c-7889-41bd-9184-8bfebc648c12)
## View performance details 
![image](https://github.com/user-attachments/assets/114b0d53-5ba9-4bc2-8a3b-887a0af6dda1)
## View Capacity details
![image](https://github.com/user-attachments/assets/ebbebb62-bf6e-4d13-bb64-edfad9379840)
## Storage screen-view and create host and application sets
![image](https://github.com/user-attachments/assets/acdadf92-d72a-4c62-a1f3-b72ce588b174)
## Configure replication partner system
![image](https://github.com/user-attachments/assets/f1d99422-6058-4885-b5a2-75491b56e906)
## Select and configure partner system, links, policies, and witness service 
![image](https://github.com/user-attachments/assets/5381ee92-d518-419b-bb06-b7ee95b8f6a9)
## Systems screen - Service and maintenance actions
![image](https://github.com/user-attachments/assets/54866735-6bea-4d3c-8eaa-3f5b329ea4a6)

---
# HPE GreenLake for Block Storage compute IO module details
![image](https://github.com/user-attachments/assets/915d4c07-98de-4668-841c-c3a1ad65a422)

# Multi-chassis, non-switched systems 


![image](https://github.com/user-attachments/assets/df4a80cf-db0f-442c-b05e-363f0cd563fc)

## 공통 사항

* 섀시(인클로저)당 최소 8개의 동일한 크기의 SSD 필요
* 기존과 동일한 용량의 SSD 2개 단위로 업그레이드
* 섀시당 2개 단위로 업그레이드 권장
* 섀시 전체에 대칭적으로 드라이브 분산 권장 (비효율적인 용량 사용 및 병목 현상 방지)
* 사용 가능한 SSD 용량: 1.92TB, 3.84TB, 7.68TB, 15.36TB

## 1 Chassis 구성

* 최소 드라이브 수: 8개
* 최대 드라이브 수: 24개
* 최적 업그레이드 단위: 2개

## 2 Chassis 구성

* 최소 드라이브 수: 16개
* 최대 드라이브 수: 48개
* 최적 업그레이드 단위: 4개

## 3 Chassis 구성

* 최소 드라이브 수: 24개
* 최대 드라이브 수: 72개
* 자동 구성: HA 케이지(인클로저) 및 RAID 6 4+2로 자동 구성
* 최적 업그레이드 단위: 6개

---
# 📌 GreenLake 활용하여 Volume 생성

## 1️⃣ GreenLake Storage 에 접속하여 Volume을 생성할 모델 선택
- GreenLake Storage 포털에 접속하여 원하는 **스토리지 모델**을 선택합니다.

![image](https://github.com/user-attachments/assets/41827736-04f0-46d2-bb22-6414336fbd33)

---

## 2️⃣ 선택한 Storage 모델을 클릭하여 Volume 설정
- 선택한 스토리지 모델의 세부 설정 화면으로 이동합니다.

![image](https://github.com/user-attachments/assets/7d64254a-34e1-4c0c-8757-3366a98c76e9)

---

## 3️⃣ 시스템 선택 (Systems)
- **HPE Alletra Storage MP 볼륨 생성 과정 중 "시스템 선택 (Systems)" 단계**
- 각 시스템의 **모델, 용량, 가용성(Headroom Availability)** 정보가 제공됩니다.

![image](https://github.com/user-attachments/assets/d1f915cb-c981-48ac-8f57-1c873059e799)

---

## 4️⃣ 옵션 선택 (Options)
### 🏷️ 1. 볼륨 이름 설정
- `Volume Set Name`: 생성할 볼륨의 이름을 입력 (예: `DemoVolume1`).

### 🔼 2. 우선순위 설정
- `Priority Level`: 볼륨의 우선순위를 **Lowest ~ Highest** 범위에서 설정.
- 기본값은 `Medium`으로 설정됨.

### ⚠️ 3. 공간 경고 (Space Warning)
- 스토리지 용량이 특정 임계값(%)을 초과할 경우 경고 발생.
- 기본값: `95%`.

### 🔗 4. 호스트 그룹 선택
- `Host Group`: 볼륨을 연결할 호스트 그룹을 선택 (예: `ESX-125`).
- `Hosts and Initiators` 옵션을 클릭하여 연결된 호스트 및 이니시에이터를 확인 가능.

### 🔢 5. 자동 LUN 할당
- `Auto LUN IDs` 체크 시, 자동으로 LUN ID가 할당됨.

### 🕒 6. 스케줄 설정 (선택 사항)
- 볼륨 보호 정책을 위한 **스냅샷 스케줄** 설정 가능.
- 예: `"Daily snapshots | 30 days Expiration"`.
- 특정 시간에 스냅샷 생성 가능 (예: `1 AM`).

### 🔘 7. 버튼 옵션
- **`Back`**: 이전 단계(`Systems`)로 이동.
- **`Continue`**: 설정 완료 후 다음 단계(`Review`)로 이동.

## 5️⃣ 검토 및 볼륨 생성 (Review & Submit)

![image](https://github.com/user-attachments/assets/5b8aa0c1-24c9-4b48-a410-eae0ff1416f9)

### 🔍 검토 단계
- 모든 볼륨 설정을 **최종적으로 검토**하는 단계입니다.
- **General, Systems, Options** 섹션에서 볼륨 생성에 대한 상세 정보를 확인할 수 있습니다.

---

### 🗂️ General (일반 정보)
| 항목            | 값 |
|----------------|-----------------------------------------------|
| **Storage Tier** | HPE GreenLake for Block Storage |
| **Workload** | VMware ESXi |
| **Number of Volumes** | 1 |
| **Capacity** | 16 GiB per volume |
| **Volume Name** | DemoVolume1 |
| **Protection Policy** | Daily snapshots \| 30 days Expiration |

---

### 🖥️ Systems (시스템 정보)
| 항목 | 값 |
|------|--------------------------------------|
| **System** | FTC-AMP-1 |
| **System Capacity** | 59.8 TiB free of 62.1 TiB |
| **Headroom Availability** | High |

---

### ⚙️ Options (설정 정보)
| 항목 | 값 |
|------|-------------------------------|
| **Host Group** | ESX-125 |
| **LUN IDs** | Automatic |
| **Volume Set Name** | DemoVolume1 |
| **Priority Level** | Medium |
| **Data Reduction** | Enabled |
| **Snapshot Schedule Time** | 1:00 AM CDT |
| **Snapshot Virtual Lock** | 90 DAYS |

---

### 🖱️ 버튼 옵션
- **`Back`**: 이전 단계(`Options`)로 이동하여 설정 변경 가능.
- **`Submit`**: 모든 설정을 확정하고 볼륨을 생성.

📌 **`Submit` 버튼을 클릭하면 볼륨이 생성되며, 이후 스토리지에 적용됩니다.**
