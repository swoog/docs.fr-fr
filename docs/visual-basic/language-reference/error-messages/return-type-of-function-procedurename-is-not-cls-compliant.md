---
title: Le type de retour de la fonction '<procedurename>' n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- bc40027
- vbc40027
helpviewer_keywords:
- BC40027
ms.assetid: 33c088c7-48e7-400c-920e-6d8967e1f3fc
ms.openlocfilehash: 8d6ac07b653a27a7c4c5534f441b9d673592124c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592259"
---
# <a name="return-type-of-function-procedurename-is-not-cls-compliant"></a><span data-ttu-id="f8204-102">Type de retour de fonction '\<nom_procédure >' n’est pas conforme CLS</span><span class="sxs-lookup"><span data-stu-id="f8204-102">Return type of function '\<procedurename>' is not CLS-compliant</span></span>
<span data-ttu-id="f8204-103">Un `Function` procédure est marquée comme `<CLSCompliant(True)>` mais retourne un type qui est marqué comme `<CLSCompliant(False)>`, n’est pas marqué ou non qualifié, car il est un type non conforme.</span><span class="sxs-lookup"><span data-stu-id="f8204-103">A `Function` procedure is marked as `<CLSCompliant(True)>` but returns a type that is marked as `<CLSCompliant(False)>`, is not marked, or does not qualify because it is a noncompliant type.</span></span>  
  
 <span data-ttu-id="f8204-104">Pour qu’une procédure soit conforme à CLS ([Indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md)), elle doit utiliser uniquement des types conformes à CLS.</span><span class="sxs-lookup"><span data-stu-id="f8204-104">For a procedure to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must use only CLS-compliant types.</span></span> <span data-ttu-id="f8204-105">Cette règle s’applique aux types des paramètres, au type de retour et aux types de toutes ses variables locales.</span><span class="sxs-lookup"><span data-stu-id="f8204-105">This applies to the types of the parameters, the return type, and the types of all its local variables.</span></span>  
  
 <span data-ttu-id="f8204-106">Les types de données Visual Basic suivants ne sont pas conformes CLS :</span><span class="sxs-lookup"><span data-stu-id="f8204-106">The following Visual Basic data types are not CLS-compliant:</span></span>  
  
- [<span data-ttu-id="f8204-107">SByte (type de données)</span><span class="sxs-lookup"><span data-stu-id="f8204-107">SByte Data Type</span></span>](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
- [<span data-ttu-id="f8204-108">UInteger (type de données)</span><span class="sxs-lookup"><span data-stu-id="f8204-108">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
- [<span data-ttu-id="f8204-109">ULong (type de données)</span><span class="sxs-lookup"><span data-stu-id="f8204-109">ULong Data Type</span></span>](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
- [<span data-ttu-id="f8204-110">UShort (type de données)</span><span class="sxs-lookup"><span data-stu-id="f8204-110">UShort Data Type</span></span>](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 <span data-ttu-id="f8204-111">Quand vous appliquez l’attribut <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité.</span><span class="sxs-lookup"><span data-stu-id="f8204-111">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="f8204-112">Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="f8204-112">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="f8204-113">Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.</span><span class="sxs-lookup"><span data-stu-id="f8204-113">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="f8204-114">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="f8204-114">By default, this message is a warning.</span></span> <span data-ttu-id="f8204-115">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="f8204-115">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="f8204-116">**ID d’erreur :** BC40027</span><span class="sxs-lookup"><span data-stu-id="f8204-116">**Error ID:** BC40027</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f8204-117">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f8204-117">To correct this error</span></span>  
  
- <span data-ttu-id="f8204-118">Si le `Function` procédure doit retourner ce type particulier, supprimez le <xref:System.CLSCompliantAttribute>.</span><span class="sxs-lookup"><span data-stu-id="f8204-118">If the `Function` procedure must return this particular type, remove the <xref:System.CLSCompliantAttribute>.</span></span> <span data-ttu-id="f8204-119">La procédure ne peut pas être conforme à CLS.</span><span class="sxs-lookup"><span data-stu-id="f8204-119">The procedure cannot be CLS-compliant.</span></span>  
  
- <span data-ttu-id="f8204-120">Si le `Function` procédure doit être conforme CLS, remplacez le type de retour par le type conforme CLS le plus proche.</span><span class="sxs-lookup"><span data-stu-id="f8204-120">If the `Function` procedure must be CLS-compliant, change the return type to the closest CLS-compliant type.</span></span> <span data-ttu-id="f8204-121">Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="f8204-121">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="f8204-122">Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.</span><span class="sxs-lookup"><span data-stu-id="f8204-122">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>  
  
- <span data-ttu-id="f8204-123">Si vous utilisez des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs différentes données que dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f8204-123">If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the .NET Framework.</span></span> <span data-ttu-id="f8204-124">Par exemple, `int` correspond souvent à 16 bits dans d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="f8204-124">For example, `int` is often 16 bits in other environments.</span></span> <span data-ttu-id="f8204-125">Si vous retournez un entier 16 bits à un tel composant, déclarez-le en tant que `Short` au lieu de `Integer` dans votre code managé de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f8204-125">If you are returning a 16-bit integer to such a component, declare it as `Short` instead of `Integer` in your managed Visual Basic code.</span></span>
