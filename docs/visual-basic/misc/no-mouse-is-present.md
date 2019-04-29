---
title: Absence de souris
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoMouseIsPresent
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
ms.openlocfilehash: c0e4e2a8cb0aa641b179d8b2608af384d7d4181e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61944935"
---
# <a name="no-mouse-is-present"></a>Absence de souris
L’une des propriétés de l’objet `My.Computer.Mouse` a été appelée, mais aucune souris ou aucun port de souris n’est installé sur l’ordinateur.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété de l’objet `My.Computer.Mouse` .  
  
     — ou —  
  
- Installez une souris sur l’ordinateur.  
  
## <a name="see-also"></a>Voir aussi

- [My.Computer.Mouse](xref:Microsoft.VisualBasic.Devices.Mouse)
- [Gestion et levée d’exceptions dans .NET](../../standard/exceptions/index.md)
- [Try...Catch...Finally (instruction)](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
