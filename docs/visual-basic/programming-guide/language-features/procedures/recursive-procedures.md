---
title: Procédures récursives (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], that call themselves
- procedures [Visual Basic], recursive
- procedures [Visual Basic], calling
- recursive procedures
- functions [Visual Basic], calling recursively
- recursion
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
ms.openlocfilehash: de9a2af9fc3cd78879b6525245727a6f52d51c63
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58832383"
---
# <a name="recursive-procedures-visual-basic"></a>Procédures récursives (Visual Basic)
Un *récursive* procédure est une qui s’appelle elle-même. En règle générale, cela n’est pas le moyen le plus efficace pour écrire du code Visual Basic.  
  
 La procédure suivante utilise la récursivité pour calculer la factorielle de son argument d’origine.  
  
 [!code-vb[VbVbcnProcedures#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#51)]  
  
## <a name="considerations-with-recursive-procedures"></a>Considérations sur les procédures récursives  
 **Conditions de limitation**. Vous devez concevoir une procédure récursive à tester pour au moins une condition qui peut s’arrêter la récursivité, et vous devez également gérer le cas où aucune de ces conditions n’est satisfaite au sein d’un nombre raisonnable d’appels récurrents. Au moins une condition qui peut être satisfaite sans erreur, votre procédure s’exécute à un risque élevé de l’exécution dans une boucle infinie.  
  
 **Utilisation de la mémoire**. Votre application dispose d’une quantité limitée d’espace pour les variables locales. Chaque fois qu’une procédure appelle lui-même, il utilise des davantage d’espace pour les copies supplémentaires de ses variables locales. Si ce processus se poursuit indéfiniment, il finit par provoque un <xref:System.StackOverflowException> erreur.  
  
 **L’efficacité**. Vous pouvez presque toujours remplacer une boucle de récursivité. Une boucle n’a pas la surcharge de passage des arguments, l’initialisation du stockage supplémentaire et retourner des valeurs. Vos performances peuvent être considérablement améliorée sans appels récurrents.  
  
 **Récurrence mutuelle**. Vous pouvez observer des performances très médiocres, ou même une boucle infinie, si deux procédures s’appellent mutuellement. Ce type de conception présente les mêmes problèmes qu’une procédure récursive simple, mais il peut être difficile à détecter et à déboguer.  
  
 **Appel avec parenthèses**. Quand un `Function` procédure appelle de manière récursive, vous devez suivre le nom de la procédure avec des parenthèses, même s’il n’existe aucune liste d’arguments. Sinon, le nom de fonction est utilisé en tant que représentant la valeur de retour de la fonction.  
  
 **Test**. Si vous écrivez une procédure récursive, vous devez la tester soigneusement pour vous assurer qu’il répond toujours à certaines conditions de limitation. Vous devez également vous assurer que vous ne pouvez pas suffisamment de mémoire en raison d’un trop grand nombre d’appels récursifs.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.StackOverflowException>
- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Procédures de dépannage](./troubleshooting-procedures.md)
- [Structures de boucle](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
