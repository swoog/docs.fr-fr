---
title: -/moduleassemblyname
ms.date: 03/13/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- moduleassemblyname compiler option [Visual Basic]
- /moduleassemblyname compiler option [Visual Basic]
- -moduleassemblyname compiler option [Visual Basic]
ms.assetid: 013a57b6-f425-4dd3-b333-512d72c42f55
author: rpetrusha
ms.author: ronpett
ms.openlocfilehash: 0a097ea8a7e30f25a0abb877dc496fb81d1c139f
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-moduleassemblyname"></a>-/moduleassemblyname
Spécifie le nom de l’assembly dont ce module doit faire partie.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-moduleassemblyname:assembly_name  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terme|Définition|  
|---|---|  
|`assembly_name`|Le nom de l’assembly de ce module fera partie.|  
  
## <a name="remarks"></a>Notes  
 Le compilateur traite la `-moduleassemblyname` option uniquement si la `-target:module` option a été spécifiée. Cela entraîne le compilateur à créer un module. Le module créé par le compilateur est valide uniquement pour l’assembly spécifié avec la `-moduleassemblyname` option. Si vous placez le module dans un assembly différent, les erreurs d’exécution seront produit.  
  
 Le `-moduleassemblyname` option est uniquement requise lorsque les conditions suivantes sont remplies :  
  
-   Un type de données dans le module a besoin d’accéder à un `Friend` type dans un assembly référencé.  
  
-   L’assembly référencé a accordé l’accès d’assembly friend à l’assembly dans lequel le module sera généré.  
  
 Pour plus d’informations sur la création d’un module, consultez [/target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md). Pour plus d’informations sur les assemblys friend, consultez [Friend Assemblies](http://msdn.microsoft.com/library/df0c70ea-2c2a-4bdc-9526-df951ad2d055).  
  
> [!NOTE]
>  Le `-moduleassemblyname` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lorsque vous compilez à partir d’une invite de commandes.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour générer un assembly multifichier](../../../framework/app-domains/how-to-build-a-multifile-assembly.md)  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)  
 [-main](../../../visual-basic/reference/command-line-compiler/main.md)  
 [-référence (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [-addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md)  
 [Assemblys et le Global Assembly Cache](../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [Assemblys friend](http://msdn.microsoft.com/library/df0c70ea-2c2a-4bdc-9526-df951ad2d055)
