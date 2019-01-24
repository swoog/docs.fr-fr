---
title: La classe ne prend pas en charge Automation ou l'interface attendue
ms.date: 07/20/2015
f1_keywords:
- vbrID430
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
ms.openlocfilehash: d5b47b39742a995be6076ddc0edc17f1ec94dade
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534162"
---
# <a name="class-does-not-support-automation-or-does-not-support-expected-interface"></a>La classe ne prend pas en charge Automation ou l'interface attendue
La classe que vous avez spécifiée dans l'appel de fonction `GetObject` ou `CreateObject` n'a exposé aucune interface programmable, ou vous avez modifié un projet .dll en .exe, ou vice versa.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez la documentation de l'application qui a créé l'objet pour connaître les limitations relatives à l'utilisation de l'automatisation avec cette classe d'objet.  
  
2.  Si vous avez modifié un projet .dll en .exe ou vice versa, vous devez annuler manuellement l'inscription de l'ancien projet .dll ou .exe.  
  
## <a name="see-also"></a>Voir aussi
- [Types d’erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)
- [Nous contacter](/visualstudio/ide/talk-to-us)
