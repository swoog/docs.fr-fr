---
title: End <keyword>, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.EndDefinition
helpviewer_keywords:
- End keyword [Visual Basic]
ms.assetid: 42d6e088-ab0f-4cda-88e8-fdce3e5fcf4f
ms.openlocfilehash: 96dc8ce6b0d3b7545f5caeef43358936e426f566
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638153"
---
# <a name="end-keyword-statement-visual-basic"></a><span data-ttu-id="badde-102">Fin \<mot clé > instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="badde-102">End \<keyword> Statement (Visual Basic)</span></span>

<span data-ttu-id="badde-103">S’il est suivi par un mot clé supplémentaire, termine la définition du bloc d’instruction introduit par ce mot clé.</span><span class="sxs-lookup"><span data-stu-id="badde-103">When followed by an additional keyword, terminates the definition of the statement block introduced by that keyword.</span></span>

## <a name="syntax"></a><span data-ttu-id="badde-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="badde-104">Syntax</span></span>

```vb
End AddHandler
End Class
End Enum
End Event
End Function
End Get
End If
End Interface
End Module
End Namespace
End Operator
End Property
End RaiseEvent  
End RemoveHandler  
End Select
End Set
End Structure
End Sub
End SyncLock
End Try
End While
End With  
```  
  
## <a name="parts"></a><span data-ttu-id="badde-105">Composants</span><span class="sxs-lookup"><span data-stu-id="badde-105">Parts</span></span>

|<span data-ttu-id="badde-106">Élément</span><span class="sxs-lookup"><span data-stu-id="badde-106">Part</span></span>|<span data-ttu-id="badde-107">Description</span><span class="sxs-lookup"><span data-stu-id="badde-107">Description</span></span>|
|---|---|
|`End`|<span data-ttu-id="badde-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="badde-108">Required.</span></span> <span data-ttu-id="badde-109">Met fin à la définition de l’élément de programmation.</span><span class="sxs-lookup"><span data-stu-id="badde-109">Terminates the definition of the programming element.</span></span>|
|`AddHandler`|<span data-ttu-id="badde-110">Requis pour terminer une `AddHandler` accesseur commencé par une mise en correspondance `AddHandler` instruction personnalisé [Event, instruction](event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-110">Required to terminate an `AddHandler` accessor begun by a matching `AddHandler` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`Class`|<span data-ttu-id="badde-111">Requis pour terminer une définition de classe commencée par un correspondant [Class, instruction](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-111">Required to terminate a class definition begun by a matching [Class Statement](class-statement.md).</span></span>|
|`Enum`|<span data-ttu-id="badde-112">Requis pour terminer une définition d’énumération commencée par un correspondant [Enum, instruction](enum-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-112">Required to terminate an enumeration definition begun by a matching [Enum Statement](enum-statement.md).</span></span>|
|`Event`|<span data-ttu-id="badde-113">Requis pour terminer un `Custom` définition d’événement commencée par une mise en correspondance [Event, instruction](event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-113">Required to terminate a `Custom` event definition begun by a matching [Event Statement](event-statement.md).</span></span>|  
|`Function`|<span data-ttu-id="badde-114">Requis pour terminer un `Function` définition de procédure commencée par un correspondant [Function, instruction](function-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-114">Required to terminate a `Function` procedure definition begun by a matching [Function Statement](function-statement.md).</span></span> <span data-ttu-id="badde-115">Si l’exécution rencontre une `End Function` instruction, contrôle retourne au code appelant.</span><span class="sxs-lookup"><span data-stu-id="badde-115">If execution encounters an `End Function` statement, control returns to the calling code.</span></span>|
|`Get`|<span data-ttu-id="badde-116">Requis pour terminer un `Property` définition de procédure commencée par un correspondant [une instruction Get](get-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-116">Required to terminate a `Property` procedure definition begun by a matching [Get Statement](get-statement.md).</span></span> <span data-ttu-id="badde-117">Si l’exécution rencontre une `End Get` instruction, contrôle retourne à l’instruction demandant la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="badde-117">If execution encounters an `End Get` statement, control returns to the statement requesting the property's value.</span></span>|
|`If`|<span data-ttu-id="badde-118">Requis pour terminer un `If`... `Then`... `Else` commencée par un correspondant `If` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-118">Required to terminate an `If`...`Then`...`Else` block definition begun by a matching `If` statement.</span></span> <span data-ttu-id="badde-119">Consultez [si... Then... Else, instruction](if-then-else-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-119">See [If...Then...Else Statement](if-then-else-statement.md).</span></span>|
|`Interface`|<span data-ttu-id="badde-120">Requis pour terminer une définition d’interface commencée par un correspondant [instruction Interface](interface-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-120">Required to terminate an interface definition begun by a matching [Interface Statement](interface-statement.md).</span></span>|
|`Module`|<span data-ttu-id="badde-121">Requis pour terminer une définition de module commencée par un correspondant [instruction Module](module-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-121">Required to terminate a module definition begun by a matching [Module Statement](module-statement.md).</span></span>|
|`Namespace`|<span data-ttu-id="badde-122">Requis pour terminer une définition d’espace de noms commencée par un correspondant [Namespace instruction](namespace-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-122">Required to terminate a namespace definition begun by a matching [Namespace Statement](namespace-statement.md).</span></span>|
|`Operator`|<span data-ttu-id="badde-123">Requis pour terminer une définition d’opérateur commencée par un correspondant [Operator Statement](operator-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-123">Required to terminate an operator definition begun by a matching [Operator Statement](operator-statement.md).</span></span>|
|`Property`|<span data-ttu-id="badde-124">Requis pour terminer une définition de propriété commencée par un correspondant [Property Statement](property-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-124">Required to terminate a property definition begun by a matching [Property Statement](property-statement.md).</span></span>|
|`RaiseEvent`|<span data-ttu-id="badde-125">Requis pour terminer un `RaiseEvent` accesseur commencé par une mise en correspondance `RaiseEvent` instruction personnalisé [Event, instruction](event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-125">Required to terminate a `RaiseEvent` accessor begun by a matching `RaiseEvent` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`RemoveHandler`|<span data-ttu-id="badde-126">Requis pour terminer un `RemoveHandler` accesseur commencé par une mise en correspondance `RemoveHandler` instruction personnalisé [Event, instruction](event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-126">Required to terminate a `RemoveHandler` accessor begun by a matching `RemoveHandler` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`Select`|<span data-ttu-id="badde-127">Requis pour terminer un `Select`... `Case` commencée par un correspondant `Select` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-127">Required to terminate a `Select`...`Case` block definition begun by a matching `Select` statement.</span></span> <span data-ttu-id="badde-128">Consultez [sélectionnez... Instruction case](select-case-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-128">See [Select...Case Statement](select-case-statement.md).</span></span>  
|`Set`|<span data-ttu-id="badde-129">Requis pour terminer un `Property` définition de procédure commencée par un correspondant [instruction Set](set-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-129">Required to terminate a `Property` procedure definition begun by a matching [Set Statement](set-statement.md).</span></span> <span data-ttu-id="badde-130">Si l’exécution rencontre une `End Set` instruction, contrôle retourne à l’instruction définissant la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="badde-130">If execution encounters an `End Set` statement, control returns to the statement setting the property's value.</span></span>  
|`Structure`|<span data-ttu-id="badde-131">Requis pour terminer une définition de structure commencée par un correspondant [instruction Structure](structure-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-131">Required to terminate a structure definition begun by a matching [Structure Statement](structure-statement.md).</span></span>  
|`Sub`|<span data-ttu-id="badde-132">Requis pour terminer un `Sub` définition de procédure commencée par un correspondant [Sub, instruction](sub-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-132">Required to terminate a `Sub` procedure definition begun by a matching [Sub Statement](sub-statement.md).</span></span> <span data-ttu-id="badde-133">Si l’exécution rencontre une `End Sub` instruction, contrôle retourne au code appelant.</span><span class="sxs-lookup"><span data-stu-id="badde-133">If execution encounters an `End Sub` statement, control returns to the calling code.</span></span>  
|`SyncLock`|<span data-ttu-id="badde-134">Requis pour terminer un `SyncLock` commencée par un correspondant `SyncLock` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-134">Required to terminate a `SyncLock` block definition begun by a matching `SyncLock` statement.</span></span> <span data-ttu-id="badde-135">Consultez [instruction SyncLock](synclock-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-135">See [SyncLock Statement](synclock-statement.md).</span></span>  
|`Try`|<span data-ttu-id="badde-136">Requis pour terminer un `Try`... `Catch`... `Finally` commencée par un correspondant `Try` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-136">Required to terminate a `Try`...`Catch`...`Finally` block definition begun by a matching `Try` statement.</span></span> <span data-ttu-id="badde-137">Consultez [essayez... Catch... Instruction finally](try-catch-finally-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-137">See [Try...Catch...Finally Statement](try-catch-finally-statement.md).</span></span>  
|`While`|<span data-ttu-id="badde-138">Requis pour terminer un `While` définition commencée par une mise en correspondance de la boucle `While` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-138">Required to terminate a `While` loop definition begun by a matching `While` statement.</span></span> <span data-ttu-id="badde-139">Consultez [tandis que... Fin While, instruction](while-end-while-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-139">See [While...End While Statement](while-end-while-statement.md).</span></span>  
|`With`| <span data-ttu-id="badde-140">Requis pour terminer un `With` commencée par un correspondant `With` instruction.</span><span class="sxs-lookup"><span data-stu-id="badde-140">Required to terminate a `With` block definition begun by a matching `With` statement.</span></span> <span data-ttu-id="badde-141">Consultez [avec... End With, instruction](with-end-with-statement.md).</span><span class="sxs-lookup"><span data-stu-id="badde-141">See [With...End With Statement](with-end-with-statement.md).</span></span>  
|||
  
## <a name="directives"></a><span data-ttu-id="badde-142">Directives</span><span class="sxs-lookup"><span data-stu-id="badde-142">Directives</span></span>

<span data-ttu-id="badde-143">Lorsque précédé par un signe dièse (`#`), le `End` mot clé termine un bloc de prétraitement introduit par la directive correspondante.</span><span class="sxs-lookup"><span data-stu-id="badde-143">When preceded by a number sign (`#`), the `End` keyword terminates a preprocessing block introduced by the corresponding directive.</span></span>  

```vb
#End ExternalSource
#End If
#End Region
```

|<span data-ttu-id="badde-144">Élément</span><span class="sxs-lookup"><span data-stu-id="badde-144">Part</span></span>|<span data-ttu-id="badde-145">Description</span><span class="sxs-lookup"><span data-stu-id="badde-145">Description</span></span>|
|---|---|
|`#End`|<span data-ttu-id="badde-146">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="badde-146">Required.</span></span> <span data-ttu-id="badde-147">Termine la définition du bloc de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="badde-147">Terminates the definition of the preprocessing block.</span></span>|
|`ExternalSource`|<span data-ttu-id="badde-148">Requis pour terminer un bloc source externe commencé par une mise en correspondance [#ExternalSource (directive)](../directives/externalsource-directive.md).</span><span class="sxs-lookup"><span data-stu-id="badde-148">Required to terminate an external source block begun by a matching [#ExternalSource Directive](../directives/externalsource-directive.md).</span></span>|
|`If`|<span data-ttu-id="badde-149">Requis pour terminer un bloc de compilation conditionnelle commencé par une mise en correspondance `#If` directive.</span><span class="sxs-lookup"><span data-stu-id="badde-149">Required to terminate a conditional compilation block begun by a matching `#If` directive.</span></span> <span data-ttu-id="badde-150">Consultez [#If... Then... #Else, Directives](../directives/if-then-else-directives.md).</span><span class="sxs-lookup"><span data-stu-id="badde-150">See [#If...Then...#Else Directives](../directives/if-then-else-directives.md).</span></span>|
|`Region`|<span data-ttu-id="badde-151">Requis pour terminer un bloc de région source commencé par une mise en correspondance [Directive #Region](../directives/region-directive.md).</span><span class="sxs-lookup"><span data-stu-id="badde-151">Required to terminate a source region block begun by a matching [#Region Directive](../directives/region-directive.md).</span></span>|
|||

## <a name="remarks"></a><span data-ttu-id="badde-152">Notes</span><span class="sxs-lookup"><span data-stu-id="badde-152">Remarks</span></span>

<span data-ttu-id="badde-153">Le [instruction End](end-statement.md), sans mot clé supplémentaire, termine l’exécution immédiatement.</span><span class="sxs-lookup"><span data-stu-id="badde-153">The [End Statement](end-statement.md), without an additional keyword, terminates execution immediately.</span></span>

## <a name="smart-device-developer-notes"></a><span data-ttu-id="badde-154">Remarques sur le développement Smart Device</span><span class="sxs-lookup"><span data-stu-id="badde-154">Smart Device Developer Notes</span></span>  

<span data-ttu-id="badde-155">La `End` instruction, sans mot clé supplémentaire, n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="badde-155">The `End` statement, without an additional keyword, is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="badde-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="badde-156">See also</span></span>

- [<span data-ttu-id="badde-157">End (instruction)</span><span class="sxs-lookup"><span data-stu-id="badde-157">End Statement</span></span>](end-statement.md)
