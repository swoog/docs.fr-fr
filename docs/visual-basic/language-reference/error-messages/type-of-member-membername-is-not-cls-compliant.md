---
title: Type de membre &#39; &lt;membername&gt; &#39; n’est pas conforme CLS
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- bc40025
- vbc40025
helpviewer_keywords:
- BC40025
ms.assetid: adbd34bb-43d2-4266-90e7-cd1afaf49b4e
caps.latest.revision: 14
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 123d19bc3b159578edc7fdfe2a36bc8c79e962ef
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="type-of-member-39ltmembernamegt39-is-not-cls-compliant"></a><span data-ttu-id="7d4dc-102">Type de membre &#39; &lt;membername&gt; &#39; n’est pas conforme CLS</span><span class="sxs-lookup"><span data-stu-id="7d4dc-102">Type of member &#39;&lt;membername&gt;&#39; is not CLS-compliant</span></span>
<span data-ttu-id="7d4dc-103">Le type de données spécifié pour ce membre n’est pas dans le cadre de la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span><span class="sxs-lookup"><span data-stu-id="7d4dc-103">The data type specified for this member is not part of the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span></span> <span data-ttu-id="7d4dc-104">Cela n’est pas une erreur dans votre composant, parce que le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] et Visual Basic prennent en charge ce type de données.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-104">This is not an error within your component, because the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] and Visual Basic support this data type.</span></span> <span data-ttu-id="7d4dc-105">Toutefois, un autre composant écrit dans un code strictement conforme CLS ne prenne pas en charge ce type de données.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-105">However, another component written in strictly CLS-compliant code might not support this data type.</span></span> <span data-ttu-id="7d4dc-106">Ce composant n’est peut-être pas en mesure d’interagir correctement avec votre composant.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-106">Such a component might not be able to interact successfully with your component.</span></span>  
  
 <span data-ttu-id="7d4dc-107">Les types de données Visual Basic suivants ne sont pas conformes CLS :</span><span class="sxs-lookup"><span data-stu-id="7d4dc-107">The following Visual Basic data types are not CLS-compliant:</span></span>  
  
-   [<span data-ttu-id="7d4dc-108">SByte (type de données)</span><span class="sxs-lookup"><span data-stu-id="7d4dc-108">SByte Data Type</span></span>](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [<span data-ttu-id="7d4dc-109">UInteger (type de données)</span><span class="sxs-lookup"><span data-stu-id="7d4dc-109">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [<span data-ttu-id="7d4dc-110">ULong (type de données)</span><span class="sxs-lookup"><span data-stu-id="7d4dc-110">ULong Data Type</span></span>](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [<span data-ttu-id="7d4dc-111">UShort (type de données)</span><span class="sxs-lookup"><span data-stu-id="7d4dc-111">UShort Data Type</span></span>](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 <span data-ttu-id="7d4dc-112">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-112">By default, this message is a warning.</span></span> <span data-ttu-id="7d4dc-113">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [configuration des avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="7d4dc-113">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="7d4dc-114">**ID d’erreur :** BC40025</span><span class="sxs-lookup"><span data-stu-id="7d4dc-114">**Error ID:** BC40025</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7d4dc-115">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="7d4dc-115">To correct this error</span></span>  
  
-   <span data-ttu-id="7d4dc-116">Si votre composant sert d’interface uniquement avec d’autres [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] composants, ou ne pas d’interface avec d’autres composants, vous n’avez pas besoin de rien modifier.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-116">If your component interfaces only with other [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] components, or does not interface with any other components, you do not need to change anything.</span></span>  
  
-   <span data-ttu-id="7d4dc-117">Si vous utilisez un composant non écrit pour le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], vous serez peut-être en mesure de déterminer, par réflexion ou à partir de la documentation, si elle prend en charge ce type de données.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-117">If you are interfacing with a component not written for the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], you might be able to determine, either through reflection or from documentation, whether it supports this data type.</span></span> <span data-ttu-id="7d4dc-118">Dans ce cas, il est inutile d’apporter de modifications.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-118">If it does, you do not need to change anything.</span></span>  
  
-   <span data-ttu-id="7d4dc-119">Si vous utilisez un composant qui ne prend pas en charge ce type de données, vous devez le remplacer par le type conforme CLS le plus proche.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-119">If you are interfacing with a component that does not support this data type, you must replace it with the closest CLS-compliant type.</span></span> <span data-ttu-id="7d4dc-120">Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-120">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="7d4dc-121">Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-121">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>  
  
-   <span data-ttu-id="7d4dc-122">Si vous interfacez avec des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs de données différentes de celles du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="7d4dc-122">If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="7d4dc-123">Par exemple, `uint` correspond souvent à 16 bits dans d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-123">For example, `uint` is often 16 bits in other environments.</span></span> <span data-ttu-id="7d4dc-124">Si vous passez un argument de 16 bits à un tel composant, déclarez-le en tant que `UShort` au lieu de `UInteger` dans votre code managé de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7d4dc-124">If you are passing a 16-bit argument to such a component, declare it as `UShort` instead of `UInteger` in your managed Visual Basic code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d4dc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d4dc-125">See Also</span></span>  
 [<span data-ttu-id="7d4dc-126">Réflexion</span><span class="sxs-lookup"><span data-stu-id="7d4dc-126">Reflection</span></span>](../../../framework/reflection-and-codedom/reflection.md)  
 
