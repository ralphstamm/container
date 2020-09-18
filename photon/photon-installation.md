# Photon Installation

## Getting Super Powers

### Change the Hostname [^1]

Changing Hostname of the appliance is easy:

```
hostnamectl set-hostname photon-master
```

{% hint style="info" %}
 I would not recommend using this workaround in your production environment without being directed to make this change by VMware support or officially documented by VMware.
{% endhint %}

Once you're strong enough, save the world:

{% code title="hello.sh" %}
```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```
{% endcode %}



[^1]: https://pingforinfo.com/change-hostname-of-vcloud-director-appliance/
