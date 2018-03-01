---
title: "Comment : créer des tâches précalculées"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, creating pre-computed
ms.assetid: a73eafa2-1f49-4106-a19e-997186029b58
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 262aa626e9e426da94de0d2ad5f2ef04a5bbc5f3
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-create-pre-computed-tasks"></a><span data-ttu-id="5def8-102">Comment : créer des tâches précalculées</span><span class="sxs-lookup"><span data-stu-id="5def8-102">How to: Create Pre-Computed Tasks</span></span>
<span data-ttu-id="5def8-103">Ce document décrit comment utiliser la méthode <xref:System.Threading.Tasks.Task.FromResult%2A?displayProperty=nameWithType> pour récupérer les résultats d’opérations de téléchargement asynchrones qui sont conservées dans un cache.</span><span class="sxs-lookup"><span data-stu-id="5def8-103">This document describes how to use the <xref:System.Threading.Tasks.Task.FromResult%2A?displayProperty=nameWithType> method to retrieve the results of asynchronous download operations that are held in a cache.</span></span> <span data-ttu-id="5def8-104">La méthode <xref:System.Threading.Tasks.Task.FromResult%2A> retourne un objet <xref:System.Threading.Tasks.Task%601> fini qui contient la valeur fournie en tant que sa propriété <xref:System.Threading.Tasks.Task%601.Result%2A>.</span><span class="sxs-lookup"><span data-stu-id="5def8-104">The <xref:System.Threading.Tasks.Task.FromResult%2A> method returns a finished <xref:System.Threading.Tasks.Task%601> object that holds the provided value as its <xref:System.Threading.Tasks.Task%601.Result%2A> property.</span></span> <span data-ttu-id="5def8-105">Cette méthode est utile lorsque vous exécutez une opération asynchrone qui retourne un objet <xref:System.Threading.Tasks.Task%601>, et que le résultat de cet objet <xref:System.Threading.Tasks.Task%601> est déjà calculé.</span><span class="sxs-lookup"><span data-stu-id="5def8-105">This method is useful when you perform an asynchronous operation that returns a <xref:System.Threading.Tasks.Task%601> object, and the result of that <xref:System.Threading.Tasks.Task%601> object is already computed.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5def8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="5def8-106">Example</span></span>  
 <span data-ttu-id="5def8-107">L’exemple suivant télécharge des chaînes à partir du web.</span><span class="sxs-lookup"><span data-stu-id="5def8-107">The following example downloads strings from the web.</span></span> <span data-ttu-id="5def8-108">Il définit la méthode `DownloadStringAsync`.</span><span class="sxs-lookup"><span data-stu-id="5def8-108">It defines the `DownloadStringAsync` method.</span></span> <span data-ttu-id="5def8-109">Cette méthode télécharge des chaînes à partir du web de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5def8-109">This method downloads strings from the web asynchronously.</span></span> <span data-ttu-id="5def8-110">Cet exemple utilise également un objet <xref:System.Collections.Concurrent.ConcurrentDictionary%602> pour mettre en cache les résultats des opérations précédentes.</span><span class="sxs-lookup"><span data-stu-id="5def8-110">This example also uses a <xref:System.Collections.Concurrent.ConcurrentDictionary%602> object to cache the results of previous operations.</span></span> <span data-ttu-id="5def8-111">Si l’adresse d’entrée est conservée dans ce cache, `DownloadStringAsync` utilise la méthode <xref:System.Threading.Tasks.Task.FromResult%2A> pour produire un objet <xref:System.Threading.Tasks.Task%601> qui contient le contenu à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5def8-111">If the input address is held in this cache, `DownloadStringAsync` uses the <xref:System.Threading.Tasks.Task.FromResult%2A> method to produce a <xref:System.Threading.Tasks.Task%601> object that holds the content at that address.</span></span> <span data-ttu-id="5def8-112">Dans le cas contraire, `DownloadStringAsync` télécharge le fichier à partir du web et ajoute le résultat dans le cache.</span><span class="sxs-lookup"><span data-stu-id="5def8-112">Otherwise, `DownloadStringAsync` downloads the file from the web and adds the result to the cache.</span></span>  
  
 [!code-csharp[TPL_CachedDownloads#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_cacheddownloads/cs/cacheddownloads.cs#1)]
 [!code-vb[TPL_CachedDownloads#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_cacheddownloads/vb/cacheddownloads.vb#1)]  
  
 <span data-ttu-id="5def8-113">Cet exemple calcule le temps nécessaire pour télécharger plusieurs chaînes deux fois.</span><span class="sxs-lookup"><span data-stu-id="5def8-113">This example computes the time that is required to download multiple strings two times.</span></span> <span data-ttu-id="5def8-114">Le deuxième ensemble d’opérations de téléchargement doit prendre moins de temps que le premier, car les résultats sont conservés dans le cache.</span><span class="sxs-lookup"><span data-stu-id="5def8-114">The second set of download operations should take less time than the first set because the results are held in the cache.</span></span> <span data-ttu-id="5def8-115">La méthode <xref:System.Threading.Tasks.Task.FromResult%2A> permet à la méthode `DownloadStringAsync` de créer des objets <xref:System.Threading.Tasks.Task%601> qui contiennent ces résultats pré-calculés.</span><span class="sxs-lookup"><span data-stu-id="5def8-115">The <xref:System.Threading.Tasks.Task.FromResult%2A> method enables the `DownloadStringAsync` method to create <xref:System.Threading.Tasks.Task%601> objects that hold these pre-computed results.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5def8-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5def8-116">Compiling the Code</span></span>  
 <span data-ttu-id="5def8-117">Copiez l’exemple de code et collez-le dans un projet Visual Studio, ou collez-le dans un fichier nommé `CachedDownloads.cs` (`CachedDownloads.vb` pour [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), puis exécutez la commande suivante dans une fenêtre d’invite de commandes Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5def8-117">Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `CachedDownloads.cs` (`CachedDownloads.vb` for [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), and then run the following command in a Visual Studio Command Prompt window.</span></span>  
  
 [!INCLUDE[csprcs](../../../includes/csprcs-md.md)]  
  
 <span data-ttu-id="5def8-118">**csc.exe CachedDownloads.cs**</span><span class="sxs-lookup"><span data-stu-id="5def8-118">**csc.exe CachedDownloads.cs**</span></span>  
  
 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]  
  
 <span data-ttu-id="5def8-119">**vbc.exe CachedDownloads.vb**</span><span class="sxs-lookup"><span data-stu-id="5def8-119">**vbc.exe CachedDownloads.vb**</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="5def8-120">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="5def8-120">Robust Programming</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5def8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5def8-121">See Also</span></span>  
 [<span data-ttu-id="5def8-122">Programmation asynchrone basée sur les tâches</span><span class="sxs-lookup"><span data-stu-id="5def8-122">Task-based Asynchronous Programming</span></span>](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
