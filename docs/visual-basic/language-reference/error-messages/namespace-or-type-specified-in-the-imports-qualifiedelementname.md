---
title: L'espace de noms ou le type spécifié dans les Imports '<qualifiedelementname>' ne contient aucun membre public ou est introuvable
ms.date: 07/20/2015
f1_keywords:
- bc40056
- vbc40056
helpviewer_keywords:
- BC40056
ms.assetid: b59f5754-444f-4378-9272-9678b437e84a
ms.openlocfilehash: 1873c0af7a251afd7754557f5dcb6aed13eb9f11
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61918318"
---
# <a name="namespace-or-type-specified-in-the-imports-qualifiedelementname-doesnt-contain-any-public-member-or-cannot-be-found"></a>Namespace ou type spécifié dans les Imports'\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable

Namespace ou type spécifié dans les Imports'\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable. Assurez-vous que l’espace de noms ou le type est défini et contient au moins un membre public. Assurez-vous que le nom d’alias ne contient pas d’autres alias.

Un `Imports` instruction spécifie un élément conteneur qui ne peut pas être trouvé ou ne définit pas `Public` membres.

Un *contenant l’élément* peut être un espace de noms, une classe, une structure, un module, une interface ou une énumération. L’élément conteneur contient des membres, tels que des variables, procédures ou d’autres éléments qui le contient.

L’objectif de l’importation consiste à autoriser votre code pour accéder aux membres de type ou espace de noms sans devoir les qualifier. Votre projet devrez peut-être également ajouter une référence à l’espace de noms ou type. Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).

Si le compilateur ne peut pas trouver l’élément conteneur spécifié, il ne peut pas résoudre les références qui l’utilisent. Si elle recherche l’élément, mais l’élément n’expose pas `Public` membres, aucune référence peut être réussie. Dans les deux cas, il est sans signification pour importer l’élément.

N’oubliez pas que si vous importez un élément de conteneur et lui affectez un alias d’importation, puis vous ne pouvez pas utiliser cet alias d’importation pour importer un autre élément. Le code suivant génère une erreur du compilateur.

```vb
Imports winfrm = System.Windows.Forms

' The following statement is INVALID  because it reuses an import alias.

Imports behave = winfrm.Design.Behavior`
```

**ID d’erreur :** BC40056

## <a name="to-correct-this-error"></a>Pour corriger cette erreur

1. Vérifiez que l’élément conteneur est accessible à partir de votre projet.

2. Vérifiez que la spécification de l’élément conteneur n’inclut pas de n’importe quel alias d’importation à partir d’une autre importation.

3. Vérifiez que l’élément conteneur expose au moins un `Public` membre.

## <a name="see-also"></a>Voir aussi

- [Imports (instruction) (espace de noms et type .NET)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Namespace (instruction)](../../../visual-basic/language-reference/statements/namespace-statement.md)
- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
