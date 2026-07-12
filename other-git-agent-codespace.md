# git-agent-codespace

## Intention
A **one-click development environment template** for Git-Agent runtimes — providing a pre-configured Codespace with multi-language toolchains (Python 3.12, Go 1.24, Node.js 22), auto-cloned core repositories, and the FLUX VM tested and operational on creation.

## How It Works
**Codespace templates** leverage GitHub's `devcontainer.json` specification to define container environments. The setup process:

1. **Container build**: Docker image with base toolchains (Python, Go, Node.js) is pulled or built.
2. **Post-create lifecycle hook** (`setup.sh`): Runs after container creation. Clones core repositories into the workspace:
   ```
   git clone https://github.com/SuperInstance/flux-runtime.git
   git clone https://github.com/SuperInstance/greenhorn-runtime.git
   git c

## What It's For
Onboarding a new agent (a "greenhorn") to the Git-Agent ecosystem requires a consistent, reproducible environment across Python, Go, and Node.js runtimes. Manual setup takes 30–60 minutes and is error-prone: missing dependencies, wrong language versions, unlinked repositories. This Codespace template encodes the entire setup as a `devcontainer.json` configuration with a post-create script that clo

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Shell

## Status Assessment
Documented with code examples and API references (66 line README).

## Honest Assessment
Has documentation (66 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/git-agent-codespace](https://github.com/SuperInstance/git-agent-codespace)*
