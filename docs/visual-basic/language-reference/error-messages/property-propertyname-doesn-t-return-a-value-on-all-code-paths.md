---
title: Propriété &#39; &lt;propertyname&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code
ms.date: 07/20/2015
f1_keywords:
- bc42107
- vbc42107
helpviewer_keywords:
- BC42107
ms.assetid: 06800966-9c3b-4844-9f13-83ac95607d32
ms.openlocfilehash: b8059ebc9b6c1de685f2f04c3ee362ab8cf6d05e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611252"
---
# <a name="property-39ltpropertynamegt39-doesn39t-return-a-value-on-all-code-paths"></a><span data-ttu-id="cee6d-102">Propriété &#39; &lt;propertyname&gt; &#39; ne&#39;t retourner une valeur pour tous les chemins de code</span><span class="sxs-lookup"><span data-stu-id="cee6d-102">Property &#39;&lt;propertyname&gt;&#39; doesn&#39;t return a value on all code paths</span></span>
<span data-ttu-id="cee6d-103">Propriété '\<nom_propriété >' ne retourne pas une valeur pour tous les chemins de code.</span><span class="sxs-lookup"><span data-stu-id="cee6d-103">Property '\<propertyname>' doesn't return a value on all code paths.</span></span> <span data-ttu-id="cee6d-104">Une exception de référence null peut se produire au moment de l'exécution lorsque le résultat est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cee6d-104">A null reference exception could occur at run time when the result is used.</span></span>  
  
 <span data-ttu-id="cee6d-105">Une propriété `Get` procédure a au moins un chemin d’accès possible via son code qui ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cee6d-105">A property `Get` procedure has at least one possible path through its code that does not return a value.</span></span>  
  
 <span data-ttu-id="cee6d-106">Vous pouvez retourner une valeur d’une propriété `Get` procédure dans une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="cee6d-106">You can return a value from a property `Get` procedure in any of the following ways:</span></span>  
  
-   <span data-ttu-id="cee6d-107">Affectez la valeur au nom de propriété, puis effectuez une `Exit Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="cee6d-107">Assign the value to the property name and then perform an `Exit Property` statement.</span></span>  
  
-   <span data-ttu-id="cee6d-108">Assignez la valeur au nom de propriété, puis exécutez le `End Get` instruction.</span><span class="sxs-lookup"><span data-stu-id="cee6d-108">Assign the value to the property name and then perform the `End Get` statement.</span></span>  
  
-   <span data-ttu-id="cee6d-109">Inclure la valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cee6d-109">Include the value in a [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).</span></span>  
  
 <span data-ttu-id="cee6d-110">Si le contrôle passe à `Exit Property` ou `End Get` et vous n’avez pas affectés n’importe quelle valeur au nom de propriété, le `Get` procédure retourne la valeur par défaut de la propriété type de données.</span><span class="sxs-lookup"><span data-stu-id="cee6d-110">If control passes to `Exit Property` or `End Get` and you have not assigned any value to the property name, the `Get` procedure returns the default value of the property's data type.</span></span> <span data-ttu-id="cee6d-111">Pour plus d’informations, consultez « Comportement » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cee6d-111">For more information, see "Behavior" in [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md).</span></span>  
  
 <span data-ttu-id="cee6d-112">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="cee6d-112">By default, this message is a warning.</span></span> <span data-ttu-id="cee6d-113">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="cee6d-113">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="cee6d-114">**ID d’erreur :** BC42107</span><span class="sxs-lookup"><span data-stu-id="cee6d-114">**Error ID:** BC42107</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="cee6d-115">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="cee6d-115">To correct this error</span></span>  
  
-   <span data-ttu-id="cee6d-116">Vérifiez votre logique de flux de contrôle et assurez-vous que vous assignez une valeur avant chaque instruction qui provoque un retour.</span><span class="sxs-lookup"><span data-stu-id="cee6d-116">Check your control flow logic and make sure you assign a value before every statement that causes a return.</span></span>  
  
     <span data-ttu-id="cee6d-117">Il est plus facile de garantir que chaque retour de la procédure retourne une valeur si vous utilisez toujours la `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="cee6d-117">It is easier to guarantee that every return from the procedure returns a value if you always use the `Return` statement.</span></span> <span data-ttu-id="cee6d-118">Si vous le faites, la dernière instruction avant `End Get` doit être un `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="cee6d-118">If you do this, the last statement before `End Get` should be a `Return` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cee6d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cee6d-119">See also</span></span>
- [<span data-ttu-id="cee6d-120">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="cee6d-120">Property Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [<span data-ttu-id="cee6d-121">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="cee6d-121">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="cee6d-122">Get (instruction)</span><span class="sxs-lookup"><span data-stu-id="cee6d-122">Get Statement</span></span>](../../../visual-basic/language-reference/statements/get-statement.md)
