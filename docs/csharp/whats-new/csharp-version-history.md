---
title: Histoire du langage C# | Guide C#
description: À quoi ressemblait le langage dans ses versions antérieures et comment a-t-il évolué depuis ?
author: erikdietrich
ms.date: 09/20/2017
ms.openlocfilehash: 1c7b91a3a5c77059ca8d7acef95252b4a3557b28
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="the-history-of-c"></a>Histoire du langage C# #

À quoi ressemblait le langage dans ses premières versions ? Et comment a-t-il évolué au fil des années ?

## <a name="c-version-10"></a>C# version 1.0

Rétrospectivement, le langage C# version 1.0 ressemblait beaucoup à Java. Dans ses [objectifs de conception énoncés pour ECMA](http://feeldotneteasy.blogspot.com/2011/01/c-design-goals.html), il cherchait à être un « langage orienté objet simple, moderne et généraliste ».  À l’époque, ressembler à Java signifiait qu’il avait atteint ces objectifs de conception.

Mais si vous repensez à C# 1.0 maintenant, cela peut vous donner le vertige. Il lui manquait des fonctionnalités asynchrones intégrées et certaines des fonctionnalités liées aux génériques qui sont aujourd’hui pour nous une évidence. En fait, il ne proposait pas du tout de génériques.  Et [LINQ](../linq/index.md) ? Pas encore disponible. Il fallait attendre encore plusieurs années.

C# version 1.0 semblait dénué de fonctionnalités, par rapport à aujourd’hui. Vous vous retrouviez à écrire plus ou moins du code détaillé. Mais il faut bien commencer quelque part. C# version 1.0 était une alternative viable à Java sur la plateforme Windows.

## <a name="c-version-20"></a>C# version 2.0

Les choses commencent alors à devenir intéressantes. Examinons certaines fonctionnalités majeures de C# 2.0, sorti en 2005, en même temps que Visual Studio 2005 :

- [Génériques](../programming-guide/generics/index.md)
- [Types partiels](../programming-guide/classes-and-structs/partial-classes-and-methods.md#partial-classes)
- [Méthodes anonymes](../programming-guide/statements-expressions-operators/anonymous-methods.md)
- [Types Nullable](../programming-guide/nullable-types/index.md)
- [Itérateurs](../programming-guide/concepts/iterators.md)
- [Covariance et contravariance](../programming-guide/concepts/covariance-contravariance/index.md)

Alors que C# avait démarré en tant que langage orienté objet assez générique, C# version 2.0 a rapidement changé tout ça. En effet, maintenant que le langage existait, il s’agissait de s’attaquer à certains problèmes majeurs que rencontraient les développeurs. Et de s’y attaquer massivement.

Avec les génériques, vous avez des types et des méthodes capables de fonctionner sur un type arbitraire tout en assurant quand même la cohérence des types. Ainsi, à titre d’exemple, un <xref:System.Collections.Generic.List%601> vous permet d’avoir `List<string>` ou `List<int>` et d’effectuer des opérations qui maintiennent la cohérence des types sur des chaînes ou entiers alors que vous itérez en leur sein. C’est mieux que de créer des héritiers `ListInt` ou de caster à partir de `Object` pour chaque opération.

C# version 2.0 a introduit les itérateurs. En bref, ils vous permettent d’itérer au sein des éléments dans un `List` (ou d’autres types énumérables) avec une boucle `foreach`. Cette nouveauté de premier ordre dans le langage en a considérablement amélioré la lisibilité et la capacité de raisonnement des utilisateurs vis-à-vis du code.

Pourtant, C# était toujours en train de courir derrière Java. Java avait déjà publié des versions qui incluaient des génériques et des itérateurs. Mais cela allait bientôt changer quand les deux langages poursuivraient des chemins différents.

## <a name="c-version-30"></a>C# version 3.0

C# version 3.0 est apparu fin 2007, en même temps que Visual Studio 2008, même si l’éventail complet des fonctionnalités du langage n’a réellement voir le jour qu’avec le .NET Framework version 3.5. Cette version a insufflé un changement majeur dans l’évolution de C#. Elle a imposé C# en tant que langage de programmation vraiment formidable. Examinons certaines fonctionnalités importantes dans cette version :

- [Propriétés implémentées automatiquement](../programming-guide/classes-and-structs/auto-implemented-properties.md)
- [Types anonymes](../programming-guide/classes-and-structs/anonymous-types.md)
- [Expressions de requête](../linq/query-expression-basics.md)
- [Expression lambda](https://www.daedtech.com/introduction-to-c-lambda-expressions/)
- [Arborescences d’expressions](https://blogs.msdn.microsoft.com/charlie/2008/01/31/expression-tree-basics/)
- [Méthodes d’extension](https://www.codeproject.com/Tips/709310/Extension-Method-In-Csharp)

Rétrospectivement, nombre de ces fonctionnalités semblent à la fois inéluctables et inséparables. Elles s’assemblent de façon stratégique. L’expression de requête, également appelée LINQ (Language-Integrated Query), était globalement considérée comme la fonctionnalité remarquable de cette version de C#.

Un point de vue plus nuancé s’intéresse aux arborescences d’expressions, aux expressions lambda et aux types anonymes sur lesquels se construit LINQ. Mais, dans les deux cas, C# 3.0 présentait un concept révolutionnaire. C# 3.0 jetait les bases qui allaient permettre à C# de devenir un langage fonctionnel/orienté objet hybride.

Plus précisément, il devint alors possible d’écrire des requêtes déclaratives de style SQL pour effectuer des opérations sur des collections, entre autres choses. Au lieu d’écrire une boucle `for` pour calculer la moyenne d’une liste d’entiers, vous pouviez alors simplement utiliser `list.Average()`. La combinaison des expressions de requête et des méthodes d’extension a permis à de telles listes d’entiers de paraître beaucoup plus intelligentes.

Il a fallu du temps aux utilisateurs pour comprendre et intégrer ce concept, mais ils y sont progressivement parvenus. Et aujourd’hui, bien des années plus tard, le code est beaucoup plus concis, simple et fonctionnel.

## <a name="c-version-40"></a>C# version 4.0

Il fut difficile pour C# version 4.0 d’être à la hauteur du concept révolutionnaire incarné par la version 3.0. Avec la version 3.0, le langage C# est bel et bien sorti de l’ombre de Java pour être propulsé sur le devant de la scène. Il allait même rapidement devenir élégant.

La version suivante introduisit de nouvelles fonctionnalités intéressantes :

- [Liaison dynamique](../language-reference/keywords/dynamic.md)
- [Arguments nommés/facultatifs](../programming-guide/classes-and-structs/named-and-optional-arguments.md)
- [Covariance et contravariance génériques](../../standard/generics/covariance-and-contravariance.md)
- [Types interop incorporés](https://stackoverflow.com/questions/20514240/whats-the-difference-setting-embed-interop-types-true-and-false-in-visual-studi)

Les types interop incorporés ont permis d’atténuer une difficulté de déploiement. La covariance et la contravariance génériques vous donnent plus de contrôle sur l’utilisation des génériques, mais elles sont un peu académiques et probablement plus appréciées des auteurs de frameworks et de bibliothèques. Les paramètres nommés et facultatifs vous permettent d’éliminer les nombreuses surcharges de méthode et s’avèrent plus pratiques. Mais aucune de ces fonctionnalités ne représente un vrai changement de paradigme.

La fonctionnalité majeure était plutôt l’introduction du mot clé `dynamic`. Le mot clé `dynamic` introduisit dans C# version 4.0 la possibilité de remplacer le compilateur lors de la saisie au moment de la compilation. En utilisant le mot clé dynamic, vous pouvez créer des constructions semblables aux langages dynamiquement typés comme JavaScript. Vous pouvez créer un `dynamic x = "a string"`, puis y ajouter six, et ainsi laisser le runtime se débrouiller avec ce qui doit se produire par la suite.

Cela vous donne la possibilité de commettre des erreurs, mais également de contrôler davantage le langage.

## <a name="c-version-50"></a>C# version 5.0

C# version 5.0 était une version très concentrée du langage. Presque tous les efforts déployés pour cette version ont porté sur un autre concept révolutionnaire du langage.  Voici la liste des fonctionnalités principales :

- [Membres asynchrones](../async.md)
- [Attributs d’informations de l’appelant](https://www.codeproject.com/Tips/606379/Caller-Info-Attributes-in-Csharp)

L’attribut d’informations de l’appelant vous permet de récupérer facilement des informations sur le contexte d’exécution sans avoir recours à une multitude de code de réflexion réutilisable. Nombre de ses usages ont trait aux diagnostics et aux tâches de journalisation.

Mais `async` et `await` sont les véritables vedettes de cette version. Quand ces fonctionnalités sont apparues en 2012, C# a encore modifié la donne en intégrant l’asynchronie en tant que participant de premier ordre dans le langage. Si vous avez déjà eu affaire à de longues opérations et à l’implémentation de rappels, vous avez probablement adoré cette fonctionnalité de langage.

## <a name="c-version-60"></a>C# version 6.0

Avec les versions 3.0 et 5.0, C# avait ajouté d’impressionnantes fonctionnalités à un langage orienté objet. Avec la version 6.0, il n’était pas question d’introduire une fonctionnalité à la pointe de la technologie mais plutôt de publier de nombreuses fonctionnalités que les utilisateurs du langage apprécieraient beaucoup. En voici quelques-unes :

- [Importations statiques](../language-reference/keywords/using-static.md)
- [Filtres d’exceptions](https://www.thomaslevesque.com/2015/06/21/exception-filters-in-c-6/)
- [Initialiseurs de propriétés](http://geekswithblogs.net/WinAZ/archive/2015/06/30/whatrsquos-new-in-c-6.0-auto-property-initializers.aspx)
- [Membres expression-bodied](https://lostechies.com/jimmybogard/2015/12/17/c-6-feature-review-expression-bodied-function-members/)
- [Propagateur Null](https://davefancher.com/2014/08/14/c-6-0-null-propagation-operator/)
- [Interpolation de chaîne](../language-reference/tokens/interpolated.md)
- [Opérateur nameof](https://stackoverflow.com/questions/31695900/what-is-the-purpose-of-nameof)
- [Initialiseur de dictionnaire](../programming-guide/classes-and-structs/how-to-initialize-a-dictionary-with-a-collection-initializer.md)

Chacune de ces fonctionnalités est intéressante individuellement. Mais si vous les examinez dans leur ensemble, un modèle intéressant se dégage. Dans cette version, C# a éliminé le texte réutilisable du langage pour rendre le code plus laconique et plus lisible. Ainsi, pour les amateurs de code propre et simple, cette version du langage était une énorme victoire.

Une autre nouveauté a été proposée avec cette version, même s’il ne s’agit pas d’une fonctionnalité de langage traditionnelle à proprement dit. [Le compilateur Roslyn a été publié en tant que service](https://github.com/dotnet/roslyn). Le compilateur C# est à présent écrit en C# et vous pouvez l’utiliser dans le cadre de vos efforts de programmation.

## <a name="c-version-70"></a>C# version 7.0

La dernière version majeure est C# version 7.0. Cette version propose des évolutions intéressantes dans l’esprit de C# 6.0, mais sans le compilateur en tant que service. Voici quelques-unes des nouvelles fonctionnalités :

- [Variables out](http://www.c-sharpcorner.com/article/out-variables-in-c-sharp-7-0/)
- [Tuples et déconstruction](https://www.thomaslevesque.com/2016/08/23/tuple-deconstruction-in-c-7/)
- [Critères spéciaux](./csharp-7.md#pattern-matching)
- [Fonctions locales](http://www.infoworld.com/article/3182416/application-development/c-7-in-depth-exploring-local-functions.html)
- [Membres expression-bodied étendus](./csharp-7.md#more-expression-bodied-members)
- [Variables locales et retours ref](./csharp-7.md#ref-locals-and-returns)

Toutes ces fonctionnalités offrent de nouvelles capacités appréciables aux développeurs ainsi que la possibilité d’écrire du code encore plus propre. Il s’agit notamment de condenser la déclaration des variables à utiliser avec le mot clé `out` et en autorisant plusieurs valeurs de retour par le biais d’un tuple.

Par ailleurs, les utilisations de C# sont de plus en plus larges. .NET Core cible à présent n’importe quel système d’exploitation et garde les yeux rivés sur le cloud et la portabilité.  Ces perspectives occupent sans aucun doute les pensées des concepteurs du langage, en plus des nouvelles fonctionnalités.

_Article_ [_initialement publié sur le blog NDepend_](https://blog.ndepend.com/c-versions-look-language-history/)_, avec l’aimable autorisation d’Erik Dietrich et de Patrick Smacchia._
