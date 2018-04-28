---
title: Ciblage de .NET Framework 2.0 sur Windows 8
description: 'En savoir plus sur le ciblage d’une version antérieure du .NET Framework lors de l’utilisation de F #.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 7c9bd8087da94a476105729b6f5b050fc66629a2
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="targeting-older-versions-of-net"></a><span data-ttu-id="a02e7-103">Ciblage des anciennes versions de .NET</span><span class="sxs-lookup"><span data-stu-id="a02e7-103">Targeting Older Versions of .NET</span></span>

> [!NOTE]
<span data-ttu-id="a02e7-104">Cet article n’est pas à jour avec la dernière version de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a02e7-104">This article is not up to date with the latest Visual Studio.</span></span>  <span data-ttu-id="a02e7-105">Il sera mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a02e7-105">It will be updated.</span></span>

<span data-ttu-id="a02e7-106">L’erreur suivante peut s’afficher si vous tentez de cibler le .NET Framework 2.0, 3.0 ou 3.5 en F # de projet Visual Studio est installé sur Windows 8.1 :</span><span class="sxs-lookup"><span data-stu-id="a02e7-106">The following error might appear if you try to target the .NET Framework 2.0, 3.0, or 3.5 in an F# project when Visual Studio is installed on Windows 8.1:</span></span> 

```
This project requires the 2.0 F# runtime, but that runtime is not installed.
```

<span data-ttu-id="a02e7-107">Cette erreur est connue pour se produire dans la combinaison de conditions suivante :</span><span class="sxs-lookup"><span data-stu-id="a02e7-107">This error is known to occur under the following combination of conditions:</span></span>


- <span data-ttu-id="a02e7-108">Vous avez installé Visual Studio sur Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a02e7-108">You installed Visual Studio on Windows 8.1.</span></span>
<br />

- <span data-ttu-id="a02e7-109">Vous n’avez pas activé le .NET Framework 3.5 avant d’installer Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a02e7-109">You didn’t enable the .NET Framework 3.5 before you installed Visual Studio.</span></span>
<br />

- <span data-ttu-id="a02e7-110">Votre projet cible le .NET Framework 2.0, 3.0 ou 3.5.</span><span class="sxs-lookup"><span data-stu-id="a02e7-110">Your project targets the .NET Framework 2.0, 3.0, or 3.5.</span></span>
<br />

<span data-ttu-id="a02e7-111">Lorsque vous installez Visual Studio, il détecte les versions installées de .NET Framework et installe le Runtime F # 2.0 uniquement si le .NET Framework 3.5 est installé et activé.</span><span class="sxs-lookup"><span data-stu-id="a02e7-111">When you install Visual Studio, it detects the installed versions of the .NET Framework and installs the F# 2.0 Runtime only if the .NET Framework 3.5 is installed and enabled.</span></span>


## <a name="resolving-the-error"></a><span data-ttu-id="a02e7-112">Résoudre l’erreur</span><span class="sxs-lookup"><span data-stu-id="a02e7-112">Resolving the Error</span></span>
<span data-ttu-id="a02e7-113">Pour résoudre cette erreur, vous pouvez soit une version plus récente du .NET Framework cible, ou vous pouvez activer le .NET Framework 3.5 sur Windows 8.1 et puis installez le runtime F # 2.0 en exécutant le programme d’installation de Visual Studio avec le **réparation** option.</span><span class="sxs-lookup"><span data-stu-id="a02e7-113">To resolve this error, you can either target a newer version of the .NET Framework, or you can enable the .NET Framework 3.5 on Windows 8.1 and then install the F# 2.0 runtime by running the setup program for Visual Studio with the **Repair** option.</span></span>


#### <a name="to-enable-the-net-framework-35-on-windows-81"></a><span data-ttu-id="a02e7-114">Pour activer le .NET Framework 3.5 sur Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a02e7-114">To enable the .NET Framework 3.5 on Windows 8.1</span></span>

1. <span data-ttu-id="a02e7-115">Sur le **Démarrer** écran, commencez à entrer **le panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="a02e7-115">On the **Start** screen, start to enter **Control Panel**.</span></span>
<br />  <span data-ttu-id="a02e7-116">Lorsque vous entrez ce nom, le **le panneau de configuration** icône s’affiche sous le **applications** titre.</span><span class="sxs-lookup"><span data-stu-id="a02e7-116">As you enter that name, the **Control Panel** icon appears under the **Apps** heading.</span></span>
<br />

2. <span data-ttu-id="a02e7-117">Choisissez le **le panneau de configuration** icône, choisissez le **programmes** icône, puis choisissez le **ou désactiver des fonctionnalités Windows d’activer** lien.</span><span class="sxs-lookup"><span data-stu-id="a02e7-117">Choose the **Control Panel** icon, choose the **Programs** icon, and then choose the **Turn Windows features on or off** link.</span></span>
<br />

3. <span data-ttu-id="a02e7-118">Assurez-vous que le **.NET Framework 3.5 (inclut .NET 2.0 et 3.0)** case à cocher est sélectionnée, puis choisissez le **OK** bouton.</span><span class="sxs-lookup"><span data-stu-id="a02e7-118">Make sure that the **.NET Framework 3.5 (includes .NET 2.0 and 3.0)** check box is selected, and then choose the **OK** button.</span></span>
<br />  <span data-ttu-id="a02e7-119">Vous n’avez pas besoin de sélectionner les cases à cocher pour tous les nœuds enfants pour les composants facultatifs du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a02e7-119">You don’t need to select the check boxes for any child nodes for optional components of the .NET Framework.</span></span>
<br />  <span data-ttu-id="a02e7-120">Le .NET Framework 3.5 est activée si elle n’était pas déjà.</span><span class="sxs-lookup"><span data-stu-id="a02e7-120">The .NET Framework 3.5 is enabled if it wasn't already.</span></span>
<br />


#### <a name="to-install-the-f-20-runtime"></a><span data-ttu-id="a02e7-121">Pour installer le runtime F # 2.0</span><span class="sxs-lookup"><span data-stu-id="a02e7-121">To install the F# 2.0 runtime</span></span>

1. <span data-ttu-id="a02e7-122">Dans le panneau de configuration, choisissez la **programmes** lier, puis choisissez le **programmes et fonctionnalités** lien.</span><span class="sxs-lookup"><span data-stu-id="a02e7-122">In the Control Panel, choose the **Programs** link, and then choose the **Programs and Features** link.</span></span>
<br />

2. <span data-ttu-id="a02e7-123">Dans la liste des programmes installés, sélectionnez l’édition de Visual Studio que vous avez installé, puis choisissez le **modification** bouton.</span><span class="sxs-lookup"><span data-stu-id="a02e7-123">In the list of installed programs, choose the edition of Visual Studio that you installed, and then choose the **Change** button.</span></span>
<br />

3. <span data-ttu-id="a02e7-124">Une fois que le programme d’installation démarre, choisissez le **réparation** bouton.</span><span class="sxs-lookup"><span data-stu-id="a02e7-124">After setup starts, choose the **Repair** button.</span></span>
<br />  <span data-ttu-id="a02e7-125">Pour plus d’informations, consultez [installation de Visual Studio](https://msdn.microsoft.com/library/e2h7fzkw.aspx).</span><span class="sxs-lookup"><span data-stu-id="a02e7-125">For more information, see [Installing Visual Studio](https://msdn.microsoft.com/library/e2h7fzkw.aspx).</span></span>
<br />
## <a name="see-also"></a><span data-ttu-id="a02e7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a02e7-126">See Also</span></span>
[<span data-ttu-id="a02e7-127">Visual F#</span><span class="sxs-lookup"><span data-stu-id="a02e7-127">Visual F#</span></span>](../index.md)
