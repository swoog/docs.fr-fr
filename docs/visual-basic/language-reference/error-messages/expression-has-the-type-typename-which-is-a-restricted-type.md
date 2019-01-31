---
title: L'expression a le type '<typename>', qui est un type restreint et qui ne peut pas être utilisé pour accéder aux membres hérités de 'Object' ou 'ValueType'
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: 6d366ec750ea5a4505ae5ea618e27f47406ba959
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55274014"
---
# <a name="expression-has-the-type-typename-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-object-or-valuetype"></a>Expression a le type '\<nom_type >' qui est un type restreint et ne peut pas être utilisé pour accéder aux membres hérités de 'Object' ou 'ValueType'
Une expression correspond à un type qui ne peut pas être converti (boxed) par le common language runtime (CLR) mais accède à un membre qui requiert un boxing.  
  
 Le*boxing* est le traitement nécessaire à la conversion d’un type en `Object` ou, à l’occasion, en <xref:System.ValueType>. Le common language runtime ne peut pas convertir certains types de structure, par exemple <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, et <xref:System.TypedReference>.  
  
 Cette expression tente d’utiliser le type restreint pour appeler une méthode héritée <xref:System.Object> ou <xref:System.ValueType>, tel que <xref:System.Object.GetHashCode%2A> ou <xref:System.Object.ToString%2A>. Pour accéder à cette méthode, Visual Basic a tenté une conversion boxing implicite qui provoque cette erreur.  
  
 **ID d’erreur :** BC31393  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Recherchez l’expression évaluée comme étant le type cité.  
  
2.  Recherchez la partie de votre instruction qui essaie d’appeler la méthode héritée <xref:System.Object> ou <xref:System.ValueType>.  
  
3.  Réécrivez l’instruction pour éviter l’appel de méthode.  
  
## <a name="see-also"></a>Voir aussi
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
