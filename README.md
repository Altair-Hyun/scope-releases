# Scope

Open Source Kubernetes IDE, forked from [OpenLens](https://github.com/Open-Lens/lens).

Powered by [Electron](https://www.electronjs.org/) and [React](https://reactjs.org/). Licensed under [MIT](./LICENSE).

## Download

Go to the [Releases](https://github.com/Altair-Hyun/scope-releases/releases) page and download the latest version for your platform.

| Platform | File |
|----------|------|
| macOS (Apple Silicon) | `Scope-*-arm64.dmg` |
| macOS (Intel) | `Scope-*-x64.dmg` |
| Windows | `Scope-*-x64.exe` |

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
| kubectl | 1.35.0 |
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

## License

[MIT](./LICENSE)
