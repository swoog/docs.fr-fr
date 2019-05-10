---
title: Aucune méthode 'Main' accessible avec une signature appropriée n'a été trouvée dans '<name>'
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 559c905d1e2e2de4500771a93d6116f9630011ba
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64591979"
---
# <a name="no-accessible-main-method-with-an-appropriate-signature-was-found-in-name"></a>Aucune méthode 'Main' accessible avec une signature appropriée a été trouvée dans '\<nom >'
Applications de ligne de commande doivent avoir un `Sub Main` défini. `Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.  
  
 **ID d’erreur :** BC30737  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Définir un `Public Sub Main` procédure pour votre projet. Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.  
  
## <a name="see-also"></a>Voir aussi

- [Structure d’un programme Visual Basic](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
