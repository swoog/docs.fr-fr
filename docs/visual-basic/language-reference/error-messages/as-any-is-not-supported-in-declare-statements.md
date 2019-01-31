---
title: "'As Any' n'est pas pris en charge dans les instructions 'Declare'"
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: bdf339e0d91106a6d6527e085608a06b0439951c
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274080"
---
# <a name="as-any-is-not-supported-in-declare-statements"></a><span data-ttu-id="6568a-102">'As Any' n'est pas pris en charge dans les instructions 'Declare'</span><span class="sxs-lookup"><span data-stu-id="6568a-102">'As Any' is not supported in 'Declare' statements</span></span>
<span data-ttu-id="6568a-103">Le `Any` type de données a été utilisé avec `Declare` instructions dans Visual Basic 6.0 et versions antérieures pour permettre l’utilisation d’arguments pouvant contenir tout type de données.</span><span class="sxs-lookup"><span data-stu-id="6568a-103">The `Any` data type was used with `Declare` statements in Visual Basic 6.0 and earlier versions to permit the use of arguments that could contain any type of data.</span></span> <span data-ttu-id="6568a-104">Prend en charge de Visual Basic surcharge, toutefois et rend ainsi la `Any` de type de données obsolète.</span><span class="sxs-lookup"><span data-stu-id="6568a-104">Visual Basic supports overloading, however, and so makes the `Any` data type obsolete.</span></span>  
  
 <span data-ttu-id="6568a-105">**ID d’erreur :** BC30828</span><span class="sxs-lookup"><span data-stu-id="6568a-105">**Error ID:** BC30828</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6568a-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="6568a-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="6568a-107">Déclarer des paramètres du type spécifique que vous souhaitez utiliser. par exemple.</span><span class="sxs-lookup"><span data-stu-id="6568a-107">Declare parameters of the specific type you want to use; for example.</span></span>  
  
     [!code-vb[VbVbalrStatements#95](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_1.vb)]  
  
2.  <span data-ttu-id="6568a-108">Utilisez le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour spécifier `As Any` lorsque `Void*` est attendu par la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="6568a-108">Use the <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribute to specify `As Any` when `Void*` is expected by the procedure being called.</span></span>  
  
     [!code-vb[VbVbalrStatements#96](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="6568a-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6568a-109">See also</span></span>
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="6568a-110">Procédure pas à pas : Appel des API Windows</span><span class="sxs-lookup"><span data-stu-id="6568a-110">Walkthrough: Calling Windows APIs</span></span>](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [<span data-ttu-id="6568a-111">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="6568a-111">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
- [<span data-ttu-id="6568a-112">Création de prototypes dans du code managé</span><span class="sxs-lookup"><span data-stu-id="6568a-112">Creating Prototypes in Managed Code</span></span>](../../../framework/interop/creating-prototypes-in-managed-code.md)
