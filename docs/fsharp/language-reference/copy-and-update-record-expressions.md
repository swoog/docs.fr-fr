---
title: 'Copier et mettre à jour des Expressions d’enregistrement (F #)'
description: Découvrez comment écrire une « copie et mise à jour enregistrement expression » qui copie un existant, ces mises à jour spécifié de champs et retourne l’enregistrement mis à jour.
author: ChrSteinert
ms.date: 06/04/2016
ms.openlocfilehash: d2b089e8a7fc5c7ee26139003e23d2eaa8a3174e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44197394"
---
# <a name="copy-and-update-record-expressions"></a>Copie et mise à jour des expressions d’enregistrement

Un *copier et mettre à jour d’expression d’enregistrement* est une expression qui copie un enregistrement existant, met à jour les champs spécifiés et retourne l’enregistrement mis à jour.

## <a name="syntax"></a>Syntaxe

```fsharp
{ record-name with
    updated-member-definitions }
```

## <a name="remarks"></a>Notes

Les enregistrements sont immuables par défaut, pour qu’il n’y a aucune mise à jour un enregistrement existant possible. Pour créer un enregistrement mis à jour tous les champs d’un enregistrement devrait être spécifiés à nouveau. Pour simplifier cette tâche un *copier et mettre à jour d’expression d’enregistrement* peut être utilisé. Cette expression prend un enregistrement existant, crée un nouveau du même type à l’aide des champs spécifiés à partir de l’expression et le champ manquant spécifié par l’expression.
Cela peut être utile lorsque vous devez copier un enregistrement existant et éventuellement modifier certaines valeurs de champ.

Prenez par exemple un enregistrement qui vient d’être créé.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1905.fs)]

Si vous deviez mettre à jour uniquement sur le champ de cet enregistrement, vous pouvez utiliser la *copier et mettre à jour d’expression d’enregistrement* comme suit :

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1906.fs)]

## <a name="see-also"></a>Voir aussi

- [Enregistrements](records.md)
- [Informations de référence du langage F#](index.md)
