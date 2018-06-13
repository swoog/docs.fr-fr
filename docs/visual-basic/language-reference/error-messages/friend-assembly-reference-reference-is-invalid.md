---
title: Référence d’assembly friend &lt;référence&gt; n’est pas valide
ms.date: 07/20/2015
f1_keywords:
- vbc31535
- bc31535
helpviewer_keywords:
- BC31535
ms.assetid: 6540c1d0-bb19-4051-a579-2e4f9094585e
ms.openlocfilehash: c47fae9c60dc04ee02b1ff015d3dde87b8920c02
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587369"
---
# <a name="friend-assembly-reference-ltreferencegt-is-invalid"></a>Référence d’assembly friend &lt;référence&gt; n’est pas valide
Référence d’assembly friend \<référence > n’est pas valide. Les assemblys signés avec un nom fort doivent spécifier une clé publique dans leurs déclarations InternalsVisibleTo.  
  
 Le nom d’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut identifie un assembly avec nom fort, mais il n’inclut pas un `PublicKey` attribut.  
  
 **ID d’erreur :** BC31535  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déterminez la clé publique de l’assembly friend avec un nom fort. Inclure la clé publique comme partie du nom de l’assembly passé à la <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> constructeur d’attribut à l’aide de la `PublicKey` attribut.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Reflection.AssemblyName>  
 [Assemblys friend](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md)  
 

