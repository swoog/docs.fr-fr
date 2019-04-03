---
title: Stop, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Stop
helpviewer_keywords:
- breakpoints, Stop statements
- Stop statements [Visual Basic], syntax
- Stop statements [Visual Basic]
- execution [Visual Basic], suspending
- processing, interrupting
- processes, interrupting
- execution [Visual Basic], stopping
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
ms.openlocfilehash: 80d6734945324f3f517b256051486273f6b687ec
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58827989"
---
# <a name="stop-statement-visual-basic"></a>Stop, instruction (Visual Basic)
Suspend l’exécution.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Stop  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez placer `Stop` instructions n’importe où dans les procédures pour suspendre l’exécution. À l’aide de la `Stop` instruction est similaire à la définition d’un point d’arrêt dans le code.  
  
 Le `Stop` instruction interrompt l’exécution, mais contrairement à `End`, il ne pas fermer tous les fichiers ou effacer toutes les variables, sauf si elle est placée dans un fichier exécutable compilé (.exe).  
  
> [!NOTE]
>  Si le `Stop` est rencontrée dans le code qui s’exécute en dehors de l’environnement de développement intégré (IDE), le débogueur est appelé. Cela est vrai quel que soit que le code a été compilé en mode débogage ou de la vente au détail.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `Stop` instruction pour interrompre l’exécution à chaque itération du `For...Next` boucle.  
  
 [!code-vb[VbVbalrStatements#56](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#56)]  
  
## <a name="see-also"></a>Voir aussi

- [End (instruction)](../../../visual-basic/language-reference/statements/end-statement.md)
