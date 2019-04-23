---
title: Erreur Automation
ms.date: 07/20/2015
f1_keywords:
- vbrID440
ms.assetid: 2c4be5c5-2f0d-4a2b-96fe-d1b24f08fc4c
ms.openlocfilehash: 8370f744b916ce4a797c808ed58c5fc9580e6278
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304309"
---
# <a name="automation-error"></a>Erreur Automation
Une erreur s'est produite pendant l'exécution d'une méthode ou l'obtention / la définition d'une propriété de variable objet. L'application qui a créé l'objet a signalé l'erreur.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez les propriétés de l'objet `Err` pour déterminer la source et la nature de l'erreur.  
  
2. Utilisez la `On Error Resume Next` instruction immédiatement avant l’instruction d’accès et recherchez les erreurs immédiatement après l’instruction d’accès.  
  
## <a name="see-also"></a>Voir aussi

- [Types d’erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)
- [Nous contacter](/visualstudio/ide/talk-to-us)
