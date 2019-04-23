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
# <a name="automation-error"></a><span data-ttu-id="21c72-102">Erreur Automation</span><span class="sxs-lookup"><span data-stu-id="21c72-102">Automation error</span></span>
<span data-ttu-id="21c72-103">Une erreur s'est produite pendant l'exécution d'une méthode ou l'obtention / la définition d'une propriété de variable objet.</span><span class="sxs-lookup"><span data-stu-id="21c72-103">An error occurred while executing a method or getting or setting a property of an object variable.</span></span> <span data-ttu-id="21c72-104">L'application qui a créé l'objet a signalé l'erreur.</span><span class="sxs-lookup"><span data-stu-id="21c72-104">The error was reported by the application that created the object.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="21c72-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="21c72-105">To correct this error</span></span>  
  
1. <span data-ttu-id="21c72-106">Vérifiez les propriétés de l'objet `Err` pour déterminer la source et la nature de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="21c72-106">Check the properties of the `Err` object to determine the source and nature of the error.</span></span>  
  
2. <span data-ttu-id="21c72-107">Utilisez la `On Error Resume Next` instruction immédiatement avant l’instruction d’accès et recherchez les erreurs immédiatement après l’instruction d’accès.</span><span class="sxs-lookup"><span data-stu-id="21c72-107">Use the `On Error Resume Next` statement immediately before the accessing statement, and then check for errors immediately after the accessing statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21c72-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21c72-108">See also</span></span>

- [<span data-ttu-id="21c72-109">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="21c72-109">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="21c72-110">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="21c72-110">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
