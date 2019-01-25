---
title: WriteOnly (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- WriteOnly
- vb.WriteOnly
helpviewer_keywords:
- write-only properties
- WriteOnly keyword [Visual Basic]
- sensitive data, protecting
- properties [Visual Basic], write-only
- sensitive data
ms.assetid: 488d2899-b09f-4cee-92f0-6f9f9fc4f944
ms.openlocfilehash: b6c8a05a4575c5d1ec01aa1b2badf2129c54bc2a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54522776"
---
# <a name="writeonly-visual-basic"></a><span data-ttu-id="a0cbb-102">WriteOnly (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0cbb-102">WriteOnly (Visual Basic)</span></span>
<span data-ttu-id="a0cbb-103">Spécifie qu’une propriété peut être écrite, mais pas lire.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-103">Specifies that a property can be written but not read.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a0cbb-104">Notes</span><span class="sxs-lookup"><span data-stu-id="a0cbb-104">Remarks</span></span>  
  
## <a name="rules"></a><span data-ttu-id="a0cbb-105">Règles</span><span class="sxs-lookup"><span data-stu-id="a0cbb-105">Rules</span></span>  
 <span data-ttu-id="a0cbb-106">**Contexte de déclaration.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-106">**Declaration Context.**</span></span> <span data-ttu-id="a0cbb-107">Vous pouvez utiliser `WriteOnly` seulement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-107">You can use `WriteOnly` only at module level.</span></span> <span data-ttu-id="a0cbb-108">Cela signifie que le contexte de déclaration pour un `WriteOnly` propriété doit être une classe, une structure ou un module et ne peut pas être un fichier source, un espace de noms ou une procédure.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-108">This means the declaration context for a `WriteOnly` property must be a class, structure, or module, and cannot be a source file, namespace, or procedure.</span></span>  
  
 <span data-ttu-id="a0cbb-109">Vous pouvez déclarer une propriété en tant que `WriteOnly`, mais pas une variable.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-109">You can declare a property as `WriteOnly`, but not a variable.</span></span>  
  
## <a name="when-to-use-writeonly"></a><span data-ttu-id="a0cbb-110">Quand utiliser WriteOnly</span><span class="sxs-lookup"><span data-stu-id="a0cbb-110">When to Use WriteOnly</span></span>  
 <span data-ttu-id="a0cbb-111">Parfois, vous souhaitez le code pour pouvoir définir une valeur mais pas découvrir ce qu’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-111">Sometimes you want the consuming code to be able to set a value but not discover what it is.</span></span> <span data-ttu-id="a0cbb-112">Par exemple, des données sensibles, comme un numéro d’enregistrement de réseaux sociaux ou un mot de passe doivent être protégé contre tout accès par tout composant qui définissait pas.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-112">For example, sensitive data, such as a social registration number or a password, needs to be protected from access by any component that did not set it.</span></span> <span data-ttu-id="a0cbb-113">Dans ce cas, vous pouvez utiliser un `WriteOnly` propriété pour définir la valeur.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-113">In these cases, you can use a `WriteOnly` property to set the value.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="a0cbb-114">Lorsque vous définissez et utilisez un `WriteOnly` propriété, envisagez les mesures de protection supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0cbb-114">When you define and use a `WriteOnly` property, consider the following additional protective measures:</span></span>  
  
-   <span data-ttu-id="a0cbb-115">**À substituer.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-115">**Overriding.**</span></span> <span data-ttu-id="a0cbb-116">Si la propriété est un membre d’une classe, laissez-le par défaut [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md)et ne la déclarez pas `Overridable` ou `MustOverride`.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-116">If the property is a member of a class, allow it to default to [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md), and do not declare it `Overridable` or `MustOverride`.</span></span> <span data-ttu-id="a0cbb-117">Cela empêche une classe dérivée d’apporter un droit d’accès via un remplacement.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-117">This prevents a derived class from making undesired access through an override.</span></span>  
  
-   <span data-ttu-id="a0cbb-118">**Niveau d’accès.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-118">**Access Level.**</span></span> <span data-ttu-id="a0cbb-119">Si vous stockez des données sensibles de la propriété dans une ou plusieurs variables, déclarez-les [privée](../../../visual-basic/language-reference/modifiers/private.md) afin qu’aucun autre code pour n’y accéder.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-119">If you hold the property's sensitive data in one or more variables, declare them [Private](../../../visual-basic/language-reference/modifiers/private.md) so that no other code can access them.</span></span>  
  
-   <span data-ttu-id="a0cbb-120">**Chiffrement.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-120">**Encryption.**</span></span> <span data-ttu-id="a0cbb-121">Store toutes les données sensibles sous forme chiffrée plutôt qu’en texte brut.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-121">Store all sensitive data in encrypted form rather than in plain text.</span></span> <span data-ttu-id="a0cbb-122">Si un code malveillant d’une certaine manière parvient à accéder à cette zone de mémoire, il est plus difficile d’utiliser des données.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-122">If malicious code somehow gains access to that area of memory, it is more difficult to make use of the data.</span></span> <span data-ttu-id="a0cbb-123">Le chiffrement est également utile s’il est nécessaire de sérialiser les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-123">Encryption is also useful if it is necessary to serialize the sensitive data.</span></span>  
  
-   <span data-ttu-id="a0cbb-124">**La réinitialisation.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-124">**Resetting.**</span></span> <span data-ttu-id="a0cbb-125">Lors de la classe, une structure ou un module définissant la propriété est terminée, réinitialisez les données sensibles aux valeurs par défaut ou avec d’autres valeurs sans signification.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-125">When the class, structure, or module defining the property is being terminated, reset the sensitive data to default values or to other meaningless values.</span></span> <span data-ttu-id="a0cbb-126">Cela offre une protection supplémentaire lorsque cette zone de mémoire est libérée pour l’accès général.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-126">This gives extra protection when that area of memory is freed for general access.</span></span>  
  
-   <span data-ttu-id="a0cbb-127">**Persistance.**</span><span class="sxs-lookup"><span data-stu-id="a0cbb-127">**Persistence.**</span></span> <span data-ttu-id="a0cbb-128">Ne sont pas conservés toutes les données sensibles, par exemple sur le disque, si vous pouvez l’éviter.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-128">Do not persist any sensitive data, for example on disk, if you can avoid it.</span></span> <span data-ttu-id="a0cbb-129">En outre, n’écrivez pas toutes les données sensibles dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a0cbb-129">Also, do not write any sensitive data to the Clipboard.</span></span>  
  
 <span data-ttu-id="a0cbb-130">Le `WriteOnly` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="a0cbb-130">The `WriteOnly` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="a0cbb-131">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="a0cbb-131">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="a0cbb-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0cbb-132">See also</span></span>
- [<span data-ttu-id="a0cbb-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a0cbb-133">ReadOnly</span></span>](../../../visual-basic/language-reference/modifiers/readonly.md)
- [<span data-ttu-id="a0cbb-134">Private</span><span class="sxs-lookup"><span data-stu-id="a0cbb-134">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)
- [<span data-ttu-id="a0cbb-135">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a0cbb-135">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
