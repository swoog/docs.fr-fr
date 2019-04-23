---
title: -unsafe (Options du compilateur C#)
ms.date: 04/25/2018
f1_keywords:
- /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
ms.openlocfilehash: 4cfd7c82bc2cbf816164b235642c0647eeb7e5b6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337329"
---
# <a name="-unsafe-c-compiler-options"></a>-unsafe (Options du compilateur C#)
L’option de compilateur **-unsafe** permet la compilation de code utilisant le mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-unsafe  
```  
  
## <a name="remarks"></a>Remarques  
 Pour plus d’informations sur le code unsafe, consultez [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md).  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1. Ouvrez la page **Propriétés** du projet.  
  
2. Cliquez sur la page de propriétés **Générer**.  
  
3. Cochez la case **Autoriser le code unsafe**.  
  
### <a name="to-add-this-option-in-a-csproj-file"></a>Pour ajouter cette option dans un fichier csproj

Ouvrez le fichier .csproj d’un projet et ajoutez les éléments suivants :

```xml
  <PropertyGroup>
    <AllowUnsafeBlocks>true</AllowUnsafeBlocks>
  </PropertyGroup>
```

 Pour plus d'informations sur la façon de définir cette option du compilateur par programme, consultez <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>.  
  
## <a name="example"></a>Exemple  
 Compilez `in.cs` selon le mode non sécurisé :  
  
```console  
csc -unsafe in.cs  
```  
  
## <a name="see-also"></a>Voir aussi

- [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
