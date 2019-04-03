---
title: L'expression appelle de manière récursive la propriété conteneur '<propertyname>'
ms.date: 07/20/2015
f1_keywords:
- vbc42026
- BC42026
helpviewer_keywords:
- BC42026
ms.assetid: 4fde9db6-3bf3-48dc-8e05-981bf08969da
ms.openlocfilehash: a758d05cca5ca71943b0ef08184aef5b2c457739
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58836842"
---
# <a name="expression-recursively-calls-the-containing-property-propertyname"></a><span data-ttu-id="0f387-102">Récursive de l’expression appelle la propriété conteneur '\<nom_propriété >'</span><span class="sxs-lookup"><span data-stu-id="0f387-102">Expression recursively calls the containing property '\<propertyname>'</span></span>
<span data-ttu-id="0f387-103">Une instruction dans le `Set` d’une définition de propriété stocke une valeur dans le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0f387-103">A statement in the `Set` procedure of a property definition stores a value into the name of the property.</span></span>  
  
 <span data-ttu-id="0f387-104">L’approche recommandée pour stocker la valeur d’une propriété consiste à définir un `Private` variable dans le conteneur de la propriété et l’utiliser à la fois dans le `Get` et `Set` procédures.</span><span class="sxs-lookup"><span data-stu-id="0f387-104">The recommended approach to holding the value of a property is to define a `Private` variable in the property's container and use it in both the `Get` and `Set` procedures.</span></span> <span data-ttu-id="0f387-105">Le `Set` procédure doit ensuite stocker la valeur entrante dans ce `Private` variable.</span><span class="sxs-lookup"><span data-stu-id="0f387-105">The `Set` procedure should then store the incoming value in this `Private` variable.</span></span>  
  
 <span data-ttu-id="0f387-106">Le `Get` procédure se comporte comme un `Function` procédure, afin de pouvoir attribuer une valeur au nom de propriété et retourner le contrôle en utilisant la `End Get` instruction.</span><span class="sxs-lookup"><span data-stu-id="0f387-106">The `Get` procedure behaves like a `Function` procedure, so it can assign a value to the property name and return control by encountering the `End Get` statement.</span></span> <span data-ttu-id="0f387-107">L’approche recommandée, cependant, consiste à inclure le `Private` variable comme valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0f387-107">The recommended approach, however, is to include the `Private` variable as the value in a [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).</span></span>  
  
 <span data-ttu-id="0f387-108">Le `Set` procédure se comporte comme un `Sub` procédure qui ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f387-108">The `Set` procedure behaves like a `Sub` procedure, which does not return a value.</span></span> <span data-ttu-id="0f387-109">Par conséquent, le nom de la procédure ou propriété n’a aucune signification spéciale dans un `Set` procédure et vous ne pouvez pas stocker une valeur dedans.</span><span class="sxs-lookup"><span data-stu-id="0f387-109">Therefore, the procedure or property name has no special meaning within a `Set` procedure, and you cannot store a value into it.</span></span>  
  
 <span data-ttu-id="0f387-110">L’exemple suivant illustre l’approche qui peut provoquer cette erreur, suivie de l’approche recommandée.</span><span class="sxs-lookup"><span data-stu-id="0f387-110">The following example illustrates the approach that can cause this error, followed by the recommended approach.</span></span>  
  
```  
Public Class illustrateProperties  
' The code in the following property causes this error.  
    Public Property badProp() As Char  
        Get  
            Dim charValue As Char  
            ' Insert code to update charValue.  
            badProp = charValue  
        End Get  
        Set(ByVal Value As Char)  
            ' The following statement causes this error.  
            badProp = Value  
            ' The value stored in the local variable badProp  
            ' is not used by the Get procedure in this property.  
        End Set  
    End Property  
' The following code uses the recommended approach.  
    Private propValue As Char  
    Public Property goodProp() As Char  
        Get  
            ' Insert code to update propValue.  
            Return propValue  
        End Get  
        Set(ByVal Value As Char)  
            propValue = Value  
        End Set  
    End Property  
End Class  
```  
  
 <span data-ttu-id="0f387-111">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="0f387-111">By default, this message is a warning.</span></span> <span data-ttu-id="0f387-112">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="0f387-112">For more information about hiding warnings or treating warnings as errors, please see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="0f387-113">**ID d’erreur :** BC42026</span><span class="sxs-lookup"><span data-stu-id="0f387-113">**Error ID:** BC42026</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0f387-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0f387-114">To correct this error</span></span>  
  
-   <span data-ttu-id="0f387-115">Réécrivez la définition de propriété pour utiliser l’approche recommandée, comme illustré dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0f387-115">Rewrite the property definition to use the recommended approach as illustrated in the preceding example.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f387-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f387-116">See also</span></span>

- [<span data-ttu-id="0f387-117">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="0f387-117">Property Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
- [<span data-ttu-id="0f387-118">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="0f387-118">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="0f387-119">Set (instruction)</span><span class="sxs-lookup"><span data-stu-id="0f387-119">Set Statement</span></span>](../../../visual-basic/language-reference/statements/set-statement.md)
