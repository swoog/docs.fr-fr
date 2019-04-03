---
title: Les constantes doivent être de type intrinsèque ou énuméré, et non de type classe, structure, paramètre de type ou tableau
ms.date: 07/20/2015
f1_keywords:
- vbc30424
- bc30424
helpviewer_keywords:
- BC30424
ms.assetid: 2d402c2f-27ad-428b-b699-d45cd62f7196
ms.openlocfilehash: f82a548c820aec7d2ae13c30a67d778fc167a8b6
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58813106"
---
# <a name="constants-must-be-of-an-intrinsic-or-enumerated-type-not-a-class-structure-type-parameter-or-array-type"></a><span data-ttu-id="6cfd0-102">Les constantes doivent être de type intrinsèque ou énuméré, et non de type classe, structure, paramètre de type ou tableau</span><span class="sxs-lookup"><span data-stu-id="6cfd0-102">Constants must be of an intrinsic or enumerated type, not a class, structure, type parameter, or array type</span></span>
<span data-ttu-id="6cfd0-103">Vous avez tenté de déclarer une constante comme une classe, une structure ou un type de tableau, ou comme un paramètre de type défini par un type générique conteneur.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-103">You have attempted to declare a constant as a class, structure, or array type, or as a type parameter defined by a containing generic type.</span></span>  
  
 <span data-ttu-id="6cfd0-104">Les constantes doivent être de type intrinsèque (`Boolean`, `Byte`, `Date`, `Decimal`, `Double`, `Integer`, `Long`, `Object`, `SByte`, `Short`, `Single`, `String`, `UInteger`, `ULong`, ou `UShort`), ou un `Enum` type basé sur l’un des types intégraux.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-104">Constants must be of an intrinsic type (`Boolean`, `Byte`, `Date`, `Decimal`, `Double`, `Integer`, `Long`, `Object`, `SByte`, `Short`, `Single`, `String`, `UInteger`, `ULong`, or `UShort`), or an `Enum` type based on one of the integral types.</span></span>  
  
 <span data-ttu-id="6cfd0-105">**ID d’erreur :** BC30424</span><span class="sxs-lookup"><span data-stu-id="6cfd0-105">**Error ID:** BC30424</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6cfd0-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="6cfd0-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="6cfd0-107">Déclarez la constante comme intrinsèque ou `Enum` type.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-107">Declare the constant as an intrinsic or `Enum` type.</span></span>  
  
2.  <span data-ttu-id="6cfd0-108">Une constante peut également être une valeur spéciale, tel que `True`, `False`, ou `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-108">A constant can also be a special value such as `True`, `False`, or `Nothing`.</span></span> <span data-ttu-id="6cfd0-109">Le compilateur considère ces valeurs prédéfinies sont du type intrinsèque approprié.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-109">The compiler considers these predefined values to be of the appropriate intrinsic type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cfd0-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cfd0-110">See also</span></span>

- [<span data-ttu-id="6cfd0-111">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="6cfd0-111">Constants and Enumerations</span></span>](../../../visual-basic/language-reference/constants-and-enumerations.md)
- [<span data-ttu-id="6cfd0-112">Types de données</span><span class="sxs-lookup"><span data-stu-id="6cfd0-112">Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="6cfd0-113">Types de données</span><span class="sxs-lookup"><span data-stu-id="6cfd0-113">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)
