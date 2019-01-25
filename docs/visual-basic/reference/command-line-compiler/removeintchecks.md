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
ms.openlocfilehash: 4c1be34cf76cfb12ea1e3b3246e9e0bc26199c24
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687958"
---
# <a name="-removeintchecks"></a><span data-ttu-id="3d783-102">-removeintchecks</span><span class="sxs-lookup"><span data-stu-id="3d783-102">-removeintchecks</span></span>
<span data-ttu-id="3d783-103">Active le dépassement de capacité de la vérification des erreurs pour les opérations sur les entiers ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="3d783-103">Turns overflow-error checking for integer operations on or off.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d783-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d783-104">Syntax</span></span>  
  
```  
-removeintchecks[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="3d783-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="3d783-105">Arguments</span></span>  
  
|<span data-ttu-id="3d783-106">Terme</span><span class="sxs-lookup"><span data-stu-id="3d783-106">Term</span></span>|<span data-ttu-id="3d783-107">Définition</span><span class="sxs-lookup"><span data-stu-id="3d783-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="3d783-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="3d783-108">`+` &#124; `-`</span></span>|<span data-ttu-id="3d783-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="3d783-109">Optional.</span></span> <span data-ttu-id="3d783-110">Le `-removeintchecks-` option indique au compilateur de vérifier tous les calculs d’entier pour les erreurs de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="3d783-110">The `-removeintchecks-` option causes the compiler to check all integer calculations for overflow errors.</span></span> <span data-ttu-id="3d783-111">La valeur par défaut est `-removeintchecks-`.</span><span class="sxs-lookup"><span data-stu-id="3d783-111">The default is `-removeintchecks-`.</span></span><br /><br /> <span data-ttu-id="3d783-112">Spécification `-removeintchecks` ou `-removeintchecks+` empêche la vérification des erreurs et peuvent effectuer des calculs d’entier plus rapides.</span><span class="sxs-lookup"><span data-stu-id="3d783-112">Specifying `-removeintchecks` or `-removeintchecks+` prevents error checking and can make integer calculations faster.</span></span> <span data-ttu-id="3d783-113">Toutefois, sans vérification des erreurs, et si les capacités de type de données sont dépassées, des résultats incorrects peuvent être stockés sans déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="3d783-113">However, without error checking, and if data type capacities are overflowed, incorrect results may be stored without raising an error.</span></span>|  
  
|<span data-ttu-id="3d783-114">Pour définir - removeintchecks dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d783-114">To set -removeintchecks in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="3d783-115">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="3d783-115">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="3d783-116">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3d783-116">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="3d783-117">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="3d783-117">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="3d783-118">3.  Cliquez sur le bouton **Avancées** .</span><span class="sxs-lookup"><span data-stu-id="3d783-118">3.  Click the **Advanced** button.</span></span><br /><span data-ttu-id="3d783-119">4.  Modifier la valeur de la **supprimer les contrôles de dépassement de capacité d’entier** boîte.</span><span class="sxs-lookup"><span data-stu-id="3d783-119">4.  Modify the value of the **Remove integer overflow checks** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="3d783-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="3d783-120">Example</span></span>  
 <span data-ttu-id="3d783-121">Le code suivant compile `Test.vb` et désactive la vérification des erreurs de dépassement de capacité d’entier.</span><span class="sxs-lookup"><span data-stu-id="3d783-121">The following code compiles `Test.vb` and turns off integer overflow-error checking.</span></span>  
  
```console
vbc -removeintchecks+ test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="3d783-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d783-122">See also</span></span>
- [<span data-ttu-id="3d783-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3d783-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="3d783-124">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="3d783-124">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
