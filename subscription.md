# Régió, Előfizetés, Erőforráscsoport parancsok

[![Cloud Shell indítása](https://learn.microsoft.com/azure/cloud-shell/media/embed-cloud-shell/launch-cloud-shell-1.png)](https://shell.azure.com)

## Parancsok Aurehoz

- Telepítés és Bejelentkezés

Ehhez a részhez a [README.md](README.md#telepítés-és-bejelentkezés)

- Aktuális előfizetés

```powershell
Get-AzContext
```

```powershell
Get-AzSubscription
```

```bash
az account list -o table
```

- Altuális előfizetés beállítása

```powershell
Set-AzContext -Subscription 'xxxx-xxxx-xxxx-xxxx'
```

```bash
az account set -s 'xxxx-xxxx-xxxx-xxxx'
```

- Régiók listázása

```powershell
Get-AzLocation | select displayname,location
```

```bash
az account list-locations --output table
```

- Virtuálisgép méretek listázása adott régióban

```powershell
Get-AzVMSize -Location 'régió'
```

```bash
az vm list-sizes --location 'régió' -o table
```

- Erőforráscsoport létrehozása adott régióban

```powershell
New-AzResourceGroup -Location 'régió' -Name 'erőforráscsoport neve'
```

```bash
az group create 'erőforráscsoport neve' --location 'régió'
```

[<< Vissza](README.md)
