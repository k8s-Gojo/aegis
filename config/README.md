# Config

- cloud-controller-patch.yaml: aktiviert externalCloudProvider für Hetzner Cloud Controller Manager

## Offen (nach VM-Verifizierung)
- Load Balancer anlegen (hcloud load-balancer create)
- talosctl gen config talos-aegis https://<LB-IP>:6443 --with-examples=false --with-docs=false --config-patch @cloud-controller-patch.yaml
- controlplane.yaml, worker.yaml, talosconfig werden dabei erzeugt
