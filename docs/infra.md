# Infra Repository

운영용 Kubernetes manifest와 GitOps 리소스는 public main repo에 포함하지 않습니다.

## Source of Truth

- private repo: `erd-tool/erd-tool-k8s-manifests`

## Why It Is Separate

- 운영 배포 설정과 환경별 values는 공개 저장소와 분리해야 합니다.
- public main repo는 온보딩, 통합 문서, 로컬 오케스트레이션, public source linking에 집중합니다.

## Access

권한이 있는 계정으로 별도 checkout 해서 사용합니다.

```bash
git clone https://github.com/erd-tool/erd-tool-k8s-manifests.git
```
