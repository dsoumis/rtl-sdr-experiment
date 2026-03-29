# RTL-SDR Experiment

A personal experiment repo for learning RTL-SDR progressively through hands-on projects on Fedora Linux.

## Setup

Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html), then run:

```bash
# Install RTL-SDR drivers and Python SDR libraries
ansible-playbook ansible/playbook.yml --tags base,python-sdr
```

Unplug and re-plug the RTL-SDR dongle after the first run (udev rules need a re-trigger).

## Projects

| # | Project | Category | Description |
|---|---------|----------|-------------|
| 01 | [Hello Spectrum](projects/01-hello-spectrum/) | spectrum | Verify dongle, capture samples, plot frequency spectrum |

## Adding a new project

1. Create `projects/NN-project-name/` with a `README.md` following the lab notebook format
2. If it needs new dependencies, add an Ansible role under `ansible/roles/` and tag it in `ansible/playbook.yml`
3. Update the project table above
