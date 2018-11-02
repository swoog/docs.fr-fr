---
title: Options F# Interactive
description: En savoir plus sur les options de ligne de commande pris en charge par F# Interactive, fsi.exe.
ms.date: 05/16/2016
ms.openlocfilehash: a461dd0eeff2de3d15e557ba37138fbd62ca43ba
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "33565803"
---
# <a name="f-interactive-options"></a>Options F# Interactive

> [!NOTE]
Cet article ne traite pour le moment que de l’expérience Windows.  Il va être réécrit.

Cette rubrique décrit les options de ligne de commande pris en charge par F# Interactive, `fsi.exe`. F#Interactive accepte la plupart des options de ligne de commande même comme le F# compilateur, mais accepte également des options supplémentaires.

## <a name="using-f-interactive-for-scripting"></a>À l’aide de F# Interactive pour le script
F#Interactif, `fsi.exe`, peut être lancé interactivement ou il peut être lancé depuis la ligne de commande pour exécuter un script. La syntaxe de ligne de commande est

```
> fsi.exe [options] [ script-file [arguments] ]
```

L’extension de fichier pour F# fichiers de script est `.fsx`.

## <a name="table-of-f-interactive-options"></a>Table de F# Options interactives
Le tableau suivant résume les options prises en charge par F# Interactive. Vous pouvez définir ces options sur la ligne de commande ou via l’IDE Visual Studio. Pour définir ces options dans l’IDE Visual Studio, ouvrez le **outils** menu, sélectionnez **Options...** , puis développez le  **F# outils** nœud et sélectionnez  **F# Interactive**.

Où les listes apparaissent dans F# arguments de l’option Interactive, les éléments de liste sont séparés par des points-virgules (`;`).

|Option|Description|
|------|-----------|
|**--**|Utilisé pour indiquer à F# Interactive pour traiter les arguments restants en tant qu’arguments de ligne de commande pour le F# programme ou script auquel vous pouvez accéder dans le code à l’aide de la liste **fsi.CommandLineArgs**.|
|**--checked**[**+**&#124;**-**]|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**page de codes-- :&lt;int&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--consolecolors**[**+**&#124;**-**]|Sorties d’avertissement et messages d’erreur en couleur.|
|**--crossoptimize**[**+**&#124;**-**]|Activer ou désactiver les optimisations intermodules.|
|**--debug**[**+**&#124;**-**]<br /><br />**--debug :**[**complète**&#124;**pdbonly**&#124;**portable**&#124;**embedded**]<br /><br />**-g**[**+**&#124;**-**]<br /><br />**-g:**[**complète**&#124;**pdbonly**&#124;**portable**&#124;**embedded**]|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--définir :&lt;chaîne&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--deterministic**[**+**&#124;**-**]|Génère un assembly déterministe (y compris la version du module GUID et timestamp).|
|**--exec**|Indique à F# interactive quitte après le chargement des fichiers ou du fichier de script donné sur la ligne de commande en cours d’exécution.|
|**fullpaths--**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--gui**[**+**&#124;**-**]|Active ou désactive la boucle d’événement Windows Forms. Les styles sont activés par défaut.|
|**--help**<br /><br />**-?**|Permet d’afficher la syntaxe de ligne de commande et une brève description de chaque option.|
|**--lib :&lt;-liste des dossiers&gt;**<br /><br />**-I&lt;-liste des dossiers&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--charger :&lt;nom de fichier&gt;**|Compile le code source donné au démarrage et charge compilé F# construit dans la session. Si la source cible contient des directives de script telles que **#use** ou **#load**, vous devez utiliser **--utiliser** ou **#use** au lieu de **--charger** ou **#load**.|
|**--mlcompatibility**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--noframework**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez [Options du compilateur](compiler-options.md)|
|**--nologo**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--nowarn :&lt;liste d’avertissements&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--optimiser**[**+**&#124;**-**]|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--preferreduilang :&lt;lang&gt;**| Spécifie le nom de culture de langue préférée de sortie (par exemple, es-ES, ja-JP). |
|**--quiet**|Supprimer F# Interactive de sortie pour le **stdout** flux.|
|**--quotations-debug**|Spécifie que les informations de débogage supplémentaires doivent être émises pour les expressions qui sont dérivées de F# littéraux de quotation et définitions réfléchies. Les informations de débogage sont ajoutées pour les attributs personnalisés d’un F# nœud arborescence d’expression. Consultez [Quotations de Code](code-quotations.md) et [Expr.CustomAttributes](https://msdn.microsoft.com/library/eb89943f-5f5b-474e-b125-030ca412edb3).|
|**--readline**[**+**&#124;**-**]|Activer ou désactiver la saisie semi-automatique par tabulation en mode interactif.|
|**--référence :&lt;nom de fichier&gt;**<br /><br />**-r:&lt;nom de fichier&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--shadowcopyreferences**[**+**&#124;**-**]|Empêche des références d’être verrouillés par le F# processus interactif.|
|**--simpleresolution**|Résout les références d’assembly à l’aide de règles basées sur le répertoire au lieu de résolution MSBuild.|
|**--tailcalls**[**+**&#124;**-**]|Activer ou désactiver l’utilisation de l’instruction de langage intermédiaire tail, ce qui provoque le frame de pile d’être réutilisé pour les fonctions récursives tail. Cette option est activée par défaut.|
|**--targetprofile :&lt;chaîne&gt;**|Spécifie le profil du framework cible de cet assembly. Les valeurs valides sont mscorlib, netcore ou netstandard.  La valeur par défaut est mscorlib.|
|**--utiliser :&lt;nom de fichier&gt;**|Indique à l’interpréteur d’utiliser le fichier donné au démarrage en tant qu’entrée initiale.|
|**--utf8output**|Identique à l’option de compilateur fsc.exe. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--avertir :&lt;niveau d’avertissement&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--warnaserror**[**+**&#124;**-**]|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|
|**--warnaserror**[**+**&#124;**-**]:**&lt;int-list&gt;**|Identique à la **fsc.exe** option du compilateur. Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).|

## <a name="related-topics"></a>Rubriques connexes

|Titre|Description|
|-----|-----------|
|[Options du compilateur](compiler-options.md)|Décrit les options de ligne de commande disponibles pour le F# compilateur, **fsc.exe**.|
