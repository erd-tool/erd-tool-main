# Infra Repository

운영용 Kubernetes manifest와 GitOps 리소스는 `erd-tool-main`에 private submodule로 연결되어 있습니다.

## Source of Truth

- private repo: `erd-tool/erd-tool-k8s-manifests`

## Why It Is Private

- 운영 배포 설정과 환경별 values는 공개 저장소와 분리해야 합니다.
- public main repo에는 연결 정보만 두고, 실제 내용은 private repo 권한으로 보호합니다.

## Submodule Path

- `infra/k8s-manifests`

## Access

```bash
git submodule update --init --recursive
```

권한이 없는 계정은 `infra/k8s-manifests` submodule checkout 단계에서 접근이 제한됩니다.
