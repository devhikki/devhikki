# hi, i'm hikki

Field telecom engineer by day. At night I run a small homelab and write down what breaks.

```text
$ whoami
hikki — telecom · homelab · android · monitoring
$ cat ~/.plan
make the lab boring: everything observed, everything restorable
```

I keep a lab journal at [hikki.dev](https://hikki.dev) — one note per solved problem,
with the commands, what was verified and what wasn't.

### in the lab

Most of this lives on my own Forgejo and moves here once it's cleaned up for public view.

| project | what it does | stack | here? |
|---|---|---|---|
| **pve-telegram-relay** | Alertmanager → Telegram with Zabbix-style alerts: one message per problem, edited in place on resolve, reply on recovery, quiet hours, anti-flap, on-disk queue with retries, bearer-auth intake. Read-only bot commands with sparkline graphs. | Python · 500+ tests | soon |
| **lab monitoring** | Prometheus + Alertmanager + Grafana over a Proxmox host: SMART, kernel DMAR/ATA/FS error counters, backup freshness (vzdump, restic), UPS via NUT, a dead-man's switch for the monitoring chain itself. | Prometheus · bash | — |
| **node probes** | Hourly probes of upstream network nodes: liveness, latency, exit checks, exported as Prometheus metrics; a picker that ranks nodes per service and drafts routing changes for review. | Python · Prometheus | later |
| **tfwatch** | Fork of tfdog: watches TestFlight public betas and pings Telegram when a seat opens. Per-link state and backoff, open / full / closed detection. | Go · AGPL-3.0 | soon |
| **hikki.dev** | This site. Static pages on Cloudflare Pages, a Worker for the now-playing widget, strict CSP, no trackers. | HTML · JS · Workers | — |
| [cifar10-resnet18-pytorch](https://github.com/devhikki/cifar10-resnet18-pytorch) | CIFAR-10 with ResNet-18, MixUp, evaluation tools and a Gradio demo. | Python · PyTorch | ✓ |

### how i work

- every change to a box gets a backup, a rollback and a check — before, not after
- configs live in git, including the router's
- "it works" means the check ran and its output is in front of me

[telegram](https://t.me/devhikki) · [hikki.dev](https://hikki.dev)
