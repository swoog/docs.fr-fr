---
title: Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: bf1f50d0d8eb9b0b8518075b0e48f40645a02a25
ms.sourcegitcommit: e08b319358a8025cc6aa38737854f7bdb87183d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "64913211"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a><span data-ttu-id="a67f0-102">Utilisez ’FilePutObject’ à la place de ’FilePut’ quand l’argument est de type ’Object’.</span><span class="sxs-lookup"><span data-stu-id="a67f0-102">Use 'FilePutObject' instead of 'FilePut' when using argument of type 'Object'</span></span>
<span data-ttu-id="a67f0-103">La méthode `FilePut` comprend un argument de type `Object`.</span><span class="sxs-lookup"><span data-stu-id="a67f0-103">The `FilePut` method includes an argument of type `Object`.</span></span> <span data-ttu-id="a67f0-104">`FilePutObject` doit être utilisé à la place de `FilePut` pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="a67f0-104">`FilePutObject` should be used in place of `FilePut` to avoid ambiguities.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a67f0-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="a67f0-105">To correct this error</span></span>  
  
- <span data-ttu-id="a67f0-106">Remplacez `FilePut` par `FilePutObject`.</span><span class="sxs-lookup"><span data-stu-id="a67f0-106">Replace `FilePut` with `FilePutObject`.</span></span>  
  
- <span data-ttu-id="a67f0-107">Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="a67f0-107">Cast the `Object` argument to a more specific type.</span></span>  
  
- <span data-ttu-id="a67f0-108">Utilisez les fonctionnalités disponibles dans l’objet `My.Computer.FileSystem` .</span><span class="sxs-lookup"><span data-stu-id="a67f0-108">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a67f0-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a67f0-109">See also</span></span>

- [<span data-ttu-id="a67f0-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="a67f0-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
- [<span data-ttu-id="a67f0-111">My.Computer.FileSystem.WriteAllBytes</span><span class="sxs-lookup"><span data-stu-id="a67f0-111">My.Computer.FileSystem.WriteAllBytes</span></span>](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
