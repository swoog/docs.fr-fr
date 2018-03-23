---
title: -warnaserror (Visual Basic)
ms.date: 03/13/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- warnaserror compiler option [Visual Basic]
- /warnaserror compiler option [Visual Basic]
- -warnaserror compiler option [Visual Basic]
ms.assetid: 49819f1d-a1bd-4201-affe-5afe6d9712e1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ae8ed68045529e626f2788f854d8e6a6933e7e2
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-warnaserror-visual-basic"></a><span data-ttu-id="8428e-102">-warnaserror (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8428e-102">-warnaserror (Visual Basic)</span></span>
<span data-ttu-id="8428e-103">Indique au compilateur de traiter la première occurrence d’un avertissement comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="8428e-103">Causes the compiler to treat the first occurrence of a warning as an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8428e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8428e-104">Syntax</span></span>  
  
```  
-warnaserror[+ | -][:numberList]  
```  
  
## <a name="arguments"></a><span data-ttu-id="8428e-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="8428e-105">Arguments</span></span>  
  
|<span data-ttu-id="8428e-106">Terme</span><span class="sxs-lookup"><span data-stu-id="8428e-106">Term</span></span>|<span data-ttu-id="8428e-107">Définition</span><span class="sxs-lookup"><span data-stu-id="8428e-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="8428e-108">+ &#124; -</span><span class="sxs-lookup"><span data-stu-id="8428e-108">+ &#124; -</span></span>|<span data-ttu-id="8428e-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8428e-109">Optional.</span></span> <span data-ttu-id="8428e-110">Par défaut, `-warnaserror-` est en vigueur ; les avertissements n’empêchent pas le compilateur de générer un fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="8428e-110">By default, `-warnaserror-` is in effect; warnings do not prevent the compiler from producing an output file.</span></span> <span data-ttu-id="8428e-111">Le `-warnaserror` option, qui est le même que `-warnaserror+`, génère des avertissements à traiter comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8428e-111">The `-warnaserror` option, which is the same as `-warnaserror+`, causes warnings to be treated as errors.</span></span>|  
|`numberList`|<span data-ttu-id="8428e-112">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8428e-112">Optional.</span></span> <span data-ttu-id="8428e-113">Liste délimitée par des virgules l’ID d’avertissement numéros à laquelle le `-warnaserror` option s’applique.</span><span class="sxs-lookup"><span data-stu-id="8428e-113">Comma-delimited list of the warning ID numbers to which the `-warnaserror` option applies.</span></span> <span data-ttu-id="8428e-114">Si aucun ID d’avertissement n’est spécifié, le `-warnaserror` option s’applique à tous les avertissements.</span><span class="sxs-lookup"><span data-stu-id="8428e-114">If no warning ID is specified, the `-warnaserror` option applies to all warnings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8428e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8428e-115">Remarks</span></span>  
 <span data-ttu-id="8428e-116">Le `-warnaserror` option traite tous les avertissements comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8428e-116">The `-warnaserror` option treats all warnings as errors.</span></span> <span data-ttu-id="8428e-117">Les messages qui seraient normalement signalés comme avertissements apparaissent comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8428e-117">Any messages that would ordinarily be reported as warnings are instead reported as errors.</span></span> <span data-ttu-id="8428e-118">Le compilateur signale les autres occurrences du même avertissement en tant qu’avertissements.</span><span class="sxs-lookup"><span data-stu-id="8428e-118">The compiler reports subsequent occurrences of the same warning as warnings.</span></span>  
  
 <span data-ttu-id="8428e-119">Par défaut, `-warnaserror-` est en vigueur, ce qui provoque les avertissements d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="8428e-119">By default, `-warnaserror-` is in effect, which causes the warnings to be informational only.</span></span> <span data-ttu-id="8428e-120">Le `-warnaserror` option, qui est le même que `-warnaserror+`, génère des avertissements à traiter comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8428e-120">The `-warnaserror` option, which is the same as `-warnaserror+`, causes warnings to be treated as errors.</span></span>  
  
 <span data-ttu-id="8428e-121">Si vous souhaitez que seuls certains avertissements spécifiques à traiter comme des erreurs, vous pouvez spécifier une liste séparée par des virgules des numéros d’avertissement à traiter comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8428e-121">If you want only a few specific warnings to be treated as errors, you may specify a comma-separated list of warning numbers to treat as errors.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8428e-122">Le `-warnaserror` option ne contrôle pas l’affichage des avertissements.</span><span class="sxs-lookup"><span data-stu-id="8428e-122">The `-warnaserror` option does not control how warnings are displayed.</span></span> <span data-ttu-id="8428e-123">Utilisez le [- nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) option pour désactiver les avertissements.</span><span class="sxs-lookup"><span data-stu-id="8428e-123">Use the [-nowarn](../../../visual-basic/reference/command-line-compiler/nowarn.md) option to disable warnings.</span></span>  
  
|<span data-ttu-id="8428e-124">Pour définir /warnaserror - pour traiter tous les avertissements comme des erreurs dans l’IDE de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8428e-124">To set -warnaserror to treat all warnings as errors in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="8428e-125">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="8428e-125">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="8428e-126">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8428e-126">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="8428e-127">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="8428e-127">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="8428e-128">3.  Assurez-vous que le **désactiver tous les avertissements** case à cocher est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8428e-128">3.  Make sure the **Disable all warnings** check box is unchecked.</span></span><br /><span data-ttu-id="8428e-129">4.  Vérifiez le **traiter tous les avertissements comme des erreurs** case à cocher.</span><span class="sxs-lookup"><span data-stu-id="8428e-129">4.  Check the **Treat all warnings as errors** check box.</span></span>|  
  
|<span data-ttu-id="8428e-130">Pour définir /warnaserror - pour traiter certains avertissements comme des erreurs dans l’IDE de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8428e-130">To set -warnaserror to treat specific warnings as errors in the Visual Studio IDE</span></span>|  
|---|  
|<span data-ttu-id="8428e-131">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="8428e-131">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="8428e-132">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8428e-132">On the **Project** menu, click **Properties**.</span></span><br /><span data-ttu-id="8428e-133">2.  Cliquez sur l’onglet **Compiler**.</span><span class="sxs-lookup"><span data-stu-id="8428e-133">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="8428e-134">3.  Assurez-vous que le **désactiver tous les avertissements** case à cocher est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8428e-134">3.  Make sure the **Disable all warnings** check box is unchecked.</span></span><br /><span data-ttu-id="8428e-135">4.  Assurez-vous que le **traiter tous les avertissements comme des erreurs** case à cocher est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8428e-135">4.  Make sure the **Treat all warnings as errors** check box is unchecked.</span></span><br /><span data-ttu-id="8428e-136">5.  Sélectionnez **erreur** à partir de la **Notification** colonne adjacente à l’avertissement qui doit être traitée comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="8428e-136">5.  Select **Error** from the **Notification** column adjacent to the warning that should be treated as an error.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="8428e-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="8428e-137">Example</span></span>  
 <span data-ttu-id="8428e-138">Le code suivant compile `In.vb` et indique au compilateur d’afficher une erreur pour la première occurrence de chaque avertissement rencontré.</span><span class="sxs-lookup"><span data-stu-id="8428e-138">The following code compiles `In.vb` and directs the compiler to display an error for the first occurrence of every warning it finds.</span></span>  
  
```console
vbc -warnaserror in.vb  
```  
  
## <a name="example"></a><span data-ttu-id="8428e-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="8428e-139">Example</span></span>  
 <span data-ttu-id="8428e-140">Le code suivant compile `T2.vb` et traite uniquement l’avertissement pour les variables locales inutilisées (42024) comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="8428e-140">The following code compiles `T2.vb` and treats only the warning for unused local variables (42024) as an error.</span></span>  
  
```console
vbc -warnaserror:42024 t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="8428e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8428e-141">See Also</span></span>  
 [<span data-ttu-id="8428e-142">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8428e-142">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="8428e-143">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="8428e-143">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="8428e-144">Configuration d’avertissements en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8428e-144">Configuring Warnings in Visual Basic</span></span>](/visualstudio/ide/configuring-warnings-in-visual-basic)
