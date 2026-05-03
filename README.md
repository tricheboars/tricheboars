<div align="center">

```
                  _            _      _
 _ __   __ _  __ _| |_ _ __(_) ___| | __ | |_ __ ___   ___   ___  _ __ ___
| '_ \ / _` |/ _` | __| '__| |/ __| |/ / | __/ _` \ \ / / |/ _ \| '__/ _ \
| |_) | (_| | (_| | |_| |  | | (__|   <  | || (_| |\ V /| | (_) | | |  __/
| .__/ \__,_|\__,_|\__|_|  |_|\___|_|\_\  \__\__,_| \_/ |_|\___/|_|  \___|
|_|
```

`●` **moorelab.cloud** &nbsp;//&nbsp; online

**cloud · cybersecurity · ai engineer**

</div>

> i ship infrastructure and ai agents for an *oncology emr* by day, and run an over-engineered homelab by night. *two-node ha firewall*, *fully segmented*, *no cloud bill*. this readme lives on github — but the rest of me lives at [moorelab.cloud](https://moorelab.cloud).

---

### `/about`

cloud engineer. cybersecurity engineer. ai engineer. currently leading internal ai engineering for a healthcare oncology platform — building production claude agents into the engineering workflow (pr review, design review, triage); patching, hardening, and shipping at the same time.

outside of work i'm a husband, a father of two, and an avid tinkerer. my stack spans linux, bsd, macos, and a healthy stack of lxc containers running on proxmox. i learn by building. lately, that means a lot of generative coding alongside claude.

---

### `/stack`

![Python](https://img.shields.io/badge/python-0a0a0a?style=flat-square&logo=python&logoColor=00ff41&labelColor=0a0a0a)
![Go](https://img.shields.io/badge/go-0a0a0a?style=flat-square&logo=go&logoColor=00ff41&labelColor=0a0a0a)
![TypeScript](https://img.shields.io/badge/typescript-0a0a0a?style=flat-square&logo=typescript&logoColor=00ff41&labelColor=0a0a0a)
![Bash](https://img.shields.io/badge/bash-0a0a0a?style=flat-square&logo=gnubash&logoColor=00ff41&labelColor=0a0a0a)
![Linux](https://img.shields.io/badge/linux-0a0a0a?style=flat-square&logo=linux&logoColor=00ff41&labelColor=0a0a0a)
![Proxmox](https://img.shields.io/badge/proxmox-0a0a0a?style=flat-square&logo=proxmox&logoColor=00ff41&labelColor=0a0a0a)
![OPNsense](https://img.shields.io/badge/opnsense-0a0a0a?style=flat-square&logo=opnsense&logoColor=00ff41&labelColor=0a0a0a)
![Terraform](https://img.shields.io/badge/terraform-0a0a0a?style=flat-square&logo=terraform&logoColor=00ff41&labelColor=0a0a0a)
![Docker](https://img.shields.io/badge/docker-0a0a0a?style=flat-square&logo=docker&logoColor=00ff41&labelColor=0a0a0a)
![nginx](https://img.shields.io/badge/nginx-0a0a0a?style=flat-square&logo=nginx&logoColor=00ff41&labelColor=0a0a0a)
![HAProxy](https://img.shields.io/badge/haproxy-0a0a0a?style=flat-square&logo=haproxy&logoColor=00ff41&labelColor=0a0a0a)
![Cloudflare](https://img.shields.io/badge/cloudflare-0a0a0a?style=flat-square&logo=cloudflare&logoColor=00ff41&labelColor=0a0a0a)
![WireGuard](https://img.shields.io/badge/wireguard-0a0a0a?style=flat-square&logo=wireguard&logoColor=00ff41&labelColor=0a0a0a)
![Ollama](https://img.shields.io/badge/ollama-0a0a0a?style=flat-square&logo=ollama&logoColor=00ff41&labelColor=0a0a0a)
![Claude](https://img.shields.io/badge/claude-0a0a0a?style=flat-square&logo=anthropic&logoColor=00ff41&labelColor=0a0a0a)
![FastAPI](https://img.shields.io/badge/fastapi-0a0a0a?style=flat-square&logo=fastapi&logoColor=00ff41&labelColor=0a0a0a)

---

### `/projects`

| project | what it is | status |
|---|---|---|
| **[H@ck3r-Z0rk](https://github.com/tricheboars/Hack3r-Z0rk)** &nbsp; · &nbsp; [▸ play](https://hackerzork.moorelab.cloud/play) | mr. robot meets zork. real linux commands, simulated unix, an ai antagonist that learns from everything you type. | `live` |
| **[BitCoinTrader](https://github.com/tricheboars/BitCoinTrader)** &nbsp; · &nbsp; [▸ play](https://bitcointrader.moorelab.cloud/) | gag finance trading game. wall street meets wsb — buy a bitcoin for a dollar, get rugged by $rugz. | `live` |
| **[moorelab-website](https://github.com/tricheboars/moorelab-website)** &nbsp; · &nbsp; [↗](https://moorelab.cloud) | the page you should actually be on. plain html/css/js, single source of truth. self-hosted. | `live` |
| **OpenClaw** &nbsp; · &nbsp; [↗](https://openclaw.moorelab.cloud) | self-hosted ai workspace with cybersec focus — rag, automated cve digesting, telegram alerting. | `live` |
| **moorelab homelab** &nbsp; · &nbsp; [↗](https://moorelab.cloud/#lab) | ha opnsense pair on proxmox, full vlan segmentation, wireguard, haproxy + le wildcard, pi-hole. | `live` |

---

### `/lab`

```
┌──────────────────────────┬──────────────────────────┐
│  proxmox nodes      :  2 │  zones · ha         :  7 │
├──────────────────────────┼──────────────────────────┤
│  vms & containers   : 19 │  monthly cloud bill : $0 │
└──────────────────────────┴──────────────────────────┘
```

- **ha firewall.** opnsense pair with carp failover. state sync over a dedicated link.
- **public ingress.** haproxy with let's encrypt dns-01 wildcard, path-based routing, split-dns for hairpin avoidance.
- **vpn.** wireguard server with split-tunnel and cloudflare ddns so the endpoint always resolves.
- **dns.** two pi-holes behind dnsmasq in `all-servers` mode for first-answer-wins.
- **ai cluster.** ollama running qwen + openwebui + a custom cybersec stack that auto-digests cves nightly.
- **maintenance.** weekly cron on every host, staggered so ha partners never reboot together.

---

### `/stats`

<a href="https://github.com/tricheboars">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=tricheboars&show_icons=true&hide_border=true&title_color=00ff41&icon_color=00ff41&text_color=f5f5f7&bg_color=0a0a0a" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=tricheboars&layout=compact&hide_border=true&title_color=00ff41&text_color=f5f5f7&bg_color=0a0a0a" />
</a>

---

### `/contact`

| | |
|---|---|
| `site`     | [moorelab.cloud](https://moorelab.cloud) |
| `linkedin` | [linkedin.com/in/patrick-moore](https://www.linkedin.com/in/patrick-moore-25a13a16/) |
| `email`    | Patrick.James.Moore@protonmail.com |
| `email · alt` | tricheboars@gmail.com |

---

<div align="center">

`moorelab.cloud · patrick moore · 2026`

`opnsense` &nbsp; `haproxy` &nbsp; `nginx` &nbsp; `self-hosted`

</div>
