---
title: "'<keyword>' est valide uniquement dans une méthode d'instance"
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: 5ff82b932f9bea4c7fd087651e34277ef94bc27c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946638"
---
# <a name="keyword-is-valid-only-within-an-instance-method"></a><span data-ttu-id="6dc41-102">'\<mot clé >' est valide uniquement dans une méthode d’instance</span><span class="sxs-lookup"><span data-stu-id="6dc41-102">'\<keyword>' is valid only within an instance method</span></span>
<span data-ttu-id="6dc41-103">Le `Me`, `MyClass`, et `MyBase` mots clés font référence aux instances de classe spécifique.</span><span class="sxs-lookup"><span data-stu-id="6dc41-103">The `Me`, `MyClass`, and `MyBase` keywords refer to specific class instances.</span></span> <span data-ttu-id="6dc41-104">Vous ne pouvez pas les utiliser à l’intérieur d’un partage `Function` ou `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="6dc41-104">You cannot use them inside a shared `Function` or `Sub` procedure.</span></span>  
  
 <span data-ttu-id="6dc41-105">**ID d’erreur :** BC30043</span><span class="sxs-lookup"><span data-stu-id="6dc41-105">**Error ID:** BC30043</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6dc41-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="6dc41-106">To correct this error</span></span>  
  
- <span data-ttu-id="6dc41-107">Supprimez le mot clé à partir de la procédure ou supprimez le `Shared` mot clé à partir de la déclaration de procédure.</span><span class="sxs-lookup"><span data-stu-id="6dc41-107">Remove the keyword from the procedure, or remove the `Shared` keyword from the procedure declaration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dc41-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc41-108">See also</span></span>

- [<span data-ttu-id="6dc41-109">Assignation des variables objets</span><span class="sxs-lookup"><span data-stu-id="6dc41-109">Object Variable Assignment</span></span>](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="6dc41-110">Me, My, MyBase et MyClass</span><span class="sxs-lookup"><span data-stu-id="6dc41-110">Me, My, MyBase, and MyClass</span></span>](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="6dc41-111">Éléments fondamentaux de l’héritage</span><span class="sxs-lookup"><span data-stu-id="6dc41-111">Inheritance Basics</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
