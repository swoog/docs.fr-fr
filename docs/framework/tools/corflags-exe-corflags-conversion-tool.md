---
title: CorFlags.exe (outil de conversion CorFlags)
ms.date: 03/30/2017
helpviewer_keywords:
- CorFlags conversion tool
- CorFlags.exe
- portable executable files, CorFlags section
ms.assetid: ef900f8f-71ca-4dde-9b8c-95ddb0d7d89c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 21b9881f1275c6a9343421131af478e11b826073
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222725"
---
# <a name="corflagsexe-corflags-conversion-tool"></a><span data-ttu-id="b0829-102">CorFlags.exe (outil de conversion CorFlags)</span><span class="sxs-lookup"><span data-stu-id="b0829-102">CorFlags.exe (CorFlags Conversion Tool)</span></span>
<span data-ttu-id="b0829-103">L’outil de conversion CorFlags vous permet de configurer la section CorFlags de l’en-tête d’une image exécutable portable.</span><span class="sxs-lookup"><span data-stu-id="b0829-103">The CorFlags Conversion tool allows you to configure the CorFlags section of the header of a portable executable image.</span></span>  
  
 <span data-ttu-id="b0829-104">Cet outil est installé automatiquement avec Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b0829-104">This tool is automatically installed with Visual Studio.</span></span> <span data-ttu-id="b0829-105">Pour exécuter l’outil, utilisez l’invite de commandes développeur pour Visual Studio (ou l’invite de commandes Visual Studio dans Windows 7).</span><span class="sxs-lookup"><span data-stu-id="b0829-105">To run the tool, use the Developer Command Prompt for Visual Studio (or the Visual Studio Command Prompt in Windows 7).</span></span> <span data-ttu-id="b0829-106">Pour plus d'informations, consultez [Invites de commandes](../../../docs/framework/tools/developer-command-prompt-for-vs.md).</span><span class="sxs-lookup"><span data-stu-id="b0829-106">For more information, see [Command Prompts](../../../docs/framework/tools/developer-command-prompt-for-vs.md).</span></span>  
  
 <span data-ttu-id="b0829-107">À l'invite de commandes, tapez le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="b0829-107">At the command prompt, type the following:</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0829-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0829-108">Syntax</span></span>  
  
```  
CorFlags.exe assembly [options]  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b0829-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0829-109">Parameters</span></span>  
  
|<span data-ttu-id="b0829-110">Paramètre requis</span><span class="sxs-lookup"><span data-stu-id="b0829-110">Required parameter</span></span>|<span data-ttu-id="b0829-111">Description</span><span class="sxs-lookup"><span data-stu-id="b0829-111">Description</span></span>|  
|------------------------|-----------------|  
|`assembly`|<span data-ttu-id="b0829-112">Nom de l'assembly pour lequel CorFlags doit être configuré.</span><span class="sxs-lookup"><span data-stu-id="b0829-112">The name of the assembly for which to configure the CorFlags.</span></span>|  
  
|<span data-ttu-id="b0829-113">Option</span><span class="sxs-lookup"><span data-stu-id="b0829-113">Option</span></span>|<span data-ttu-id="b0829-114">Description</span><span class="sxs-lookup"><span data-stu-id="b0829-114">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="b0829-115">**/32BIT[REQ]+**</span><span class="sxs-lookup"><span data-stu-id="b0829-115">**/32BIT[REQ]+**</span></span>|<span data-ttu-id="b0829-116">Définit l'indicateur 32BITREQUIRED.</span><span class="sxs-lookup"><span data-stu-id="b0829-116">Sets the 32BITREQUIRED flag.</span></span>|  
|<span data-ttu-id="b0829-117">**/32BIT[REQ]-**</span><span class="sxs-lookup"><span data-stu-id="b0829-117">**/32BIT[REQ]-**</span></span>|<span data-ttu-id="b0829-118">Efface l'indicateur 32BITREQUIRED.</span><span class="sxs-lookup"><span data-stu-id="b0829-118">Clears the 32BITREQUIRED flag.</span></span>|  
|<span data-ttu-id="b0829-119">**/32BITPREF+**</span><span class="sxs-lookup"><span data-stu-id="b0829-119">**/32BITPREF+**</span></span>|<span data-ttu-id="b0829-120">Définit l'indicateur 32BITPREFERRED.</span><span class="sxs-lookup"><span data-stu-id="b0829-120">Sets the 32BITPREFERRED flag.</span></span> <span data-ttu-id="b0829-121">L'application s'exécute comme un processus 32 bits même sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b0829-121">The app runs as a 32-bit process even on 64-bit platforms.</span></span> <span data-ttu-id="b0829-122">Affectez cet indicateur uniquement sur les fichiers EXE.</span><span class="sxs-lookup"><span data-stu-id="b0829-122">Set this flag only on EXE files.</span></span> <span data-ttu-id="b0829-123">Si l'indicateur est défini sur une DLL, la DLL ne charge pas dans les processus 64 bits, et une exception <xref:System.BadImageFormatException> est levée.</span><span class="sxs-lookup"><span data-stu-id="b0829-123">If the flag is set on a DLL, the DLL fails to load in 64-bit processes, and a <xref:System.BadImageFormatException> exception is thrown.</span></span> <span data-ttu-id="b0829-124">Un fichier EXE avec cet indicateur peut être chargé dans un processus 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b0829-124">An EXE file with this flag can be loaded into a 64-bit process.</span></span><br /><br /> <span data-ttu-id="b0829-125">Nouveau dans le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b0829-125">New in the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].</span></span>|  
|<span data-ttu-id="b0829-126">**/32BITPREF-**</span><span class="sxs-lookup"><span data-stu-id="b0829-126">**/32BITPREF-**</span></span>|<span data-ttu-id="b0829-127">Efface l'indicateur 32BITPREFERRED.</span><span class="sxs-lookup"><span data-stu-id="b0829-127">Clears the 32BITPREFERRED flag.</span></span><br /><br /> <span data-ttu-id="b0829-128">Nouveau dans le [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b0829-128">New in the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].</span></span>|  
|<span data-ttu-id="b0829-129">**/?**</span><span class="sxs-lookup"><span data-stu-id="b0829-129">**/?**</span></span>|<span data-ttu-id="b0829-130">Affiche la syntaxe et les options de commande de l'outil.</span><span class="sxs-lookup"><span data-stu-id="b0829-130">Displays command syntax and options for the tool.</span></span>|  
|<span data-ttu-id="b0829-131">**/Force**</span><span class="sxs-lookup"><span data-stu-id="b0829-131">**/Force**</span></span>|<span data-ttu-id="b0829-132">Force une mise à jour même si l'assembly est associé à un nom fort.</span><span class="sxs-lookup"><span data-stu-id="b0829-132">Forces an update even if the assembly is strong-named.</span></span> <span data-ttu-id="b0829-133">**Important :**  Si vous mettez à jour un assembly avec nom fort, vous devez le signer à nouveau avant d'exécuter son code.</span><span class="sxs-lookup"><span data-stu-id="b0829-133">**Important:**  If you update a strong-named assembly, you must sign it again before executing its code.</span></span>|  
|<span data-ttu-id="b0829-134">**/help**</span><span class="sxs-lookup"><span data-stu-id="b0829-134">**/help**</span></span>|<span data-ttu-id="b0829-135">Affiche la syntaxe et les options de commande de l'outil.</span><span class="sxs-lookup"><span data-stu-id="b0829-135">Displays command syntax and options for the tool.</span></span>|  
|<span data-ttu-id="b0829-136">**/ILONLY+**</span><span class="sxs-lookup"><span data-stu-id="b0829-136">**/ILONLY+**</span></span>|<span data-ttu-id="b0829-137">Définit l'indicateur ILONLY.</span><span class="sxs-lookup"><span data-stu-id="b0829-137">Sets the ILONLY flag.</span></span>|  
|<span data-ttu-id="b0829-138">**/ILONLY-**</span><span class="sxs-lookup"><span data-stu-id="b0829-138">**/ILONLY-**</span></span>|<span data-ttu-id="b0829-139">Efface l'indicateur ILONLY.</span><span class="sxs-lookup"><span data-stu-id="b0829-139">Clears the ILONLY flag.</span></span>|  
|<span data-ttu-id="b0829-140">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="b0829-140">**/nologo**</span></span>|<span data-ttu-id="b0829-141">Supprime l'affichage de la bannière de démarrage Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0829-141">Suppresses the Microsoft startup banner display.</span></span>|  
|<span data-ttu-id="b0829-142">**/RevertCLRHeader**</span><span class="sxs-lookup"><span data-stu-id="b0829-142">**/RevertCLRHeader**</span></span>|<span data-ttu-id="b0829-143">Rétablit l'en-tête du CLR à la version 2.0.</span><span class="sxs-lookup"><span data-stu-id="b0829-143">Reverts the CLR header version to 2.0.</span></span>|  
|<span data-ttu-id="b0829-144">**/UpgradeCLRHeader**</span><span class="sxs-lookup"><span data-stu-id="b0829-144">**/UpgradeCLRHeader**</span></span>|<span data-ttu-id="b0829-145">Met à niveau l'en-tête du CLR à la version 2.5.</span><span class="sxs-lookup"><span data-stu-id="b0829-145">Upgrades the CLR header version to 2.5.</span></span> <span data-ttu-id="b0829-146">**Remarque :**  Les assemblys doivent avoir la version 2.5 ou une version ultérieure de l'en-tête du CLR pour être exécutés en mode natif.</span><span class="sxs-lookup"><span data-stu-id="b0829-146">**Note:**  Assemblies must have a CLR header version of 2.5 or greater to run natively.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b0829-147">Notes</span><span class="sxs-lookup"><span data-stu-id="b0829-147">Remarks</span></span>  
 <span data-ttu-id="b0829-148">Si aucune option n'est spécifiée, l'outil de conversion CorFlags affiche les indicateurs pour l'assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="b0829-148">If no options are specified, the CorFlags Conversion tool displays the flags for the specified assembly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0829-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0829-149">See Also</span></span>  
 [<span data-ttu-id="b0829-150">Outils</span><span class="sxs-lookup"><span data-stu-id="b0829-150">Tools</span></span>](../../../docs/framework/tools/index.md)  
 [<span data-ttu-id="b0829-151">Applications 64 bits</span><span class="sxs-lookup"><span data-stu-id="b0829-151">64-bit Applications</span></span>](../../../docs/framework/64-bit-apps.md)  
 [<span data-ttu-id="b0829-152">Invites de commandes</span><span class="sxs-lookup"><span data-stu-id="b0829-152">Command Prompts</span></span>](../../../docs/framework/tools/developer-command-prompt-for-vs.md)
