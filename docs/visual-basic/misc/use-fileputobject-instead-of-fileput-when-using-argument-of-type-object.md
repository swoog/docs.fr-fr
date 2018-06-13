---
title: Utilisez &#39;FilePutObject&#39; au lieu de &#39;FilePut&#39; quand l’argument de type &#39;objet&#39;
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: 529352d98c175981c20861205ce04c8a2ebcdca9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33641126"
---
# <a name="use-39fileputobject39-instead-of-39fileput39-when-using-argument-of-type-39object39"></a><span data-ttu-id="734dc-102">Utilisez &#39;FilePutObject&#39; au lieu de &#39;FilePut&#39; quand l’argument de type &#39;objet&#39;</span><span class="sxs-lookup"><span data-stu-id="734dc-102">Use &#39;FilePutObject&#39; instead of &#39;FilePut&#39; when using argument of type &#39;Object&#39;</span></span>
<span data-ttu-id="734dc-103">Le `FilePut` méthode inclut un argument de type `Object`.</span><span class="sxs-lookup"><span data-stu-id="734dc-103">The `FilePut` method includes an argument of type `Object`.</span></span> <span data-ttu-id="734dc-104">`FilePutObject` doit être utilisé à la place de `FilePut` pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="734dc-104">`FilePutObject` should be used in place of `FilePut` to avoid ambiguities.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="734dc-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="734dc-105">To correct this error</span></span>  
  
-   <span data-ttu-id="734dc-106">Remplacez `FilePut` par `FilePutObject`.</span><span class="sxs-lookup"><span data-stu-id="734dc-106">Replace `FilePut` with `FilePutObject`.</span></span>  
  
-   <span data-ttu-id="734dc-107">Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="734dc-107">Cast the `Object` argument to a more specific type.</span></span>  
  
-   <span data-ttu-id="734dc-108">Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .</span><span class="sxs-lookup"><span data-stu-id="734dc-108">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="734dc-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="734dc-109">See Also</span></span>  
   
 [<span data-ttu-id="734dc-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="734dc-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)  
 [<span data-ttu-id="734dc-111">My.Computer.FileSystem.WriteAllBytes</span><span class="sxs-lookup"><span data-stu-id="734dc-111">My.Computer.FileSystem.WriteAllBytes</span></span>](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
