---
title: -quiet
ms.date: 07/20/2015
f1_keywords:
- -quiet
- quiet
helpviewer_keywords:
- -quiet compiler option [Visual Basic]
- /quiet compiler option [Visual Basic]
- quiet compiler option [Visual Basic]
ms.assetid: 5d77fa23-4c50-4708-8535-649912b098e8
ms.openlocfilehash: 32f82eb428c1d3bc427a10b9ca7a1a5feb9e339a
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58816536"
---
# <a name="-quiet"></a>-quiet
Empêche le compilateur d'afficher le code pour les erreurs et les avertissements liés à la syntaxe.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-quiet  
```  
  
## <a name="remarks"></a>Notes  
 Par défaut, l'option `-quiet` n'est pas activée. Lorsque le compilateur signale une erreur de syntaxe ou un avertissement, il génère également la ligne de code source. Pour les applications qui analysent la sortie du compilateur, il peut être plus pratique, le compilateur doit générer uniquement le texte de diagnostic.  
  
 Dans l’exemple suivant, `Module1` génère une erreur qui inclut le code source compilé sans `-quiet`.  
  
```vb  
Module Module1  
    Sub Main()  
        x()  
    End Sub  
End Module  
```  
  
 Sortie :  
 
```console
C:\projects\vb2.vb(3) : error BC30451: 'x' is not declared. It may be inaccessible due to its protection level.

        x()
        ~
``` 
 Compilé avec `-quiet`, le compilateur génère uniquement les éléments suivants :  
  
 `E:\test\t2.vb(3) : error BC30451: Name 'x' is not declared.`  
  
> [!NOTE]
>  Le `-quiet` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant compile `T2.vb` et n’affiche pas de code pour les diagnostics du compilateur liés à la syntaxe :  
  
```  
vbc -quiet t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
