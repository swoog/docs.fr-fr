---
title: Sélectionnez la version linguistique de Visual Basic
description: Configurer le compilateur pour effectuer une validation de syntaxe à l’aide d’une version de compilateur spécifique.
ms.date: 05/24/2018
ms.openlocfilehash: 3b6d8055dbf64f2a5c38f46b6d66794fc48a1cea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797031"
---
# <a name="select-the-visual-basic-language-version"></a>Sélectionnez la version linguistique de Visual Basic

Le compilateur Visual Basic par défaut est la dernière version principale de la langue qui a été libérée. Vous pouvez choisir de compiler n’importe quel projet à l’aide d’une nouvelle version intermédiaire du langage. En choisissant une version plus récente du langage, vous permettez à votre projet d’utiliser les dernières fonctionnalités de langage. Dans d’autres scénarios, vous devrez peut-être vérifier qu’un projet est correctement compilé en cas d’utilisation d’une ancienne version de langage.

Cette fonctionnalité dissocie la décision d’installer de nouvelles versions du kit SDK et des outils dans votre environnement de développement de la décision d’incorporer de nouvelles fonctionnalités de langage dans un projet. Vous pouvez installer la dernière version du SDK et des outils sur votre ordinateur de build. Chaque projet peut être configuré pour utiliser une version spécifique du langage pour sa build.

Il existe trois façons de définir la version de langage :

- Modifiez manuellement votre [ **.vbproj** fichier](#edit-the-vbproj-file)
- Définissez la version de langage [pour plusieurs projets dans un sous-répertoire](#configure-multiple-projects)
- Configurer le [ `-langversion` option du compilateur](#set-the-langversion-compiler-option)

## <a name="edit-the-vbproj-file"></a>Modifiez le fichier vbproj

Vous pouvez définir la version de langage dans votre **.vbproj** fichier. Ajoutez l’élément suivant :

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

La valeur `latest` utilise la dernière version mineure du langage Visual Basic. Les valeurs valides sont les suivantes :

|Value|Signification|
|------------|-------------|
|default|Le compilateur accepte toute la syntaxe de langage valide de la dernière version principale qu’il peut prendre en charge.|
|9|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 9.0 ou inférieure.|
|10|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 10.0 ou inférieure.|
|11|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 11.0 ou inférieure.|
|12|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 12.0 ou inférieure.|
|14|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 14.0 ou inférieure.|
|15|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 15.0 ou inférieure.|
|15.3|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 15.3 ou inférieure.|
|15.5|Le compilateur accepte uniquement la syntaxe qui est incluse dans Visual Basic 15.5 ou inférieure.|
|latest|Le compilateur accepte toute la syntaxe de langage valide qu’il peut prendre en charge.|

Les chaînes spéciales `default` et `latest` définissent respectivement la dernière version majeure et la dernière version mineure du langage installées sur l’ordinateur de build.

## <a name="configure-multiple-projects"></a>Configurer plusieurs projets

Vous pouvez créer un fichier **Directory.build.props** contenant l’élément `<LangVersion>` pour configurer plusieurs répertoires. En règle générale, vous faites cela dans votre répertoire de solution. Ajoutez ce qui suit à un fichier **Directory.build.props** dans votre répertoire de solution :

```xml
<Project>
 <PropertyGroup>
   <LangVersion>15.5</LangVersion>
 </PropertyGroup>
</Project>
```

Maintenant, builds dans chaque sous-répertoire du répertoire contenant ce fichier utilise la syntaxe de la version 15.5 Visual Basic. Pour plus d’informations, consultez l’article sur [Personnaliser votre build](/visualstudio/msbuild/customize-your-build).

## <a name="set-the-langversion-compiler-option"></a>Définir l’option de compilateur langversion

Vous pouvez utiliser l’option de ligne de commande `-langversion`. Pour plus d’informations, consultez l’article sur l’option de compilateur [-langversion](../reference/command-line-compiler/langversion.md). Vous pouvez voir une liste des valeurs valides en tapant `vbc -langversion:?` .
