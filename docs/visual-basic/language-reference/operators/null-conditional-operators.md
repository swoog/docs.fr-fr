---
title: Opérateurs conditionnels null (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: 4815fe7ad337634cfb56127fbd24a47a37fdd74b
ms.sourcegitcommit: ca2ca60e6f5ea327f164be7ce26d9599e0f85fe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65062944"
---
# <a name="-and--null-conditional-operators-visual-basic"></a>?. et ? opérateurs de condition null () (Visual Basic)

Teste la valeur de l’opérande de gauche pour la valeur null (`Nothing`) avant d’effectuer un accès au membre (`?.`) ou d’un index (`?()`) de l’opération ; retourne `Nothing` si l’opérande de gauche a la valeur `Nothing`. Notez que dans les expressions qui retournent des types valeur en règle générale, l’opérateur conditionnel null renvoie un <xref:System.Nullable%601>.

Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications « null », en particulier lors de la descente dans les structures de données. Exemple :

```vb
' Nothing if customers is Nothing  
Dim length As Integer? = customers?.Length  

' Nothing if customers is Nothing
Dim first As Customer = customers?(0)

' Nothing if customers, the first customer, or Orders is Nothing
Dim count As Integer? = customers?(0)?.Orders?.Count()   
```

Pour la comparaison, le code de remplacement pour la première de ces expressions sans opérateur conditionnel null est :

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

Parfois, vous devez entreprendre une action sur un objet qui peut être null, selon la valeur d’un membre Boolean sur cet objet (telles que la propriété booléenne `IsAllowedFreeShipping` dans l’exemple suivant) :

```vb
  Dim customer = FindCustomerByID(123) 'customer will be Nothing if not found.
  
  If customer IsNot Nothing AndAlso customer.IsAllowedFreeShipping Then
   ApplyFreeShippingToOrders(customer)
  End If
```

Vous pouvez raccourcir votre code et éviter de vérifier manuellement les valeurs null à l’aide de l’opérateur conditionnel null comme suit :

```vb
 Dim customer = FindCustomerByID(123) 'customer will be Nothing if not found.
 
 If customer?.IsAllowedFreeShipping Then ApplyFreeShippingToOrders(customer)
```

Les opérateurs conditionnels Null ont un effet de court-circuit.  Si une opération dans une chaîne d’opérations d’accès et des index membre conditionnel retourne `Nothing`, le reste de le de la chaîne exécution s’arrête.  Dans l’exemple suivant, `C(E)` n’est pas évaluée si `A`, `B`, ou `C` prend la valeur `Nothing`.

```vb
A?.B?.C?(E);
```

Utilisez un autre pour l’accès aux membres conditionnels null consiste à appeler des délégués de façon thread-safe avec beaucoup moins de code.  L’exemple suivant définit deux types, un `NewsBroadcaster` et un `NewsReceiver`. Éléments de News sont envoyés au destinataire par le `NewsBroadcaster.SendNews` déléguer.

```vb
Public Module NewsBroadcaster
   Dim SendNews As Action(Of String) 

   Public Sub Main()
      Dim rec As New NewsReceiver()
      Dim rec2 As New NewsReceiver()
      SendNews?.Invoke("Just in: A newsworthy item...")
   End Sub

   Public Sub Register(client As Action(Of String))
      SendNews = SendNews.Combine({SendNews, client})
   End Sub
End Module

Public Class NewsReceiver
   Public Sub New()
      NewsBroadcaster.Register(AddressOf Me.DisplayNews)
   End Sub

   Public Sub DisplayNews(newsItem As String)
      Console.WriteLine(newsItem)
   End Sub
End Class
```

Si aucun élément dans le `SendNews` liste d’appel, le `SendNews` délégué lève un <xref:System.NullReferenceException>. Avant les opérateurs conditionnels null, de code comme celui-ci assuré que la liste d’appel de délégué n’était pas `Nothing`:

```vb  
SendNews = SendNews.Combine({SendNews, client})  
If SendNews IsNot Nothing Then 
   SendNews("Just in...")
End If
```

La nouvelle méthode est beaucoup plus simple :  

```vb
SendNews = SendNews.Combine({SendNews, client})  
SendNews?.Invoke("Just in...")
```

La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `SendNews` une seule fois, en conservant le résultat dans une variable temporaire. Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `SendNews?(String)`.  

## <a name="see-also"></a>Voir aussi

- [Opérateurs (Visual Basic)](index.md)
- [Guide de programmation Visual Basic](../../../visual-basic/programming-guide/index.md)
- [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md)
