# 🎉 **SoftBank Hackathon 2025 Final**
    
>  **Theme - *Run Functions Instantly over HTTP***

Lambda나 Cloud Run처럼, 서버리스 함수는 배포 없이 즉시 실행되는 개발 경험을 제공합니다.<br>
이번 해커톤의 목표는 이러한 Serverless 모델을 직접 EC2/Kubernetes 위에서 구현하는 것이었습니다.


<br>

---

# 🍀 Team Green

<div align="center">
    <strong>🏆 SoftBank Hackathon 2025 Final — Second Prize Winner</strong>
</div>

<br>

<table align="center" style="table-layout: fixed; width: 100%;"> <tr> <td align="center"><img width="120" src="https://github.com/drghdtjr.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/DuckOriDuck.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/jiu-jung.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/hjs0410hc.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/Clear-Wisdom.png" style="border-radius:50%;" /></td> </tr> <tr> <td align="center" style="padding-top:10px;"> <b>김홍석</b><br> <sub><a href="https://github.com/drghdtjr">@drghdtjr</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>서창덕</b><br> <sub><a href="https://github.com/DuckOriDuck">@DuckOriDuck</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>정지우</b><br> <sub><a href="https://github.com/jiu-jung">@jiu-jung</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>현진섭</b><br> <sub><a href="https://github.com/hjs0410hc">@hjs0410hc</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>황서호</b><br> <sub><a href="https://github.com/Clear-Wisdom">@Clear-Wisdom</a></sub> </td> </tr> </table> <br>

<br>

---


# 🚀 Cutty-X: Lightweight & User-Friendly FaaS
> Knative 기반 Lightweight Runtime + Developer-Friendly Workflow

Cutty-X는 FaaS의 핵심 가치인 **개발자 편의성**과 **프로바이더 효율성**을 중심으로 설계되었습니다.

### 👨‍💻 For Developers — *Convenience & Observability*
- 코드만 제출하면 자동 빌드·배포되는 **Zero-Config Build**
- 함수 관계를 시각적으로 보여주는 **Bounding-Box Diagram**
- 배포 전 오류를 잡아주는 **AI Code Assistant**

<br>

### 🏗️ For Provider — *Efficiency & Isolation*
- **k3s** 기반 경량 Control Plane으로 낮은 비용 · 빠른 부팅
- **gVisor Sandbox**로 안전한 멀티테넌시
- **Cluster-level Logging** 기반 경량 운영 가시성 확보

<br>


---

# 💡 Why Cutty-X? (Key Strengths)

### **1. Zero Config, Just Code**
> 개발자는 오직 코드에만 집중하면 됩니다.  
- **No Dockerfile:** Buildpacks가 의존성·환경을 자동 감지  
- **One-Click Deploy:** Build → Push → Deploy 완전 자동화  

### **2. Instant Execution**
> 배포된 함수는 HTTP 요청에 즉시 반응합니다.
- **Auto Routing:** 각 함수마다 고유 Endpoint 자동 생성  
- **Scale-to-Zero:** 요청 없으면 0, 요청 시 즉시 기동  

### **3. Efficient & Secure**
> 효율성과 보안을 동시에 잡았습니다.
- **k3s 경량 제어평면:** 불필요한 리소스 소모 최소화  
- **gVisor Sandbox:** 커널 격리로 강력한 멀티테넌시 보안  
<br>

---

# **🛠 Technical Architecture Highlights**

Cutty-X가 이 강점들을 어떻게 기술적으로 구현했는지 소개합니다.

### ⚡️ **Run: Knative 기반 Serverless Orchestration**

> *"Cloud Run의 핵심 기술을 직접 구현"*

  * **Mechanism:** Knative Serving을 활용하여 트래픽 기반의 오토스케일링과 리비전(Revision) 관리를 구현했습니다.
  * **Benefit:** 트래픽이 몰려도 안정적으로 처리하며, 무중단 배포를 지원합니다.

### 🏗️ **Build: Buildpacks + SQS 비동기 파이프라인**

> *"Dockerfile 없는 세상"*

  * **Mechanism:** AWS SQS와 CodeBuild를 연동하여 빌드 요청을 비동기로 처리합니다. Buildpacks가 코드를 분석해 최적의 이미지를 생성합니다.
  * **Benefit:** 대규모 빌드 요청이 들어와도 큐(Queue)를 통해 안정적으로 처리하며, 개발자는 이미지 빌드 과정에서 완전히 해방됩니다.

### 🛡️ **Core: k3s + gVisor Secure Runtime**

> *"빠르고 안전한 샌드박스"*

  * **Mechanism:** 일반 컨테이너 런타임(runc) 대신 gVisor(runsc)를 런타임 클래스로 지정하여 커널 레벨의 격리를 수행합니다.
  * **Benefit:** EC2 위에서도 안심하고 여러 사용자의 코드를 동시에 실행할 수 있는 **Provider-Friendly** 환경을 완성했습니다.

<br>

---

# **🧰 Main Tech Stack**

### 🧠 Core Runtime
<div> <img src="https://img.shields.io/badge/Knative-0865AD?style=for-the-badge&logo=knative&logoColor=white"/> <img src="https://img.shields.io/badge/k3s-FFC61C?style=for-the-badge&logo=kubernetes&logoColor=black"/> <img src="https://img.shields.io/badge/gVisor-4285F4?style=for-the-badge&logo=google&logoColor=white"/> </div>

### 🚀 Build & Deployment
<div> <img src="https://img.shields.io/badge/Cloud%20Native%20Buildpacks-3C3C3C?style=for-the-badge&logo=cloudfoundry&logoColor=white"/> <img src="https://img.shields.io/badge/AWS%20CodeBuild-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white"/> <img src="https://img.shields.io/badge/SQS-EE4F3D?style=for-the-badge&logo=amazon-aws&logoColor=white"/> </div>

### 🔭 Observability
<div> <img src="https://img.shields.io/badge/FluentBit-0E83C8?style=for-the-badge&logo=fluentbit&logoColor=white"/> <img src="https://img.shields.io/badge/Athena-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white"/> </div>
<br>

---

# 📂 Repository Structure

| 저장소                | 설명                                                       |
| ------------------ | -------------------------------------------------------- |
| **[infra](./infra)**          | Terraform Cloud로 AWS 인프라를 IaC 방식으로 관리합니다.                |
| **[web](./web)**            | Next.js 기반 Amplify 앱으로, 함수 생성·배포 UI를 제공합니다.              |
| **[codebuild-repo](./codebuild-repo)** | Cloud Native Buildpacks와 CodeBuild 빌드 파이프라인 스크립트를 포함합니다. |
| **[manifest](./manifest)**       | k3s 상에서 실행되는 Knative 및 서비스 매니페스트를 관리합니다.                 |



