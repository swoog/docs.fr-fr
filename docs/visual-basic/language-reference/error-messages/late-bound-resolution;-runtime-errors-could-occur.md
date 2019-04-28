---
title: Résolution à liaison tardive ; des erreurs d’exécution peuvent se produire
ms.date: 07/20/2015
f1_keywords:
- vbc42017
- BC42017
helpviewer_keywords:
- BC42017
ms.assetid: 45f552c8-57c6-44c0-97d3-e510119b257a
ms.openlocfilehash: 4fe79c74b6ff634223a4f10d8c5dc54bb77571cc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921145"
---
# <a name="late-bound-resolution-runtime-errors-could-occur"></a><span data-ttu-id="c09e9-102">Résolution à liaison tardive ; des erreurs d’exécution peuvent se produire</span><span class="sxs-lookup"><span data-stu-id="c09e9-102">Late bound resolution; runtime errors could occur</span></span>
<span data-ttu-id="c09e9-103">Un objet est assigné à une variable déclarée comme étant de la [Object Data Type](../../../visual-basic/language-reference/data-types/object-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c09e9-103">An object is assigned to a variable declared to be of the [Object Data Type](../../../visual-basic/language-reference/data-types/object-data-type.md).</span></span>  
  
 <span data-ttu-id="c09e9-104">Lorsque vous déclarez une variable en tant que `Object`, le compilateur doit exécuter *liaison tardive*, ce qui entraîne des opérations supplémentaires au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c09e9-104">When you declare a variable as `Object`, the compiler must perform *late binding*, which causes extra operations at run time.</span></span> <span data-ttu-id="c09e9-105">Cela expose également votre application à des erreurs d’exécution potentielles.</span><span class="sxs-lookup"><span data-stu-id="c09e9-105">It also exposes your application to potential run-time errors.</span></span> <span data-ttu-id="c09e9-106">Par exemple, si vous assignez un <xref:System.Windows.Forms.Form> à la `Object` variable et réessayez d’accéder à la <xref:System.Xml.XmlDocument.NameTable%2A?displayProperty=nameWithType> propriété, le runtime lève un <xref:System.MemberAccessException> , car le <xref:System.Windows.Forms.Form> classe n’expose pas un `NameTable` propriété.</span><span class="sxs-lookup"><span data-stu-id="c09e9-106">For example, if you assign a <xref:System.Windows.Forms.Form> to the `Object` variable and then try to access the <xref:System.Xml.XmlDocument.NameTable%2A?displayProperty=nameWithType> property, the runtime throws a <xref:System.MemberAccessException> because the <xref:System.Windows.Forms.Form> class does not expose a `NameTable` property.</span></span>  
  
 <span data-ttu-id="c09e9-107">Si vous déclarez la variable comme étant d’un type spécifique, le compilateur peut exécuter *liaison anticipée* au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="c09e9-107">If you declare the variable to be of a specific type, the compiler can perform *early binding* at compile time.</span></span> <span data-ttu-id="c09e9-108">Cela entraîne des performances améliorées, un accès contrôlé aux membres du type spécifique et une meilleure lisibilité de votre code.</span><span class="sxs-lookup"><span data-stu-id="c09e9-108">This results in improved performance, controlled access to the members of the specific type, and better readability of your code.</span></span>  
  
 <span data-ttu-id="c09e9-109">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="c09e9-109">By default, this message is a warning.</span></span> <span data-ttu-id="c09e9-110">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="c09e9-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="c09e9-111">**ID d’erreur :** BC42017</span><span class="sxs-lookup"><span data-stu-id="c09e9-111">**Error ID:** BC42017</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c09e9-112">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c09e9-112">To correct this error</span></span>  
  
- <span data-ttu-id="c09e9-113">Si possible, déclarez la variable comme étant d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="c09e9-113">If possible, declare the variable to be of a specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c09e9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c09e9-114">See also</span></span>

- [<span data-ttu-id="c09e9-115">Liaison anticipée et liaison tardive</span><span class="sxs-lookup"><span data-stu-id="c09e9-115">Early and Late Binding</span></span>](../../../visual-basic/programming-guide/language-features/early-late-binding/index.md)
- [<span data-ttu-id="c09e9-116">Déclaration des variables objets</span><span class="sxs-lookup"><span data-stu-id="c09e9-116">Object Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
