---
title: Opérateurs conditionnels null (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: d30d452a7c140a0c56529386b14ef3a3512df490
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722151"
---
# <a name="-and--null-conditional-operators-visual-basic"></a>?. et ? opérateurs de condition null () (Visual Basic)

Teste la valeur de l’opérande de gauche pour la valeur null (`Nothing`) avant d’effectuer un accès au membre (`?.`) ou d’un index (`?()`) de l’opération ; retourne `Nothing` si l’opérande de gauche a la valeur `Nothing`. Notez que, dans les expressions qui renverrait habituellement des types valeur, l’opérateur conditionnel null renvoie un <xref:System.Nullable%601>.

Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications « null », en particulier lors de la descente dans les structures de données. Exemple :

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

Pour la comparaison, le code de remplacement pour la première de ces expressions sans opérateur conditionnel null est :

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

Les opérateurs conditionnels Null ont un effet de court-circuit.  Si une opération dans une chaîne d’opérations d’accès et des index membre conditionnel ne retourne rien, le reste de l’exécution de la chaîne s’arrête.  Dans l’exemple suivant, c (e) n’est pas évaluée si `A`, `B`, ou `C` a la valeur Nothing.

```vb
A?.B?.C?(E);
```

Utilisez un autre pour l’accès aux membres conditionnels null consiste à appeler des délégués de façon thread-safe avec beaucoup moins de code.  Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

La nouvelle méthode est beaucoup plus simple :  

```vb
PropertyChanged?.Invoke(…)
```

La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire. Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.  

## <a name="see-also"></a>Voir aussi

- [Opérateurs (Visual Basic)](index.md)
- [Guide de programmation Visual Basic](../../../visual-basic/programming-guide/index.md)
- [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md)
