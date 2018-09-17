---
title: -langversion (Options du compilateur C#)
ms.date: 05/14/2018
f1_keywords:
- /langversion
helpviewer_keywords:
- /langversion compiler option [C#]
- -langversion compiler option [C#]
- langversion compiler option [C#]
ms.assetid: 3fb00b05-a0ff-4782-b313-13a4c0f62d94
ms.openlocfilehash: 9ebc90b3d4f610aec58f950f375d97fd2abf3617
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43857269"
---
# <a name="-langversion-c-compiler-options"></a>-langversion (Options du compilateur C#)

Force le compilateur à accepter uniquement la syntaxe incluse dans la spécification choisie du langage C#.  
  
## <a name="syntax"></a>Syntaxe  

```console
-langversion:option  
```

## <a name="arguments"></a>Arguments

 `option`  
 Les valeurs suivantes sont valides :  
  
|Option|Signification|  
|------------|-------------|  
|default|Le compilateur accepte toute la syntaxe de langage valide de la dernière version principale qu’il peut prendre en charge.|
|ISO-1|Le compilateur accepte uniquement la syntaxe qui est incluse dans ISO/IEC 23270:2003 C# (1.0/1.2) <sup id="TISO1">[ISO1](#FISO1)</sup>|  
|ISO-2|Le compilateur accepte uniquement la syntaxe qui est incluse dans ISO/IEC 23270:2006 C# (2.0) <sup id="TISO2">[ISO2](#FISO2)</sup>|
|3|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 3.0 ou inférieure <sup id="TCS3">[CS3](#FCS3)</sup>|
|4|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 4.0 ou inférieure <sup id="TCS4">[CS4](#FCS4)</sup>|
|5|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 5.0 ou inférieure <sup id="TCS5">[CS5](#FCS5)</sup>|
|6|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 6.0 ou inférieure <sup id="TCS6">[CS6](#FCS6)</sup>|
|7|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 7.0 ou inférieure <sup id="TCS7">[CS7](#FCS7)</sup>|
|7.1|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 7.1 ou inférieure <sup id="TCS71">[CS71](#FCS71)</sup>|
|7.2|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 7.2 ou inférieure <sup id="TCS72">[CS72](#FCS72)</sup>|
|7.3|Le compilateur accepte uniquement la syntaxe qui est incluse dans C# version 7.3 ou inférieure <sup id="TCS73">[CS73](#FCS73)</sup>|
|latest|Le compilateur accepte toute la syntaxe de langage valide qu’il peut prendre en charge.|

<!--- Uncomment and move these above
|8|The compiler accepts only syntax that is included in C# 8 or lower <sup id="TCS8">[CS8](#FCS8)</sup>|
-->

## <a name="remarks"></a>Notes

 Les métadonnées référencées par votre application C# ne sont pas visées par l’option de compilateur **-langversion**.  
  
 Sachant que chaque version du compilateur C# contient des extensions de la spécification du langage, **-langversion** ne vous offre pas les fonctionnalités équivalentes d’une version antérieure du compilateur.  

 De plus, alors que les mises à jour de la version de C# coïncident généralement avec les versions principales du .NET Framework, la nouvelle syntaxe et les nouvelles fonctionnalités ne sont pas nécessairement liées à cette version spécifique du framework. Alors que les nouvelles fonctionnalités nécessitent une nouvelle mise à jour du compilateur, publiée en même temps que la révision de C#, chaque fonctionnalité spécifique a ses propres exigences minimales relatives à l’API .NET ou au Common Language Runtime pour pouvoir s’exécuter sur des frameworks de bas niveau en incluant des packages NuGet ou d’autres bibliothèques.
  
 Quel que soit le paramètre **-langversion** que vous utiliserez, vous vous servirez de la version active du common language runtime pour créer votre fichier .exe ou .dll. Les assemblys friend et [-moduleassemblyname (Option du compilateur C#)](../../../csharp/language-reference/compiler-options/moduleassemblyname-compiler-option.md), qui fonctionnent sous **-langversion:ISO-1**, représentent la seule exception.  

 Pour connaître d’autres moyens de spécifier la version du langage C#, consultez la rubrique [Sélectionner la version du langage C#](../configure-language-version.md).
  
 Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.LanguageVersion%2A>.  

## <a name="see-also"></a>Voir aussi

- [Options du compilateur C#](index.md)  
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)  

### <a name="c-language-specification"></a>Spécification du langage C#

|Version|Lien|Description|
|-------|----|-----------|
|C# 1.0|[Télécharger DOC](https://download.microsoft.com/download/a/9/e/a9e229b9-fee5-4c3e-8476-917dee385062/csharp%20language%20specification%20v1.0.doc)|Spécification du langage C# version 1.0 : Microsoft Corporation|
|C# 1.2|[Télécharger DOC](https://download.microsoft.com/download/5/e/5/5e58be0a-b02b-41ac-a4a3-7a22286214ff/csharp%20language%20specification%20v1.2.doc)|Spécification du langage C# version 1.2 : Microsoft Corporation|
|C# 2.0|[Télécharger PDF](https://www.ecma-international.org/publications/files/ECMA-ST-ARCH/Ecma-334%204th%20edition%20June%202006.pdf)|Norme ECMA-334 4e édition|
|C# 3.0|[Télécharger DOC](https://download.microsoft.com/download/3/8/8/388e7205-bc10-4226-b2a8-75351c669b09/CSharp%20Language%20Specification.doc)|Spécification du langage C# version 3.0 : Microsoft Corporation|
|C# 5.0|[Télécharger PDF](https://www.ecma-international.org/publications/files/ECMA-ST/Ecma-334.pdf)|Norme ECMA-334 5e édition|
|C# 6.0|[Lien](../language-specification/index.md)|Spécification du langage C# version 6 - Ébauche non officielle : .NET Foundation|
|C# 7.0 et versions ultérieures||actuellement non disponible|

### <a name="minimum-compiler-version-needed-to-support-all-language-features"></a>Version minimale obligatoire du compilateur pour une prise en charge de toutes les fonctionnalités du langage

[↩](#TISO1)<a name="FISO1">ISO1</a> : compilateur Microsoft Visual Studio/Build Tools .Net 2002 ou .Net Framework 1.0 en bundle [↩](#TISO2)<a name="FISO2">ISO2</a> : compilateur Microsoft Visual Studio/Build Tools 2005 ou .Net Framework 2.0 en bundle [↩](#TCS3)<a name="FCS3">CS3</a> : compilateur Microsoft Visual Studio/Build Tools 2008 ou .Net Framework 3.5 en bundle [↩](#TCS4)<a name="FCS4">CS4</a> : compilateur Microsoft Visual Studio/Build Tools 2010 ou .Net Framework 4.0 en bundle [↩](#TCS5)<a name="FCS5">CS5</a> : compilateur Microsoft Visual Studio/Build Tools 2012 ou .Net Framework 4.5 en bundle [↩](#TCS6)<a name="FCS6">CS6</a> : Microsoft Visual Studio/Build Tools 2015 [↩](#TCS7)<a name="FCS7">CS7</a> : Microsoft Visual Studio/Build Tools 2017 [↩](#TCS71)<a name="FCS71">CS71</a> : Microsoft Visual Studio/Build Tools 2017, version 15.3 [↩](#TCS72)<a name="FCS72">CS72</a> : Microsoft Visual Studio/Build Tools 2017, version 15.5 [↩](#TCS73)<a name="FCS73">CS73</a> : Microsoft Visual Studio/Build Tools 2017, version 15.7

<!--- Uncomment and add to the above when they become officially released
[↩](#TCS8)<a name="FCS8">CS8</a>: Microsoft Visual Studio/Build Tools 20??    
-->
