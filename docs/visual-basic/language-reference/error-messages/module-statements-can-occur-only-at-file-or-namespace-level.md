---
title: Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: fc3c102dbfe7c55e66093421bc11379d48ba000d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592094"
---
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a>Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms
`Module` les instructions doivent apparaître en haut de votre fichier source immédiatement après `Option` et `Imports` instructions, les attributs globaux et les déclarations d’espace de noms, mais avant toutes les autres déclarations.  
  
 **ID d’erreur :** BC30617  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Déplacez l’instruction `Module` en haut de votre déclaration d’espace de noms ou de votre fichier source.  
  
## <a name="see-also"></a>Voir aussi

- [Module (instruction)](../../../visual-basic/language-reference/statements/module-statement.md)
