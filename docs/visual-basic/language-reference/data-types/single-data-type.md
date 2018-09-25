---
title: Single, type de données (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Single
helpviewer_keywords:
- Single data type
- F literal type character [Visual Basic]
- trailing zeros
- real numbers
- literal type characters [Visual Basic], F
- trailing 0 characters [Visual Basic]
- identifier type characters [Visual Basic], !
- single-precision numbers
- '! identifier type character'
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- floating-point numbers [Visual Basic], Single data type
- numbers [Visual Basic], real
- zeros, trailing
- numbers [Visual Basic], floating point
ms.assetid: 224a2795-4cd5-496c-8f7a-a4f05a06d45d
ms.openlocfilehash: 98433c0f1d1008664bb994f3b43fe48a753a432c
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47086734"
---
# <a name="single-data-type-visual-basic"></a>Single, type de données (Visual Basic)
Contient des nombres à virgule flottante IEEE 32 bits (4 octets) simple précision compris entre - 3,4028235E + 38 signés et - 1, 401298E-45 pour les valeurs négatives et entre 1, 401298E-45 et 3,4028235E + 38 pour les valeurs positives. Nombres en simple précision stockent une approximation d’un nombre réel.  
  
## <a name="remarks"></a>Notes  
 Utilisez le `Single` type de données pour contenir des valeurs à virgule flottante qui ne nécessitent pas la largeur totale des données de `Double`. Dans certains cas, le common language runtime peut être en mesure de compresser vos `Single` variables étroitement ensemble et d’enregistrer la consommation de mémoire.  
  
 La valeur par défaut de `Single` est 0.  
  
## <a name="programming-tips"></a>Conseils de programmation  
  
-   **Précision.** Lorsque vous travaillez avec des nombres à virgule flottante, n’oubliez pas qu’ils n’ont pas toujours de représentation précise dans la mémoire. Cela peut entraîner des résultats inattendus à partir de certaines opérations, comme la comparaison de valeurs et les `Mod` opérateur. Pour plus d’informations, consultez [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).  
  
-   **Étendues.** Le `Single` type de données s’étend à `Double`. Cela signifie que vous pouvez convertir `Single` à `Double` sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.  
  
-   **Les zéros de fin.** Les types de données à virgule flottante n’ont pas d’aucune représentation interne du 0 de fin. Par exemple, ils n'effectuent pas de distinction entre 4,2000 et 4.2. Par conséquent, les caractères 0 de fin n’apparaissent pas lorsque vous affichez ou imprimez les valeurs à virgule flottante.  
  
-   **Caractères de type.** L'ajout du caractère de type littéral `F` à un littéral force ce dernier en type de données `Single`. L'ajout du caractère de type identificateur `!` à un identificateur force ce dernier en type `Single`.  
  
-   **Type de Framework.** Le type correspondant dans le .NET Framework est la structure <xref:System.Single?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Single?displayProperty=nameWithType>  
 [Types de données](../../../visual-basic/language-reference/data-types/index.md)  
 [Decimal (type de données)](../../../visual-basic/language-reference/data-types/decimal-data-type.md)  
 [Double (type de données)](../../../visual-basic/language-reference/data-types/double-data-type.md)  
 [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)  
 [Liste des conversions](../../../visual-basic/language-reference/keywords/conversion-summary.md)  
 [Utilisation efficace des types de données](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)  
 [Dépannage des types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
