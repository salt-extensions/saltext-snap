# Installation

Generally, extensions need to be installed into the same Python environment Salt uses.

:::{tab} State
```yaml
Install Salt Snap extension:
  pip.installed:
    - name: saltext-snap
```
:::

:::{tab} Onedir installation
```bash
salt-pip install saltext-snap
```
:::

:::{tab} Regular installation
```bash
pip install saltext-snap
```
:::

:::{important}
Currently, there is [an issue][issue-second-saltext] where the installation of a Saltext fails silently
if the environment already has another one installed. You can workaround this by
removing all Saltexts and reinstalling them in one transaction.
:::

:::{hint}
Saltexts are not distributed automatically via the fileserver like custom modules, they need to be installed
on each node you want them to be available on.
:::

[issue-second-saltext]: https://github.com/saltstack/salt/issues/65433
