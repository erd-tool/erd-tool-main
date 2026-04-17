# ERD Tool Main Repository

이 저장소는 ERD Tool 시스템의 공개 진입점입니다.

> [!IMPORTANT]
> 이 저장소가 현재 canonical entrypoint 입니다.
> 기존 `monorepo` 저장소는 reference-only 용도로 유지하며, 신규 개발/배포 기준은 `erd-tool-main + submodules` 입니다.

## Repository Layout

- `apps/frontend`: 프론트엔드 애플리케이션
- `infra/k8s-manifests`: private Kubernetes manifest 및 GitOps 리소스
- `services/gateway-service`: API gateway
- `services/auth-service`: 인증 서비스
- `services/team-service`: 팀 서비스
- `services/erd-service`: ERD 서비스
- `services/collaboration`: 실시간 협업 서비스
- `packages/backend-common`: 공통 Java 라이브러리

운영용 Kubernetes manifest는 private submodule로 연결되어 있습니다. 자세한 내용은 [docs/infra.md](docs/infra.md)를 참고하세요.

## Getting Started

```bash
git clone https://github.com/erd-tool/erd-tool-main.git
cd erd-tool-main
git submodule update --init --recursive
```

private `infra/k8s-manifests` submodule은 접근 권한이 있는 계정에서만 초기화할 수 있습니다.

각 하위 저장소의 빌드/실행 방법은 해당 submodule의 README 또는 repo 내부 build 설정을 기준으로 따릅니다.
