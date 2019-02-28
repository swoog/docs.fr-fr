---
title: 'Procédure : déterminer les versions du .NET Framework installées'
ms.date: 02/20/2019
dev_langs:
- csharp
- vb
ms.custom: updateeachrelease
helpviewer_keywords:
- versions, determining for .NET Framework
- .NET Framework, determining version
ms.assetid: 40a67826-e4df-4f59-a651-d9eb0fdc755d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7661b3ebaa8f29d6d3b2adbc56c405c8f0945f3
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584172"
---
# <a name="how-to-determine-which-net-framework-versions-are-installed"></a>Procédure : déterminer les versions du .NET Framework installées

Les utilisateurs peuvent installer et exécuter plusieurs versions de .NET Framework sur leurs ordinateurs. Quand vous développez ou déployez votre application, vous pouvez avoir besoin de savoir quelles versions de .NET Framework sont installées sur l'ordinateur de l'utilisateur. Notez que .NET Framework comporte deux principaux composants, dont les versions sont définies séparément :  
  
- Un jeu d'assemblys, qui correspondent aux collections de types et de ressources qui fournissent les fonctionnalités de vos applications. .NET Framework et les assemblys partagent le même numéro de version.  
  
- Le Common Language Runtime (CLR), qui gère et exécute le code de votre application. Le CLR est identifié par son propre numéro de version (consultez [Versions et dépendances](~/docs/framework/migration-guide/versions-and-dependencies.md)).  
  
Pour obtenir la liste précise des versions de .NET Framework installées sur un ordinateur, vous pouvez consulter le Registre ou l'interroger en utilisant du code :  
  
 [Identifier les versions 1-4 de .NET Framework dans le Registre](#net_a)  
 [Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre](#net_b)  
 [Utilisation de code pour interroger le Registre (versions 1-4)](#net_c)  
 [Utilisation de code pour interroger le Registre (version 4.5 et ultérieure)](#net_d)  
 [Utilisation de PowerShell pour interroger le Registre (version 4.5 et ultérieure)](#ps_a)  

 Pour rechercher la version CLR, vous pouvez utiliser un outil ou du code :  
  
 [Utilisation de l’outil Clrver](#clr_a)  
 [Utilisation de code pour interroger la classe System.Environment](#clr_b)  

> [!NOTE]
> Il existe une différence entre la version de .NET Framework et celle du common language runtime (CLR). Les versions de .NET Framework dépendent du jeu d’assemblys qui constituent la bibliothèque de classes .NET Framework. Par exemple, 4.5, 4.6.1 et 4.7.2 sont des versions de .NET Framework. Les versions du CLR sont créées selon le runtime sur lequel s’exécutent les applications .NET Framework ; une même version du CLR prend généralement en charge plusieurs versions de .NET Framework. Le CLR version 4.30319.*xxxxx* prend en charge les versions 4 à 4.5.2 de .NET Framework ; le CLR version 4.30319.42000 prend en charge toutes les versions de .NET Framework à partir de .NET Framework 4.6. Pour plus d'informations, consultez la propriété <xref:System.Environment.Version?displayProperty=nameWithType>.

 Pour plus d’informations sur la détection des mises à jour installées pour chaque version de .NET Framework, consultez [Guide pratique pour déterminer les mises à jour .NET Framework installées](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md). Pour plus d’informations sur l’installation du .NET Framework, consultez [Installer le .NET Framework pour les développeurs](../../../docs/framework/install/guide-for-developers.md).  
  
<a name="net_a"></a>   
## <a name="find-net-framework-versions-1-4-in-the-registry"></a>Identifier les versions 1-4 de .NET Framework dans le Registre 
  
1.  Dans le menu **Démarrer**, choisissez **Exécuter**.  
  
2.  Dans la zone **Ouvrir**, entrez **regedit.exe**.  
  
     Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.  
  
3.  Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :  
  
     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP`  
  
     Pour les versions 1.1 à 3.5 de .NET Framework, les versions installées sont présentées sous la forme de sous-clés sous la sous-clé `NDP`. Le numéro de version est stocké dans l’entrée **Version** de la sous-clé de version. 
     
     Pour .NET Framework 4, l’entrée **Version** se trouve sous la sous-clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Client`, `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4.0\Full` ou les deux.

    > [!NOTE]
    > Le dossier d’installation « NET Framework Setup » dans le Registre ne commence pas par un point.

    L’illustration suivante montre la sous-clé de .NET Framework 3.5 avec son entrée **Version**.

     ![Entrée de Registre pour .NET Framework 3.5](../../../docs/framework/migration-guide/media/net-4-and-earlier.png ".NET Framework 4 et versions antérieures")

<a name="net_b"></a> 
## <a name="find-net-framework-versions-45-and-later-in-the-registry"></a>Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre

1. Dans le menu **Démarrer**, choisissez **Exécuter**.

2. Dans la zone **Ouvrir**, entrez **regedit.exe**.

     Vous devez disposer d'informations d'identification d'administration pour exécuter regedit.exe.

3. Dans l'Éditeur du Registre, ouvrez la sous-clé suivante :

     `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full`

     Notez que le chemin d'accès à la sous-clé `Full` inclut le `Net Framework` de la sous-clé plutôt que `.NET Framework`.

    > [!NOTE]
    > Si la sous-clé `Full` n'est pas disponible, le .NET Framework 4.5 ou version ultérieure n'est pas installé.

     Recherchez une valeur DWORD nommée `Release`. La présence du DWORD `Release` indique que .NET Framework 4.5 (ou une version ultérieure) est installé sur l’ordinateur. Sa valeur est une clé de version correspondant à une version particulière de .NET Framework. Dans l’illustration suivante, par exemple, la valeur DWORD `Release` est 378389, à savoir la clé de version de .NET Framework 4.5. 

     ![L’entrée du Registre du .NET Framework 4.5.](../../../docs/framework/migration-guide/media/clr-installdir.png "CLR_InstallDir")

Le tableau suivant présente la valeur minimale de la valeur DWORD `Release` pour chaque version de .NET Framework. Vous pouvez utiliser ces valeurs de différentes manières :

- Pour déterminer si une version minimale de .NET Framework est présente, testez si la valeur DWORD `Release` trouvée dans le Registre est *supérieure ou égale à* la valeur figurant dans le tableau. Par exemple, si votre application exige .NET Framework 4.7 ou une version ultérieure, vérifiez que la valeur de clé de version est au minimum 460798.

- Pour tester plusieurs versions, commencez par la dernière version de .NET Framework, puis passez successivement à des versions de plus en plus anciennes.

[!INCLUDE[Release key values note](~/includes/version-keys-note.md)]

|Version du .NET Framework|Valeur du paramètre DWORD Release|
|--------------------------------|-------------|
|.NET Framework 4.5|378389|
|.NET Framework 4.5.1|378675|
|.NET Framework 4.5.2|379893|
|.NET Framework 4.6|393295|
|.NET Framework 4.6.1|394254|
|.NET Framework 4.6.2|394802|
|.NET Framework 4.7|460798|
|.NET Framework 4.7.1|461308|
|.NET Framework 4.7.2|461808|

Pour un tableau complet des clés de version de .NET Framework sur des versions spécifiques du système d’exploitation Windows, voir [Clés de version de .NET Framework et versions du système d’exploitation Windows](release-keys-and-os-versions.md).

<a name="net_c"></a> 
## <a name="find-net-framework-versions-1-4-with-code"></a>Identifier les versions 1-4 de .NET Framework avec du code

- Utilisez la classe <xref:Microsoft.Win32.RegistryKey?displayProperty=nameWithType> pour accéder à la sous-clé `Software\Microsoft\NET Framework Setup\NDP\` sous la branche `HKEY_LOCAL_MACHINE` dans le Registre Windows.

     Le code ci-dessous est un exemple de cette requête.

    > [!NOTE]
    > Ce code ne montre pas comment détecter .NET Framework 4.5 et les versions ultérieures. Examinez la valeur de DWORD `Release` pour détecter ces versions, comme décrit dans la section précédente. Pour passer au code qui détecte .NET Framework 4.5 et les versions ultérieures, voir la section suivante de cet article.

     [!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed1.cs)]
     [!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed1.vb)]

<a name="net_d"></a> 
## <a name="find-net-framework-versions-45-and-later-with-code"></a>Identifier les versions 4.5 et ultérieures de .NET Framework avec du code

1. L'existence de la valeur DWORD `Release` dans la clé `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full` indique que .NET Framework 4.5 (ou une version ultérieure) est installé sur l’ordinateur. La valeur du mot clé indique la version installée. Pour vérifier ce mot clé, utilisez les méthodes <xref:Microsoft.Win32.RegistryKey.OpenBaseKey%2A?displayProperty=nameWithType> et <xref:Microsoft.Win32.RegistryKey.OpenSubKey%2A?displayProperty=nameWithType> afin d’accéder à la sous-clé dans le Registre Windows.

2. Vérifiez la valeur du mot clé `Release` pour déterminer la version installée. Dans une optique de compatibilité ascendante, vous pouvez vérifier la présence d’une valeur supérieure ou égale à celle du tableau de la section [Identifier les versions 4.5 et ultérieures de .NET Framework dans le Registre](#net_b).

L’exemple suivant vérifie la valeur `Release` dans le Registre pour déterminer si .NET Framework 4.5 ou une version ultérieure est installée.

[!code-csharp[ListVersions#5](../../../samples/snippets/csharp/framework/migration-guide/versions-installed3.cs)]
[!code-vb[ListVersions#5](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed3.vb)]

Cet exemple suit la pratique recommandée concernant la vérification de version :

- Il vérifie si la valeur de l’entrée `Release` est *supérieure ou égale à* la valeur des clés de version connues.

- Il effectue sa vérification en partant de la version la plus récente vers la version la plus ancienne.

<a name="ps_a"></a> 
## <a name="check-for-a-minimum-required-net-framework-version-45-and-later-with-powershell"></a>Rechercher une version minimale requise de .NET Framework (4.5 ou ultérieure) avec PowerShell

L’exemple suivant vérifie la valeur du mot clé `Release` pour déterminer si .NET Framework 4.6.2 ou une version ultérieure est installé (retourne `True` si la condition est vérifiée, `False` sinon).

    ```PowerShell
    # PowerShell 5
    Get-ChildItem 'HKLM:\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full\' | Get-ItemPropertyValue -Name Release | Foreach-Object { $_ -ge 394802 } 
    ```

    ```PowerShell
    # PowerShell 4
    (Get-ItemProperty "HKLM:SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full").Release -gt 394802
    ```

    You can replace `394802` in the previous example with another value from the following table in the [Find .NET Framework versions 4.5 and later in the registry](#net_b) section to check for a different minimum required .NET Framework version.
  
<a name="clr_a"></a> 
## <a name="find-the-current-clr-version-with-clrverexe"></a>Identifier la version actuelle du CLR avec Clrver.exe

Utilisez l'outil de version CLR (Clrver.exe) pour déterminer quelles versions du CLR (Common Language Runtime) sont installées sur un ordinateur.

À partir d’une invite de commandes développeur pour Visual Studio, entrez `clrver`. Cette commande produit un résultat similaire au suivant :

```console
Versions installed on the machine:
v2.0.50727
v4.0.30319
```

Pour plus d’informations sur l’utilisation de cet outil, consultez [Clrver.exe (CLR Version Tool)](~/docs/framework/tools/clrver-exe-clr-version-tool.md).

<a name="clr_b"></a> 
## <a name="find-the-current-clr-version-with-the-environment-class"></a>Identifier la version actuelle du CLR avec la classe Environment

Vous pouvez récupérer la valeur de la propriété <xref:System.Environment.Version?displayProperty=nameWithType> pour obtenir un objet <xref:System.Version> identifiant la version du runtime. Cette propriété retourne une valeur unique reflétant la version du runtime qui exécute actuellement le code, et non les versions d’assembly ou d’autres versions du runtime qui peuvent avoir été installées sur l’ordinateur. Vous pouvez utiliser la propriété <xref:System.Version.Major%2A?displayProperty=nameWithType> pour obtenir l’identificateur de version majeure (par exemple, « 4 » pour la version 4.0), la propriété <xref:System.Version.Minor%2A?displayProperty=nameWithType> pour l’identificateur de version mineure (par exemple, « 0 » pour la version 4.0) ou la méthode <xref:System.Version.ToString%2A?displayProperty=nameWithType> pour la totalité de la chaîne de version (par exemple, « 4.0.30319.18010 », comme dans le code suivant). 

Pour .NET Framework versions 4, 4.5, 4.5.1 et 4.5.2, la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> retourne un objet <xref:System.Version> dont la représentation sous forme de chaîne se présente sous la forme `4.0.30319.xxxxx`. Pour .NET Framework 4.6 et versions ultérieures, le format est `4.0.30319.42000`.

> [!IMPORTANT]
> Avec .NET Framework 4.5 et les versions ultérieures, nous déconseillons d’utiliser la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour détecter la version du runtime. Nous recommandons plutôt d’interroger le Registre, comme décrit dans la section [Pour déterminer les versions de .NET Framework en interrogeant le Registre à l’aide de code (.NET Framework 4.5 et ultérieur)](#net_d), plus haut dans cet article.

L’exemple suivant utilise la propriété <xref:System.Environment.Version%2A?displayProperty=nameWithType> pour récupérer les informations de version du runtime :

[!code-csharp[ListVersions](../../../samples/snippets/csharp/framework/migration-guide/versions-installed2.cs)]
[!code-vb[ListVersions](../../../samples/snippets/visualbasic/framework/migration-guide/versions-installed2.vb)]

## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Déterminer les mises à jour .NET Framework installées](~/docs/framework/migration-guide/how-to-determine-which-net-framework-updates-are-installed.md)
- [Installer le .NET Framework pour les développeurs](../../../docs/framework/install/guide-for-developers.md)
- [Versions et dépendances](~/docs/framework/migration-guide/versions-and-dependencies.md)
