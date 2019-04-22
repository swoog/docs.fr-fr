---
title: Assignation des variables objets (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Nothing keyword [Visual Basic], object variable assignment
- object variables [Visual Basic], initializing
- variables [Visual Basic], initializing
- objects [Visual Basic], current instance
- object variables [Visual Basic], assigning
- variables [Visual Basic], object variables
- current instance [Visual Basic], defined
- variables [Visual Basic], assigning
- assignment statements [Visual Basic], object variable assignment
- Me keyword [Visual Basic], as object variable
ms.assetid: 3706811d-fd40-44fe-8727-d692e8e55d6d
ms.openlocfilehash: dff1b9bb9e87f827663786cac3f33531db41b2c1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58840274"
---
# <a name="object-variable-assignment-visual-basic"></a><span data-ttu-id="5c791-102">Assignation des variables objets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5c791-102">Object Variable Assignment (Visual Basic)</span></span>
<span data-ttu-id="5c791-103">Vous utilisez une instruction d’assignation normale pour assigner un objet à une variable objet.</span><span class="sxs-lookup"><span data-stu-id="5c791-103">You use a normal assignment statement to assign an object to an object variable.</span></span> <span data-ttu-id="5c791-104">Vous pouvez affecter une expression d’objet ou le [rien](../../../../visual-basic/language-reference/nothing.md) mot clé, comme dans l’exemple suivant illustre.</span><span class="sxs-lookup"><span data-stu-id="5c791-104">You can assign an object expression or the [Nothing](../../../../visual-basic/language-reference/nothing.md) keyword, as the following example illustrates.</span></span>  
  
```  
Dim thisObject As Object  
' The following statement assigns an object reference.  
thisObject = Form1  
' The following statement discontinues association with any object.  
thisObject = Nothing  
```  
  
 <span data-ttu-id="5c791-105">`Nothing` signifie qu’il n’existe aucun objet actuellement affecté à la variable.</span><span class="sxs-lookup"><span data-stu-id="5c791-105">`Nothing` means there is no object currently assigned to the variable.</span></span>  
  
## <a name="initialization"></a><span data-ttu-id="5c791-106">Initialisation</span><span class="sxs-lookup"><span data-stu-id="5c791-106">Initialization</span></span>  
 <span data-ttu-id="5c791-107">Lorsque votre code commence à exécuter, vos variables objet sont initialisées à `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="5c791-107">When your code begins running, your object variables are initialized to `Nothing`.</span></span> <span data-ttu-id="5c791-108">Ceux dont les déclarations incluent l’initialisation sont réinitialisés aux valeurs que vous spécifiez quand les instructions de déclaration sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="5c791-108">Those whose declarations include initialization are reinitialized to the values you specify when the declaration statements are executed.</span></span>  
  
 <span data-ttu-id="5c791-109">Vous pouvez inclure l’initialisation dans votre déclaration à l’aide de la [New](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé.</span><span class="sxs-lookup"><span data-stu-id="5c791-109">You can include initialization in your declaration by using the [New](../../../../visual-basic/language-reference/operators/new-operator.md) keyword.</span></span> <span data-ttu-id="5c791-110">Les instructions de déclaration suivantes déclarent des variables objets `testUri` et `ver` et leur attribuer des objets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5c791-110">The following declaration statements declare object variables `testUri` and `ver` and assign specific objects to them.</span></span> <span data-ttu-id="5c791-111">Chacun utilise un des constructeurs surchargés de la classe appropriée pour initialiser l’objet.</span><span class="sxs-lookup"><span data-stu-id="5c791-111">Each uses one of the overloaded constructors of the appropriate class to initialize the object.</span></span>  
  
```  
Dim testUri As New System.Uri("https://www.microsoft.com")  
Dim ver As New System.Version(6, 1, 0)  
```  
  
## <a name="disassociation"></a><span data-ttu-id="5c791-112">Disassociation</span><span class="sxs-lookup"><span data-stu-id="5c791-112">Disassociation</span></span>  
 <span data-ttu-id="5c791-113">Affectation à une variable objet `Nothing` interrompt l’association de la variable et un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="5c791-113">Setting an object variable to `Nothing` discontinues the association of the variable with any specific object.</span></span> <span data-ttu-id="5c791-114">Cela vous empêche de modifier accidentellement l’objet en modifiant la variable.</span><span class="sxs-lookup"><span data-stu-id="5c791-114">This prevents you from accidentally changing the object by changing the variable.</span></span> <span data-ttu-id="5c791-115">Il vous permet également de tester si la variable objet pointe vers un objet valide, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5c791-115">It also allows you to test whether the object variable points to a valid object, as the following example shows.</span></span>  
  
```  
If otherObject IsNot Nothing Then  
    ' otherObject refers to a valid object, so your code can use it.  
End If  
```  
  
 <span data-ttu-id="5c791-116">Si l’objet désigné par votre variable est dans une autre application, ce test ne peut pas déterminer si cette application a terminé ou invalider l’objet.</span><span class="sxs-lookup"><span data-stu-id="5c791-116">If the object your variable refers to is in another application, this test cannot determine whether that application has terminated or just invalidated the object.</span></span>  
  
 <span data-ttu-id="5c791-117">Une variable objet avec la valeur `Nothing` est également appelé un *référence null*.</span><span class="sxs-lookup"><span data-stu-id="5c791-117">An object variable with a value of `Nothing` is also called a *null reference*.</span></span>  
  
## <a name="current-instance"></a><span data-ttu-id="5c791-118">Instance actuelle</span><span class="sxs-lookup"><span data-stu-id="5c791-118">Current Instance</span></span>  
 <span data-ttu-id="5c791-119">Le *instance actuelle* d’un objet est celui dans lequel le code est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5c791-119">The *current instance* of an object is the one in which the code is currently executing.</span></span> <span data-ttu-id="5c791-120">Dans la mesure où tout le code s’exécute à l’intérieur d’une procédure, l’instance actuelle est celui dans lequel la procédure a été appelée.</span><span class="sxs-lookup"><span data-stu-id="5c791-120">Since all code executes inside a procedure, the current instance is the one in which the procedure was invoked.</span></span>  
  
 <span data-ttu-id="5c791-121">Le `Me` mot clé agit comme une variable objet faisant référence à l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="5c791-121">The `Me` keyword acts as an object variable referring to the current instance.</span></span> <span data-ttu-id="5c791-122">Si une procédure n’est pas [partagé](../../../../visual-basic/language-reference/modifiers/shared.md), il peut utiliser le `Me` mot clé pour obtenir un pointeur vers l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="5c791-122">If a procedure is not [Shared](../../../../visual-basic/language-reference/modifiers/shared.md), it can use the `Me` keyword to obtain a pointer to the current instance.</span></span> <span data-ttu-id="5c791-123">Les procédures partagées ne peut pas être associés à une instance spécifique d’une classe.</span><span class="sxs-lookup"><span data-stu-id="5c791-123">Shared procedures cannot be associated with a specific instance of a class.</span></span>  
  
 <span data-ttu-id="5c791-124">À l’aide de `Me` est particulièrement utile pour passer l’instance actuelle à une procédure dans un autre module.</span><span class="sxs-lookup"><span data-stu-id="5c791-124">Using `Me` is particularly useful for passing the current instance to a procedure in another module.</span></span> <span data-ttu-id="5c791-125">Par exemple, supposons que vous avez un nombre de documents XML et que vous souhaitez ajouter un texte standard à toutes les.</span><span class="sxs-lookup"><span data-stu-id="5c791-125">For example, suppose you have a number of XML documents and wish to add some standard text to all of them.</span></span> <span data-ttu-id="5c791-126">L’exemple suivant définit une procédure pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="5c791-126">The following example defines a procedure to do this.</span></span>  
  
```  
Sub addStandardText(XmlDoc As System.Xml.XmlDocument)  
    XmlDoc.CreateTextNode("This text goes into every XML document.")  
End Sub  
```  
  
 <span data-ttu-id="5c791-127">Chaque objet de document XML peut ensuite appeler la procédure et passer son instance actuelle en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="5c791-127">Every XML document object could then call the procedure and pass its current instance as an argument.</span></span> <span data-ttu-id="5c791-128">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5c791-128">The following example demonstrates this.</span></span>  
  
```  
addStandardText(Me)  
```  
  
## <a name="see-also"></a><span data-ttu-id="5c791-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c791-129">See also</span></span>

- [<span data-ttu-id="5c791-130">Variables objets</span><span class="sxs-lookup"><span data-stu-id="5c791-130">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="5c791-131">Déclaration des variables objets</span><span class="sxs-lookup"><span data-stu-id="5c791-131">Object Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [<span data-ttu-id="5c791-132">Valeurs des variables objets</span><span class="sxs-lookup"><span data-stu-id="5c791-132">Object Variable Values</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
- [<span data-ttu-id="5c791-133">Guide pratique pour Déclarer une Variable objet et lui assigner un objet en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5c791-133">How to: Declare an Object Variable and Assign an Object to It in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-declare-an-object-variable-and-assign-an-object-to-it.md)
- [<span data-ttu-id="5c791-134">Guide pratique pour Crée un objet de Variable ne fait pas référence à une Instance</span><span class="sxs-lookup"><span data-stu-id="5c791-134">How to: Make an Object Variable Not Refer to Any Instance</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-make-an-object-variable-not-refer-to-any-instance.md)
- [<span data-ttu-id="5c791-135">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="5c791-135">Me, My, MyBase, and MyClass</span></span>](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
