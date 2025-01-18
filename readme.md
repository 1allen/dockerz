# Self-Hosted Setup README

## Overview

This repository provides a comprehensive **self-hosted setup** designed for personal and educational use. It includes various pre-configured self-hosted services managed with Docker, **Traefik** for reverse proxying, and **Watchtower** for automated container updates.

---

## Prerequisites

1. **Install Docker**:  
   Use this one-liner to install Docker quickly:

```shell script
curl -fsSL https://gist.github.com/1allen/ecb5353c92ea22f1843f91cad4ce3b52 | bash
```

The script is well-documented and can also be followed as a step-by-step guide if needed.

2. **Create the Traefik Network**:  
   The setup relies on an **external Docker network** named `traefik`. Create it using the following command:

```shell script
docker network create traefik
```

---

## Watchtower Integration

This setup uses **Watchtower** to automate container updates. To enable Watchtower for specific containers, ensure they include the following label in their configuration:

```yaml
labels:
  - "com.centurylinklabs.watchtower.enable=true"
```

---

## Getting Started

1. Ensure Docker is installed (use the script above).
2. Create the required `traefik` network.
3. Deploy and start the stack using the Docker configurations provided in this repository.

---

## Included Services

The self-hosted setup includes a variety of useful services for personal and educational use. These services are pre-configured to work seamlessly with Traefik for routing and Watchtower for container updates. Feel free to explore and customize the stack to meet your needs.

---

## Notes

- **Traefik**:  
  Traefik serves as the core reverse proxy, handling the routing of all services. Ensure its configuration aligns with your environment.

- **Watchtower**:  
  Containers must include the `com.centurylinklabs.watchtower.enable=true` label to be automatically updated.

- **Customization**:  
  You can inspect and adjust the provided Docker configurations to suit your unique setup.

---

## Final Thoughts

This self-hosted stack is a simple and robust way to deploy and manage helpful services for personal or educational use. Get started today and enjoy the benefits of running your own self-hosted tools! 🚀