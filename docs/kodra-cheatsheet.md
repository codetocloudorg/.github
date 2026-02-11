# Kodra Cheat Sheet

> Your quick reference guide to Kodra's cloud-native development capabilities

---

## 🚀 What is Kodra?

Kodra is a cloud-native platform that accelerates application development and deployment workflows, providing developers and engineers with a seamless path from code to cloud.

---

## ⚡ Key Value Propositions

| Feature | Benefit |
|---------|---------|
| **One-Click Environments** | Spin up dev environments in seconds, not hours |
| **Pre-configured Toolchains** | No more "works on my machine" issues |
| **Cloud-Native by Default** | Kubernetes-ready from day one |
| **Integrated CI/CD** | Push code, deploy automatically |
| **Secure by Design** | Built-in secrets management and RBAC |

---

## 🎯 Quick Start

### Kodra (Cloud)
```bash
# Access the platform
https://kodra.codetocloud.io

# Initialize a new project
kodra init <project-name>

# Deploy to cloud
kodra deploy
```

### Kodra-WSL (Local Development)
```bash
# Access the WSL environment
https://kodra.wsl.codetocloud.io

# Start local development environment
kodra-wsl start

# Sync with cloud environment
kodra-wsl sync
```

### WSL Prerequisites

**Tested Configuration:**
- Windows 11 Pro (24H2)
- WSL2 with **Ubuntu 24.04.1 LTS** (from Microsoft Store)
- Azure VM: Standard_D4s_v5 (West US 2)

**Installation Steps:**
```powershell
# 1. Install WSL (run as Administrator)
wsl --install

# 2. Restart your machine

# 3. Install Ubuntu 24.04.1 LTS from Microsoft Store
# Or via command line:
wsl --install -d Ubuntu-24.04
```

> **⚠️ Azure VM Requirements:** If running Kodra-WSL on Azure Windows VMs:
> - Use VM sizes with nested virtualization support (Dv3, Ev3, Dv4, Ev4, Dv5, Ev5 series)
> - Windows 10/11 Pro/Enterprise is recommended for best WSL experience
> - Windows Server 2022 requires nested virtualization to be explicitly enabled

---

## 🛠️ Core Commands

| Command | Description |
|---------|-------------|
| `kodra init` | Initialize a new Kodra project |
| `kodra dev` | Start local development server |
| `kodra build` | Build container image |
| `kodra deploy` | Deploy to Kubernetes cluster |
| `kodra logs` | Stream application logs |
| `kodra status` | Check deployment status |
| `kodra rollback` | Rollback to previous version |

---

## 🔧 Environment Configuration

```yaml
# kodra.yaml
name: my-app
version: 1.0.0
runtime: node:20
resources:
  cpu: 500m
  memory: 512Mi
services:
  - name: api
    port: 3000
    replicas: 3
  - name: worker
    type: background
```

---

## 🏗️ Supported Stacks

| Language/Framework | Support Level |
|-------------------|---------------|
| Node.js / TypeScript | ✅ Full |
| Python | ✅ Full |
| Go | ✅ Full |
| .NET | ✅ Full |
| Java / Spring | ✅ Full |
| Rust | ✅ Full |
| React / Vue / Angular | ✅ Full |

---

## 🔐 Security Features

- **Secrets Management** - Encrypted secrets storage with automatic injection
- **RBAC** - Role-based access control for team collaboration
- **Network Policies** - Isolated namespaces and network segmentation
- **Compliance** - SOC2, HIPAA-ready configurations
- **Audit Logs** - Complete activity tracking

---

## 📊 Monitoring & Observability

```bash
# View real-time metrics
kodra metrics

# Access Grafana dashboards
kodra dashboard

# Export traces to your observability stack
kodra traces export --format=otlp
```

---

## 🤝 Team Collaboration

| Feature | Description |
|---------|-------------|
| **Shared Environments** | Collaborate on the same deployment |
| **Preview Deployments** | Automatic PR preview environments |
| **Branch Deployments** | Every branch gets its own URL |
| **Access Controls** | Fine-grained permissions |

---

## 💡 Pro Tips

1. **Use `.kodraignore`** to exclude files from builds
2. **Set up webhooks** for Slack/Teams notifications
3. **Enable auto-scaling** for production workloads
4. **Use `kodra doctor`** to diagnose environment issues
5. **Leverage templates** for consistent project structures

---

## 🔗 Resources

- **Kodra Cloud**: [kodra.codetocloud.io](https://kodra.codetocloud.io)
- **Kodra-WSL**: [kodra.wsl.codetocloud.io](https://kodra.wsl.codetocloud.io)
- **Documentation**: [docs.codetocloud.io](https://docs.codetocloud.io)
- **Community Discord**: [discord.gg/vwfwq2EpXJ](https://discord.gg/vwfwq2EpXJ)

---

<div align="center">

**Built with ❤️ by Code to Cloud**

*Ship It. Scale It.*

</div>
