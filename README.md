# srv6-usid-aidc

A simple **Containerlab + Juniper cJunosEvolved** demo of an **SRv6 uSID (micro-SID)** spine–leaf fabric for **AI-backend deterministic path placement**.

## What’s in this repo
- `usid-sl-cevo.yml` — Containerlab topology
- `s1.conf`, `s2.conf` — spine configs
- `l1.conf`, `l2.conf` — leaf configs
- `usidspineleaf.drawio` — topology diagram
- `ops-cli` — helper script/CLI (optional)

## Prerequisites
- Linux host with **Docker** + **Containerlab**
- **CPU virtualization** enabled (KVM/nested virt) for cJunosEvolved
- cJunosEvolved image available locally

## Quickstart
```bash
git clone https://github.com/hmali/srv6-usid-aidc.git
cd srv6-usid-aidc
sudo clab deploy -t usid-sl-cevo.yml

Basic checks (examples)

sudo clab inspect -t usid-sl-cevo.yml
sudo clab exec -t usid-sl-cevo.yml --name s1 -- cli

References

cEVO Image https://support.juniper.net/support/downloads/?p=cjunos-evolved

IETF draft: SRv6 for Deterministic Path Placement in AI Backends
https://datatracker.ietf.org/doc/draft-filsfils-srv6ops-srv6-ai-backend/

Juniper blog: SRv6 Micro-SID (uSID) Basics
https://community.juniper.net/blogs/krzysztof-szarkowicz/2025/09/30/srv6-micro-sid-basics

