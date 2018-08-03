---
title: Fin &lt;mot clé&gt; instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.EndDefinition
helpviewer_keywords:
- End keyword [Visual Basic]
ms.assetid: 42d6e088-ab0f-4cda-88e8-fdce3e5fcf4f
ms.openlocfilehash: 8137434bfd8c26144d78b1761b784cdba4894eaf
ms.sourcegitcommit: 7fe772c6c05a982153655d618c826e9839d39cac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/03/2018
ms.locfileid: "33605262"
---
# <a name="end-ltkeywordgt-statement-visual-basic"></a>Fin &lt;mot clé&gt; instruction (Visual Basic)

S’il est suivi par un mot clé supplémentaire, termine la définition du bloc d’instruction introduit par ce mot clé.

## <a name="syntax"></a>Syntaxe

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
  
## <a name="parts"></a>Composants

|Élément|Description|
|---|---|
|`End`|Obligatoire. Met fin à la définition de l’élément de programmation.|
|`AddHandler`|Requis pour terminer une `AddHandler` accesseur commencé par une mise en correspondance `AddHandler` instruction personnalisé [Event, instruction](event-statement.md).|
|`Class`|Requis pour terminer une définition de classe commencée par un correspondant [Class, instruction](class-statement.md).|
|`Enum`|Requis pour terminer une définition d’énumération commencée par un correspondant [Enum, instruction](enum-statement.md).|
|`Event`|Requis pour terminer un `Custom` définition d’événement commencée par une mise en correspondance [Event, instruction](event-statement.md).|  
|`Function`|Requis pour terminer un `Function` définition de procédure commencée par un correspondant [Function, instruction](function-statement.md). Si l’exécution rencontre une `End Function` instruction, contrôle retourne au code appelant.|
|`Get`|Requis pour terminer un `Property` définition de procédure commencée par un correspondant [une instruction Get](get-statement.md). Si l’exécution rencontre une `End Get` instruction, contrôle retourne à l’instruction demandant la valeur de propriété.|
|`If`|Requis pour terminer un `If`... `Then`... `Else` commencée par un correspondant `If` instruction. Consultez [si... Then... Else, instruction](if-then-else-statement.md).|
|`Interface`|Requis pour terminer une définition d’interface commencée par un correspondant [instruction Interface](interface-statement.md).|
|`Module`|Requis pour terminer une définition de module commencée par un correspondant [instruction Module](module-statement.md).|
|`Namespace`|Requis pour terminer une définition d’espace de noms commencée par un correspondant [Namespace instruction](namespace-statement.md).|
|`Operator`|Requis pour terminer une définition d’opérateur commencée par un correspondant [Operator Statement](operator-statement.md).|
|`Property`|Requis pour terminer une définition de propriété commencée par un correspondant [Property Statement](property-statement.md).|
|`RaiseEvent`|Requis pour terminer un `RaiseEvent` accesseur commencé par une mise en correspondance `RaiseEvent` instruction personnalisé [Event, instruction](event-statement.md).|
|`RemoveHandler`|Requis pour terminer un `RemoveHandler` accesseur commencé par une mise en correspondance `RemoveHandler` instruction personnalisé [Event, instruction](event-statement.md).|
|`Select`|Requis pour terminer un `Select`... `Case` commencée par un correspondant `Select` instruction. Consultez [sélectionnez... Instruction case](select-case-statement.md).  
|`Set`|Requis pour terminer un `Property` définition de procédure commencée par un correspondant [instruction Set](set-statement.md). Si l’exécution rencontre une `End Set` instruction, contrôle retourne à l’instruction définissant la valeur de propriété.  
|`Structure`|Requis pour terminer une définition de structure commencée par un correspondant [instruction Structure](structure-statement.md).  
|`Sub`|Requis pour terminer un `Sub` définition de procédure commencée par un correspondant [Sub, instruction](sub-statement.md). Si l’exécution rencontre une `End Sub` instruction, contrôle retourne au code appelant.  
|`SyncLock`|Requis pour terminer un `SyncLock` commencée par un correspondant `SyncLock` instruction. Consultez [instruction SyncLock](synclock-statement.md).  
|`Try`|Requis pour terminer un `Try`... `Catch`... `Finally` commencée par un correspondant `Try` instruction. Consultez [essayez... Catch... Instruction finally](try-catch-finally-statement.md).  
|`While`|Requis pour terminer un `While` définition commencée par une mise en correspondance de la boucle `While` instruction. Consultez [tandis que... Fin While, instruction](while-end-while-statement.md).  
|`With`| Requis pour terminer un `With` commencée par un correspondant `With` instruction. Consultez [avec... End With, instruction](with-end-with-statement.md).  
|||
  
## <a name="directives"></a>Directives

Lorsque précédé par un signe dièse (`#`), le `End` mot clé termine un bloc de prétraitement introduit par la directive correspondante.  

```vb
#End ExternalSource
#End If
#End Region
```

|Élément|Description|
|---|---|
|`#End`|Obligatoire. Termine la définition du bloc de prétraitement.|
|`ExternalSource`|Requis pour terminer un bloc source externe commencé par une mise en correspondance [#ExternalSource (directive)](../directives/externalsource-directive.md).|
|`If`|Requis pour terminer un bloc de compilation conditionnelle commencé par une mise en correspondance `#If` directive. Consultez [#If... Then... #Else, Directives](../directives/if-then-else-directives.md).|
|`Region`|Requis pour terminer un bloc de région source commencé par une mise en correspondance [Directive #Region](../directives/region-directive.md).|
|||

## <a name="remarks"></a>Notes

Le [instruction End](end-statement.md), sans mot clé supplémentaire, termine l’exécution immédiatement.

## <a name="smart-device-developer-notes"></a>Remarques sur le développement Smart Device  

La `End` instruction, sans mot clé supplémentaire, n’est pas pris en charge.  
  
## <a name="see-also"></a>Voir aussi

[End (instruction)](end-statement.md)
