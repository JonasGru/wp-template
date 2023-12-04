# wp-template
Paruoštukas skirtas Wordpress ir MySQL paleidimui ant OKD

# Template paleidimas iš failo per komandinę eilutę
Reikalinga turėti įsidiegus [oc komandinės eilutės įrankį](https://docs.openshift.com/container-platform/latest/cli_reference/openshift_cli/getting-started-cli.html) ir iš OKD pasiimti savo prisijungimo komandą (Prisijungus prie OKD viršuje dešinėje paspaudus ant savo naudotojo vardo pasirinkti "Copy login command". Ją panaudoti per oc komandinės eilutės įrankį).
1. Sukuriame naują projektą (galima naudoti ir jau turimą)
```bash
oc new-project projekto-pavadinimas
```
2. Pasirenkame projektą, kuriame norėsime panaudoti Template
```bash
oc project projekto-pavadinimas
```
3. Inicijuojame Template.
```bash
oc new-app wp_template.yaml -p ROUTER_CANONICAL_HOSTNAME=apps.okd-cluster2.litnet.lt
```
Gyvai pabandyti galima ant https://console-openshift-console.apps.okd-cluster2.litnet.lt/
