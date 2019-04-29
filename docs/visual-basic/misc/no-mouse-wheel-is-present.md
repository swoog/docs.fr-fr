---
title: Absence de roulette de souris
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoWheelIsPresent
ms.assetid: e924ffba-4af1-4247-9a6f-d19a03738f62
ms.openlocfilehash: 073d086931d70508b176bf00773b030a55c272ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61944922"
---
# <a name="no-mouse-wheel-is-present"></a>Absence de roulette de souris
La propriété `My.Computer.Mouse.WheelScrollLines` a été appelée, mais la souris ne possède pas de roulette de défilement.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Vérifiez la propriété `My.Computer.Mouse.WheelExists` pour déterminer si la souris a une roulette de défilement avant d’appeler la propriété `My.Computer.Mouse.WheelScrollLines` .  
  
     - ou -  
  
- Installez une souris dotée d’une roulette de défilement sur l’ordinateur.  
  
## <a name="see-also"></a>Voir aussi

- [My.Computer.Mouse.WheelScrollLines](xref:Microsoft.VisualBasic.Devices.Mouse.WheelScrollLines)
- [My.Computer.Mouse.WheelExists](xref:Microsoft.VisualBasic.Devices.Mouse.WheelExists)
- [Gestion et levée d’exceptions dans .NET](../../standard/exceptions/index.md)
