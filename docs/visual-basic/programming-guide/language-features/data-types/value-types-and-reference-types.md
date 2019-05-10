---
title: Types valeur et types référence
ms.date: 07/20/2015
helpviewer_keywords:
- reference data types [Visual Basic]
- reference types [Visual Basic]
- value types [Visual Basic]
- value data types [Visual Basic]
- types [Visual Basic]
- data types [Visual Basic], value types
- data types [Visual Basic], reference types
ms.assetid: fc82ce15-5a40-4c5c-a1e1-a556830e7391
ms.openlocfilehash: f823d9e80eb644487eab1ed84345dd8bdc10efc2
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64600940"
---
# <a name="value-types-and-reference-types"></a>Types valeur et types référence
En Visual Basic, les types de données sont implémentés en fonction de leur classification. Les types de données Visual Basic peuvent être classées selon qu’une variable d’un type particulier stocke ses propres données ou un pointeur vers les données. Il stocke ses propres données de cas d’un *type valeur*; si elle contient un pointeur vers les données ailleurs dans la mémoire, il est un *type référence*.  
  
## <a name="value-types"></a>Types valeur  
 Un type de données est un *type valeur* s’il conserve des données au sein de sa propre allocation de mémoire. Les types valeur sont les suivantes :  
  
- Tous les types de données numériques  
  
- `Boolean`, `Char`et `Date`  
  
- Toutes les structures, même si leurs membres sont des types référence  
  
- Énumérations, dans la mesure où leur type sous-jacent est toujours `SByte`, `Short`, `Integer`, `Long`, `Byte`, `UShort`, `UInteger`, ou `ULong`  
  
 Chaque structure est un type valeur, même s’il contient des membres de type référence. Pour cette raison, types valeur tels que `Char` et `Integer` sont implémentés par les structures de .NET Framework.  
  
 Vous pouvez déclarer un type valeur à l’aide du mot clé réservé, par exemple, `Decimal`. Vous pouvez également utiliser le `New` mot clé pour initialiser un type valeur. Cela est particulièrement utile si le type a un constructeur qui accepte des paramètres. Un exemple de ceci est le <xref:System.Decimal.%23ctor%28System.Int32%2CSystem.Int32%2CSystem.Int32%2CSystem.Boolean%2CSystem.Byte%29> constructeur, ce qui génère un nouveau `Decimal` valeur à partir des parties fournis.  
  
## <a name="reference-types"></a>Types référence  
 Un *type référence* contient un pointeur vers un autre emplacement de mémoire qui contient les données. Types de référence sont les suivants :  
  
- `String`  
  
- Tous les tableaux, même si leurs éléments sont des types valeur  
  
- Types de classe, tels que <xref:System.Windows.Forms.Form>  
  
- Délégués  
  
 Une classe est un *type référence*. Pour cette raison, les types référence comme `Object` et `String` sont pris en charge par [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classes. Notez que chaque tableau est un type référence, même si ses membres sont des types valeur.  
  
 Étant donné que chaque type de référence représente une classe sous-jacente de .NET Framework, vous devez utiliser le [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé lorsque vous l’initialisez. L’instruction suivante initialise un tableau.  
  
```  
Dim totals() As Single = New Single(8) {}  
```  
  
## <a name="elements-that-are-not-types"></a>Éléments qui ne sont pas des Types  
 Les éléments de programmation suivants ne sont pas éligibles en tant que types, car vous ne pouvez pas spécifier une d'entre elles comme type de données pour un élément déclaré :  
  
- Espaces de noms  
  
- Modules  
  
- Événements  
  
- Propriétés et procédures  
  
- Variables, constantes et champs  
  
## <a name="working-with-the-object-data-type"></a>Utilisation du Type de données d’objet  
 Vous pouvez affecter un type référence ou un type valeur à une variable de la `Object` type de données. Un `Object` variable contienne toujours un pointeur vers les données, jamais les données elles-mêmes. Toutefois, si vous affectez un type valeur à une `Object` variable, il se comporte comme si elle contient ses propres données. Pour plus d’informations, consultez [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md).  
  
 Vous pouvez déterminer si un `Object` variable agit comme un type référence ou un type valeur en la passant à la <xref:Microsoft.VisualBasic.Information.IsReference%2A> méthode dans le <xref:Microsoft.VisualBasic.Information> classe de la <xref:Microsoft.VisualBasic?displayProperty=nameWithType> espace de noms. <xref:Microsoft.VisualBasic.Information.IsReference%2A?displayProperty=nameWithType> Retourne `True` si le contenu de la `Object` variable représente un type référence.  
  
## <a name="see-also"></a>Voir aussi

- [Types valeur Nullable](../../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [Utilisation efficace des types de données](../../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
- [Object (type de données)](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
