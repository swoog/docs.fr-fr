---
title: public, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- public
- public_CSharpKeyword
helpviewer_keywords:
- public keyword [C#]
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
ms.openlocfilehash: 84a3bc49b6eea047d518edc01dab7f2301854b6a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518184"
---
# <a name="public-c-reference"></a>public (référence C#)

Le mot clé `public` est un modificateur d’accès pour les types et les membres de types. L’accès public est le niveau d’accès le plus permissif. Il n’existe pas de restrictions d’accès aux membres publics, comme dans cet exemple :

```csharp
class SampleClass
{
    public int x; // No access restrictions.
}
```

Pour plus d’informations, consultez [Modificateurs d’accès](../../programming-guide/classes-and-structs/access-modifiers.md) et [Niveaux d’accessibilité](accessibility-levels.md).

## <a name="example"></a>Exemple

Dans l’exemple suivant, deux classes sont déclarées, `PointTest` et `MainClass`. L’accès aux membres publics `x` et `y` de `PointTest` s’effectue directement à partir de `MainClass`.

[!code-csharp[csrefKeywordsModifiers#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#13)]

Si vous remplacez le niveau d’accès `public` par [private](private.md) ou [protected](protected.md), le message d’erreur suivant s’affiche :

'PointTest.y' est inaccessible en raison de son niveau de protection.

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Modificateurs d’accès](../../programming-guide/classes-and-structs/access-modifiers.md)
- [Mots clés C#](index.md)
- [Modificateurs d’accès](access-modifiers.md)
- [Niveaux d’accessibilité](accessibility-levels.md)
- [Modificateurs](modifiers.md)
- [private](private.md)
- [protected](protected.md)
- [internal](internal.md)