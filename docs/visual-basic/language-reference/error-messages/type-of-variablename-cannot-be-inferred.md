---
title: Le type de '<variablename>' ne peut pas être déduit, car les limites de la boucle et la clause d'incrémentation ne sont pas converties en un même type
ms.date: 07/20/2015
f1_keywords:
- bc30982
- vbc30982
helpviewer_keywords:
- BC30982
ms.assetid: 741e85d9-a747-42ad-a1e1-a3f1928aaff5
ms.openlocfilehash: e90e881546c12df2c8b19ff03a4d4c7304c4596c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58815873"
---
# <a name="type-of-variablename-cannot-be-inferred-because-the-loop-bounds-and-the-step-variable-do-not-widen-to-the-same-type"></a><span data-ttu-id="acd3f-102">Type de '\<nom_variable >' ne peut pas être déduit, car les limites de la boucle et la variable étape s’étend pas au même type</span><span class="sxs-lookup"><span data-stu-id="acd3f-102">Type of '\<variablename>' cannot be inferred because the loop bounds and the step variable do not widen to the same type</span></span>
<span data-ttu-id="acd3f-103">Vous avez écrit un `For...Next` boucle dans laquelle le compilateur ne peut pas déduire un type de données pour la variable de contrôle de boucle, car les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="acd3f-103">You have written a `For...Next` loop in which the compiler cannot infer a data type for the loop control variable because the following conditions are true:</span></span>  
  
-   <span data-ttu-id="acd3f-104">Le type de données de la variable de contrôle de boucle n’est pas spécifié avec une clause `As` .</span><span class="sxs-lookup"><span data-stu-id="acd3f-104">The data type of the loop control variable is not specified with an `As` clause.</span></span>  
  
-   <span data-ttu-id="acd3f-105">Les limites de la boucle et l’incrémentation contiennent au moins deux types de données.</span><span class="sxs-lookup"><span data-stu-id="acd3f-105">The loop bounds and step variable contain at least two data types.</span></span>  
  
-   <span data-ttu-id="acd3f-106">Il n’existe aucune conversion standard entre les types de données.</span><span class="sxs-lookup"><span data-stu-id="acd3f-106">No standard conversions exist between the data types.</span></span>  
  
 <span data-ttu-id="acd3f-107">Par conséquent, le compilateur ne peut pas déduire le type de données de variable de contrôle d’une boucle.</span><span class="sxs-lookup"><span data-stu-id="acd3f-107">Therefore, the compiler cannot infer the data type of a loop's control variable.</span></span>  
  
 <span data-ttu-id="acd3f-108">Dans l’exemple suivant, la variable de l’étape est un caractère et les limites de la boucle sont les deux entiers.</span><span class="sxs-lookup"><span data-stu-id="acd3f-108">In the following example, the step variable is a character and the loop bounds are both integers.</span></span> <span data-ttu-id="acd3f-109">Comme il n’existe aucune conversion standard entre les caractères et les entiers, cette erreur est signalée.</span><span class="sxs-lookup"><span data-stu-id="acd3f-109">Because there is no standard conversion between characters and integers, this error is reported.</span></span>  
  
```vb  
Dim stepVar = "1"c  
Dim m = 0  
Dim n = 20  
  
' Not valid.  
' For i = 1 To 10 Step stepVar  
    ' Loop processing  
' Next  
```  
  
 <span data-ttu-id="acd3f-110">**ID d’erreur :** BC30982</span><span class="sxs-lookup"><span data-stu-id="acd3f-110">**Error ID:** BC30982</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="acd3f-111">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="acd3f-111">To correct this error</span></span>  
  
-   <span data-ttu-id="acd3f-112">Modifier les types des limites de la boucle et selon vos besoins afin qu’au moins un d'entre eux est un type de la clause d’incrémentation.</span><span class="sxs-lookup"><span data-stu-id="acd3f-112">Change the types of the loop bounds and step variable as necessary so that at least one of them is a type that the others widen to.</span></span> <span data-ttu-id="acd3f-113">Dans l’exemple précédent, remplacez le type de `stepVar` à `Integer`.</span><span class="sxs-lookup"><span data-stu-id="acd3f-113">In the preceding example, change the type of `stepVar` to `Integer`.</span></span>  
  
    ```  
    Dim stepVar = 1  
    ```  
  
     <span data-ttu-id="acd3f-114">- ou -</span><span class="sxs-lookup"><span data-stu-id="acd3f-114">—or—</span></span>  
  
    ```  
    Dim stepVar As Integer = 1  
    ```  
  
-   <span data-ttu-id="acd3f-115">Utiliser les fonctions de conversion explicite pour convertir les limites de la boucle et la variable de l’étape pour les types appropriés.</span><span class="sxs-lookup"><span data-stu-id="acd3f-115">Use explicit conversion functions to convert the loop bounds and step variable to the appropriate types.</span></span> <span data-ttu-id="acd3f-116">Dans l’exemple précédent, vous devez appliquer le `Val` à fonction `stepVar`.</span><span class="sxs-lookup"><span data-stu-id="acd3f-116">In the preceding example, apply the `Val` function to `stepVar`.</span></span>  
  
    ```  
    For i = 1 To 10 Step Val(stepVar)  
        ' Loop processing  
    Next  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="acd3f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acd3f-117">See also</span></span>

- <xref:Microsoft.VisualBasic.Conversion.Val%2A>
- [<span data-ttu-id="acd3f-118">For...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="acd3f-118">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [<span data-ttu-id="acd3f-119">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="acd3f-119">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="acd3f-120">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="acd3f-120">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="acd3f-121">Option Infer (instruction)</span><span class="sxs-lookup"><span data-stu-id="acd3f-121">Option Infer Statement</span></span>](../../../visual-basic/language-reference/statements/option-infer-statement.md)
- [<span data-ttu-id="acd3f-122">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="acd3f-122">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="acd3f-123">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="acd3f-123">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
