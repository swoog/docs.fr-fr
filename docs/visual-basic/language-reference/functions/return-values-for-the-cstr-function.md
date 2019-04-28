---
title: Valeurs de retour pour la fonction CStr (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- times [Visual Basic], CStr Function return values
- type conversion [Visual Basic]
- dates [Visual Basic], CStr Function return values
- CStr function
- strings [Visual Basic], return value
- Date data type [Visual Basic], converting
- dates [Visual Basic]
- String data type [Visual Basic], converting
ms.assetid: 3aa744e7-1419-45d5-85e3-e5abc2953673
ms.openlocfilehash: 3653194c7e48533e664ac7513ca7f4f48d1c69f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61801528"
---
# <a name="return-values-for-the-cstr-function-visual-basic"></a>Valeurs de retour pour la fonction CStr (Visual Basic)
Le tableau suivant décrit les valeurs de retour pour `CStr` pour différents types de données de `expression`.  
  
|Si `expression` est de type|Retours `CStr`|  
|-----------------------------|--------------------|  
|[Booléen (type de données)](../../../visual-basic/language-reference/data-types/boolean-data-type.md)|Chaîne contenant « True » ou « False ».|  
|[Date (type de données)](../../../visual-basic/language-reference/data-types/date-data-type.md)|Une chaîne contenant un `Date` valeur (date et heure) dans le format de date courte de votre système.|  
|[Types de données numériques](../../../visual-basic/programming-guide/language-features/data-types/numeric-data-types.md)|Chaîne représentant le nombre.|  
  
## <a name="cstr-and-date"></a>Date et la fonction CStr  
 Le `Date` type contient toujours les informations de date / heure. À des fins de conversion de type, Visual Basic prend en compte la 1/1/0001 (le 1er janvier de l’année 1) pour être un *valeur neutre* pour la date et 00:00:00 (minuit) comme une valeur neutre pour l’heure. `CStr` n’inclut pas de valeurs neutres dans la chaîne résultante. Par exemple, si vous convertissez `#January 1, 0001 9:30:00#` vers une chaîne, le résultat est « 9:30:00 AM » ; les informations de date sont supprimées. Toutefois, les informations de date sont toujours présentes dans la version d’origine `Date` valeur et peuvent être récupérées avec des fonctions telles que <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A>.  
  
> [!NOTE]
>  Le `CStr` fonction effectue sa conversion en fonction des paramètres de culture actuels de l’application. Pour obtenir la représentation sous forme de chaîne d’un nombre dans une culture particulière, utilisez le nombre `ToString(IFormatProvider)` (méthode). Par exemple, utilisez <xref:System.Double.ToString%2A?displayProperty=nameWithType> lors de la conversion d’une valeur de type `Double` à un `String`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A>
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Booléen (type de données)](../../../visual-basic/language-reference/data-types/boolean-data-type.md)
- [Date (type de données)](../../../visual-basic/language-reference/data-types/date-data-type.md)
