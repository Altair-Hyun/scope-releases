# Scope

<!-- DEVELOPMENT-HISTORY-2026 -->
[2026 개발 이력 및 변경 근거](docs/development-history/README.md) · 원본 변경 기록을 바탕으로 2026-11-09 정리
<!-- /DEVELOPMENT-HISTORY-2026 -->


Open Source Kubernetes IDE, forked from [OpenLens](https://github.com/Open-Lens/lens).

Powered by [Electron](https://www.electronjs.org/) and [React](https://reactjs.org/). Licensed under [MIT](./LICENSE).

## Download

Go to the [Releases](https://github.com/Altair-Hyun/scope-releases/releases) page and download the latest version for your platform.

| Platform | File |
|----------|------|
| macOS (Apple Silicon) | `Scope-*-arm64.dmg` |
| Windows (x64) | `Scope-Setup-*.exe` |

macOS 는 코드 서명이 없어 첫 실행이 차단될 수 있습니다. 설치한 뒤 터미널에서 `xattr -cr /Applications/Scope.app` 을 실행하세요.

## Bundled Extensions

| Extension | Description |
|-----------|-------------|
| [Node Pod Menu](https://github.com/alebcay/openlens-node-pod-menu) | Node and Pod context menu (Logs, Shell, Attach) |
| [Multi Pod Logs](https://github.com/andrea-falco/lens-multi-pod-logs) | Get logs from multiple pods and containers |
| [Certificate Info](https://github.com/jkroepke/lens-certificate-info) | Certificate expiry info from secrets |
| [NetworkPolicy Viewer](https://github.com/artturik/lens-extension-network-policy-viewer) | Visual graph of NetworkPolicy manifests |
| [Bunyan Log Viewer](https://github.com/jdinsel-xealth/bunyan-lens-ext) | View bunyan-formatted logs |
| [Resource Map](https://github.com/nevalla/lens-resource-map-extension) | Visualisation of Kubernetes resources and relations |

## Bundled Binaries

| Binary | Version |
|--------|---------|
| kubectl | 1.34.5 |
| Helm | 3.19.5 |
| lens-k8s-proxy | 0.3.1 |

## Features

### Catalog
- **Checkbox multi-select** with bulk actions (folder move, kubeconfig export)
- **Kubeconfig YAML export**: merge and download selected clusters' kubeconfig
- **Offline distro detection**: EKS, GKE, AKS, DigitalOcean, Alibaba, Huawei, Tencent, NCloud, OpenShift without cluster connection
- **Cluster API (CAPI)** management cluster detection
- **Duplicate cluster deduplication** across multiple kubeconfig files
- **Column resize** via drag on table headers
- **N-level nested folders** in hotbar and catalog

### Helm Charts
- **Refresh button** and repository update caching
- **Parallel loading** for chart README and versions

## 패치노트

<!-- AUTO-APPEND: 태그 push마다 이 줄 바로 아래에 최신 릴리스 섹션이 추가됩니다. -->
### v1.3.20 — 2026-11-25

**변경**
- 앱의 기반인 Electron 을 22 에서 45 로 올렸습니다. 최신 Chromium 과 Node.js 위에서 동작합니다.
- 화면을 그리는 React 를 17 에서 19 로 올렸습니다.
- 클러스터 화면을 옮겨 다닐 때 이벤트 목록을 매번 다시 받지 않습니다. 파드·디플로이먼트 같은 목록과 상세 패널 사이를 오가는 것이 가벼워졌습니다.
- 클러스터 전체 조회 권한이 있으면 연결할 때 네임스페이스마다 권한을 묻지 않습니다. 네임스페이스가 많은 클러스터에서 연결이 빨라집니다.

### v1.3.19 — 2026-11-24

**추가**
- 목록에서 체크박스로 고르면 머리줄에 고른 개수가 함께 보입니다. 카탈로그와 모든 리소스 목록에 적용됩니다.
**변경**
- 앱 아이콘과 메뉴 막대 트레이 아이콘을 Scope 아이콘으로 바꿨습니다.
- 앱을 켤 때 뜨는 로딩 화면을 새 Scope 로고와 진행 막대로 바꿨습니다.
- 첫 화면(Welcome)을 카드 형식으로 바꾸고, 주요 기능을 한눈에 볼 수 있게 했습니다.
- Windows 설치 파일 이름이 공백 없는 Scope-Setup-버전.exe 로 바뀝니다.
- App 목록을 Pod 같은 다른 리소스 목록과 같은 표로 바꿨습니다. 검색, 네임스페이스 고르기, 열 정렬과 숨기기를 쓸 수 있습니다. Edit 는 각 행의 메뉴로, 삭제는 다른 목록처럼 목록 아래 휴지통 버튼으로 옮겼습니다.
**수정**
- Prometheus Operator(kube-prometheus-stack)로 모니터링을 설치한 클러스터에서 메트릭 제공자를 찾지 못해 차트가 비거나 값이 틀리던 문제를 고쳤습니다.


## License

[MIT](./LICENSE)
