---
title: -warnaserror (Options du compilateur C#)
ms.date: 07/20/2015
f1_keywords:
- /warnaserror
helpviewer_keywords:
- /warnaserror compiler option [C#]
- -warnaserror compiler option [C#]
- warnaserror compiler option [C#]
ms.assetid: 04680ec3-08d6-4e2e-a274-38310e10e33c
ms.openlocfilehash: 2ae555c2e049e687f508e62b5b46fd8a744e827f
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59329101"
---
# <a name="-warnaserror-c-compiler-options"></a>-warnaserror (Options du compilateur C#)
L’option **-warnaserror+** considère tous les avertissements comme des erreurs.  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-warnaserror[+ | -][:warning-list]  
```  
  
## <a name="remarks"></a>Remarques  
 Les messages qui d’ordinaire auraient été signalés comme des avertissements s’affichent en tant qu’erreurs, et le processus de génération est arrêté (aucun fichier de sortie n’est généré).  
  
 Comme **-warnaserror** est activé par défaut, les avertissements n’empêchent pas la génération d’un fichier de sortie. Du fait de **-warnaserror**, qui est identique à **-warnaserror+**, les avertissements sont considérés comme des erreurs.  
  
 Le cas échéant, si vous voulez que seuls certains avertissements spécifiques soient considérés comme des erreurs, vous pouvez spécifier une liste séparée par des virgules qui liste les numéros d’avertissement à considérer comme des erreurs.  
  
 Utilisez [-warn](../../../csharp/language-reference/compiler-options/warn-compiler-option.md) pour spécifier le niveau des avertissements que le compilateur doit afficher. Utilisez [-nowarn](../../../csharp/language-reference/compiler-options/nowarn-compiler-option.md) pour désactiver certains avertissements.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1. Ouvrez la page **Propriétés** du projet.  
  
2. Cliquez sur la page de propriétés **Générer**.  
  
3. Modifiez la propriété **Considérer les avertissements comme des erreurs**.  
  
 Pour définir cette option du compilateur par programmation, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.TreatWarningsAsErrors>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs` et faites en sorte que le compilateur n’affiche aucun avertissement :  
  
```console  
csc -warnaserror in.cs  
csc -warnaserror:642,649,652 in.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
