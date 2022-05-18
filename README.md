# Vagrant Images

Vagrant Images provisioned via `ansible` for Ubuntu base boxes

## Environment
- [x] __Ubuntu 20.04__
- [x] __Ubuntu 22.04__

with `docker` CLI, `docker compose v2`, `python3`, `pip`

## Usage
To use either or both of the images

### __Ubuntu 20.04__

```bash
$ cd ubuntu/2004
```

Bring machine up and provision it via `ansible`:

```bash
$ vagrant up # bring the environment up and provision it
```

To log into the image use:

```bash
$ vagrant ssh
```

If you want to delete the machine:

```bash
$ vagrant destroy
```

### __Ubuntu 22.04__

```bash
$ cd ubuntu/2204
```

Bring machine up and provision it via `ansible`:

```bash
$ vagrant up # bring the environment up and provision it
```

To log into the image use:

```bash
$ vagrant ssh
```

If you want to delete the machine:

```bash
$ vagrant destroy
```

## Development

Within each `Vagrantfile` the `ubuntu/<version>` directory on the host machine
is mapped to `/home/vagrant` direcotry in the guest machine.

Any changes made either on host or guest machine will be instantly be available
to either machine.

## System Description

### Host Machine

```bash
Linux <hostname> 5.10.114-1-MANJARO #1 SMP PREEMPT Mon May 9 07:52:55 UTC 2022 x86_64 GNU/Linux
```
### Provider 

Oracle VM Virtual Box 

```bash
Oracle VM VirtualBox VM Selector v6.1.34
```

### Provisioner

make sure to install `ansible` on the host machine.

For Manjaro Linux use:

```bash
$ sudo pamac install ansible
$ ansible --version
  ansible [core 2.12.5]
```