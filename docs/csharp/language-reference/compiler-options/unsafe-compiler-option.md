---
title: -unsafe (Options du compilateur C#)
ms.date: 04/25/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 35868923ed2f34587c66f04395324489e8b36538
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="-unsafe-c-compiler-options"></a>-unsafe (Options du compilateur C#)
L’option de compilateur **-unsafe** permet la compilation de code utilisant le mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```console  
-unsafe  
```  
  
## <a name="remarks"></a>Notes  
 Pour plus d’informations sur le code unsafe, consultez [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md).  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Pour définir cette option du compilateur dans l'environnement de développement Visual Studio  
  
1.  Ouvrez la page **Propriétés** du projet.  
  
2.  Cliquez sur la page de propriétés **Générer**.  
  
3.  Cochez la case **Autoriser le code unsafe**.  
  
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
 [Options du compilateur C#](../../../csharp/language-reference/compiler-options/index.md)  
 [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
