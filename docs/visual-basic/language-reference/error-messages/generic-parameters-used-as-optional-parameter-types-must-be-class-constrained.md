---
title: Les paramètres génériques utilisés comme types de paramètres optionnels doivent être contraints par classe
ms.date: 07/20/2015
f1_keywords:
- vbc32124
- bc32124
helpviewer_keywords:
- BC32124
ms.assetid: 55aa8b2a-9ce3-4620-a710-2f9b0feb6143
ms.openlocfilehash: 11cf4f8d9457ebff385a601786dc97334f274324
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662059"
---
# <a name="generic-parameters-used-as-optional-parameter-types-must-be-class-constrained"></a><span data-ttu-id="0ae3b-102">Les paramètres génériques utilisés comme types de paramètres optionnels doivent être contraints par classe</span><span class="sxs-lookup"><span data-stu-id="0ae3b-102">Generic parameters used as optional parameter types must be class constrained</span></span>
<span data-ttu-id="0ae3b-103">Une procédure est déclarée avec un paramètre optionnel qui utilise un paramètre de type qui n’est pas contraint à être un type référence.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-103">A procedure is declared with an optional parameter that uses a type parameter that is not constrained to be a reference type.</span></span>  
  
 <span data-ttu-id="0ae3b-104">Vous devez toujours fournir une valeur par défaut pour chaque paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-104">You must always supply a default value for each optional parameter.</span></span> <span data-ttu-id="0ae3b-105">Si le paramètre est de type référence, la valeur facultative doit être `Nothing`, qui est une valeur valide pour tout type référence.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-105">If the parameter is of a reference type, the optional value must be `Nothing`, which is a valid value for any reference type.</span></span> <span data-ttu-id="0ae3b-106">Toutefois, si le paramètre est d’un type valeur, ce type doit être un type de données élémentaire prédéfini par Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-106">However, if the parameter is of a value type, that type must be an elementary data type predefined by Visual Basic.</span></span> <span data-ttu-id="0ae3b-107">Il s’agit, car un type de valeur composite, comme une structure définie par l’utilisateur, n’a aucune valeur par défaut valide.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-107">This is because a composite value type, such as a user-defined structure, has no valid default value.</span></span>  
  
 <span data-ttu-id="0ae3b-108">Lorsque vous utilisez un paramètre de type pour un paramètre facultatif, vous devez vous assurer qu’il s’agit d’un type référence afin d’éviter l’éventualité d’un type valeur sans valeur par défaut valide.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-108">When you use a type parameter for an optional parameter, you must guarantee that it is of a reference type to avoid the possibility of a value type with no valid default value.</span></span> <span data-ttu-id="0ae3b-109">Cela signifie que vous devez contraindre le paramètre de type avec le `Class` mot clé ou avec le nom d’une classe spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-109">This means you must constrain the type parameter either with the `Class` keyword or with the name of a specific class.</span></span>  
  
 <span data-ttu-id="0ae3b-110">**ID d’erreur :** BC32124</span><span class="sxs-lookup"><span data-stu-id="0ae3b-110">**Error ID:** BC32124</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0ae3b-111">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0ae3b-111">To correct this error</span></span>  
  
- <span data-ttu-id="0ae3b-112">Contraindre le paramètre de type pour accepter uniquement un type référence, ou ne l’utilisez pas pour le paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="0ae3b-112">Constrain the type parameter to accept only a reference type, or do not use it for the optional parameter.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ae3b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ae3b-113">See also</span></span>

- [<span data-ttu-id="0ae3b-114">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0ae3b-114">Generic Types in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [<span data-ttu-id="0ae3b-115">Liste de types</span><span class="sxs-lookup"><span data-stu-id="0ae3b-115">Type List</span></span>](../../../visual-basic/language-reference/statements/type-list.md)
- [<span data-ttu-id="0ae3b-116">Class (instruction)</span><span class="sxs-lookup"><span data-stu-id="0ae3b-116">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)
- [<span data-ttu-id="0ae3b-117">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="0ae3b-117">Optional Parameters</span></span>](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
- [<span data-ttu-id="0ae3b-118">Structures</span><span class="sxs-lookup"><span data-stu-id="0ae3b-118">Structures</span></span>](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="0ae3b-119">Nothing</span><span class="sxs-lookup"><span data-stu-id="0ae3b-119">Nothing</span></span>](../../../visual-basic/language-reference/nothing.md)
