---
title: -noconfig
ms.date: 03/13/2018
helpviewer_keywords:
- noconfig compiler option [Visual Basic]
- -noconfig compiler option [Visual Basic]
- /noconfig compiler option [Visual Basic]
ms.assetid: a7405067-bd21-4171-adf4-a126fa3ad6c3
ms.openlocfilehash: b707899c845b6b08e008fe229497f682c930044a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65588844"
---
# <a name="-noconfig"></a>-noconfig
Spécifie que le compilateur ne doit pas automatiquement référencer les assemblys .NET Framework couramment utilisés ou importer les `System` et `Microsoft.VisualBasic` espaces de noms.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-noconfig  
```  
  
## <a name="remarks"></a>Notes  
 Le `-noconfig` option indique au compilateur de ne pas compiler avec le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe. Le fichier Vbc.rsp référence les assemblys .NET Framework couramment utilisés et importe le `System` et `Microsoft.VisualBasic` espaces de noms. Le compilateur fait implicitement référence à l’assembly System.dll, sauf si le `-nostdlib` option est spécifiée. Le `-nostdlib` option indique au compilateur de ne pas compiler avec Vbc.rsp ou de référencer automatiquement l’assembly System.dll.  
  
> [!NOTE]
>  Les assemblys Mscorlib.dll et de Microsoft.VisualBasic.dll sont toujours référencés.  
  
 Vous pouvez modifier le fichier Vbc.rsp pour spécifier les options de compilateur supplémentaires qui doivent être incluses dans chaque compilation Vbc.exe (sauf lorsque vous spécifiez la `-noconfig` option). Pour plus d’informations, consultez [@ (Spécifier un fichier réponse)](../../../visual-basic/reference/command-line-compiler/specify-response-file.md).  
  
 Le compilateur traite les options passées à la `vbc` commande dernière. Par conséquent, toute option sur la ligne de commande remplace le paramètre de la même option dans le fichier Vbc.rsp.  
  
> [!NOTE]
>  Le `-noconfig` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="see-also"></a>Voir aussi

- [-nostdlib (Visual Basic)](../../../visual-basic/reference/command-line-compiler/nostdlib.md)
- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [@ (spécifier un fichier réponse)](../../../visual-basic/reference/command-line-compiler/specify-response-file.md)
- [-référence (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md)
