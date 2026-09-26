# Pubblicare su `wizardmorgan/nebbie-mudlet-dashboard`

Il **cloud agent** può pushare solo su `nebbietest`, non sul repo personale (GitHub risponde `403` per `cursor[bot]`).

Il codice aggiornato è già su GitHub nel branch:

**https://github.com/wizardmorgan/nebbietest/tree/nebbie-mudlet-dashboard**

## Copia nel repo personale (da PC, una tantum)

Con [GitHub CLI](https://cli.github.com/) loggato come **wizardmorgan**:

```bash
git clone --branch nebbie-mudlet-dashboard --single-branch \
  https://github.com/wizardmorgan/nebbietest.git nebbie-mudlet-dashboard
cd nebbie-mudlet-dashboard
git remote remove origin
git remote add origin https://github.com/wizardmorgan/nebbie-mudlet-dashboard.git
git push -u origin main
```

Se il repo personale ha già un commit iniziale (README), usa:

```bash
git push -u origin main --force
```

(solo se sei sicuro che non ci sia nulla da tenere lì.)

## URL del package

Dopo il push su `nebbie-mudlet-dashboard`:

`https://raw.githubusercontent.com/wizardmorgan/nebbie-mudlet-dashboard/main/nebbie-complete-dashboard-package.mpackage`

**Finché il repo personale è vuoto**, puoi installare dalla copia su nebbietest:

`https://raw.githubusercontent.com/wizardmorgan/nebbietest/nebbie-mudlet-dashboard/nebbie-complete-dashboard-package.mpackage`

(in Mudlet: Gestione pacchetti → Installa da URL, oppure `npackageupdate` se il package in gioco punta già a quell’URL.)
