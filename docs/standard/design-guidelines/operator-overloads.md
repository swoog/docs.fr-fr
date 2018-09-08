---
title: Surcharges d'opérateurs
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- operators [.NET Framework], overloads
- names [.NET Framework], overloaded operators
- member design guidelines, operators
- overloaded operators
ms.assetid: 37585bf2-4c27-4dee-849a-af70e3338cc1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ca42d25a5f3456c6a10eff76d7015656322abae
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44131245"
---
# <a name="operator-overloads"></a>Surcharges d'opérateurs
Surcharges d’opérateur autorisent les types de framework apparaisse comme si elles étaient des primitives de langage intégrées.  
  
 Bien qu’autorisées et utile dans certaines situations, les surcharges d’opérateur doivent être utilisés avec précaution. Il existe de nombreux cas dans l’opérateur qui surcharge ont été abusée, telles que lorsque les concepteurs de framework comment à utiliser des opérateurs pour les opérations qui doivent être des méthodes simples. Les instructions suivantes vous permettent de choisir quand et comment utiliser la surcharge d’opérateur.  
  
 **X AVOID** définissant les surcharges d’opérateur, sauf dans les types qui vous devraient vous sentir comme des types primitifs (intégrés).  
  
 **✓ CONSIDER** définissant les surcharges d’opérateur dans un type que vous devriez vous sentir comme un type primitif.  
  
 Par exemple, <xref:System.String?displayProperty=nameWithType> a `operator==` et `operator!=` défini.  
  
 **✓ DO** définir de surcharges d’opérateur dans les structures représentant des nombres (tel que <xref:System.Decimal?displayProperty=nameWithType>).  
  
 **X DO NOT** être jolies lors de la définition de surcharges d’opérateur.  
  
 Surcharge d’opérateur est utile dans les cas dans lesquels il est immédiatement évident quel sera le résultat de l’opération. Par exemple, il est judicieux de pouvoir soustraire une <xref:System.DateTime> à partir d’un autre `DateTime` et obtenir un <xref:System.TimeSpan>. Toutefois, il n’est pas appropriée à utiliser l’opérateur d’union logique pour des requêtes union de deux bases de données ou à utiliser l’opérateur de décalage pour écrire dans un flux.  
  
 **X DO NOT** fournissent des surcharges, sauf si au moins un des opérandes est du type définissant la surcharge d’opérateur.  
  
 **✓ DO** surchargez les opérateurs de manière symétrique.  
  
 Par exemple, si vous surchargez la `operator==`, vous devez également surcharger le `operator!=`. De même, si vous surchargez la `operator<`, vous devez également surcharger le `operator>`, et ainsi de suite.  
  
 **✓ CONSIDER** fournissant des méthodes avec des noms conviviaux qui correspondent à chaque opérateur surchargé.  
  
 De nombreux langages ne gèrent pas la surcharge d’opérateur. Pour cette raison, il est recommandé que les types qui surchargent des opérateurs incluent une méthode secondaire avec un nom spécifique à un domaine approprié qui fournit des fonctionnalités équivalentes.  
  
 Le tableau suivant contient une liste d’opérateurs et les noms de méthode convivial correspondants.  
  
|Symbole d’opérateur c#|Nom des métadonnées|Nom convivial|  
|-------------------------|-------------------|-------------------|  
|`N/A`|`op_Implicit`|`To<TypeName>/From<TypeName>`|  
|`N/A`|`op_Explicit`|`To<TypeName>/From<TypeName>`|  
|`+ (binary)`|`op_Addition`|`Add`|  
|`- (binary)`|`op_Subtraction`|`Subtract`|  
|`* (binary)`|`op_Multiply`|`Multiply`|  
|`/`|`op_Division`|`Divide`|  
|`%`|`op_Modulus`|`Mod or Remainder`|  
|`^`|`op_ExclusiveOr`|`Xor`|  
|`& (binary)`|`op_BitwiseAnd`|`BitwiseAnd`|  
|<code>&#124;</code>|`op_BitwiseOr`|`BitwiseOr`|  
|`&&`|`op_LogicalAnd`|`And`|  
|<code>&#124;&#124;</code>|`op_LogicalOr`|`Or`|  
|`=`|`op_Assign`|`Assign`|  
|`<<`|`op_LeftShift`|`LeftShift`|  
|`>>`|`op_RightShift`|`RightShift`|  
|`N/A`|`op_SignedRightShift`|`SignedRightShift`|  
|`N/A`|`op_UnsignedRightShift`|`UnsignedRightShift`|  
|`==`|`op_Equality`|`Equals`|  
|`!=`|`op_Inequality`|`Equals`|  
|`>`|`op_GreaterThan`|`CompareTo`|  
|`<`|`op_LessThan`|`CompareTo`|  
|`>=`|`op_GreaterThanOrEqual`|`CompareTo`|  
|`<=`|`op_LessThanOrEqual`|`CompareTo`|  
|`*=`|`op_MultiplicationAssignment`|`Multiply`|  
|`-=`|`op_SubtractionAssignment`|`Subtract`|  
|`^=`|`op_ExclusiveOrAssignment`|`Xor`|  
|`<<=`|`op_LeftShiftAssignment`|`LeftShift`|  
|`%=`|`op_ModulusAssignment`|`Mod`|  
|`+=`|`op_AdditionAssignment`|`Add`|  
|`&=`|`op_BitwiseAndAssignment`|`BitwiseAnd`|  
|<code>&#124;=</code>|`op_BitwiseOrAssignment`|`BitwiseOr`|  
|`,`|`op_Comma`|`Comma`|  
|`/=`|`op_DivisionAssignment`|`Divide`|  
|`--`|`op_Decrement`|`Decrement`|  
|`++`|`op_Increment`|`Increment`|  
|`- (unary)`|`op_UnaryNegation`|`Negate`|  
|`+ (unary)`|`op_UnaryPlus`|`Plus`|  
|`~`|`op_OnesComplement`|`OnesComplement`|  
  
### <a name="overloading-operator-"></a>Surcharge d’opérateur ==  
 La surcharge `operator ==` est beaucoup plus compliqué. La sémantique de l’opérateur doivent être compatibles avec plusieurs autres membres, tels que <xref:System.Object.Equals%2A?displayProperty=nameWithType>.  
  
### <a name="conversion-operators"></a>Conversion, opérateurs  
 Opérateurs de conversion sont les opérateurs unaires qui permettent la conversion d’un type vers un autre. Les opérateurs doivent être définis en tant que membres statiques sur l’opérande ou le type de retour. Il existe deux types d’opérateurs de conversion : implicites et explicites.  
  
 **X DO NOT** fournissent un opérateur de conversion si cette conversion n’est pas clairement attendue par les utilisateurs finaux.  
  
 **X DO NOT** définir des opérateurs de conversion en dehors du domaine d’un type.  
  
 Par exemple, <xref:System.Int32>, <xref:System.Double>, et <xref:System.Decimal> sont tous les types numériques, tandis que <xref:System.DateTime> n’est pas. Par conséquent, il ne doit y avoir aucun opérateur de conversion pour convertir un `Double(long)` à un `DateTime`. Un constructeur est recommandé dans ce cas.  
  
 **X DO NOT** fournissent un opérateur de conversion implicite si la conversion est potentiellement avec perte de données.  
  
 Par exemple, il ne doit pas y avoir une conversion implicite de `Double` à `Int32` car `Double` a une plage plus large que `Int32`. Un opérateur de conversion explicite peut être fourni même si la conversion est potentiellement avec perte de données.  
  
 **X DO NOT** lever des exceptions de casts implicites.  
  
 Il est très difficile pour les utilisateurs finaux à comprendre ce qui se passe, car ils ne peuvent pas être prenant en charge qu’une conversion a lieu.  
  
 **✓ DO** lever <xref:System.InvalidCastException?displayProperty=nameWithType> si un appel à un opérateur de cast entraîne une conversion avec perte de données et le contrat de l’opérateur n’autorise pas les conversions avec perte de données.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
