---
title: Variable &#39; &lt;variablename&gt; &#39; masque une variable dans un bloc englobant
ms.date: 07/20/2015
f1_keywords:
- vbc30616
- bc30616
helpviewer_keywords:
- BC30616
ms.assetid: e7658ebc-da45-451b-a409-a0f8915f0beb
ms.openlocfilehash: 23ec659535b71ee9af189f5c4fec0dec2bb1cd8f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54719428"
---
# <a name="variable-39ltvariablenamegt39-hides-a-variable-in-an-enclosing-block"></a><span data-ttu-id="9996c-102">Variable &#39; &lt;variablename&gt; &#39; masque une variable dans un bloc englobant</span><span class="sxs-lookup"><span data-stu-id="9996c-102">Variable &#39;&lt;variablename&gt;&#39; hides a variable in an enclosing block</span></span>
<span data-ttu-id="9996c-103">Une variable dans un bloc a le même nom qu’une autre variable locale.</span><span class="sxs-lookup"><span data-stu-id="9996c-103">A variable enclosed in a block has the same name as another local variable.</span></span>  
  
 <span data-ttu-id="9996c-104">**ID d’erreur :** BC30616</span><span class="sxs-lookup"><span data-stu-id="9996c-104">**Error ID:** BC30616</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9996c-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9996c-105">To correct this error</span></span>  
  
-   <span data-ttu-id="9996c-106">Renommez la variable du bloc englobé afin qu’il ne soit pas identique à toutes les variables locales.</span><span class="sxs-lookup"><span data-stu-id="9996c-106">Rename the variable in the enclosed block so that it is not the same as any other local variables.</span></span> <span data-ttu-id="9996c-107">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9996c-107">For example:</span></span>  
  
    ```  
    Dim a, b, x As Integer  
    If a = b Then  
       Dim y As Integer = 20 ' Uniquely named block variable.  
    End If  
    ```  
  
-   <span data-ttu-id="9996c-108">Une cause courante de cette erreur est l’utilisation de `Catch e As Exception` à l’intérieur d’un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="9996c-108">A common cause for this error is the use of `Catch e As Exception` inside an event handler.</span></span> <span data-ttu-id="9996c-109">Si c’est le cas, nommez le `Catch` variable bloc `ex` plutôt que `e`.</span><span class="sxs-lookup"><span data-stu-id="9996c-109">If this is the case, name the `Catch` block variable `ex` rather than `e`.</span></span>  
  
-   <span data-ttu-id="9996c-110">Une autre source courante de cette erreur est une tentative d’accès d’une variable locale déclarée dans un `Try` bloquer dans une fonction `Catch` bloc.</span><span class="sxs-lookup"><span data-stu-id="9996c-110">Another common source of this error is an attempt to access a local variable declared within a `Try` block in a separate `Catch` block.</span></span> <span data-ttu-id="9996c-111">Pour corriger ce problème, déclarez la variable en dehors de la `Try...Catch...Finally` structure.</span><span class="sxs-lookup"><span data-stu-id="9996c-111">To correct this, declare the variable outside the `Try...Catch...Finally` structure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9996c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9996c-112">See also</span></span>
- [<span data-ttu-id="9996c-113">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="9996c-113">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [<span data-ttu-id="9996c-114">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="9996c-114">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
