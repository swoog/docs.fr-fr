---
title: -nowarn
ms.date: 07/20/2015
helpviewer_keywords:
- nowarn compiler option [Visual Basic]
- /nowarn compiler option [Visual Basic]
- -nowarn compiler option [Visual Basic]
ms.assetid: 7ebf2106-0652-4fdc-bf60-70fc86465d83
ms.openlocfilehash: 338b4672d215968275c30d37a2f8061e764aed8e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653440"
---
# <a name="-nowarn"></a><span data-ttu-id="82a2b-102">-nowarn</span><span class="sxs-lookup"><span data-stu-id="82a2b-102">-nowarn</span></span>
<span data-ttu-id="82a2b-103">Supprime la capacité du compilateur à générer des avertissements.</span><span class="sxs-lookup"><span data-stu-id="82a2b-103">Suppresses the compiler's ability to generate warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82a2b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82a2b-104">Syntax</span></span>  
  
```  
-nowarn[:numberList]  
```  
  
## <a name="arguments"></a><span data-ttu-id="82a2b-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="82a2b-105">Arguments</span></span>  
  
|<span data-ttu-id="82a2b-106">Terme</span><span class="sxs-lookup"><span data-stu-id="82a2b-106">Term</span></span>|<span data-ttu-id="82a2b-107">Définition</span><span class="sxs-lookup"><span data-stu-id="82a2b-107">Definition</span></span>|  
|---|---|  
|`numberList`|<span data-ttu-id="82a2b-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="82a2b-108">Optional.</span></span> <span data-ttu-id="82a2b-109">Liste délimitée les ID des numéros d’avertissement que le compilateur doit supprimer.</span><span class="sxs-lookup"><span data-stu-id="82a2b-109">Comma-delimited list of the warning ID numbers that the compiler should suppress.</span></span> <span data-ttu-id="82a2b-110">Si l’ID d’avertissement ne sont pas spécifié, tous les avertissements sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="82a2b-110">If the warning IDs are not specified, all warnings are suppressed.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="82a2b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="82a2b-111">Remarks</span></span>  
 <span data-ttu-id="82a2b-112">La `-nowarn` option, le compilateur ne génère ne pas les avertissements.</span><span class="sxs-lookup"><span data-stu-id="82a2b-112">The `-nowarn` option causes the compiler to not generate warnings.</span></span> <span data-ttu-id="82a2b-113">Pour supprimer un avertissement, fournissez l’ID d’avertissement pour le `-nowarn` option suit le signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="82a2b-113">To suppress an individual warning, supply the warning ID to the `-nowarn` option following the colon.</span></span> <span data-ttu-id="82a2b-114">Séparez plusieurs numéros d’avertissement par des virgules.</span><span class="sxs-lookup"><span data-stu-id="82a2b-114">Separate multiple warning numbers with commas.</span></span>  
  
 <span data-ttu-id="82a2b-115">Vous devez spécifier uniquement la partie numérique de l’identificateur d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="82a2b-115">You need to specify only the numeric part of the warning identifier.</span></span> <span data-ttu-id="82a2b-116">Par exemple, si vous souhaitez supprimer BC42024, numéro d’avertissement pour les variables locales inutilisées, spécifiez `-nowarn:42024`.</span><span class="sxs-lookup"><span data-stu-id="82a2b-116">For example, if you want to suppress BC42024, the warning for unused local variables, specify `-nowarn:42024`.</span></span>  
  
 <span data-ttu-id="82a2b-117">Pour plus d’informations sur les numéros d’avertissement, consultez [configuration des avertissements en Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="82a2b-117">For more information on the warning ID numbers, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
|<span data-ttu-id="82a2b-118">Pour définir /nowarn - dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82a2b-118">To set -nowarn in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="82a2b-119">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="82a2b-119">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="82a2b-120">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="82a2b-120">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="82a2b-121">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="82a2b-121">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="82a2b-122">3.  Sélectionnez le **désactiver tous les avertissements** case à cocher pour désactiver tous les avertissements.</span><span class="sxs-lookup"><span data-stu-id="82a2b-122">3.  Select the **Disable all warnings** check box to disable all warnings.</span></span><br />     <span data-ttu-id="82a2b-123">ou</span><span class="sxs-lookup"><span data-stu-id="82a2b-123">- or -</span></span><br />     <span data-ttu-id="82a2b-124">Pour désactiver un avertissement particulier, cliquez sur **aucun** dans la liste déroulante adjacente à l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="82a2b-124">To disable a particular warning, click **None** from the drop-down list adjacent to the warning.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="82a2b-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="82a2b-125">Example</span></span>  
 <span data-ttu-id="82a2b-126">Le code suivant compile `T2.vb` et n’affiche pas les avertissements.</span><span class="sxs-lookup"><span data-stu-id="82a2b-126">The following code compiles `T2.vb` and does not display any warnings.</span></span>  
  
```console
vbc -nowarn t2.vb  
```  
  
## <a name="example"></a><span data-ttu-id="82a2b-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="82a2b-127">Example</span></span>  
 <span data-ttu-id="82a2b-128">Le code suivant compile `T2.vb` et n’affiche pas les avertissements pour les variables locales inutilisées (42024).</span><span class="sxs-lookup"><span data-stu-id="82a2b-128">The following code compiles `T2.vb` and does not display the warnings for unused local variables (42024).</span></span>  
  
```console
vbc -nowarn:42024 t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="82a2b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82a2b-129">See Also</span></span>  
 [<span data-ttu-id="82a2b-130">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="82a2b-130">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="82a2b-131">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="82a2b-131">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="82a2b-132">Configuration d’avertissements en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="82a2b-132">Configuring Warnings in Visual Basic</span></span>](/visualstudio/ide/configuring-warnings-in-visual-basic)
