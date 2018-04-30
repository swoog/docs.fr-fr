---
title: '* , opérateur (Informations de référence sur C#)'
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
caps.latest.revision: 14
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 07d06d668ba43ebc3f4fae394d7b6641b122f4a6
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="-operator-c-reference"></a>*, opérateur (référence C#)
L’opérateur de multiplication (`*`) calcule le produit de ses opérandes. Tous les types numériques ont des opérateurs de multiplication prédéfinis.  

Par ailleurs, `*` sert d’opérateur de déréférencement qui permet de lire un pointeur et d’écrire sur celui-ci.
  
## <a name="remarks"></a>Notes  
 L’opérateur `*` est aussi utilisé pour déclarer des types pointeur et déréférencer des pointeurs. Cet opérateur ne peut être utilisé que dans des contextes unsafe signalés par l’utilisation du mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md). Il nécessite l’option de compilateur [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md).  L’opérateur de déréférencement est également appelé opérateur d’indirection.  
  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `*` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#50](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_1.cs)]  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#51](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_2.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
