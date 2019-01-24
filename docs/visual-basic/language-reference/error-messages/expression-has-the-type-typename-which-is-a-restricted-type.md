---
title: Expression a le type &#39; &lt;typename&gt; &#39; qui est un type restreint et ne peut pas être utilisé pour accéder aux membres hérités de &#39;objet&#39; ou &#39;ValueType&#39;
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: d44b9a29f0848508d8cd814e857d9b01819ce7ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535955"
---
# <a name="expression-has-the-type-39lttypenamegt39-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-39object39-or-39valuetype39"></a>Expression a le type &#39; &lt;typename&gt; &#39; qui est un type restreint et ne peut pas être utilisé pour accéder aux membres hérités de &#39;objet&#39; ou &#39;ValueType&#39;
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
