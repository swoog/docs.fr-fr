---
title: Variables objet dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], about object variables
- variables [Visual Basic], object
- objects [Visual Basic], accessing
- object variables [Visual Basic]
ms.assetid: 6169a196-2b13-4ba5-a205-154bc1b87844
ms.openlocfilehash: cc5be13293a89e73d1790e94a99d7936f1711e12
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352969"
---
# <a name="object-variables-in-visual-basic"></a>Variables objet dans Visual Basic

Outre le stockage des valeurs directement, une variable peut faire référence à un objet. Vous affectez un objet à une variable pour les mêmes raisons que vous assignez une valeur à une variable :

- Un nom de variable est souvent plus court et plus facile à retenir que le chemin d’accès complet des méthodes et propriétés nécessaires pour accéder à l’objet lui-même.

- À l’aide d’une variable qui fait référence à un objet est plus efficace que plusieurs fois l’accès à l’objet lui-même via les méthodes ou propriétés nécessaires.

- Vous pouvez modifier une variable pour faire référence à d’autres objets pendant l’exécution de votre code.

## <a name="making-code-shorter"></a>En rendant le Code plus court

Vous pouvez utiliser des variables d’objet pour raccourcir le code que vous devez taper. L’exemple suivant utilise le chemin d’accès complet des méthodes et propriétés pour accéder à un <xref:System.Windows.Forms.Control> objet.

```vb
' Assume Me is a valid Form, or replace Me with a valid Form.
Me.ActiveForm.ActiveControl.Text = "Test"
Me.ActiveForm.ActiveControl.Location = New Point(100, 100)
Me.ActiveForm.ActiveControl.Show()
```

Vous pouvez raccourcir ce code et accélérer l’exécution, si vous utilisez une variable d’objet pour le contrôle. Vous devez déclarer la variable objet avec la classe spécifique que vous avez l’intention de lui assigner (`Control` dans ce cas). Une fois que vous affectez un objet à la variable, vous pouvez traitez-le exactement comme vous traitez l’objet auquel il fait référence. Vous pouvez définir ou récupérer les propriétés de l’objet ou utiliser une de ses méthodes. L’exemple suivant utilise une variable objet pour simplifier le code dans l’exemple précédent.

```vb
Dim ctrlActv As System.Windows.Forms.Control = Me.ActiveForm.ActiveControl
ctrlActv.Text = "Test"
ctrlActv.Location = New Point(100, 100)
ctrlActv.Show()
```

## <a name="see-also"></a>Voir aussi

- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Guide pratique pour Accélérer l’accès à un objet avec un chemin d’accès de Qualification Long](../../../../visual-basic/programming-guide/language-features/variables/how-to-speed-up-access-to-an-object-with-a-long-qualification-path.md)
- [Déclaration des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [Assignation des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Valeurs des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
