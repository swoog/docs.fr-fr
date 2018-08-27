---
title: -&gt;, opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: fb95e508ce1339868723bcc3178851e8c1355c1f
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42930302"
---
# <a name="-gt-operator-c-reference"></a>-&gt;, opérateur (Informations de référence sur C#)
L’opérateur `->` allie l’annulation de la référence d’un pointeur et l’accès au membre.  
  
## <a name="remarks"></a>Notes  
 Une expression de forme  
  
```csharp  
x->y  
```  
  
 (où `x` est un pointeur de type `T*` et `y` un membre de `T`) est équivalente à  
  
```csharp  
(*x).y  
```  
  
 L’opérateur `->` peut être utilisé uniquement dans du code marqué comme [unsafe](../../../csharp/language-reference/keywords/unsafe.md).  
  
 L’opérateur `->` ne peut pas être surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#15](../../../csharp/language-reference/operators/codesnippet/CSharp/dereference-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
