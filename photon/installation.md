# Installation

## Photon Installation

### Pre-Installation

### Installation

### Post-Installation

#### Change the Hostname 

The Hostname can be changed with:

```text
hostnamectl set-hostname photon-master
```

{% hint style="info" %}
I would not recommend using this workaround in your production environment without being directed to make this change by VMware support or officially documented by VMware.
{% endhint %}

The Output should then be:

{% code title="hostnamectl" %}
```bash
# Ain't no code for that yet, sorry
 Static hostname: photon-master
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 
           Boot ID: 
    Virtualization: vmware
  Operating System: VMware Photon OS/Linux
            Kernel: Linux 4.19.138-11.ph3-esx
      Architecture: x86-64
```
{% endcode %}

