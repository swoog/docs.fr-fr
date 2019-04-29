---
title: "'As Any' n'est pas pris en charge dans les instructions 'Declare'"
ms.date: 07/20/2015
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
ms.openlocfilehash: 3593f238c72cbcce911c72e42552d6a75188b628
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61935328"
---
# <a name="as-any-is-not-supported-in-declare-statements"></a><span data-ttu-id="20c23-102">'As Any' n'est pas pris en charge dans les instructions 'Declare'</span><span class="sxs-lookup"><span data-stu-id="20c23-102">'As Any' is not supported in 'Declare' statements</span></span>
<span data-ttu-id="20c23-103">Le `Any` type de données a été utilisé avec `Declare` instructions dans Visual Basic 6.0 et versions antérieures pour permettre l’utilisation d’arguments pouvant contenir tout type de données.</span><span class="sxs-lookup"><span data-stu-id="20c23-103">The `Any` data type was used with `Declare` statements in Visual Basic 6.0 and earlier versions to permit the use of arguments that could contain any type of data.</span></span> <span data-ttu-id="20c23-104">Prend en charge de Visual Basic surcharge, toutefois et rend ainsi la `Any` de type de données obsolète.</span><span class="sxs-lookup"><span data-stu-id="20c23-104">Visual Basic supports overloading, however, and so makes the `Any` data type obsolete.</span></span>  
  
 <span data-ttu-id="20c23-105">**ID d’erreur :** BC30828</span><span class="sxs-lookup"><span data-stu-id="20c23-105">**Error ID:** BC30828</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="20c23-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="20c23-106">To correct this error</span></span>  
  
1. <span data-ttu-id="20c23-107">Déclarer des paramètres du type spécifique que vous souhaitez utiliser. par exemple.</span><span class="sxs-lookup"><span data-stu-id="20c23-107">Declare parameters of the specific type you want to use; for example.</span></span>  
  
     [!code-vb[VbVbalrStatements#95](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class5.vb#95)]  
  
2. <span data-ttu-id="20c23-108">Utilisez le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour spécifier `As Any` lorsque `Void*` est attendu par la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="20c23-108">Use the <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribute to specify `As Any` when `Void*` is expected by the procedure being called.</span></span>  
  
     [!code-vb[VbVbalrStatements#96](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class5.vb#96)]  
  
## <a name="see-also"></a><span data-ttu-id="20c23-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c23-109">See also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="20c23-110">Procédure pas à pas : Appel des API Windows</span><span class="sxs-lookup"><span data-stu-id="20c23-110">Walkthrough: Calling Windows APIs</span></span>](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [<span data-ttu-id="20c23-111">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="20c23-111">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
- [<span data-ttu-id="20c23-112">Création de prototypes dans du code managé</span><span class="sxs-lookup"><span data-stu-id="20c23-112">Creating Prototypes in Managed Code</span></span>](../../../framework/interop/creating-prototypes-in-managed-code.md)
