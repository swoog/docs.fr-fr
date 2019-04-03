---
title: 'Procédure : Convertir un objet en un autre Type dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- objects [Visual Basic], converting
ms.assetid: 60cb5fc7-7ba4-4ab5-9c24-480fa12ddcdc
ms.openlocfilehash: 1e515c0f4ce8e787754c61a9b53d247fa93c49f2
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58814378"
---
# <a name="how-to-convert-an-object-to-another-type-in-visual-basic"></a>Procédure : Convertir un objet en un autre Type dans Visual Basic
Vous convertissez un `Object` à un autre type de données à l’aide d’un mot clé de conversion telles que la variable [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant convertit un `Object` variable à un `Integer` et un `String`.  
  
```  
Public Sub objectConversion(ByVal anObject As Object)  
    Dim anInteger As Integer  
    Dim aString As String  
    anInteger = CType(anObject, Integer)  
    aString = CType(anObject, String)  
End Sub  
```  
  
 Si vous savez que le contenu d’un `Object` variable sont d’un type de données particulier, il est préférable de convertir la variable à ce type de données. Si vous continuez à utiliser le `Object` variable, vous encourez soit *boxing* et *unboxing* (pour un type valeur) ou *liaison tardive* (pour un type référence). Ces opérations tous prennent le temps d’exécution et ralentissent les performances.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une référence à l'espace de noms <xref:System?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Object>
- [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Conversion entre des chaînes et d’autres types](../../../../visual-basic/programming-guide/language-features/data-types/conversions-between-strings-and-other-types.md)
- [Conversions de tableau](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)
- [Structures](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Types de données](../../../../visual-basic/language-reference/data-types/index.md)
- [Fonctions de conversion de types](../../../../visual-basic/language-reference/functions/type-conversion-functions.md)
