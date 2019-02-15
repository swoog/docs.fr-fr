---
title: Absence de souris
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoMouseIsPresent
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
ms.openlocfilehash: 26b8ca04706489f681b9811173f9944ed3cbbeee
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303463"
---
# <a name="no-mouse-is-present"></a>Absence de souris
L’une des propriétés de l’objet `My.Computer.Mouse` a été appelée, mais aucune souris ou aucun port de souris n’est installé sur l’ordinateur.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété de l’objet `My.Computer.Mouse` .  
  
     — ou —  
  
-   Installez une souris sur l’ordinateur.  
  
## <a name="see-also"></a>Voir aussi
- [My.Computer.Mouse](xref:Microsoft.VisualBasic.Devices.Mouse)
- [Gestion et levée d’exceptions dans .NET](../../standard/exceptions/index.md)
- [Try...Catch...Finally (instruction)](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
