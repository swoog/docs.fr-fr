---
title: 'Procédure : Déclarer une Variable objet et lui assigner un objet en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], declaring
- declaring object variables [Visual Basic]
ms.assetid: 2fa77dde-1fb2-439a-80d4-3e9787649fad
ms.openlocfilehash: fb6411efc190dce335422369a8d2bbff564b9523
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819669"
---
# <a name="how-to-declare-an-object-variable-and-assign-an-object-to-it-in-visual-basic"></a><span data-ttu-id="0d72e-102">Procédure : Déclarer une Variable objet et lui assigner un objet en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0d72e-102">How to: Declare an Object Variable and Assign an Object to It in Visual Basic</span></span>
<span data-ttu-id="0d72e-103">Vous déclarez une variable de la [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) en spécifiant `As Object` dans un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0d72e-103">You declare a variable of the [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) by specifying `As Object` in a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md).</span></span> <span data-ttu-id="0d72e-104">Vous assignez un objet à cette variable en plaçant l’objet après le signe égal (`=`) dans une clause d’instruction ou de l’initialisation de l’attribution.</span><span class="sxs-lookup"><span data-stu-id="0d72e-104">You assign an object to such a variable by placing the object after the equal sign (`=`) in an assignment statement or initialization clause.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0d72e-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="0d72e-105">Example</span></span>  
 <span data-ttu-id="0d72e-106">L’exemple suivant déclare une `Object` variable et assigne actuel d’instance.</span><span class="sxs-lookup"><span data-stu-id="0d72e-106">The following example declares an `Object` variable and assigns the current instance to it.</span></span>  
  
```  
      Dim thisObject As Object  
thisObject = "This is an Object"  
```  
  
 <span data-ttu-id="0d72e-107">Vous pouvez combiner la déclaration et l’affectation en initialisant la variable dans le cadre de sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="0d72e-107">You can combine the declaration and assignment by initializing the variable as part of its declaration.</span></span> <span data-ttu-id="0d72e-108">L’exemple suivant est équivalent à l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0d72e-108">The following example is equivalent to the preceding example.</span></span>  
  
```  
Dim thisObject As Object= "This is an Object"  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0d72e-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0d72e-109">Compiling the Code</span></span>  
 <span data-ttu-id="0d72e-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0d72e-110">This example requires:</span></span>  
  
-   <span data-ttu-id="0d72e-111">une référence à l'espace de noms <xref:System>.</span><span class="sxs-lookup"><span data-stu-id="0d72e-111">A reference to the <xref:System> namespace.</span></span>  
  
-   <span data-ttu-id="0d72e-112">Une classe, une structure ou un module dans lequel placer la `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="0d72e-112">A class, structure, or module in which to put the `Dim` statement.</span></span>  
  
-   <span data-ttu-id="0d72e-113">Une procédure dans laquelle placer l’instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="0d72e-113">A procedure in which to put the assignment statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d72e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d72e-114">See also</span></span>

- [<span data-ttu-id="0d72e-115">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="0d72e-115">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="0d72e-116">Variables objets</span><span class="sxs-lookup"><span data-stu-id="0d72e-116">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="0d72e-117">Déclaration des variables objets</span><span class="sxs-lookup"><span data-stu-id="0d72e-117">Object Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [<span data-ttu-id="0d72e-118">Object (type de données)</span><span class="sxs-lookup"><span data-stu-id="0d72e-118">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="0d72e-119">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="0d72e-119">Dim Statement</span></span>](../../../../visual-basic/language-reference/statements/dim-statement.md)
- [<span data-ttu-id="0d72e-120">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="0d72e-120">Local Type Inference</span></span>](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="0d72e-121">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="0d72e-121">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
