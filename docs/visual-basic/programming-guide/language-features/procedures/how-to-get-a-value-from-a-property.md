---
title: 'Procédure : Obtenir une valeur d’une propriété (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- Visual Basic code, properties
- properties [Visual Basic], values
ms.assetid: 3954423e-6ab7-4a4c-b55c-a8d27be47891
ms.openlocfilehash: 356230a0b5a2c575ee554ce7f2cdb4a2f741ecac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543368"
---
# <a name="how-to-get-a-value-from-a-property-visual-basic"></a><span data-ttu-id="aadac-102">Procédure : Obtenir une valeur d’une propriété (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="aadac-102">How to: Get a Value from a Property (Visual Basic)</span></span>
<span data-ttu-id="aadac-103">Vous récupérez des valeur d’une propriété en incluant le nom de propriété dans une expression.</span><span class="sxs-lookup"><span data-stu-id="aadac-103">You retrieve a property's value by including the property name in an expression.</span></span>  
  
 <span data-ttu-id="aadac-104">La propriété `Get` procédure récupère la valeur, mais vous ne l’appelez pas explicitement par son nom.</span><span class="sxs-lookup"><span data-stu-id="aadac-104">The property's `Get` procedure retrieves the value, but you do not explicitly call it by name.</span></span> <span data-ttu-id="aadac-105">Vous utilisez la propriété tout comme vous utiliseriez une variable.</span><span class="sxs-lookup"><span data-stu-id="aadac-105">You use the property just as you would use a variable.</span></span> <span data-ttu-id="aadac-106">Visual Basic effectue les appels à des procédures de la propriété.</span><span class="sxs-lookup"><span data-stu-id="aadac-106">Visual Basic makes the calls to the property's procedures.</span></span>  
  
### <a name="to-retrieve-a-value-from-a-property"></a><span data-ttu-id="aadac-107">Pour récupérer une valeur à partir d’une propriété</span><span class="sxs-lookup"><span data-stu-id="aadac-107">To retrieve a value from a property</span></span>  
  
1.  <span data-ttu-id="aadac-108">Utilisez le nom de propriété dans une expression de la même façon que vous utiliseriez un nom de variable.</span><span class="sxs-lookup"><span data-stu-id="aadac-108">Use the property name in an expression the same way you would use a variable name.</span></span> <span data-ttu-id="aadac-109">Vous pouvez utiliser une propriété partout où vous pouvez utiliser une variable ou une constante.</span><span class="sxs-lookup"><span data-stu-id="aadac-109">You can use a property anywhere you can use a variable or a constant.</span></span>  
  
     <span data-ttu-id="aadac-110">ou</span><span class="sxs-lookup"><span data-stu-id="aadac-110">-or-</span></span>  
  
     <span data-ttu-id="aadac-111">Utilisez le nom de propriété suivant égaux (`=`) connectez-vous à une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="aadac-111">Use the property name following the equal (`=`) sign in an assignment statement.</span></span>  
  
     <span data-ttu-id="aadac-112">L’exemple suivant lit la valeur de Visual Basic `Now` propriété implicitement en appelant son `Get` procédure.</span><span class="sxs-lookup"><span data-stu-id="aadac-112">The following example reads the value of the Visual Basic `Now` property, implicitly calling its `Get` procedure.</span></span>  
  
     [!code-vb[VbVbalrDateProperties#4](./codesnippet/VisualBasic/how-to-get-a-value-from-a-property_1.vb)]  
  
2.  <span data-ttu-id="aadac-113">Si la propriété prend des arguments, faites suivre le nom de propriété entre parenthèses pour encadrer la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="aadac-113">If the property takes arguments, follow the property name with parentheses to enclose the argument list.</span></span> <span data-ttu-id="aadac-114">S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="aadac-114">If there are no arguments, you can optionally omit the parentheses.</span></span>  
  
3.  <span data-ttu-id="aadac-115">Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="aadac-115">Place the arguments in the argument list within the parentheses, separated by commas.</span></span> <span data-ttu-id="aadac-116">Veillez à que vous fournir les arguments dans le même ordre que la propriété définit les paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="aadac-116">Be sure you supply the arguments in the same order that the property defines the corresponding parameters.</span></span>  
  
 <span data-ttu-id="aadac-117">La valeur de la propriété participe à l’expression comme une variable ou constante serait, ou il est stocké dans la variable ou la propriété sur le côté gauche de l’instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="aadac-117">The value of the property participates in the expression just as a variable or constant would, or it is stored in the variable or property on the left side of the assignment statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aadac-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aadac-118">See also</span></span>
- [<span data-ttu-id="aadac-119">Procédures</span><span class="sxs-lookup"><span data-stu-id="aadac-119">Procedures</span></span>](./index.md)
- [<span data-ttu-id="aadac-120">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="aadac-120">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="aadac-121">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="aadac-121">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="aadac-122">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="aadac-122">Property Statement</span></span>](../../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="aadac-123">Différences entre les propriétés et les Variables en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aadac-123">Differences Between Properties and Variables in Visual Basic</span></span>](./differences-between-properties-and-variables.md)
- [<span data-ttu-id="aadac-124">Guide pratique pour Créer une propriété</span><span class="sxs-lookup"><span data-stu-id="aadac-124">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="aadac-125">Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes</span><span class="sxs-lookup"><span data-stu-id="aadac-125">How to: Declare a Property with Mixed Access Levels</span></span>](./how-to-declare-a-property-with-mixed-access-levels.md)
- [<span data-ttu-id="aadac-126">Guide pratique pour Appeler une procédure de propriété</span><span class="sxs-lookup"><span data-stu-id="aadac-126">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="aadac-127">Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aadac-127">How to: Declare and Call a Default Property in Visual Basic</span></span>](./how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="aadac-128">Guide pratique pour Placer une valeur dans une propriété</span><span class="sxs-lookup"><span data-stu-id="aadac-128">How to: Put a Value in a Property</span></span>](./how-to-put-a-value-in-a-property.md)
