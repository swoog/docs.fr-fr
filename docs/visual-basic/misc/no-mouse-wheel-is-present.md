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
# <a name="no-mouse-wheel-is-present"></a><span data-ttu-id="f9e27-102">Absence de roulette de souris</span><span class="sxs-lookup"><span data-stu-id="f9e27-102">No mouse wheel is present</span></span>
<span data-ttu-id="f9e27-103">La propriété `My.Computer.Mouse.WheelScrollLines` a été appelée, mais la souris ne possède pas de roulette de défilement.</span><span class="sxs-lookup"><span data-stu-id="f9e27-103">The `My.Computer.Mouse.WheelScrollLines` property was called, but the mouse has no scroll wheel.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f9e27-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f9e27-104">To correct this error</span></span>  
  
- <span data-ttu-id="f9e27-105">Vérifiez la propriété `My.Computer.Mouse.WheelExists` pour déterminer si la souris a une roulette de défilement avant d’appeler la propriété `My.Computer.Mouse.WheelScrollLines` .</span><span class="sxs-lookup"><span data-stu-id="f9e27-105">Check the `My.Computer.Mouse.WheelExists` property to see if the mouse has a scroll wheel before calling the `My.Computer.Mouse.WheelScrollLines` property.</span></span>  
  
     <span data-ttu-id="f9e27-106">- ou -</span><span class="sxs-lookup"><span data-stu-id="f9e27-106">-or-</span></span>  
  
- <span data-ttu-id="f9e27-107">Installez une souris dotée d’une roulette de défilement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f9e27-107">Install a mouse with a scroll wheel on the computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9e27-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9e27-108">See also</span></span>

- [<span data-ttu-id="f9e27-109">My.Computer.Mouse.WheelScrollLines</span><span class="sxs-lookup"><span data-stu-id="f9e27-109">My.Computer.Mouse.WheelScrollLines</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse.WheelScrollLines)
- [<span data-ttu-id="f9e27-110">My.Computer.Mouse.WheelExists</span><span class="sxs-lookup"><span data-stu-id="f9e27-110">My.Computer.Mouse.WheelExists</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse.WheelExists)
- [<span data-ttu-id="f9e27-111">Gestion et levée d’exceptions dans .NET</span><span class="sxs-lookup"><span data-stu-id="f9e27-111">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
