---
title: In (modificateur générique) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.VarianceIn
helpviewer_keywords:
- contravariance, In keyword [Visual Basic]
- In keyword [Visual Basic]
ms.assetid: 59bb13c5-fe96-42b8-8286-86293d1661c5
ms.openlocfilehash: d8d503f0814a89c977cdc208eced026b2d8cb1fd
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58838927"
---
# <a name="in-generic-modifier-visual-basic"></a>In (modificateur générique) (Visual Basic)
Pour les paramètres de type générique, le mot clé `In` spécifie que le paramètre de type est contravariant.  
  
## <a name="remarks"></a>Notes  
 La contravariance permet d’utiliser un type moins dérivé que celui spécifié par le paramètre générique. Cela permet la conversion implicite des classes qui implémentent des interfaces variantes, ainsi que la conversion implicite des types délégués.  
  
 Pour plus d’informations, consultez [Covariance et contravariance](../../programming-guide/concepts/covariance-contravariance/index.md).  
  
## <a name="rules"></a>Règles  
 Vous pouvez utiliser le mot clé `In` dans les interfaces et délégués génériques.  
  
 Un paramètre de type peut être déclaré comme étant contravariant dans une interface générique ou un délégué s’il est utilisé uniquement comme un type d’arguments de méthode et non utilisé comme type de retour de méthode. `ByRef` paramètres ne peuvent être covariants ou contravariant.  
  
 La covariance et la contravariance sont prises en charge pour les types référence et pas pris en charge pour les types valeur.  
  
 En Visual Basic, vous ne pouvez pas déclarer des événements dans des interfaces contravariantes sans spécifier le type de délégué. En outre, les interfaces de contravariant ne peut pas avoir de classes, des énumérations ou des structures imbriqués, mais ont des interfaces imbriquées.  
  
## <a name="behavior"></a>Comportement  
 Une interface qui possède un paramètre de type contravariant permet à ses méthodes d’accepter des arguments de types moins dérivés que ceux spécifiés par le paramètre de type d’interface. Par exemple, comme dans le .NET Framework 4, dans l’interface <xref:System.Collections.Generic.IComparer%601>, le type T est contravariant, vous pouvez assigner un objet du type `IComparer(Of Person)` à un objet du type `IComparer(Of Employee)` sans utiliser de méthode de conversion spéciale si `Person` hérite de `Employee`.  
  
 Un délégué contravariant peut être assigné à un autre délégué du même type, mais avec un paramètre de type générique moins dérivé.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment déclarer, étendre et implémenter une interface générique contravariante. Il montre également comment utiliser la conversion implicite pour les classes qui implémentent cette interface.  
  
 [!code-vb[vbVarianceKeywords#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#1)]  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment déclarer, instancier et invoquer un délégué générique contravariant. Il montre également comment convertir implicitement un type délégué.  
  
 [!code-vb[vbVarianceKeywords#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvariancekeywords/vb/module1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Variance dans les interfaces génériques](../../programming-guide/concepts/covariance-contravariance/variance-in-generic-interfaces.md)
- [Out](../../../visual-basic/language-reference/modifiers/out-generic-modifier.md)
