---
title: Instructions relatives aux collections
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 297b8f1d-b11f-4dc6-960a-8e990817304e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3571ebb2fdd2bcdfd8be1f0087d096e01f18790a
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45674089"
---
# <a name="guidelines-for-collections"></a>Instructions relatives aux collections
Une collection peut être considéré comme n’importe quel type spécifiquement conçu pour manipuler un groupe d’objets ayant des caractéristiques communes. C’est presque toujours approprié pour ces types d’implémenter <xref:System.Collections.IEnumerable> ou <xref:System.Collections.Generic.IEnumerable%601>, de sorte que dans cette section, nous considérons uniquement types implémentant une ou deux de ces interfaces doivent être des collections.  
  
 **X DO NOT** utiliser des collections faiblement typées dans les API publiques.  
  
 Le type de toutes les valeurs de retour et paramètres représentant les éléments de collecte doit être le type d’élément exacte, pas un de ses types de base (cela s’applique uniquement aux membres publics de la collection).  
  
 **X DO NOT** utiliser <xref:System.Collections.ArrayList> ou <xref:System.Collections.Generic.List%601> dans les API publiques.  
  
 Ces types sont des structures de données conçus pour être utilisé dans l’implémentation interne, pas dans les API publiques. `List<T>` est optimisé pour les performances et la puissance au détriment de la propreté de l’API et de flexibilité. Par exemple, si vous retournez `List<T>`, pas jamais pouvoir recevoir des notifications lorsque le code client modifiera la collection. En outre, `List<T>` expose de nombreux membres, tels que <xref:System.Collections.Generic.List%601.BinarySearch%2A>, qui ne sont pas utiles ou applicable dans de nombreux scénarios. Les deux sections suivantes décrivent les types (abstractions) conçus spécifiquement pour une utilisation dans les API publiques.  
  
 **X DO NOT** utiliser `Hashtable` ou `Dictionary<TKey,TValue>` dans les API publiques.  
  
 Ces types sont des structures de données conçus pour être utilisé dans l’implémentation interne. Les API publiques doivent utiliser <xref:System.Collections.IDictionary>, `IDictionary <TKey, TValue>`, ou un type personnalisé implémentant une ou les deux interfaces.  
  
 **X DO NOT** utiliser <xref:System.Collections.Generic.IEnumerator%601>, <xref:System.Collections.IEnumerator>, ou tout autre type qui implémente une de ces interfaces, sauf comme type de retour d’un `GetEnumerator` (méthode).  
  
 Types de retour autre que les énumérateurs de méthodes `GetEnumerator` ne peut pas être utilisé avec la `foreach` instruction.  
  
 **X DO NOT** implémenter les deux `IEnumerator<T>` et `IEnumerable<T>` sur le même type. Va de même pour les interfaces non génériques `IEnumerator` et `IEnumerable`.  
  
## <a name="collection-parameters"></a>Paramètres de collecte  
 **✓ DO** utiliser possibles spécialisée au moins un type comme type de paramètre. La plupart des membres en prenant les collections comme paramètres utilisent la `IEnumerable<T>` interface.  
  
 **X AVOID** à l’aide de <xref:System.Collections.Generic.ICollection%601> ou <xref:System.Collections.ICollection> en tant que paramètre uniquement pour accéder à la `Count` propriété.  
  
 Au lieu de cela, envisagez d’utiliser `IEnumerable<T>` ou `IEnumerable` et dynamiquement la vérification si l’objet implémente `ICollection<T>` ou `ICollection`.  
  
## <a name="collection-properties-and-return-values"></a>Propriétés de la collection et les valeurs de retour  
 **X DO NOT** fournissent des propriétés de collection définissable.  
  
 Les utilisateurs peuvent remplacer le contenu de la collection en effaçant tout d’abord de la collection, puis ajouter le nouveau contenu. Si le remplacement de l’ensemble de la collection est un scénario courant, si possible, donnez le `AddRange` méthode sur la collection.  
  
 **✓ DO** utiliser `Collection<T>` ou une sous-classe de `Collection<T>` pour les collections en lecture/écriture qui représentent des valeurs de propriétés ou retour.  
  
 Si `Collection<T>` ne répond pas à certaines conditions (par exemple, la collection ne doit pas implémenter <xref:System.Collections.IList>), utilisez une collection personnalisée en implémentant `IEnumerable<T>`, `ICollection<T>`, ou <xref:System.Collections.Generic.IList%601>.  
  
 **✓ DO** utiliser <xref:System.Collections.ObjectModel.ReadOnlyCollection%601>, une sous-classe de `ReadOnlyCollection<T>`, ou dans de rares cas `IEnumerable<T>` pour les valeurs de propriétés ou retour qui représentent des collections en lecture seule.  
  
 En général, préférez `ReadOnlyCollection<T>`. Si elle ne remplit pas certaines conditions (par exemple, la collection ne doit pas implémenter `IList`), utilisez une collection personnalisée en implémentant `IEnumerable<T>`, `ICollection<T>`, ou `IList<T>`. Si vous implémentez une collection en lecture seule personnalisée, implémentez `ICollection<T>.IsReadOnly` pour retourner `true`.  
  
 Dans les cas où vous êtes sûr que le seul scénario sera jamais à prendre en charge est itération avant uniquement, vous pouvez simplement utiliser `IEnumerable<T>`.  
  
 **✓ CONSIDER** à l’aide des sous-classes de collections génériques de base au lieu d’utiliser directement les collections.  
  
 Ainsi, pour un nom plus et pour ajouter des membres d’assistance qui ne sont pas présents sur les types de collection de base. Cela s’applique en particulier à l’API de haut niveau.  
  
 **✓ CONSIDER** retournant une sous-classe de `Collection<T>` ou `ReadOnlyCollection<T>` à partir des méthodes et propriétés fréquemment utilisées.  
  
 Cela rend possible pour ajouter des méthodes d’assistance ou de modifier l’implémentation de la collection à l’avenir.  
  
 **✓ CONSIDER** à l’aide d’une collection à clé si les éléments stockés dans la collection ont des clés uniques (nom, ID, etc.). Collections à clé sont des collections qui peuvent être indexées par un entier et une clé et sont généralement implémentées en héritant de `KeyedCollection<TKey,TItem>`.  
  
 Généralement, des collections à clé ont une plus grande empreinte mémoire et ne doivent pas être utilisées si la surcharge de mémoire dépasse les avantages d’avoir les clés.  
  
 **X DO NOT** retournent des valeurs null à partir des propriétés de collection ou les méthodes de retourner des collections. Retourne une collection vide ou un tableau vide à la place.  
  
 La règle générale est que les collections (0 élément) null et vides ou les tableaux doivent être traités de la même.  
  
### <a name="snapshots-versus-live-collections"></a>Captures instantanées par rapport aux Collections en direct  
 Représentant un état à un moment donné dans le temps de collections sont appelées des collections d’instantanés. Par exemple, une collection contenant les lignes retournées à partir d’une requête de base de données serait un instantané. Les collections qui représentent toujours l’état actuel sont appelées des collections en direct. Par exemple, une collection de `ComboBox` éléments est une collection en direct.  
  
 **X DO NOT** retournent des collections de l’instantané à partir des propriétés. Propriétés ne doivent retourner des collections en direct.  
  
 Accesseurs Get de propriété doit être des opérations très légers. Retour d’une capture instantanée requiert la création d’une copie d’une collection interne dans une opération o (n).  
  
 **✓ DO** utiliser une collection de capture instantanée ou live `IEnumerable<T>` (ou son sous-type) pour représenter les collections sont volatiles (autrement dit, qui peut changer sans modification explicite de la collection).  
  
 En règle générale, toutes les collections qui représente une ressource partagée (par exemple, les fichiers dans un répertoire) sont volatiles. Ces collections sont très difficile ou impossible de mettre en œuvre en tant que collections en direct, sauf si l’implémentation est simplement un énumérateur avant uniquement.  
  
## <a name="choosing-between-arrays-and-collections"></a>Choix entre les tableaux et Collections  
 **✓ DO** préférer les collections sur des tableaux.  
  
 Collections offrent un contrôle accru de contenu peuvent évoluer au fil du temps et ne sont plus utilisables. En outre, l’utilisation de tableaux pour les scénarios en lecture seule est déconseillée, car le coût de clonage du tableau est excessif. Études de convivialité ont montré que certains développeurs convient le mieux à l’aide des API basées sur la collection.  
  
 Toutefois, si vous développez des API de bas niveau, il peut être préférable d’utiliser des tableaux pour les scénarios en lecture-écriture. Les tableaux ont un plus faible encombrement mémoire, ce qui permet de réduire la plage de travail, et accéder aux éléments dans un tableau est plus rapide, car elle est optimisée par le runtime.  
  
 **✓ CONSIDER** à l’aide de tableaux dans les API de bas niveau pour réduire la consommation de mémoire et optimiser les performances.  
  
 **✓ DO** utiliser des tableaux d’octets au lieu de collections d’octets.  
  
 **X DO NOT** utiliser des tableaux pour les propriétés si la propriété devrait retourner un tableau (par exemple, une copie d’un tableau interne) chaque fois que l’accesseur Get de propriété est appelée.  
  
## <a name="implementing-custom-collections"></a>Implémentation de Collections personnalisées  
 **✓ CONSIDER** héritant de `Collection<T>`, `ReadOnlyCollection<T>`, ou `KeyedCollection<TKey,TItem>` lors de la création de nouvelles collections.  
  
 **✓ DO** implémenter `IEnumerable<T>` lors de la création de nouvelles collections. Envisagez d’implémenter `ICollection<T>` , voire `IList<T>` où il est préférable.  
  
 Lors de l’implémentation de ce type de collection personnalisé, suivez le modèle de API établi par `Collection<T>` et `ReadOnlyCollection<T>` autant que possible. Autrement dit, implémenter les mêmes membres explicitement, nommez les paramètres tels que ces deux collections nommer les et ainsi de suite.  
  
 **✓ CONSIDER** implémentant des interfaces de collection non générique (`IList` et `ICollection`) si la collection doit souvent être passée à l’API en prenant ces interfaces en tant qu’entrée.  
  
 **X AVOID** implémenter des interfaces de collection sur des types avec les API complexes sans rapport avec le concept d’une collection.  
  
 **X DO NOT** héritent des collections de base non génériques comme `CollectionBase`. Utilisez `Collection<T>`, `ReadOnlyCollection<T>`, et `KeyedCollection<TKey,TItem>` à la place.  
  
### <a name="naming-custom-collections"></a>Regroupements personnalisés d’affectation de noms  
 Collections (types qui implémentent `IEnumerable`) sont créés principalement pour deux raisons : (1) pour créer une nouvelle structure de données avec des opérations spécifiques à la structure et souvent les caractéristiques de performances différentes à des structures de données existantes (par exemple, <xref:System.Collections.Generic.List%601>, <xref:System.Collections.Generic.LinkedList%601>, <xref:System.Collections.Generic.Stack%601>) et (2) pour créer une collection spécialisée pour conserver un ensemble spécifique d’éléments (par exemple, <xref:System.Collections.Specialized.StringCollection>). Structures de données sont souvent utilisées dans l’implémentation interne des applications et des bibliothèques. Collections spécialisées sont principalement d’être exposée dans les API (les types de propriété et de paramètre).  
  
 **✓ DO** utiliser le suffixe « Dictionnaire » dans les noms de mise en œuvre des abstractions `IDictionary` ou `IDictionary<TKey,TValue>`.  
  
 **✓ DO** utiliser le suffixe « Collection » dans les noms de types implémentant `IEnumerable` (ou un de ses descendants) et qui représente une liste d’éléments.  
  
 **✓ DO** utiliser le nom de structure de données approprié pour les structures de données personnalisées.  
  
 **X AVOID** à l’aide de tous les suffixes, ce qui implique une implémentation particulière, telles que « LinkedList » ou « Table de hachage », dans les noms des abstractions de la collection.  
  
 **✓ CONSIDER** en ajoutant le préfixe des noms de collection avec le nom du type d’élément. Par exemple, une collection de stockage des éléments de type `Address` (implémentation `IEnumerable<Address>`) doit être nommé `AddressCollection`. Si le type d’élément est une interface, préfixe « I » de l’élément de type peut être omis. Par conséquent, une collection de <xref:System.IDisposable> éléments peuvent être appelées `DisposableCollection`.  
  
 **✓ CONSIDER** à l’aide du préfixe « ReadOnly » dans les noms de collections en lecture seule si une collection accessible en écriture correspondante peut-être être ajoutée ou existe déjà dans l’infrastructure.  
  
 Par exemple, une collection en lecture seule de chaînes doit être appelée `ReadOnlyStringCollection`.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Indications relatives à l’utilisation](../../../docs/standard/design-guidelines/usage-guidelines.md)
