---
title: 'Procédure : Reportez-vous à l’Instance actuelle d’un objet (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: 70955cd55dfb91d4111e59ae58bfe409a4470433
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663527"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a><span data-ttu-id="78b1f-102">Procédure : Reportez-vous à l’Instance actuelle d’un objet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="78b1f-102">How to: Refer to the Current Instance of an Object (Visual Basic)</span></span>
<span data-ttu-id="78b1f-103">Le *instance actuelle* d’un objet est l’instance dans laquelle le code est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="78b1f-103">The *current instance* of an object is the instance in which the code is currently executing.</span></span>  
  
 <span data-ttu-id="78b1f-104">Vous utilisez le `Me` mot clé pour faire référence à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="78b1f-104">You use the `Me` keyword to refer to the current instance.</span></span>  
  
### <a name="to-refer-to-the-current-instance"></a><span data-ttu-id="78b1f-105">Pour faire référence à l’instance actuelle</span><span class="sxs-lookup"><span data-stu-id="78b1f-105">To refer to the current instance</span></span>  
  
- <span data-ttu-id="78b1f-106">Utiliser le `Me` mot clé où vous utiliseriez normalement le nom d’une variable objet.</span><span class="sxs-lookup"><span data-stu-id="78b1f-106">Use the `Me` keyword where you would normally use the name of an object variable.</span></span>  
  
    ```  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     <span data-ttu-id="78b1f-107">Bien que `Me` se comporte comme un objet variable, vous ne pouvez pas déclarez-le ou quoi que ce soit à lui affecter.</span><span class="sxs-lookup"><span data-stu-id="78b1f-107">Although `Me` behaves like an object variable, you cannot declare it or assign anything to it.</span></span> <span data-ttu-id="78b1f-108">`Me` fait toujours référence à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="78b1f-108">`Me` always refers to the current instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78b1f-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78b1f-109">See also</span></span>

- [<span data-ttu-id="78b1f-110">Variables objets</span><span class="sxs-lookup"><span data-stu-id="78b1f-110">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="78b1f-111">Assignation des variables objets</span><span class="sxs-lookup"><span data-stu-id="78b1f-111">Object Variable Assignment</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="78b1f-112">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="78b1f-112">Me, My, MyBase, and MyClass</span></span>](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
