---
title: Comment déterminer si un objet .NET Standard est sérialisable
description: Montre comment déterminer si un type .NET Standard peut être sérialisé en cours d’exécution.
ms.date: 10/20/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- serializing objects
- objects, serializing steps
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 196e99ab1f1a0baae53c6a1dc295b135e36fbfe0
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45675611"
---
# <a name="how-to-determine-if-a-net-standard-object-is-serializable"></a>Comment déterminer si un objet .NET Standard est sérialisable

.NET Standard est une spécification qui définit les types et membres qui doivent être présents sur les implémentations de .NET spécifiques qui sont conformes à cette version de la norme. Toutefois, .NET Standard ne définit pas si un type est sérialisable. Les types définis dans la bibliothèque .NET Standard ne sont pas marqués avec le <xref:System.SerializableAttribute> attribut. Au lieu de cela, les implémentations .NET spécifiques, telles que le .NET Framework et .NET Core, sont gratuites déterminer si un type particulier est sérialisable. 

Si vous avez développé une bibliothèque qui cible .NET Standard, votre bibliothèque peut être consommée par une implémentation .NET qui prend en charge .NET Standard. Cela signifie que vous ne pouvez pas savoir à l’avance si un type particulier est sérialisable ; Vous ne pouvez déterminer s’il est sérialisable en cours d’exécution.

Vous pouvez déterminer si un objet est sérialisable lors de l’exécution en récupérant la valeur de la <xref:System.Type.IsSerializable> propriété d’un <xref:System.Type> objet qui représente le type de l’objet. L’exemple suivant fournit une implémentation. Il définit un `IsSerializable(Object)` méthode d’extension qui indique si une <xref:System.Object> instance peut être sérialisée.

[!code-csharp[is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/csharp/program.cs#2)]
[!code-vb[is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/vb/library.vb#2)]

Vous pouvez ensuite passer n’importe quel objet à la méthode pour déterminer si elle peut être sérialisé et désérialisé sur l’implémentation actuelle de .NET, comme le montre l’exemple suivant :

[!code-csharp[test-is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/csharp/program.cs#1)]
[!code-vb[test-is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/vb/program.vb#1)]

## <a name="see-also"></a>Voir aussi

- [Sérialisation binaire](binary-serialization.md)
- <xref:System.SerializableAttribute?displayProperty=nameWithType>
- <xref:System.Type.IsSerializable?displayProperty=nameWithType>
