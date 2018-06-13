---
title: Non accessible &#39;principal&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 6a60e26a2bd0e31c0f92dbbfb2518c75f304d9f1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593218"
---
# <a name="no-accessible-39main39-method-with-an-appropriate-signature-was-found-in-39ltnamegt39"></a>Non accessible &#39;principal&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;
Les applications de ligne de commande doivent avoir un `Sub Main` défini. `Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.  
  
 **ID d’erreur :** BC30737  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Définir un `Public Sub Main` procédure pour votre projet. Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.  
  
## <a name="see-also"></a>Voir aussi  
 [Structure d’un programme Visual Basic](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)  
 [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
