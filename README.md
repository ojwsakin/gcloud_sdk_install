# gcloud_sdk_install
본 목적은 CKS를 학습하기 위해 GCP의 gloud CLI를 설치하는 목적도 있지만 추후 GCP를 활용할 상황을 대비해 공부하는 것에 목적을 두었습니다.
---
- gcloud CLI docs : https://cloud.google.com/sdk/docs/install?hl=ko
---

### 본인의 환경 확인하기
- 제 환경은 MacOS로 진행했습니다

### tar file install
```
wget https://cloud.google.com/sdk/docs/install\?hl\=ko\#:\~:text\=google%2Dcloud%2Dcli%2D443.0.0%2Ddarwin%2Dx86_64.tar.gz
```

### tar xzf
```
tar xzf google-cloud-cli-443.0.0-darwin-x86_64.tar.gz\?hl=ko
```

### google-cloud-sdk 확인
<img width="418" alt="image" src="https://github.com/ojwsakin/gcloud_sdk_install/assets/93701762/018a7095-674f-407d-b086-72f5c7ba09a0">

### sdk에 존재하는 install.sh 스크립트 실행
```
cd google-cloud-skd
sh install.sh
```

### install 확인
```
gcloud -h
```
<img width="498" alt="image" src="https://github.com/ojwsakin/gcloud_sdk_install/assets/93701762/d2a62fe0-6771-47b5-a0ba-b1c6c053e435">


### GCP와 연동하기 위한 auth 작업 진행
```
# 아래의 작업을 진행하게 되면 링크로 연결됩니다. 링크를 통해 GCP 계정과 연동시켜줍니다.
gcloud auth login
```

### GCP Project list확인하며 잘 연동되었는지 확인
```
# GCP에 존재하는 Project list를 보여줍니다.
# 현재 저는 기본적으로 생성되어 있는 프로젝트만 존재하는 것을 확인할 수 있습니다.
gcloud projects list
```
<img width="505" alt="image" src="https://github.com/ojwsakin/gcloud_sdk_install/assets/93701762/412bd2ec-dbcb-4965-84de-2b5aeafba538">

### project와 연결
```
# 이제 인스턴스나 리소스 생성을 위해 프로젝트와 연결해줍니다.
gcloud config set project grand-xxxx-000000
```
### compute instances list 확인
```
# 아직 생성한 인스턴스는 없지만 인스턴스의 리스트를 확인할 수 있습니다.
gcloud comppute instances list
```
---
#### 여기까지 gcloud CLI 설치 방법이였습니다.
