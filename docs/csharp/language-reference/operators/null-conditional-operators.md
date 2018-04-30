---
title: Opérateurs conditionnels Null (C# et Visual Basic)
ms.date: 04/03/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- null-conditional operators [C#]
- null-conditional operators [Visual Basic]
- ?. operator [C#]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 3ffeaa3c2088d0bb2c000704cfe312b0f9453b68
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a>Opérateurs conditionnels Null ?. et ?[] (C# et Visual Basic)
Ces opérateurs sont utilisés pour rechercher les valeurs Null avant d'effectuer une opération d'accès au membre (`?.`) ou d'indexation (`?[]`).  Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications Null, notamment pour l’exploration des structures de données.  
  
```csharp  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
```  
  
```vb  
Dim length = customers?.Length  ' null if customers is null  
Dim first as Customer = customers?(0)  ' null if customers is null  
Dim count as Integer? = customers?(0)?.Orders?.Count()  ' null if customers, the first customer, or Orders is null  
```  
  
 Les opérateurs conditionnels Null ont un effet de court-circuit.  Si une opération dans une chaîne d'opérations d'accès au membre et d'indexation conditionnelles retourne une valeur Null, l'exécution du reste de la chaîne s'arrête.  Dans l’exemple ci-dessous, `E` ne s’exécute pas si `A`, `B` ou `C` a une valeur Null.
  
```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

```vb
A?.B?.C?.Do(E);
A?.B?.C?(E);
```  
  
 L'accès au membre conditionnel Null s'utilise également pour appeler des délégués de façon thread-safe, avec beaucoup moins de code.  Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :  
  
```csharp  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…);
```  
  
```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```  
  
 La nouvelle méthode est beaucoup plus simple :  
  
```csharp
PropertyChanged?.Invoke(e)  
```  

```vb
PropertyChanged?.Invoke(e)
```  
  
 La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire.  
  
 Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.  
  
## <a name="language-specifications"></a>Spécifications du langage  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
 Pour plus d’informations, consultez [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md).  
  
## <a name="see-also"></a>Voir aussi  
 [?? (opérateur de fusion Null)](null-conditional-operator.md)  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md)  
 [Guide de programmation Visual Basic](../../../visual-basic/programming-guide/index.md)
