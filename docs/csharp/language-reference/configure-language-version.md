---
title: Sélectionner la version du langage C# - Guide C#
description: Configurer le compilateur pour effectuer la validation de la syntaxe à l’aide d’une version de compilateur spécifique
ms.date: 02/28/2019
ms.openlocfilehash: 6d31a757171bd2eecdcc1fbd3da765dcb3fe45c0
ms.sourcegitcommit: 79066169e93d9d65203028b21983574ad9dcf6b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57212025"
---
# <a name="select-the-c-language-version"></a>Sélectionner la version du langage C#

Le compilateur C# détermine une version du langage par défaut en fonction du ou des versions cibles de .NET Framework du projet concerné. Lorsqu’il s’agit d’une préversion cible pour laquelle il existe une préversion du langage correspondante, c’est cette dernière qui est utilisée. Dans le cas contraire, la version du langage sera la dernière version mineure.

Par exemple, pendant la période de préversion de .NET Core 3.0, un projet ciblant `netcoreapp3.0` ou `netstandard2.1` (les deux en préversion) utilisera le langage C# 8.0 (également en préversion). Les projets dont la version ciblée est en production emploieront C# 7.3 (la dernière version publiée). Grâce à ce comportement, tout projet ciblant .NET Framework bénéficiera de la dernière version (C# 7.3). 

Cette fonctionnalité dissocie la décision d’installer de nouvelles versions du kit SDK et des outils dans votre environnement de développement de la décision d’incorporer de nouvelles fonctionnalités de langage dans un projet. Vous pouvez installer la dernière version du SDK et des outils sur votre ordinateur de build. Chaque projet peut être configuré pour utiliser une version spécifique du langage pour sa build. Dans le comportement par défaut, les fonctionnalités du langage qui s’appuient sur de nouveaux types ou comportements CLR ne sont activées que pour les projets ciblant ces versions de .NET Framework.

Pour remplacer le comportement par défaut, spécifiez une version du langage. Il existe plusieurs façons de définir la version du langage :

- Utilisez l’[action rapide Visual Studio](#visual-studio-quick-action).
- Définissez la version du langage dans l’[IU Visual Studio](#set-the-language-version-in-visual-studio).
- Modifiez manuellement votre [fichier **.csproj**](#edit-the-csproj-file).
- Définissez la version du langage [pour plusieurs projets d’un sous-répertoire](#configure-multiple-projects).
- Configurez l’[option de compilateur `-langversion`](#set-the-langversion-compiler-option).

## <a name="visual-studio-quick-action"></a>Action rapide Visual Studio

Visual Studio vous aide à déterminer la version de langage dont vous avez besoin. Si vous utilisez une fonctionnalité de langage qui n’est pas disponible pour la version configurée, Visual Studio affiche un correctif potentiel pour mettre à jour la version de langage du projet.

## <a name="set-the-language-version-in-visual-studio"></a>Définir la version du langage dans Visual Studio

Vous pouvez définir la version dans Visual Studio. Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le nœud de projet, puis sélectionnez **Propriétés**. Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**. Dans la liste déroulante, sélectionnez la version. L’image suivante montre le paramètre "latest" :

![Capture d’écran des paramètres de build avancés où vous pouvez spécifier la version du langage](./media/configure-language-version/advanced-build-settings.png)

> [!NOTE]
> Si vous utilisez l’IDE Visual Studio pour mettre à jour vos fichiers csproj, il crée des nœuds distincts pour chaque configuration de build. Vous définissez généralement la même valeur dans toutes les configurations de build, mais vous devez la définir explicitement pour chaque configuration de build ou sélectionner « Toutes les configurations » quand vous modifiez ce paramètre. Vous voyez alors ceci dans votre fichier csproj :
>
>```xml
> <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
>  <LangVersion>latest</LangVersion>
></PropertyGroup>
>
> <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
>  <LangVersion>latest</LangVersion>
> </PropertyGroup>
> ```
>

## <a name="edit-the-csproj-file"></a>Modifier le fichier csproj

Vous pouvez définir la version du langage dans votre fichier **.csproj**. Ajoutez un élément tel que celui-ci :

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

La valeur `latest` utilise la dernière version mineure du langage C#. Les valeurs valides sont les suivantes :

|Value|Signification|
|------------|-------------|
|preview|Le compilateur accepte toute la syntaxe de langage valide de la dernière préversion.|
|latest|Le compilateur accepte la syntaxe de la dernière version publiée du compilateur (versions mineures incluses).|
|latestMajor|Le compilateur accepte la syntaxe de la dernière version principale publiée du compilateur.|
|8.0|Le compilateur accepte uniquement la syntaxe incluse dans C# 8.0 ou une version antérieure.|
|7.3|Le compilateur accepte uniquement la syntaxe incluse dans C# 7.3 ou une version antérieure.|
|7.2|Le compilateur accepte uniquement la syntaxe incluse dans C# 7.2 ou une version antérieure.|
|7.1|Le compilateur accepte uniquement la syntaxe incluse dans C# 7.1 ou une version antérieure.|
|7|Le compilateur accepte uniquement la syntaxe incluse dans C# 7.0 ou une version antérieure.|
|6|Le compilateur accepte uniquement la syntaxe incluse dans C# 6.0 ou une version antérieure.|
|5|Le compilateur accepte uniquement la syntaxe incluse dans C# 5.0 ou une version antérieure.|
|4|Le compilateur accepte uniquement la syntaxe incluse dans C# 4.0 ou une version antérieure.|
|3|Le compilateur accepte uniquement la syntaxe incluse dans C# 3.0 ou une version antérieure.|
|ISO-2|Le compilateur accepte uniquement la syntaxe incluse dans ISO/IEC 23270:2006 C# (2.0) |
|ISO-1|Le compilateur accepte uniquement la syntaxe incluse dans ISO/IEC 23270:2003 C# (1.0/1.2) |

## <a name="configure-multiple-projects"></a>Configurer plusieurs projets

Vous pouvez créer un fichier **Directory.build.props** contenant l’élément `<LangVersion>` pour configurer plusieurs répertoires. En règle générale, vous faites cela dans votre répertoire de solution. Ajoutez ce qui suit à un fichier **Directory.build.props** dans votre répertoire de solution :

```xml
<Project>
 <PropertyGroup>
   <LangVersion>7.3</LangVersion>
 </PropertyGroup>
</Project>
```

Désormais, les builds de chaque sous-répertoire du répertoire contenant ce fichier vont utiliser la syntaxe C# version 7.3. Pour plus d’informations, consultez l’article sur [Personnaliser votre build](/visualstudio/msbuild/customize-your-build).

## <a name="set-the-langversion-compiler-option"></a>Définir l’option de compilateur langversion

Vous pouvez utiliser l’option de ligne de commande `-langversion`. Pour plus d’informations, consultez l’article sur l’option de compilateur [-langversion](../language-reference/compiler-options/langversion-compiler-option.md). Vous pouvez voir une liste des valeurs valides en tapant `csc -langversion:?`.
