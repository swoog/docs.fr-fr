---
title: Non accessible &#39;Main&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 3398195ef9d503e47ab569ff85cb2a827c4270f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54501488"
---
# <a name="no-accessible-39main39-method-with-an-appropriate-signature-was-found-in-39ltnamegt39"></a>Non accessible &#39;Main&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;
Applications de ligne de commande doivent avoir un `Sub Main` défini. `Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.  
  
 **ID d’erreur :** BC30737  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Définir un `Public Sub Main` procédure pour votre projet. Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.  
  
## <a name="see-also"></a>Voir aussi
- [Structure d’un programme Visual Basic](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
