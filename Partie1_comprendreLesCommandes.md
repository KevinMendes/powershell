# Les commandes de bases

## Get-Help

Get-Help permet d'obtenir de l'aide sur des commandes spécifiques.

```powershell
Get-Help -Name 'command-name'
```

### Exemple : 
```powershell
Get-Help -Name "ls"
```

Output : 
```powershell
NOM
    Get-ChildItem

SYNTAXE
    Get-ChildItem [[-Path] <string[]>] [[-Filter] <string>]  [<CommonParameters>]

    Get-ChildItem [[-Filter] <string>]  [<CommonParameters>]


ALIAS
    gci
    ls
    dir


REMARQUES
    Get-Help ne parvient pas à trouver les fichiers d’aide de cette applet de commande sur cet ordinateur. Il ne
    trouve qu’une aide partielle.
        -- Pour télécharger et installer les fichiers d’aide du module comportant cette applet de commande, utilisez
    Update-Help.
        -- Pour afficher en ligne la rubrique d’aide de cette applet de commande, tapez : «Get-Help Get-ChildItem
    -Online» ou
           accédez à https://go.microsoft.com/fwlink/?LinkID=113308.
```

"NOM" désigne le vrai nom de la commande, ici "ls" est en réalité un raccourci (un alias) de la commande Get-ChilItem, permettant d'écrire plus vite cette commande. On le voit d'ailleurs dans la partie "ALIAS", ou 3 alias font la même chose - gci, ls, dir. 

"SYNTAXE" explique comment fonctionne cette commande. La syntaxe est capitalisée pour des raisons de lisibilitées, mais PowerShell ne respect pas la casse.

Les paramètres sont donné par un "-" devant leur nom (par exemple -Path), les éléments facultatifs sont notés entre [ ], comme "[-Path]", et le type (type .NET) est lui spécifié entre <> comme "<string[]>" signifiant qu'un tableau de chaine de charactère est attendu. 

Pour plus d'information sur les types se référer à la [documentation officiel de .NET](https://docs.microsoft.com/fr-fr/dotnet/api/system?view=net-6.0)

### Améliorer le get-help

Comme vu dans l'output, l'aide n'est que partielle. Pour obtenir une aide complète il faut télécharger l'aide manquante. <span style="color:red">/!\ L'aide ne sera pas forcément en français malgré tout /!\ </span>.

Pour ce faire il faut utiliser la commande Update-Help (en mode administrateur)

```powershell
Update-Help -UICulture fr-FR -Verbose
``` 

Cette commande va update uniquement en Français, des erreurs peuvent donc surgir pour les modules (très souvent non propriétaire Windows) qui n'ont pas de documentation en Français.


Le PowerShell va alors se mettre à jour en récupérant la totalité des fichiers manquants. 

Vous pouvez obtenir une aide succinte grâce à la commande help

```powershell
help "dir"
```

Ou obtenir un exemple avec cette même commande

```powershell
help "dir" -example
```

# Exercice

Un exercice pour vous tester sur la commande get-help et vous voir que vous savez déjà utiliser n'importe quelle commande uniquement grâce à celle-ci pour peut que vous en connaissiez le nom!

[Lien vers l'exercice](Partie1_exo/Exercice.md)