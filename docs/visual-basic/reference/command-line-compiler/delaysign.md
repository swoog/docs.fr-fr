---
title: -delaysign
ms.date: 03/10/2018
helpviewer_keywords:
- delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
ms.assetid: c76e61a4-1884-4252-9fb2-377f99caa690
ms.openlocfilehash: 1a784dc57331ed4cbaeb8524dbb3b6ea9a06eca1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605589"
---
# <a name="-delaysign"></a><span data-ttu-id="5a68c-102">-delaysign</span><span class="sxs-lookup"><span data-stu-id="5a68c-102">-delaysign</span></span>
<span data-ttu-id="5a68c-103">Spécifie si l'assembly sera complètement ou partiellement signé.</span><span class="sxs-lookup"><span data-stu-id="5a68c-103">Specifies whether the assembly will be fully or partially signed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5a68c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a68c-104">Syntax</span></span>  
  
```  
-delaysign[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="5a68c-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="5a68c-105">Arguments</span></span>  
 <span data-ttu-id="5a68c-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="5a68c-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="5a68c-107">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5a68c-107">Optional.</span></span> <span data-ttu-id="5a68c-108">Utilisez `-delaysign-` si vous souhaitez obtenir un assembly complètement signé.</span><span class="sxs-lookup"><span data-stu-id="5a68c-108">Use `-delaysign-` if you want a fully signed assembly.</span></span> <span data-ttu-id="5a68c-109">Utilisez `-delaysign+` si vous souhaitez placer la clé publique dans l’espace d’assembly et réserve pour le hachage signé.</span><span class="sxs-lookup"><span data-stu-id="5a68c-109">Use `-delaysign+` if you want to place the public key in the assembly and reserve space for the signed hash.</span></span> <span data-ttu-id="5a68c-110">La valeur par défaut est `-delaysign-`.</span><span class="sxs-lookup"><span data-stu-id="5a68c-110">The default is `-delaysign-`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5a68c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5a68c-111">Remarks</span></span>  
 <span data-ttu-id="5a68c-112">Le `-delaysign` option est sans effet sauf si utilisée avec [- keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md) ou [- keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5a68c-112">The `-delaysign` option has no effect unless used with [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md) or [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md).</span></span>  
  
 <span data-ttu-id="5a68c-113">Quand vous demandez un assembly totalement signé, le compilateur hache le fichier qui contient le manifeste (métadonnées de l’assembly) et signe ce hachage avec la clé privée.</span><span class="sxs-lookup"><span data-stu-id="5a68c-113">When you request a fully signed assembly, the compiler hashes the file that contains the manifest (assembly metadata) and signs that hash with the private key.</span></span> <span data-ttu-id="5a68c-114">La signature numérique obtenue est stockée dans le fichier qui contient le manifeste.</span><span class="sxs-lookup"><span data-stu-id="5a68c-114">The resulting digital signature is stored in the file that contains the manifest.</span></span> <span data-ttu-id="5a68c-115">Lorsqu’un assembly est à signature différée, le compilateur ne calcule pas et stocker l’espace de signature mais les réserves de ressources dans le fichier pour la signature puisse être ajoutée plus tard.</span><span class="sxs-lookup"><span data-stu-id="5a68c-115">When an assembly is delay signed, the compiler does not compute and store the signature but reserves space in the file so the signature can be added later.</span></span>  
  
 <span data-ttu-id="5a68c-116">Par exemple, en utilisant `-delaysign+`, un développeur d’une organisation peut distribuer des versions de test non signé d’un assembly qui les testeurs peuvent enregistrer dans le global assembly cache et utiliser.</span><span class="sxs-lookup"><span data-stu-id="5a68c-116">For example, by using `-delaysign+`, a developer in an organization can distribute unsigned test versions of an assembly that testers can register with the global assembly cache and use.</span></span> <span data-ttu-id="5a68c-117">Lorsque le travail sur l’assembly est terminé, la personne responsable de la clé privée de l’organisation peut signer complètement l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5a68c-117">When work on the assembly is completed, the person responsible for the organization's private key can fully sign the assembly.</span></span> <span data-ttu-id="5a68c-118">Ce compartimentage protège la clé privée de l’organisation contre toute divulgation, tout en autorisant tous les développeurs de travailler sur les assemblys.</span><span class="sxs-lookup"><span data-stu-id="5a68c-118">This compartmentalization protects the organization's private key from disclosure, while allowing all developers to work on the assemblies.</span></span>  
  
 <span data-ttu-id="5a68c-119">Consultez [création et assemblys avec nom fort](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) pour plus d’informations sur la signature d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="5a68c-119">See [Creating and Using Strong-Named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) for more information on signing an assembly.</span></span>  
  
### <a name="to-set--delaysign-in-the-visual-studio-integrated-development-environment"></a><span data-ttu-id="5a68c-120">Pour définir delaysign - dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5a68c-120">To set -delaysign in the Visual Studio integrated development environment</span></span>  
  
1.  <span data-ttu-id="5a68c-121">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="5a68c-121">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="5a68c-122">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5a68c-122">On the **Project** menu, click **Properties**.</span></span>   
  
2.  <span data-ttu-id="5a68c-123">Cliquez sur l’onglet **Signature**.</span><span class="sxs-lookup"><span data-stu-id="5a68c-123">Click the **Signing** tab.</span></span>  
  
3.  <span data-ttu-id="5a68c-124">Définissez la valeur dans le **différer la signature uniquement** boîte.</span><span class="sxs-lookup"><span data-stu-id="5a68c-124">Set the value in the **Delay sign only** box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a68c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a68c-125">See also</span></span>
- [<span data-ttu-id="5a68c-126">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5a68c-126">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="5a68c-127">-keyfile</span><span class="sxs-lookup"><span data-stu-id="5a68c-127">-keyfile</span></span>](../../../visual-basic/reference/command-line-compiler/keyfile.md)
- [<span data-ttu-id="5a68c-128">-keycontainer</span><span class="sxs-lookup"><span data-stu-id="5a68c-128">-keycontainer</span></span>](../../../visual-basic/reference/command-line-compiler/keycontainer.md)
- [<span data-ttu-id="5a68c-129">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="5a68c-129">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
