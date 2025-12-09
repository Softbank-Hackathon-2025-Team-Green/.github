# 🎉 **SoftBank Hackathon 2025 Final**
    
>  **Theme - *Run Functions Instantly over HTTP***

Lambda나 Cloud Run처럼, 서버리스 함수는 배포 없이 즉시 실행되는 개발 경험을 제공합니다.<br>
이번 해커톤의 목표는 이러한 Serverless 모델을 직접 EC2/Kubernetes 위에서 구현하는 것이었습니다.


<br>

---

# 🍀 Team Green

<div align="center">
  <h3>🏆 SoftBank Hackathon 2025 Final — Second Prize Winner</h3>
    <img width="681" height="491" alt="image" src="https://github.com/user-attachments/assets/ce2093ad-b733-42c4-847e-1c7a24956b90" />

</div>

<table align="center" style="table-layout: fixed; width: 100%;"> <tr> <td align="center"><img width="120" src="https://github.com/drghdtjr.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/DuckOriDuck.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/jiu-jung.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/hjs0410hc.png" style="border-radius:50%;" /></td> <td align="center"><img width="120" src="https://github.com/Clear-Wisdom.png" style="border-radius:50%;" /></td> </tr> <tr> <td align="center" style="padding-top:10px;"> <b>김홍석</b><br> <sub><a href="https://github.com/drghdtjr">@drghdtjr</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>서창덕</b><br> <sub><a href="https://github.com/DuckOriDuck">@DuckOriDuck</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>정지우</b><br> <sub><a href="https://github.com/jiu-jung">@jiu-jung</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>현진섭</b><br> <sub><a href="https://github.com/hjs0410hc">@hjs0410hc</a></sub> </td> <td align="center" style="padding-top:10px;"> <b>황서호</b><br> <sub><a href="https://github.com/Clear-Wisdom">@Clear-Wisdom</a></sub> </td> </tr> </table> <br>

<br>

---


# 🚀 Cutty-X: Lightweight & User-Friendly FaaS
> Knative 기반 Lightweight Runtime + Developer-Friendly Workflow

Cutty-X는 FaaS의 핵심 가치인 **개발자 편의성**과 **프로바이더 효율성**을 중심으로 설계되었습니다.

### 👨‍💻 For Developers — *Convenience & Observability*
- 코드만 제출하면 자동 빌드·배포되는 buildpacks 기반 **Zero-Config Build**
- 함수 관계를 시각적으로 보여주는 **Bounding-Box Diagram**
- 배포 전 오류를 잡아주는 **AI Code Assistant**

<br>

### 🏗️ For Provider — *Efficiency & Isolation*
- **k3s** 기반 경량 Control Plane으로 낮은 비용 · 빠른 부팅
- **gVisor Sandbox**로 안전한 멀티테넌시
- **Cluster-level Logging** 기반 경량 운영 가시성 확보

<br>


---

# **🧰 Core Tech Stack**

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
| **[infra](https://github.com/Softbank-Hackathon-2025-Team-Green/infra)**          | Terraform Cloud로 AWS 인프라를 IaC 방식으로 관리합니다.                |
| **[web](https://github.com/Softbank-Hackathon-2025-Team-Green/web)**            | Next.js 기반 Amplify 앱으로, 함수 생성·배포 UI를 제공합니다.              |
| **[codebuild-repo](https://github.com/Softbank-Hackathon-2025-Team-Green/codebuild-repo)** | Cloud Native Buildpacks와 CodeBuild 빌드 파이프라인 스크립트를 포함합니다. |
| **[manifest](https://github.com/Softbank-Hackathon-2025-Team-Green/manifest)**       | k3s 상에서 실행되는 Knative 및 서비스 매니페스트를 관리합니다.                 |



