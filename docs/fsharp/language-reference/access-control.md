---
title: Contrôle d'accès
description: Découvrez comment contrôler l’accès aux éléments de programmation, tels que les types, méthodes et fonctions, dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: a284d2fa4f98e444279276f58b70a15560537ca4
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645607"
---
# <a name="access-control"></a>Contrôle d'accès

*Contrôle d’accès* fait référence à la déclaration de clients qui peuvent utiliser certains éléments de programme, tels que les types, méthodes et fonctions.

## <a name="basics-of-access-control"></a>Principes de base du contrôle d’accès

Dans F#, les spécificateurs de contrôle d’accès `public`, `internal`, et `private` peuvent être appliquées à des modules, types, méthodes, des définitions de valeur, fonctions, propriétés et champs explicites.

- `public` Indique que l’entité est accessible par tous les appelants.

- `internal` Indique que l’entité est accessible uniquement à partir du même assembly.

- `private` Indique que l’entité est accessible uniquement à partir de type ou un module englobant.

> [!NOTE]
> Le spécificateur d’accès `protected` n’est pas utilisé dans F#, bien qu’il soit acceptable si vous utilisez des types créés dans les langages qui prennent en charge `protected` accès. Par conséquent, si vous substituez une méthode protégée, votre méthode reste accessible uniquement au sein de la classe et ses descendants.

En général, le spécificateur est placé devant le nom de l’entité, sauf quand une `mutable` ou `inline` spécificateur est utilisé, qui apparaît après le spécificateur de contrôle d’accès.

Si aucun spécificateur d’accès n’est utilisé, la valeur par défaut est `public`, à l’exception de `let` liaisons dans un type, qui sont toujours `private` au type.

Signatures dans F# fournissent un autre mécanisme pour contrôler l’accès à F# éléments de programme. Les signatures ne sont pas requises pour le contrôle d’accès. Pour plus d’informations, consultez [Signatures](signatures.md).

## <a name="rules-for-access-control"></a>Règles de contrôle d’accès

Contrôle d’accès est soumis aux règles suivantes :

- Déclarations d’héritage (autrement dit, l’utilisation de `inherit` pour spécifier une classe de base pour une classe), déclarations d’interface (c'est-à-dire spécifier qu’une classe implémente une interface) et d’abstraire membres ont toujours la même accessibilité que le type englobant. Par conséquent, un spécificateur de contrôle d’accès ne peut pas être utilisé sur ces constructions.

- Accessibilité pour les cas individuels dans une union discriminée est déterminée par l’accessibilité de l’union discriminée lui-même. Autrement dit, un cas d’union particulier n’est pas moins accessible que l’union elle-même.

- Accessibilité pour les champs individuels d’un type d’enregistrement ne peut pas est déterminée par l’accessibilité de l’enregistrement lui-même. Autrement dit, une étiquette d’enregistrement particulier n’est pas moins accessible que l’enregistrement lui-même.

## <a name="example"></a>Exemple

Le code suivant illustre l’utilisation de spécificateurs de contrôle d’accès. Il existe deux fichiers dans le projet, `Module1.fs` et `Module2.fs`. Chaque fichier est implicitement un module. Par conséquent, il existe deux modules, `Module1` et `Module2`. Un type privé et un type interne sont définis dans `Module1`. Le type privé n’est pas accessible à partir de `Module2`, mais le type interne.

[!code-fsharp[Main](../../../samples/snippets/fsharp/access-control/snippet1.fs)]

Le code suivant teste l’accessibilité des types créés dans `Module1.fs`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/access-control/snippet2.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Signatures](signatures.md)
