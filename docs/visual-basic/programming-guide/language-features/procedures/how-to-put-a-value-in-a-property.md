---
title: 'Procédure : Placer une valeur dans une propriété (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- Visual Basic code, properties
- properties [Visual Basic], values
ms.assetid: c39401e5-b5fc-4439-8f31-ed640f7ce6ed
ms.openlocfilehash: ee2449ff905bfdacaeeee4cc244db1ce50e00104
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824302"
---
# <a name="how-to-put-a-value-in-a-property-visual-basic"></a><span data-ttu-id="1aa3a-102">Procédure : Placer une valeur dans une propriété (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1aa3a-102">How to: Put a Value in a Property (Visual Basic)</span></span>
<span data-ttu-id="1aa3a-103">Vous stockez une valeur dans une propriété en plaçant le nom de propriété sur le côté gauche d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-103">You store a value in a property by putting the property name on the left side of an assignment statement.</span></span>  
  
 <span data-ttu-id="1aa3a-104">La propriété `Set` stocke une valeur, mais vous ne l’appelez pas explicitement par son nom.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-104">The property's `Set` procedure stores a value, but you do not explicitly call it by name.</span></span> <span data-ttu-id="1aa3a-105">Vous utilisez la propriété tout comme vous utiliseriez une variable.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-105">You use the property just as you would use a variable.</span></span> <span data-ttu-id="1aa3a-106">Visual Basic effectue les appels à des procédures de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-106">Visual Basic makes the calls to the property's procedures.</span></span>  
  
### <a name="to-store-a-value-in-a-property"></a><span data-ttu-id="1aa3a-107">Pour stocker une valeur dans une propriété</span><span class="sxs-lookup"><span data-stu-id="1aa3a-107">To store a value in a property</span></span>  
  
1.  <span data-ttu-id="1aa3a-108">Utilisez le nom de propriété sur le côté gauche d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-108">Use the property name on the left side of an assignment statement.</span></span>  
  
     <span data-ttu-id="1aa3a-109">L’exemple suivant définit la valeur de Visual Basic `TimeOfDay` propriété à midi, en appelant implicitement sa `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-109">The following example sets the value of the Visual Basic `TimeOfDay` property to noon, implicitly calling its `Set` procedure.</span></span>  
  
     [!code-vb[VbVbcnProcedures#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#11)]  
  
2.  <span data-ttu-id="1aa3a-110">Si la propriété prend des arguments, faites suivre le nom de propriété entre parenthèses pour encadrer la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-110">If the property takes arguments, follow the property name with parentheses to enclose the argument list.</span></span> <span data-ttu-id="1aa3a-111">S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-111">If there are no arguments, you can optionally omit the parentheses.</span></span>  
  
3.  <span data-ttu-id="1aa3a-112">Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-112">Place the arguments in the argument list within the parentheses, separated by commas.</span></span> <span data-ttu-id="1aa3a-113">Veillez à que vous fournir les arguments dans le même ordre que la propriété définit les paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-113">Be sure you supply the arguments in the same order that the property defines the corresponding parameters.</span></span>  
  
4.  <span data-ttu-id="1aa3a-114">La valeur générée sur le côté droit de l’instruction d’assignation est stockée dans la propriété.</span><span class="sxs-lookup"><span data-stu-id="1aa3a-114">The value generated on the right side of the assignment statement is stored in the property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1aa3a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aa3a-115">See also</span></span>

- <xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay%2A>
- [<span data-ttu-id="1aa3a-116">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="1aa3a-116">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="1aa3a-117">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="1aa3a-117">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="1aa3a-118">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="1aa3a-118">Property Statement</span></span>](../../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="1aa3a-119">Différences entre les propriétés et les Variables en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1aa3a-119">Differences Between Properties and Variables in Visual Basic</span></span>](./differences-between-properties-and-variables.md)
- [<span data-ttu-id="1aa3a-120">Guide pratique pour Créer une propriété</span><span class="sxs-lookup"><span data-stu-id="1aa3a-120">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="1aa3a-121">Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes</span><span class="sxs-lookup"><span data-stu-id="1aa3a-121">How to: Declare a Property with Mixed Access Levels</span></span>](./how-to-declare-a-property-with-mixed-access-levels.md)
- [<span data-ttu-id="1aa3a-122">Guide pratique pour Appeler une procédure de propriété</span><span class="sxs-lookup"><span data-stu-id="1aa3a-122">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="1aa3a-123">Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1aa3a-123">How to: Declare and Call a Default Property in Visual Basic</span></span>](./how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="1aa3a-124">Guide pratique pour Obtenir une valeur d’une propriété</span><span class="sxs-lookup"><span data-stu-id="1aa3a-124">How to: Get a Value from a Property</span></span>](./how-to-get-a-value-from-a-property.md)
