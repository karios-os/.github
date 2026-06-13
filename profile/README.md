# Hey, this is the Karios community 👋

**Karios** is an infrastructure platform for building and operating private
clouds on FreeBSD. It brings together virtualization (bhyve VMs and jails),
networking and IPAM, Kubernetes/OpenShift integration, DNS/DHCP, and
monitoring into a single control plane with a web UI.

## Try Karios

The easiest way to experience Karios is to boot the prebuilt ISO:

- **Download**: [kariosbsd-14.3-custom.iso](https://s3.us-east-1.amazonaws.com/amzn-kariosbsd-14.3/kariosbsd-14.3-custom.iso)
- **Install**: see [INSTALL.md](./INSTALL.md) for step-by-step installation instructions

## Why Karios?

- **Run VMs and jails on FreeBSD**: Manage bhyve virtual machines and jails
  through a single API and UI, without hand-editing config files on each
  host.

- **Manage networking and IPAM**: NetBox-backed DCIM/IPAM (via
  [karios-atlas](./karios-atlas) and [karios-ipam](./karios-ipam)) for
  prefixes, IP ranges, VLANs, and VRFs, with DNS/DHCP allocation handled
  automatically.

- **Integrate with Kubernetes**: Provision and manage k3s/OpenShift clusters
  alongside traditional VMs and jails from the same platform.

- **DNS/DHCP out of the box**: Technitium-based DNS/DHCP integration keeps
  lease and reservation data in sync with your IPAM source of truth.

- **Observability built in**: Prometheus, Grafana, and InfluxDB integration
  give you metrics and dashboards for hosts, VMs, and clusters out of the
  box.

- **One UI for everything**: [karios-web](./karios-web) provides a unified
  web interface for VMs, jails, networking, clusters, and datacenter
  inventory.

## Components

This repository is the umbrella workspace for the Karios platform, made up
of several services and libraries:

| Repository | Description |
|---|---|
| [karios-apis](./karios-apis) | Backend REST API — VM/jail management, networking, Kubernetes integration, monitoring |
| [karios-web](./karios-web) | Web GUI (React / Nx monorepo) |
| [karios-ipam](./karios-ipam) | IPAM/DDI orchestration library (NetBox + Technitium) |
| [karios-atlas](./karios-atlas) | NetBox DCIM/IPAM Go SDK |
| [karios-common](./karios-common) | Shared logging, tracing, metrics, and middleware library |

Each component has its own README with setup, build, and environment
variable details.

## Documentation

See each component's README for setup and usage instructions:

- [karios-apis](./karios-apis/README.md)
- [karios-web](./karios-web/README.md)
- [karios-ipam](./karios-ipam/README.md)
- [karios-atlas](./karios-atlas/README.md)
- [karios-common](./karios-common/README.md)

## Community

Issues, discussions, and contributions are welcome — see the issue tracker
for each repository above.
