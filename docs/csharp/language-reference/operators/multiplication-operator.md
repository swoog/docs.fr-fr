---
title: '* , opérateur (Informations de référence sur C#)'
ms.date: 04/04/2018
f1_keywords:
- '*_CSharpKeyword'
helpviewer_keywords:
- multiplication operator (*) [C#]
- '* operator [C#]'
ms.assetid: abd9a5f0-9b24-431e-971a-09ee1c45c50e
ms.openlocfilehash: 873cc1dc0d81425117f1784353acf08b35158133
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45596973"
---
# <a name="-operator-c-reference"></a>*, opérateur (référence C#)
L’opérateur de multiplication (`*`) calcule le produit de ses opérandes. Tous les types numériques ont des opérateurs de multiplication prédéfinis.  

Par ailleurs, `*` sert d’opérateur de déréférencement qui permet de lire un pointeur et d’écrire sur celui-ci.
  
## <a name="remarks"></a>Notes  
 L’opérateur `*` est aussi utilisé pour déclarer des types pointeur et déréférencer des pointeurs. Cet opérateur ne peut être utilisé que dans des contextes unsafe signalés par l’utilisation du mot clé [unsafe](../../../csharp/language-reference/keywords/unsafe.md). Il nécessite l’option de compilateur [/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md).  L’opérateur de déréférencement est également appelé opérateur d’indirection.  
  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `*` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp-interactive[csRefOperators#50](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_1.cs)]  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#51](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-operator_2.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
