## github actions 로 배포하기

### CI CD 간단 요약
- CI → 레퍼지토리 (깃헙등 코드 버전관리) push / merge 되었을때 자동으로 빌드 및 유닛 테스트(필요에 따라)    
- CD → CI를 통한 결과물 (빌드된 도커 이미지 등) 서버에 자동으로 배포

### CI CD 간단 큰 그림
- 로컬에서 코드 작업 → 깃 푸시 → **트리거** 발동 빌드 or 유닛 테스트 → 사용하는 **서버에 배포**
- 이것들을 자동으로 하게끔 해주는 것
> 트리거 역할 해줄때 **허스키**를 사용하는 경우도 있음 의외였음….
```text
    예전에는 프론트 서버가 따로 존재하지 않았지만
    SPA의 등장으로 CSR 방식의 웹 어플리케이션이 대다수를 이루면서
    프론트 서버와 백엔드 서버에 분리가 이루어짐 

    프론트 CI CD는 간단하게 말해 React 나 Vue 등으로 만든 Javascript 파일을 잘 번들링 빌드해서 
    html 파일 하나 잘 빌드된 (번들링된) js 파일들 마찬가지로 잘 번들링된 CSS 파일들을
    서버에 올려놓는다라고 생각하면 될듯
```

### 시중에 대표적인 ci cd 플랫폼

- CircleCI
    
    [Continuous Integration and Delivery](https://circleci.com/)
    
- ArgoCD
    - manifest 파일을 계속 감시 해서 서버에 배포 주안을 둔 플랫폼
    - 요즘 핫한 Kubernets(쿠버네티스)를 위한 CD 플랫폼
    
    [Argo CD](https://argoproj.github.io/cd/)
    
- github action
    
    [GitHub.com Help Documentation](https://docs.github.com/en)
    
- Jenkins
    - CI 서버 개념이 등장 , 선행 지식이 많이 필요함
    
    [Jenkins](https://www.jenkins.io/)
    

### **DOCKER** 도커 (feat_ 쿠버네티스)

[쿠버네티스 알아보기 1편: 쿠버네티스와 컨테이너, 도커에 대한 기본 개념](https://www.samsungsds.com/kr/insights/220222_kubernetes1.html)

```text
    컨테이너 용어 설명과 추가로 핫한 쿠버네티스 지식도 얕게  파악 할 수있는 좋은 자료
    기존 next.js 프로젝트의 CI/CD는 Jenkins로 빌드후 ECR에 docker image 올려주고
    argocd 가 ECR을 바라보고 변경되면 해당 docker image를 배포 해주는 형태
    Jenkins 의 보안이슈 등 여러가지 문제로 github actions migration 결정
```
