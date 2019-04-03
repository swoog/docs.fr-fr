---
title: La référence d'assembly Friend <reference> n'est pas valide
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: 0966cea26c5dde8f116081c7a6411b4275e50f40
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817043"
---
# <a name="friend-assembly-reference-reference-is-invalid"></a>Référence d’assembly friend \<référence > n’est pas valide
Référence d’assembly friend \<référence > n’est pas valide. Les assemblys signés avec un nom fort doivent spécifier une clé publique dans leurs déclarations InternalsVisibleTo.  
  
 Le nom de l’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut identifie un assembly avec nom fort, mais elle n’inclut pas un `PublicKey` attribut.  
  
 **ID d’erreur :** BC31535  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déterminer la clé publique pour l’assembly friend avec nom fort. Inclure la clé publique comme partie du nom d’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut à l’aide de la `PublicKey` attribut.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Reflection.AssemblyName>
- [Assemblys friend](../../../standard/assembly/friend-assemblies.md)
