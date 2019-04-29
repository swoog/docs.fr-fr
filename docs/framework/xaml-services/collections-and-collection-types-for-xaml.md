---
title: Collections et types de collections pour XAML
ms.date: 03/30/2017
ms.assetid: 58f8e7c6-9a41-4f25-8551-c042f1315baa
ms.openlocfilehash: 4123b64545f7c47a96c4cae496046a89b7e576b0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954178"
---
# <a name="collections-and-collection-types-for-xaml"></a>Collections et types de collections pour XAML

Cette rubrique décrit comment définir les propriétés des types qui sont destinés à prendre en charge une collection et pour prendre en charge la syntaxe XAML pour l’instanciation des éléments de collecte en tant qu’éléments enfants d’un élément de propriété ou un élément d’objet parent.

## <a name="xaml-collection-concepts"></a>Concepts de Collection XAML

Conceptuellement, toute relation dans XAML où il existe plusieurs des éléments enfants de l’étendue d’un élément d’objet XAML ou élément de propriété XAML doit être implémentée en tant que collection. Cette collection doit être associée à une propriété XAML particulière du type XAML qui est le parent dans cette relation. La propriété doit être une collection, car un processeur XAML attend assigner chaque élément dans le balisage en être un élément qui vient d’être ajouté de la propriété de collection de sauvegarde.

Au niveau du langage XAML, les spécifications exactes de prise en charge de la collection ne sont pas définies entièrement. Le concept qu’une collection peut être une liste ou un dictionnaire (mais pas les deux) est défini au niveau du langage XAML, mais les types de sauvegarde représentent deux listes ou dictionnaires n’est pas défini par le langage XAML.

Dans les Services XAML .NET Framework, le concept de prise en charge de la collection XAML est plus clairement défini en termes de types de stockage de .NET Framework. Plus précisément, la prise en charge XAML pour les collections repose sur plusieurs concepts de .NET Framework et les API qui sont utilisées pour les listes et les dictionnaires dans généraux de la programmation .NET Framework.

1. Le <xref:System.Collections.IList> interface indique une collection de listes.

2. Le <xref:System.Collections.IDictionary> interface indique une collection de dictionnaires.

3. <xref:System.Array> représente un tableau et un tableau prend en charge <xref:System.Collections.IList> méthodes.

Dans chacun de ces concepts de collection, un processeur XAML de Services XAML .NET Framework s’attend à appeler le `Add` méthode sur une instance spécifique de la collection du type de propriété. Ou, dans un scénario de sérialisation, un processeur XAML produit des instances de type XAML discrètes pour chaque élément trouvé dans la liste, un dictionnaire ou un tableau basé sur un concept spécifique de chaque collection de « Éléments ». Il s’agit de : <xref:System.Collections.IList.Item%2A>; <xref:System.Collections.IDictionary.Item%2A>; explicites <xref:System.Array.System%23Collections%23IList%23Item%2A> pour <xref:System.Array>.

## <a name="generic-collections"></a>Collections génériques

Collections génériques peuvent être utiles pour la programmation .NET Framework générales et peuvent également être utilisées pour les propriétés de collection XAML. Toutefois, les interfaces génériques <xref:System.Collections.Generic.IList%601> et <xref:System.Collections.Generic.IDictionary%602> ne sont pas identifiées par les processeurs XAML de Services XAML .NET Framework comme étant équivalent à non générique <xref:System.Collections.IList> ou <xref:System.Collections.IDictionary>. Plutôt que d’implémenter les interfaces, une approche recommandée pour les types de propriété de collection générique consiste à dériver à partir des classes <xref:System.Collections.Generic.List%601> ou <xref:System.Collections.Generic.Dictionary%602>. Ces classes implémentent les interfaces non génériques et donc incluent la prise en charge attendue pour les collections XAML dans l’implémentation de base.

## <a name="read-only-collections-and-initialization-logic"></a>Collections en lecture seule et la logique d’initialisation

Dans la programmation .NET Framework, il est un modèle de conception courantes pour rendre une propriété qui contient une valeur d’une collection comme une collection en lecture seule. Ce modèle permet à l’instance qui possède la propriété de collection afin de mieux contrôler ce qui se passe à la collection... Plus précisément, le modèle empêche le remplacement accidentel de la collection entière préexistante en définissant la propriété. Dans ce modèle, tout accès à la collection par les appelants doivent plutôt être effectuées en appelant des méthodes ou propriétés pris en charge par le type de collection et/ou les interfaces de collection pertinentes telles que <xref:System.Collections.IList>.

À l’aide de ce modèle implique que n’importe quelle classe qui expose une propriété de collection en lecture seule doit d’abord initialiser cette propriété pour stocker une collection vide. En règle générale, l’initialisation est exécutée en tant que partie du comportement de construction de la classe. Pour être utile pour XAML, il est important que cette logique est toujours référencée par le constructeur par défaut, étant donné que XAML appelle généralement le constructeur par défaut avant le traitement des propriétés (propriétés de la collection ou autre).

## <a name="xaml-type-system-support-and-collections"></a>Collections et prise en charge de système de Type XAML

Au-delà des mécanismes de base de l’analyse XAML et de remplissage ou de sérialisation des propriétés de collection, le système de type XAML tel qu’implémenté dans les Services XAML .NET Framework inclut plusieurs fonctionnalités de conception qui se rapportent aux collections dans XAML.

1. <xref:System.Xaml.XamlType.IsCollection%2A> Retourne la valeur true si le type XAML est soutenu par un type qui fournit la prise en charge de la collection XAML.

2. <xref:System.Xaml.XamlType.IsDictionary%2A> et <xref:System.Xaml.XamlType.IsArray%2A> peut identifier plus précisément quel mode de collecte prend en charge par le type XAML. Pour XAML personnalisé processeurs qui sont basées sur les Services XAML .NET Framework et le XAML système de type, mais pas basée sur existant <xref:System.Xaml.XamlWriter> implémentations, connaître le mode de collection utilisé peut être nécessaire afin de savoir quelle méthode à appeler pour traitement de la collection.

3. Chacune des valeurs de propriété précédentes sont potentiellement influencées par les substitutions de <xref:System.Xaml.XamlType.LookupCollectionKind%2A> sur un type XAML.
