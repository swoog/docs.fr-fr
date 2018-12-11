---
title: Conception des propriétés
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines, properties
- properties [.NET Framework], design guidelines
ms.assetid: 127cbc0c-cbed-48fd-9c89-7c5d4f98f163
author: KrzysztofCwalina
ms.openlocfilehash: 1d119b48f0524b3e997aa2cb9ea2cbbd855afdf0
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131454"
---
# <a name="property-design"></a>Conception des propriétés
Bien que les propriétés sont techniquement très similaires aux méthodes, elles sont très différentes en termes de scénarios de leur utilisation. Ils doivent être considérés comme des champs intelligents. Elles disposent de la syntaxe d’appel de champs et la flexibilité des méthodes.  
  
 **✓ DO** créer des propriétés get-only si l’appelant ne doit pas être en mesure de modifier la valeur de la propriété.  
  
 N’oubliez pas qu’en cas le type de la propriété est un type référence mutable, la valeur de propriété peut être modifiée même si la propriété est get-only.  
  
 **X DO NOT** fournissent des propriétés ou propriétés à définir uniquement avec la méthode setter ayant le plus large d’accessibilité de l’accesseur Get.  
  
 Par exemple, n’utilisez pas de propriétés avec un accesseur Set public et un accesseur Get protégé.  
  
 Si l’accesseur Get de propriété ne peut pas être fourni, implémenter les fonctionnalités en tant que méthode à la place. Pensez à démarrer avec le nom de la méthode `Set` et suivez avec ce que vous aurait nommé la propriété. Par exemple, <xref:System.AppDomain> possède une méthode appelée `SetCachePath` au lieu d’avoir une propriété de jeu uniquement appelée `CachePath`.  
  
 **✓ DO** fournissent des valeurs par défaut raisonnables pour toutes les propriétés, garantissant que les valeurs par défaut n’entraînent pas une faille de sécurité ou du code très inefficace.  
  
 **✓ DO** permettent d’être définie dans n’importe quel ordre, même si cela aboutit à un état temporaire non valide de l’objet.  
  
 Il est courant que les deux ou plusieurs propriétés être reliés entre eux à un point où certaines valeurs d’une propriété ne soient pas valides selon les valeurs d’autres propriétés sur le même objet. Dans ce cas, les exceptions résultant de l’état non valide doivent être différées jusqu'à ce que les propriétés liées entre elles sont effectivement utilisées conjointement par l’objet.  
  
 **✓ DO** conserver la valeur précédente si un accesseur Set de propriété lève une exception.  
  
 **X AVOID** lever des exceptions à partir des accesseurs Get de propriété.  
  
 Accesseurs Get de propriété doit-elle être des opérations simples et ne doivent pas toutes les conditions préalables. Si une méthode getter peut lever une exception, il doit probablement être retravaillée pour être une méthode. Notez que cette règle ne s’applique pas aux indexeurs, où les exceptions à la suite de valider les arguments devrait.  
  
### <a name="indexed-property-design"></a>Conception de la propriété indexée  
 Une propriété indexée est une propriété spéciale qui peut avoir des paramètres et peut être appelée avec une syntaxe spéciale semblable à l’indexation de tableau.  
  
 Propriétés indexées sont communément appelé indexeurs. Indexeurs doivent être utilisées uniquement dans les API qui permettent d’accéder aux éléments dans une collection logique. Par exemple, une chaîne est une collection de caractères et de l’indexeur sur <xref:System.String?displayProperty=nameWithType> a été ajouté à accéder à ses caractères.  
  
 **✓ CONSIDER** des indexeurs pour fournir l’accès aux données stockées dans un tableau interne.  
  
 **✓ CONSIDER** fournir des indexeurs sur les types de collections d’éléments.  
  
 **X AVOID** à l’aide des propriétés avec plusieurs paramètres indexées.  
  
 Si la conception nécessite plusieurs paramètres, reconsidérez si la propriété représente réellement un accesseur à une collection logique. Si elle n’est pas le cas, utilisez à la place des méthodes. Pensez à démarrer avec le nom de la méthode `Get` ou `Set`.  
  
 **X AVOID** indexeurs avec les types de paramètres autres que <xref:System.Int32?displayProperty=nameWithType>, <xref:System.Int64?displayProperty=nameWithType>, <xref:System.String?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType>, ou d’un enum.  
  
 Si la conception nécessite d’autres types de paramètres, réévaluez fortement si l’API représente réellement un accesseur à une collection logique. Si elle n’est pas le cas, utilisez une méthode. Pensez à démarrer avec le nom de la méthode `Get` ou `Set`.  
  
 **✓ DO** utiliser le nom `Item` pour des propriétés indexées, sauf s’il existe un meilleur nom (par exemple, consultez la <xref:System.String.Chars%2A> propriété sur `System.String`).  
  
 En c#, les indexeurs sont par défaut nommée Item. Le <xref:System.Runtime.CompilerServices.IndexerNameAttribute> peut être utilisé pour personnaliser ce nom.  
  
 **X DO NOT** fournissent à la fois un indexeur et des méthodes qui sont sémantiquement équivalents.  
  
 **X DO NOT** fournissent plusieurs familles d’indexeurs surchargés dans un type.  
  
 Elle est appliquée par le compilateur c#.  
  
 **X DO NOT** différent de l’utilisation des propriétés indexées.  
  
 Elle est appliquée par le compilateur c#.  
  
### <a name="property-change-notification-events"></a>Événements de Notification de modification de propriété  
 Il est parfois utile de fournir un événement informe l’utilisateur des modifications dans une valeur de propriété. Par exemple, `System.Windows.Forms.Control` déclenche un `TextChanged` événement après la valeur de son `Text` propriété a été modifiée.  
  
 **✓ CONSIDER** modifier les déclenchement d’événements de notification lorsque les valeurs de propriété dans les API de niveau supérieur (composants de concepteur généralement) sont modifiés.  
  
 S’il existe un scénario bonne pour un utilisateur de savoir quand une propriété d’un objet change, l’objet doit déclencher un événement de notification de modification de la propriété.  
  
 Toutefois, il est peu de chances d’être intéressant de la surcharge pour déclencher des événements pour l’API de bas niveau tels que les types de base ou des regroupements. Par exemple, <xref:System.Collections.Generic.List%601> ne déclenchera pas ces événements quand un nouvel élément est ajouté à la liste et le `Count` les modifications de propriété.  
  
 **✓ CONSIDER** déclenchement modifier les événements de notification lorsque la valeur d’une propriété modifiée via la force externe.  
  
 Si une valeur de propriété change via une force externe (de façon différente en appelant des méthodes sur l’objet), déclencher des événements indiquent au développeur que la valeur change et qu’il a changé. Un bon exemple est le `Text` propriété d’un contrôle de zone de texte. Lorsque l’utilisateur tape du texte dans un `TextBox`, la valeur de propriété change automatiquement.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
