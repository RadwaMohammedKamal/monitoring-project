---

## Monitoring Architecture

- **Node Exporter**: collects CPU, RAM, and system metrics from the VM.
- **Prometheus**: scrapes metrics from Node Exporter at intervals.
- **Alertmanager**: receives alerts from Prometheus if metrics exceed thresholds.
- **Grafana**: visualizes Prometheus metrics in dashboards.

**Ports:**

| Component       | Container | Port       |
|-----------------|-----------|------------|
| Prometheus      | Podman    | 9090       |
| Alertmanager    | Podman    | 9093       |
| Grafana         | Podman    | 3000       |
| Node Exporter   | Podman    | 9100       |

---

## Inventory

`inventory/hosts`:

```ini
[monitoring]
localhost ansible_connection=local

