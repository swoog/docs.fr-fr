---
title: Le type <typename> n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- bc40041
- vbc40041
helpviewer_keywords:
- BC40041
ms.assetid: 634132c2-5646-44aa-98c6-f773e2e63882
ms.openlocfilehash: 243f51b3e6c798c82fdbe7b28557c4f96c728bf2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281721"
---
# <a name="type-typename-is-not-cls-compliant"></a><span data-ttu-id="7f8b1-102">Type \<typename > n’est pas conforme CLS</span><span class="sxs-lookup"><span data-stu-id="7f8b1-102">Type \<typename> is not CLS-compliant</span></span>
<span data-ttu-id="7f8b1-103">Une variable, une propriété ou un retour de fonction est déclaré avec un type de données qui n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-103">A variable, property, or function return is declared with a data type that is not CLS-compliant.</span></span>  
  
 <span data-ttu-id="7f8b1-104">Pour une application à laquelle se conformer les [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS), il doit utiliser uniquement des types conformes CLS.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-104">For an application to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must use only CLS-compliant types.</span></span>  
  
 <span data-ttu-id="7f8b1-105">Les types de données Visual Basic suivants ne sont pas conformes CLS :</span><span class="sxs-lookup"><span data-stu-id="7f8b1-105">The following Visual Basic data types are not CLS-compliant:</span></span>  
  
-   [<span data-ttu-id="7f8b1-106">SByte (type de données)</span><span class="sxs-lookup"><span data-stu-id="7f8b1-106">SByte Data Type</span></span>](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [<span data-ttu-id="7f8b1-107">UInteger (type de données)</span><span class="sxs-lookup"><span data-stu-id="7f8b1-107">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [<span data-ttu-id="7f8b1-108">ULong (type de données)</span><span class="sxs-lookup"><span data-stu-id="7f8b1-108">ULong Data Type</span></span>](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [<span data-ttu-id="7f8b1-109">UShort (type de données)</span><span class="sxs-lookup"><span data-stu-id="7f8b1-109">UShort Data Type</span></span>](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 <span data-ttu-id="7f8b1-110">**ID d’erreur :** BC40041</span><span class="sxs-lookup"><span data-stu-id="7f8b1-110">**Error ID:** BC40041</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7f8b1-111">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="7f8b1-111">To correct this error</span></span>  
  
-   <span data-ttu-id="7f8b1-112">Si votre application doit être conforme CLS, modifiez le type de données de cet élément vers le type conforme CLS le plus proche.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-112">If your application needs to be CLS-compliant, change the data type of this element to the closest CLS-compliant type.</span></span> <span data-ttu-id="7f8b1-113">Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-113">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="7f8b1-114">Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-114">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>  
  
-   <span data-ttu-id="7f8b1-115">Si votre application n’a pas besoin être conforme CLS, il est inutile de modifier quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-115">If your application does not need to be CLS-compliant, you do not need to change anything.</span></span> <span data-ttu-id="7f8b1-116">Vous devez connaître son non-conformité, toutefois.</span><span class="sxs-lookup"><span data-stu-id="7f8b1-116">You should be aware of its noncompliance, however.</span></span>