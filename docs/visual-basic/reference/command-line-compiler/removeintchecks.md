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
ms.openlocfilehash: f061497083dc23fd07f61108938a4129c0af5f3a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188526"
---
# <a name="-removeintchecks"></a><span data-ttu-id="ad43d-102">-removeintchecks</span><span class="sxs-lookup"><span data-stu-id="ad43d-102">-removeintchecks</span></span>
<span data-ttu-id="ad43d-103">Active le dépassement de capacité de la vérification des erreurs pour les opérations sur les entiers ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="ad43d-103">Turns overflow-error checking for integer operations on or off.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad43d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad43d-104">Syntax</span></span>  
  
```  
-removeintchecks[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="ad43d-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="ad43d-105">Arguments</span></span>  
  
|<span data-ttu-id="ad43d-106">Terme</span><span class="sxs-lookup"><span data-stu-id="ad43d-106">Term</span></span>|<span data-ttu-id="ad43d-107">Définition</span><span class="sxs-lookup"><span data-stu-id="ad43d-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="ad43d-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="ad43d-108">`+` &#124; `-`</span></span>|<span data-ttu-id="ad43d-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="ad43d-109">Optional.</span></span> <span data-ttu-id="ad43d-110">Le `-removeintchecks-` option indique au compilateur de vérifier tous les calculs d’entier pour les erreurs de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="ad43d-110">The `-removeintchecks-` option causes the compiler to check all integer calculations for overflow errors.</span></span> <span data-ttu-id="ad43d-111">La valeur par défaut est `-removeintchecks-`.</span><span class="sxs-lookup"><span data-stu-id="ad43d-111">The default is `-removeintchecks-`.</span></span><br /><br /> <span data-ttu-id="ad43d-112">Spécification `-removeintchecks` ou `-removeintchecks+` empêche la vérification des erreurs et peuvent effectuer des calculs d’entier plus rapides.</span><span class="sxs-lookup"><span data-stu-id="ad43d-112">Specifying `-removeintchecks` or `-removeintchecks+` prevents error checking and can make integer calculations faster.</span></span> <span data-ttu-id="ad43d-113">Toutefois, sans vérification des erreurs, et si les capacités de type de données sont dépassées, des résultats incorrects peuvent être stockés sans déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="ad43d-113">However, without error checking, and if data type capacities are overflowed, incorrect results may be stored without raising an error.</span></span>|  
  
|<span data-ttu-id="ad43d-114">Pour définir - removeintchecks dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad43d-114">To set -removeintchecks in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="ad43d-115">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="ad43d-115">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="ad43d-116">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ad43d-116">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="ad43d-117">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="ad43d-117">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="ad43d-118">3.  Cliquez sur le bouton **Avancées** .</span><span class="sxs-lookup"><span data-stu-id="ad43d-118">3.  Click the **Advanced** button.</span></span><br /><span data-ttu-id="ad43d-119">4.  Modifier la valeur de la **supprimer les contrôles de dépassement de capacité d’entier** boîte.</span><span class="sxs-lookup"><span data-stu-id="ad43d-119">4.  Modify the value of the **Remove integer overflow checks** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ad43d-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad43d-120">Example</span></span>  
 <span data-ttu-id="ad43d-121">Le code suivant compile `Test.vb` et désactive la vérification des erreurs de dépassement de capacité d’entier.</span><span class="sxs-lookup"><span data-stu-id="ad43d-121">The following code compiles `Test.vb` and turns off integer overflow-error checking.</span></span>  
  
```console
vbc -removeintchecks+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="ad43d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad43d-122">See Also</span></span>  
 [<span data-ttu-id="ad43d-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ad43d-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="ad43d-124">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="ad43d-124">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
