# Savoir lire la documentation d'une commande

## Syntaxe

Y a-t-il une différence entre ces 2 commandes ?

```powershell
Get-ChildItem
```

```powershell
dir
```

### Non, dir étant une alias de Get-ChildItem, la commande sera appelée à l'utilisation de son alias.

***

Y a-t-il une différence entre ces 2 commandes ?

```powershell

get-help -name "dir"
```

```powershell

Get-Help -Name "dir"
```

### Non, PowerShell n'est pas sensible à la casse


## Lire le retour de Get-Help

A l'aide de la commande `get-date` obtenir de la date du jour.

### Réponse (d'autres réponses peuvent exister): 

```powershell
get-date
```

A l'aide de la commande `get-date` obtenir la date du jour au format "dd/MM/yyyy".

### Réponse (d'autres réponses peuvent exister): 

```powershell
get-date -format "dd/MM/yyyy"
OU
get-date -format "d"
```

A l'aide de la commande `get-date` obtenir le jour en toute lettre.

```powershell
get-date -format "dddd"
```

Quel(s) est/sont le(s) alias de la commande `get-date` (Utilisez la commande `get-alias`)?

Il n'y en a pas, comme expliqué par le retour de la commande get-alias : 

```powershell
Get-Alias : Cette commande ne trouve pas d’alias correspondant, car l’alias avec definition « Get-Date » n’existe pas.
Au caractère Ligne:1 : 1
+ Get-Alias -Definition Get-Date
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Get-Date:String) [Get-Alias], ItemNotFoundException
    + FullyQualifiedErrorId : ItemNotFoundException,Microsoft.PowerShell.Commands.GetAliasCommand
```
