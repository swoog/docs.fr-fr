---
title: Erreur Automation
ms.date: 07/20/2015
f1_keywords:
- vbrID440
ms.assetid: 2c4be5c5-2f0d-4a2b-96fe-d1b24f08fc4c
ms.openlocfilehash: 8a00efe988eb39be75818b5c2c401b58e5f7f2ef
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54490880"
---
# <a name="automation-error"></a><span data-ttu-id="4d3a4-102">Erreur Automation</span><span class="sxs-lookup"><span data-stu-id="4d3a4-102">Automation error</span></span>
<span data-ttu-id="4d3a4-103">Une erreur s'est produite pendant l'exécution d'une méthode ou l'obtention / la définition d'une propriété de variable objet.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-103">An error occurred while executing a method or getting or setting a property of an object variable.</span></span> <span data-ttu-id="4d3a4-104">L'application qui a créé l'objet a signalé l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-104">The error was reported by the application that created the object.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4d3a4-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="4d3a4-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="4d3a4-106">Vérifiez les propriétés de l'objet `Err` pour déterminer la source et la nature de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-106">Check the properties of the `Err` object to determine the source and nature of the error.</span></span>  
  
2.  <span data-ttu-id="4d3a4-107">Utilisez la `On Error Resume Next` instruction immédiatement avant l’instruction d’accès et recherchez les erreurs immédiatement après l’instruction d’accès.</span><span class="sxs-lookup"><span data-stu-id="4d3a4-107">Use the `On Error Resume Next` statement immediately before the accessing statement, and then check for errors immediately after the accessing statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d3a4-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d3a4-108">See also</span></span>
- [<span data-ttu-id="4d3a4-109">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="4d3a4-109">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="4d3a4-110">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="4d3a4-110">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
