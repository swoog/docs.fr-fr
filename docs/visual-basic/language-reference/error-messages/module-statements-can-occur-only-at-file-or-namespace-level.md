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
# <a name="module-statements-can-occur-only-at-file-or-namespace-level"></a><span data-ttu-id="f43b2-102">Les instructions 'Module' ne peuvent intervenir qu'au niveau du fichier ou de l'espace de noms</span><span class="sxs-lookup"><span data-stu-id="f43b2-102">'Module' statements can occur only at file or namespace level</span></span>
<span data-ttu-id="f43b2-103">`Module` les instructions doivent apparaître en haut de votre fichier source immédiatement après `Option` et `Imports` instructions, les attributs globaux et les déclarations d’espace de noms, mais avant toutes les autres déclarations.</span><span class="sxs-lookup"><span data-stu-id="f43b2-103">`Module` statements must appear at the top of your source file immediately after `Option` and `Imports` statements, global attributes, and namespace declarations, but before all other declarations.</span></span>  
  
 <span data-ttu-id="f43b2-104">**ID d’erreur :** BC30617</span><span class="sxs-lookup"><span data-stu-id="f43b2-104">**Error ID:** BC30617</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f43b2-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f43b2-105">To correct this error</span></span>  
  
-   <span data-ttu-id="f43b2-106">Déplacez l’instruction `Module` en haut de votre déclaration d’espace de noms ou de votre fichier source.</span><span class="sxs-lookup"><span data-stu-id="f43b2-106">Move the `Module` statement to the top of your namespace declaration or source file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f43b2-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f43b2-107">See also</span></span>
- [<span data-ttu-id="f43b2-108">Module (instruction)</span><span class="sxs-lookup"><span data-stu-id="f43b2-108">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)
