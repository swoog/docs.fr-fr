---
title: Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: bf0239422fb5a98e4670aea407f684753d3a7ea4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58825441"
---
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a><span data-ttu-id="19d39-102">Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms</span><span class="sxs-lookup"><span data-stu-id="19d39-102">'Module' statements can occur only at file or namespace level</span></span>
<span data-ttu-id="19d39-103">`Module` les instructions doivent apparaître en haut de votre fichier source immédiatement après `Option` et `Imports` instructions, les attributs globaux et les déclarations d’espace de noms, mais avant toutes les autres déclarations.</span><span class="sxs-lookup"><span data-stu-id="19d39-103">`Module` statements must appear at the top of your source file immediately after `Option` and `Imports` statements, global attributes, and namespace declarations, but before all other declarations.</span></span>  
  
 <span data-ttu-id="19d39-104">**ID d’erreur :** BC30617</span><span class="sxs-lookup"><span data-stu-id="19d39-104">**Error ID:** BC30617</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="19d39-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="19d39-105">To correct this error</span></span>  
  
-   <span data-ttu-id="19d39-106">Déplacez l’instruction `Module` en haut de votre déclaration d’espace de noms ou de votre fichier source.</span><span class="sxs-lookup"><span data-stu-id="19d39-106">Move the `Module` statement to the top of your namespace declaration or source file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19d39-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19d39-107">See also</span></span>

- [<span data-ttu-id="19d39-108">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="19d39-108">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)
