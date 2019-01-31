---
title: Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: 0820763cce9cc27f9a379ed5e766e0691a75f36b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271263"
---
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a>Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms
`Module` les instructions doivent apparaître en haut de votre fichier source immédiatement après `Option` et `Imports` instructions, les attributs globaux et les déclarations d’espace de noms, mais avant toutes les autres déclarations.  
  
 **ID d’erreur :** BC30617  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Déplacez l’instruction `Module` en haut de votre déclaration d’espace de noms ou de votre fichier source.  
  
## <a name="see-also"></a>Voir aussi
- [Module (instruction)](../../../visual-basic/language-reference/statements/module-statement.md)
