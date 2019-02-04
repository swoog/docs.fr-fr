---
title: Fonctions de conversion de types de données (Visual Basic)
ms.date: 10/24/2018
f1_keywords:
- vb.CUShort
- vb.csng
- vb.CDate
- CByte
- CSng
- vb.CDec
- CBool
- CStr
- vb.CULng
- CDec
- CVErr
- CDbl
- CShort
- vb.CObj
- vb.CVErr
- CULng
- vb.cdbl
- vb.cbool
- CObj
- CDate
- CLng
- vb.cstr
- vb.cbyte
- vb.clng
- vb.CChar
- CUShort
- vb.CUInt
- vb.cint
- vb.CShort
- CInt
- CUInt
- CChar
helpviewer_keywords:
- CDate function
- CByte function
- Integer data type [Visual Basic], converting
- string conversion [Visual Basic], conversion functions
- fractions
- data types [Visual Basic], converting
- text, converting
- CDec function
- Char data type [Visual Basic], converting
- type conversion [Visual Basic], functions for
- Single data type [Visual Basic], converting
- numbers [Visual Basic], rounding
- rounding numbers [Visual Basic], type conversion
- CUShort function
- Long data type [Visual Basic], converting
- return values [Visual Basic], data types
- single-precision numbers [Visual Basic], converting
- data type conversion [Visual Basic], functions for
- CStr function
- times [Visual Basic], converting
- CSng function
- conversions [Visual Basic], type conversion functions
- CBool function
- CDbl function
- CUInt function
- Currency data type [Visual Basic], conversion functions
- numbers [Visual Basic], converting
- Double data type [Visual Basic], converting
- CLng function
- CSByte function
- double-precision numbers
- Decimal data type [Visual Basic], converting
- Boolean data type [Visual Basic], converting
- integers [Visual Basic], type conversion functions
- dates [Visual Basic], converting
- CULng function
- CInt function
- Date data type [Visual Basic], converting
- Byte data type [Visual Basic], converting
- String data type [Visual Basic], converting
- CChar function
- banker's rounding
- Short data type [Visual Basic], converting
- rounding numbers [Visual Basic], banker's rounding
- type conversion [Visual Basic], Visual Basic vs. .NET Framework
ms.assetid: d9d8d165-f967-44ff-a6cd-598e4740a99e
ms.openlocfilehash: be5e1b5fff1feb8ef4cc2ff7fcbca193aafcd781
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2019
ms.locfileid: "55674878"
---
# <a name="type-conversion-functions-visual-basic"></a>Fonctions de conversion de types de données (Visual Basic)
Ces fonctions sont compilé "inline", ce qui signifie que le code de conversion fait partie du code qui évalue l’expression. Parfois, il n’existe aucun appel à une procédure pour effectuer la conversion, ce qui améliore les performances. Chaque fonction convertit une expression en un type de données spécifique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
CBool(expression)  
CByte(expression)  
CChar(expression)  
CDate(expression)  
CDbl(expression)  
CDec(expression)  
CInt(expression)  
CLng(expression)  
CObj(expression)  
CSByte(expression)  
CShort(expression)  
CSng(expression)  
CStr(expression)  
CUInt(expression)  
CULng(expression)  
CUShort(expression)  
```  
  
## <a name="part"></a>Élément  
 `expression`  
 Obligatoire. Toute expression de type de données source.  
  
## <a name="return-value-data-type"></a>Type de données valeur de retour  
 Le nom de la fonction détermine le type de données de la valeur de que retour, comme indiqué dans le tableau suivant.  
  
|Nom de la fonction|Type de données de retour|Plage pour `expression` argument|  
|-------------------|----------------------|-------------------------------------|  
|`CBool`|[Booléen (type de données)](../../../visual-basic/language-reference/data-types/boolean-data-type.md)|Valide `Char` ou `String` ou expression numérique.|  
|`CByte`|[Byte (type de données)](../../../visual-basic/language-reference/data-types/byte-data-type.md)|<xref:System.Byte.MinValue?displayProperty=nameWithType> (0) par le biais <xref:System.Byte.MaxValue?displayProperty=nameWithType> (255) (non signé) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances de la virgule flottante pour la conversion d’octets avec la `CByte` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CChar`|[Char (type de données)](../../../visual-basic/language-reference/data-types/char-data-type.md)|Valide `Char` ou `String` expression ; seul premier caractère d’un `String` est convertie ; valeur peut être 0 et 65 535 (non signé).|  
|`CDate`|[Date (type de données)](../../../visual-basic/language-reference/data-types/date-data-type.md)|Une représentation valide d’une date et une heure.|  
|`CDbl`|[Double (type de données)](../../../visual-basic/language-reference/data-types/double-data-type.md)|-1, 79769313486231570E + 308 à - 4, 94065645841246544E-324 pour les valeurs négatives ; 4, 94065645841246544E-324 à 1, 79769313486231570E + 308 pour les valeurs positives.|  
|`CDec`|[Decimal (type de données)](../../../visual-basic/language-reference/data-types/decimal-data-type.md)|+/-79,228,162,514,264,337,593,543,950,335 pour les nombres à échelle zéro, autrement dit, les nombres sans décimales. Pour les nombres à 28 décimales, la plage est +/-7,9228162514264337593543950335. Le plus petit nombre possible de zéro est 0,0000000000000000000000000001 (+/-1E-28).|  
|`CInt`|[Integer (type de données)](../../../visual-basic/language-reference/data-types/integer-data-type.md)|<xref:System.Int32.MinValue?displayProperty=nameWithType> (allant de -2,147,483,648) via <xref:System.Int32.MaxValue?displayProperty=nameWithType> (2 147 483 647) ; parties fractionnaires sont arrondies.<sup> 1</sup> <br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances de la virgule flottante pour la conversion d’un entier avec la `CInt` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple. |  
|`CLng`|[Long (type de données)](../../../visual-basic/language-reference/data-types/long-data-type.md)|<xref:System.Int64.MinValue?displayProperty=nameWithType> (-9,223,372,036,854,775,808) via <xref:System.Int64.MaxValue?displayProperty=nameWithType> (9,223,372,036,854,775,807) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances de la virgule flottante pour la conversion d’entier 64 bits avec le `CLng` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CObj`|[Object (type de données)](../../../visual-basic/language-reference/data-types/object-data-type.md)|Toute expression valide.|  
|`CSByte`|[SByte (type de données)](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)|<xref:System.SByte.MinValue?displayProperty=nameWithType> -(128) via <xref:System.SByte.MaxValue?displayProperty=nameWithType> (127) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À compter de 15.8 de Visual Basic, Visual Basic optimise les performances des valeurs à virgule flottante conversion octet signé avec la `CSByte` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CShort`|[Short (type de données)](../../../visual-basic/language-reference/data-types/short-data-type.md)|<xref:System.Int16.MinValue?displayProperty=nameWithType> (-32 768) via <xref:System.Int16.MaxValue?displayProperty=nameWithType> (32 767) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances des valeurs à virgule flottante conversion entier 16 bits avec le `CShort` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CSng`|[Single (type de données)](../../../visual-basic/language-reference/data-types/single-data-type.md)|-3, 402823E + 38 à - 1, 401298E-45 pour les valeurs négatives ; 1, 401298E-45 et 3, 402823E + 38 pour les valeurs positives.|  
|`CStr`|[String (type de données)](../../../visual-basic/language-reference/data-types/string-data-type.md)|Retourne pour `CStr` varient selon le `expression` argument. Consultez [retournent des valeurs pour la fonction CStr](../../../visual-basic/language-reference/functions/return-values-for-the-cstr-function.md).|  
|`CUInt`|[UInteger (type de données)](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)|<xref:System.UInt32.MinValue?displayProperty=nameWithType> (0) par le biais <xref:System.UInt32.MaxValue?displayProperty=nameWithType> (4 294 967 295) (non signé) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances de la virgule flottante pour la conversion d’un entier non signé avec la `CUInt` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CULng`|[ULong (type de données)](../../../visual-basic/language-reference/data-types/ulong-data-type.md)|<xref:System.UInt64.MinValue?displayProperty=nameWithType> (0) par le biais <xref:System.UInt64.MaxValue?displayProperty=nameWithType> (18,446,744,073,709,551,615) (non signé) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À partir de Visual Basic 15.8, Visual Basic optimise les performances de la virgule flottante pour la conversion d’entier long non signé avec la `CULng` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
|`CUShort`|[UShort (type de données)](../../../visual-basic/language-reference/data-types/ushort-data-type.md)|<xref:System.UInt16.MinValue?displayProperty=nameWithType> (0) par le biais <xref:System.UInt16.MaxValue?displayProperty=nameWithType> (65 535) (non signé) ; parties fractionnaires sont arrondies.<sup> 1</sup><br/><br/>À compter de 15.8 de Visual Basic, Visual Basic optimise les performances des valeurs à virgule flottante conversion entier 16 bits non signé avec la `CUShort` fonction ; consultez la [notes](#remarks) section pour plus d’informations. Consultez le [CInt exemple](#cint-example) section pour obtenir un exemple.|  
  
 <sup>1</sup> fractionnaire peut être soumis à un type spécial de l’arrondi appelée *l’arrondi bancaire*. Pour plus d’informations, consultez « Remarques ».  
  
## <a name="remarks"></a>Notes  
 En règle générale, vous devez utiliser les fonctions de conversion de type Visual Basic plutôt que les méthodes .NET Framework, tel que `ToString()`, soit sur le <xref:System.Convert> classe ou sur une structure de type classe. Les fonctions Visual Basic sont conçues pour une interaction optimale avec code Visual Basic, et elles rendent également votre code source plus courte et plus facile à lire. En outre, les méthodes de conversion de .NET Framework ne produisent pas toujours les mêmes résultats que les fonctions Visual Basic, par exemple lors de la conversion `Boolean` à `Integer`. Pour plus d’informations, consultez [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).  


À partir de Visual Basic 15.8, les performances de la conversion de flottante-virgule en entier sont optimisée quand vous passez le <xref:System.Single> ou <xref:System.Double> valeur retournée par les méthodes suivantes à une des fonctions de conversion d’entier (`CByte`, `CShort`, `CInt`, `CLng`, `CSByte`, `CUShort`, `CUInt`, `CULng`):

- <xref:Microsoft.VisualBasic.Conversion.Fix(System.Double)?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Conversion.Fix(System.Object)?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Conversion.Fix(System.Single)?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Conversion.Int(System.Double)?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Conversion.Int(System.Object)?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Conversion.Int(System.Single)?displayProperty=nameWithType>
- <xref:System.Math.Ceiling(System.Double)?displayProperty=nameWithType>
- <xref:System.Math.Floor(System.Double)?displayProperty=nameWithType>
- <xref:System.Math.Round(System.Double)?displayProperty=nameWithType>
- <xref:System.Math.Truncate(System.Double)?displayProperty=nameWithType>

Cette optimisation permet au code qui effectue un grand nombre de conversions entier à s’exécuter jusqu'à deux fois plus vite. L’exemple suivant illustre ces conversions flottante virgule à entier optimisées :

```vb
Dim s As Single = 173.7619
Dim d As Double = s 

Dim i1 As Integer = CInt(Fix(s))               ' Result: 173
Dim b1 As Byte = CByte(Int(d))                 ' Result: 173
Dim s1 AS Short = CShort(Math.Truncate(s))     ' Result: 173
Dim i2 As Integer = CInt(Math.Ceiling(d))      ' Result: 174
Dim i3 As Integer = CInt(Math.Round(s))        ' Result: 174
```

## <a name="behavior"></a>Comportement  
  
-   **Coercion.** En règle générale, vous pouvez utiliser les fonctions de conversion de type de données à forcer le résultat d’une opération à un type de données particulier plutôt que le type de données par défaut. Par exemple, utilisez `CDec` à arithmétique décimale dans les cas où le simple précision, double précision ou arithmétique sur les entiers serait normalement avoir lieu.  
  
-   **Échecs de conversion.** Si le `expression` passé à la fonction est en dehors de la plage du type de données vers lequel il doit être converti, un <xref:System.OverflowException> se produit.  
  
-   **Parties fractionnaires.** Tapez lorsque vous convertissez une valeur non entière en un type intégral, les fonctions de conversion d’entier (`CByte`, `CInt`, `CLng`, `CSByte`, `CShort`, `CUInt`, `CULng`, et `CUShort`) supprimer le fractions de seconde partie et arrondir la valeur à l’entier le plus proche.  
  
     Si la partie fractionnaire est exactement égale à 0,5, les fonctions de conversion d’entier arrondissent à l’entier pair le plus proche de. Par exemple, 0,5 est arrondi à 0 et 1,5 et 2,5 que sont arrondis à 2. On parle parfois *l’arrondi bancaire*, et son objectif est de compenser un écart qui pourrait s’accumuler lors de l’ajout de plusieurs nombres ensemble.  
  
     `CInt` et `CLng` diffère la <xref:Microsoft.VisualBasic.Conversion.Int%2A> et <xref:Microsoft.VisualBasic.Conversion.Fix%2A> fonctions tronquent arrondissent, la partie fractionnaire d’un nombre. En outre, `Fix` et `Int` retournent toujours une valeur du même type de données que vous passez.  
  
-   **Conversions de date/heure.** Utilisez le <xref:Microsoft.VisualBasic.Information.IsDate%2A> fonction permettant de déterminer si une valeur peut être convertie en date et heure. `CDate` reconnaît les littéraux de date et heure mais pas de valeurs numériques. Pour convertir un Visual Basic 6.0 `Date` valeur un `Date` valeur en Visual Basic 2005 ou versions ultérieures, vous pouvez utiliser le <xref:System.DateTime.FromOADate%2A?displayProperty=nameWithType> (méthode).  
  
-   **Indépendant de valeurs de Date/heure.** Le [Type de données Date](../../../visual-basic/language-reference/data-types/date-data-type.md) contient toujours les informations de date / heure. À des fins de conversion de type, Visual Basic prend en compte la 1/1/0001 (le 1er janvier de l’année 1) pour être un *valeur neutre* pour la date et 00:00:00 (minuit) comme une valeur neutre pour l’heure. Si vous convertissez un `Date` valeur à une chaîne, `CStr` n’inclut pas de valeurs neutres dans la chaîne résultante. Par exemple, si vous convertissez `#January 1, 0001 9:30:00#` vers une chaîne, le résultat est « 9:30:00 AM » ; les informations de date sont supprimées. Toutefois, les informations de date sont toujours présentes dans la version d’origine `Date` valeur et peuvent être récupérées avec des fonctions telles que <xref:Microsoft.VisualBasic.DateAndTime.DatePart%2A> (fonction).  
  
-   **Respect de la culture.** Les fonctions de conversion de type impliquant des chaînes effectuent des conversions en fonction des paramètres de culture actuelle pour l’application. Par exemple, `CDate` reconnaît les formats de date selon les paramètres régionaux de votre système. Vous devez fournir le jour, le mois et l’année dans le bon ordre pour vos paramètres régionaux, ou la date ne peut pas être interprétée correctement. Un format de date longue n’est pas reconnu s’il contient une chaîne de day of week, tels que « Mercredi ».  
  
     Si vous souhaitez convertir vers ou depuis une représentation sous forme de chaîne d’une valeur dans un format différent de celui spécifié par vos paramètres régionaux, vous ne pouvez pas utiliser les fonctions de conversion de type Visual Basic. Pour ce faire, utilisez le `ToString(IFormatProvider)` et `Parse(String, IFormatProvider)` méthodes du type de cette valeur. Par exemple, utilisez <xref:System.Double.Parse%2A?displayProperty=nameWithType> lors de la conversion d’une chaîne à un `Double`et utiliser <xref:System.Double.ToString%2A?displayProperty=nameWithType> lors de la conversion d’une valeur de type `Double` vers une chaîne.  
  
## <a name="ctype-function"></a>CType Function  
 Le [CType Function](../../../visual-basic/language-reference/functions/ctype-function.md) accepte un deuxième argument, `typename`et force `expression` à `typename`, où `typename` peut être n’importe quel type de données, de structure, classe ou interface à laquelle il existe une conversion valide.  
  
 Pour obtenir une comparaison de `CType` avec les autres mots-clés de conversion de type, consultez [opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) et [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md).  
  
## <a name="cbool-example"></a>CBool, exemple  
 L’exemple suivant utilise le `CBool` fonction pour convertir les expressions à `Boolean` valeurs. Si une expression correspond à une valeur différente de zéro, `CBool` retourne `True`; sinon, elle retourne `False`.  
  
 [!code-vb[VbVbalrFunctions#1](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_1.vb)]  
  
## <a name="cbyte-example"></a>CByte, exemple  
 L’exemple suivant utilise le `CByte` fonction pour convertir une expression à un `Byte`.  
  
 [!code-vb[VbVbalrFunctions#2](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_2.vb)]  
  
## <a name="cchar-example"></a>CChar, exemple  
 L’exemple suivant utilise le `CChar` fonction pour convertir le premier caractère d’un `String` expression à un `Char` type.  
  
 [!code-vb[VbVbalrFunctions#3](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_3.vb)]  
  
 L’argument d’entrée `CChar` doit être de type de données `Char` ou `String`. Vous ne pouvez pas utiliser `CChar` pour convertir un nombre en un caractère, car `CChar` ne peut pas accepter un type de données numérique. L’exemple suivant obtient un nombre représentant un point de code (code de caractère) et le convertit en caractère correspondant. Il utilise le <xref:Microsoft.VisualBasic.Interaction.InputBox%2A> fonction pour obtenir la chaîne de chiffres, `CInt` pour convertir la chaîne en type `Integer`, et `ChrW` pour convertir le nombre en type `Char`.  
  
 [!code-vb[VbVbalrFunctions#4](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_4.vb)]  
  
## <a name="cdate-example"></a>CDate, exemple  
 L’exemple suivant utilise le `CDate` fonction pour convertir des chaînes à `Date` valeurs. En règle générale, coder en dur les dates et heures sous forme de chaînes (comme indiqué dans cet exemple) est déconseillé. Utiliser des littéraux de date et heure, telles que #Feb 12, 1969 # et # 4:45:23 PM #, à la place.  
  
 [!code-vb[VbVbalrFunctions#5](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_5.vb)]  
  
## <a name="cdbl-example"></a>CDbl, exemple  
 [!code-vb[VbVbalrFunctions#6](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_6.vb)]  
  
## <a name="cdec-example"></a>CDec, exemple  
 L’exemple suivant utilise le `CDec` fonction pour convertir une valeur numérique à `Decimal`.  
  
 [!code-vb[VbVbalrFunctions#7](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_7.vb)]  
  
## <a name="cint-example"></a>Exemple de CInt  
 L’exemple suivant utilise le `CInt` fonction pour convertir une valeur à `Integer`.  
  
 [!code-vb[VbVbalrFunctions#8](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_8.vb)]  

## <a name="clng-example"></a>CLng, exemple
 L’exemple suivant utilise le `CLng` fonction pour convertir des valeurs à `Long`.  
  
 [!code-vb[VbVbalrFunctions#9](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_9.vb)]  
  
## <a name="cobj-example"></a>CObj, exemple  
 L’exemple suivant utilise le `CObj` fonction pour convertir une valeur numérique à `Object`. Le `Object` variable contient uniquement un pointeur de quatre octets, qui pointe vers le `Double` valeur qui lui est assignée.  
  
 [!code-vb[VbVbalrFunctions#10](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_10.vb)]  
  
## <a name="csbyte-example"></a>Exemple CSByte  
 L’exemple suivant utilise le `CSByte` fonction pour convertir une valeur numérique à `SByte`.  
  
 [!code-vb[VbVbalrFunctions#11](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_11.vb)]  
  
## <a name="cshort-example"></a>CShort, exemple  
 L’exemple suivant utilise le `CShort` fonction pour convertir une valeur numérique à `Short`.  
  
 [!code-vb[VbVbalrFunctions#12](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_12.vb)]  
  
## <a name="csng-example"></a>CSng, exemple  
 L’exemple suivant utilise le `CSng` fonction pour convertir des valeurs à `Single`.  
  
 [!code-vb[VbVbalrFunctions#13](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_13.vb)]  
  
## <a name="cstr-example"></a>Exemple de la fonction CStr  
 L’exemple suivant utilise le `CStr` fonction pour convertir une valeur numérique à `String`.  
  
 [!code-vb[VbVbalrFunctions#14](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_14.vb)]  
  
 L’exemple suivant utilise le `CStr` fonction pour convertir `Date` valeurs `String` valeurs.  
  
 [!code-vb[VbVbalrFunctions#15](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_15.vb)]  
  
 `CStr` affiche toujours une `Date` valeur dans le format de date courte pour les paramètres régionaux, par exemple, « 6/15/2003 4:35:47 PM ». Toutefois, `CStr` supprime le *valeurs neutres* de 1/1/0001 pour la date et 00:00:00 pour l’heure.  
  
 Pour plus d’informations sur les valeurs retournées par `CStr`, consultez [les valeurs de retour pour la fonction CStr](../../../visual-basic/language-reference/functions/return-values-for-the-cstr-function.md).  
  
## <a name="cuint-example"></a>Exemple CUInt  
 L’exemple suivant utilise le `CUInt` fonction pour convertir une valeur numérique à `UInteger`.  
  
 [!code-vb[VbVbalrFunctions#16](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_16.vb)]  
  
## <a name="culng-example"></a>CULng, exemple  
 L’exemple suivant utilise le `CULng` fonction pour convertir une valeur numérique à `ULong`.  
  
 [!code-vb[VbVbalrFunctions#17](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_17.vb)]  
  
## <a name="cushort-example"></a>CUShort, exemple  
 L’exemple suivant utilise le `CUShort` fonction pour convertir une valeur numérique à `UShort`.  
  
 [!code-vb[VbVbalrFunctions#18](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/type-conversion-functions_18.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Strings.Asc%2A>
- <xref:Microsoft.VisualBasic.Strings.AscW%2A>
- <xref:Microsoft.VisualBasic.Strings.Chr%2A>
- <xref:Microsoft.VisualBasic.Strings.ChrW%2A>
- <xref:Microsoft.VisualBasic.Conversion.Int%2A>
- <xref:Microsoft.VisualBasic.Conversion.Fix%2A>
- <xref:Microsoft.VisualBasic.Strings.Format%2A>
- <xref:Microsoft.VisualBasic.Conversion.Hex%2A>
- <xref:Microsoft.VisualBasic.Conversion.Oct%2A>
- <xref:Microsoft.VisualBasic.Conversion.Str%2A>
- <xref:Microsoft.VisualBasic.Conversion.Val%2A>
- [Fonctions de conversion](../../../visual-basic/language-reference/functions/conversion-functions.md)
- [Conversions de type en Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
