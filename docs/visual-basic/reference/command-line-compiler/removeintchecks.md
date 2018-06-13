---
title: -removeintchecks
ms.date: 03/13/2018
f1_keywords:
- removeintchecks
- -removeintchecks
helpviewer_keywords:
- removeintchecks compiler option [Visual Basic]
- /removeintchecks compiler option [Visual Basic]
- -removeintchecks compiler option [Visual Basic]
ms.assetid: c1835bd5-1e38-4fba-bd2f-6984774765d4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 26485fe2ba3f5647266147744cbe53f978694a9d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33656124"
---
# <a name="-removeintchecks"></a><span data-ttu-id="5f1c8-102">-removeintchecks</span><span class="sxs-lookup"><span data-stu-id="5f1c8-102">-removeintchecks</span></span>
<span data-ttu-id="5f1c8-103">Active la vérification des opérations sur les entiers ou désactivez les erreurs de dépassement.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-103">Turns overflow-error checking for integer operations on or off.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f1c8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f1c8-104">Syntax</span></span>  
  
```  
-removeintchecks[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="5f1c8-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="5f1c8-105">Arguments</span></span>  
  
|<span data-ttu-id="5f1c8-106">Terme</span><span class="sxs-lookup"><span data-stu-id="5f1c8-106">Term</span></span>|<span data-ttu-id="5f1c8-107">Définition</span><span class="sxs-lookup"><span data-stu-id="5f1c8-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="5f1c8-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="5f1c8-108">`+` &#124; `-`</span></span>|<span data-ttu-id="5f1c8-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-109">Optional.</span></span> <span data-ttu-id="5f1c8-110">La `-removeintchecks-` option, le compilateur à vérifier tous les calculs d’entier pour les erreurs de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-110">The `-removeintchecks-` option causes the compiler to check all integer calculations for overflow errors.</span></span> <span data-ttu-id="5f1c8-111">La valeur par défaut est `-removeintchecks-`.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-111">The default is `-removeintchecks-`.</span></span><br /><br /> <span data-ttu-id="5f1c8-112">Spécification de `-removeintchecks` ou `-removeintchecks+` empêche la vérification des erreurs et peuvent effectuer des calculs d’entier plus rapides.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-112">Specifying `-removeintchecks` or `-removeintchecks+` prevents error checking and can make integer calculations faster.</span></span> <span data-ttu-id="5f1c8-113">Toutefois, sans vérification des erreurs, et si les capacités de type données sont dépassées, des résultats incorrects peuvent être stockées sans déclencher d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-113">However, without error checking, and if data type capacities are overflowed, incorrect results may be stored without raising an error.</span></span>|  
  
|<span data-ttu-id="5f1c8-114">Pour définir des - removeintchecks dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5f1c8-114">To set -removeintchecks in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="5f1c8-115">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-115">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="5f1c8-116">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-116">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="5f1c8-117">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-117">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="5f1c8-118">3.  Cliquez sur le bouton **Avancées** .</span><span class="sxs-lookup"><span data-stu-id="5f1c8-118">3.  Click the **Advanced** button.</span></span><br /><span data-ttu-id="5f1c8-119">4.  Modifier la valeur de la **supprimer les contrôles de dépassement de capacité d’entier** boîte.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-119">4.  Modify the value of the **Remove integer overflow checks** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="5f1c8-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f1c8-120">Example</span></span>  
 <span data-ttu-id="5f1c8-121">Le code suivant compile `Test.vb` et désactive la vérification des erreurs de dépassement de capacité d’entier.</span><span class="sxs-lookup"><span data-stu-id="5f1c8-121">The following code compiles `Test.vb` and turns off integer overflow-error checking.</span></span>  
  
```console
vbc -removeintchecks+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="5f1c8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f1c8-122">See Also</span></span>  
 [<span data-ttu-id="5f1c8-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5f1c8-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="5f1c8-124">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="5f1c8-124">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
