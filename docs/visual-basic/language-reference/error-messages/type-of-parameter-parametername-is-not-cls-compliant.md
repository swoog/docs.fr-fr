---
title: Le type de paramètre '<parametername>' n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- vbc40028
- bc40028
helpviewer_keywords:
- BC40028
ms.assetid: dfa1f6f9-bb88-44ad-b85f-149144363d41
ms.openlocfilehash: e7cf058ef5e6b007a39213aa0ca5748a3b77458a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590645"
---
# <a name="type-of-parameter-parametername-is-not-cls-compliant"></a><span data-ttu-id="243fa-102">Type de paramètre '\<nom_paramètre >' n’est pas conforme CLS</span><span class="sxs-lookup"><span data-stu-id="243fa-102">Type of parameter '\<parametername>' is not CLS-compliant</span></span>
<span data-ttu-id="243fa-103">Une procédure est marquée comme `<CLSCompliant(True)>` mais déclare un paramètre avec un type qui est marqué comme `<CLSCompliant(False)>`, n’est pas marqué ou non qualifié, car il est un type non conforme.</span><span class="sxs-lookup"><span data-stu-id="243fa-103">A procedure is marked as `<CLSCompliant(True)>` but declares a parameter with a type that is marked as `<CLSCompliant(False)>`, is not marked, or does not qualify because it is a noncompliant type.</span></span>  
  
 <span data-ttu-id="243fa-104">Pour qu’une procédure soit conforme à CLS ([Indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md)), elle doit utiliser uniquement des types conformes à CLS.</span><span class="sxs-lookup"><span data-stu-id="243fa-104">For a procedure to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must use only CLS-compliant types.</span></span> <span data-ttu-id="243fa-105">Cette règle s’applique aux types des paramètres, au type de retour et aux types de toutes ses variables locales.</span><span class="sxs-lookup"><span data-stu-id="243fa-105">This applies to the types of the parameters, the return type, and the types of all its local variables.</span></span>  
  
 <span data-ttu-id="243fa-106">Les types de données Visual Basic suivants ne sont pas conformes CLS :</span><span class="sxs-lookup"><span data-stu-id="243fa-106">The following Visual Basic data types are not CLS-compliant:</span></span>  
  
- [<span data-ttu-id="243fa-107">SByte (type de données)</span><span class="sxs-lookup"><span data-stu-id="243fa-107">SByte Data Type</span></span>](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
- [<span data-ttu-id="243fa-108">UInteger (type de données)</span><span class="sxs-lookup"><span data-stu-id="243fa-108">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
- [<span data-ttu-id="243fa-109">ULong (type de données)</span><span class="sxs-lookup"><span data-stu-id="243fa-109">ULong Data Type</span></span>](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
- [<span data-ttu-id="243fa-110">UShort (type de données)</span><span class="sxs-lookup"><span data-stu-id="243fa-110">UShort Data Type</span></span>](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 <span data-ttu-id="243fa-111">Quand vous appliquez l’attribut <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité.</span><span class="sxs-lookup"><span data-stu-id="243fa-111">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="243fa-112">Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="243fa-112">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="243fa-113">Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.</span><span class="sxs-lookup"><span data-stu-id="243fa-113">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="243fa-114">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="243fa-114">By default, this message is a warning.</span></span> <span data-ttu-id="243fa-115">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="243fa-115">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="243fa-116">**ID d’erreur :** BC40028</span><span class="sxs-lookup"><span data-stu-id="243fa-116">**Error ID:** BC40028</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="243fa-117">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="243fa-117">To correct this error</span></span>  
  
- <span data-ttu-id="243fa-118">Si la procédure doit prendre un paramètre de ce type particulier, supprimez le <xref:System.CLSCompliantAttribute>.</span><span class="sxs-lookup"><span data-stu-id="243fa-118">If the procedure must take a parameter of this particular type, remove the <xref:System.CLSCompliantAttribute>.</span></span> <span data-ttu-id="243fa-119">La procédure ne peut pas être conforme à CLS.</span><span class="sxs-lookup"><span data-stu-id="243fa-119">The procedure cannot be CLS-compliant.</span></span>  
  
- <span data-ttu-id="243fa-120">Si la procédure doit être conforme CLS, modifier le type de ce paramètre pour le type conforme CLS le plus proche.</span><span class="sxs-lookup"><span data-stu-id="243fa-120">If the procedure must be CLS-compliant, change the type of this parameter to the closest CLS-compliant type.</span></span> <span data-ttu-id="243fa-121">Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="243fa-121">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="243fa-122">Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.</span><span class="sxs-lookup"><span data-stu-id="243fa-122">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>  
  
- <span data-ttu-id="243fa-123">Si vous utilisez des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs différentes données que dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="243fa-123">If you are interfacing with Automation or COM objects, keep in mind that some types have different data widths than in the .NET Framework.</span></span> <span data-ttu-id="243fa-124">Par exemple, `int` correspond souvent à 16 bits dans d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="243fa-124">For example, `int` is often 16 bits in other environments.</span></span> <span data-ttu-id="243fa-125">Si vous passez un entier 16 bits à partir d’un tel composant, déclarez-le en tant que `Short` au lieu de `Integer` dans votre code managé de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="243fa-125">If you are accepting a 16-bit integer from such a component, declare it as `Short` instead of `Integer` in your managed Visual Basic code.</span></span>
