---
title: '&#39;En tant que&#39; n’est pas pris en charge dans &#39;Declare&#39; instructions'
ms.date: 07/20/2015
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30828
- vbc30828
helpviewer_keywords:
- BC30828
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
caps.latest.revision: 11
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d8146e339ac5cb005b99c9a1e02f1cd248c4558b
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="39as-any39-is-not-supported-in-39declare39-statements"></a><span data-ttu-id="39214-102">&#39;En tant que&#39; n’est pas pris en charge dans &#39;Declare&#39; instructions</span><span class="sxs-lookup"><span data-stu-id="39214-102">&#39;As Any&#39; is not supported in &#39;Declare&#39; statements</span></span>
<span data-ttu-id="39214-103">Le `Any` type de données a été utilisé avec `Declare` instructions dans Visual Basic 6.0 et versions antérieures pour permettre l’utilisation d’arguments qui peut contenir n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="39214-103">The `Any` data type was used with `Declare` statements in Visual Basic 6.0 and earlier versions to permit the use of arguments that could contain any type of data.</span></span> <span data-ttu-id="39214-104">Visual Basic prend en charge la surcharge, toutefois et rend ainsi le `Any` de type de données obsolète.</span><span class="sxs-lookup"><span data-stu-id="39214-104">Visual Basic supports overloading, however, and so makes the `Any` data type obsolete.</span></span>  
  
 <span data-ttu-id="39214-105">**ID d’erreur :** BC30828</span><span class="sxs-lookup"><span data-stu-id="39214-105">**Error ID:** BC30828</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="39214-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="39214-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="39214-107">Déclarer des paramètres du type spécifique que vous souhaitez utiliser. par exemple.</span><span class="sxs-lookup"><span data-stu-id="39214-107">Declare parameters of the specific type you want to use; for example.</span></span>  
  
     [!code-vb[VbVbalrStatements#95](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_1.vb)]  
  
2.  <span data-ttu-id="39214-108">Utilisez le <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribut pour spécifier `As Any` lorsque `Void*` est attendue par la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="39214-108">Use the <xref:System.Runtime.InteropServices.MarshalAsAttribute> attribute to specify `As Any` when `Void*` is expected by the procedure being called.</span></span>  
  
     [!code-vb[VbVbalrStatements#96](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/as-any-is-not-supported-in-declare-statements_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="39214-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39214-109">See Also</span></span>  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [<span data-ttu-id="39214-110">Procédure pas à pas : appel des API Windows</span><span class="sxs-lookup"><span data-stu-id="39214-110">Walkthrough: Calling Windows APIs</span></span>](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)  
 [<span data-ttu-id="39214-111">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="39214-111">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
 [<span data-ttu-id="39214-112">Création de prototypes dans du code managé</span><span class="sxs-lookup"><span data-stu-id="39214-112">Creating Prototypes in Managed Code</span></span>](../../../framework/interop/creating-prototypes-in-managed-code.md)
