---
title: IEnumRAWINPUTDEVICE
ms.date: 03/30/2017
helpviewer_keywords:
- IEnumRAWINPUTDEVICE interface [WPF]
ms.assetid: 88c8b389-a48b-46b9-b895-8ed7b1e26fea
ms.openlocfilehash: e0e5a112b7444872dd74cb70bb044ae233334d2a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47076900"
---
# <a name="ienumrawinputdevice"></a><span data-ttu-id="0f702-102">IEnumRAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="0f702-102">IEnumRAWINPUTDEVICE</span></span>
<span data-ttu-id="0f702-103">Cette interface énumère les périphériques d'entrée brute ; elle est uniquement utilisée par PresentationHost.exe.</span><span class="sxs-lookup"><span data-stu-id="0f702-103">This interface enumerates the raw input devices, and is only used by PresentationHost.exe.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f702-104">Cette API est conçue et pris en charge uniquement sur l'ordinateur client local</span><span class="sxs-lookup"><span data-stu-id="0f702-104">This API is only intended and supported for use on the local client machine</span></span>  
  
## <a name="members"></a><span data-ttu-id="0f702-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0f702-105">Members</span></span>  
  
|<span data-ttu-id="0f702-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0f702-106">Member</span></span>|<span data-ttu-id="0f702-107">Description</span><span class="sxs-lookup"><span data-stu-id="0f702-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0f702-108">IEnumRAWINPUTDEVIC:Next</span><span class="sxs-lookup"><span data-stu-id="0f702-108">IEnumRAWINPUTDEVIC:Next</span></span>](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md)|<span data-ttu-id="0f702-109">Énumère les éléments `celt` suivants (c'est-à-dire les structures RAWINPUTDEVICE) dans la liste de l'énumérateur, en les retournant dans `rgelt` avec le nombre réel d'éléments énumérés dans `pceltFetched`.</span><span class="sxs-lookup"><span data-stu-id="0f702-109">Enumerates the next `celt` elements (that is, RAWINPUTDEVICE structures) in the enumerator's list, returning them in `rgelt` along with the actual number of enumerated elements in `pceltFetched`.</span></span>|  
|[<span data-ttu-id="0f702-110">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="0f702-110">IEnumRAWINPUTDEVIC:Skip</span></span>](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-skip.md)|<span data-ttu-id="0f702-111">Demande à l’énumérateur d’ignorer les `celt` éléments dans l’énumération afin que l’appel suivant à [IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md) ne retourne pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="0f702-111">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md) will not return those elements.</span></span>|  
|[<span data-ttu-id="0f702-112">IEnumRAWINPUTDEVIC:Reset</span><span class="sxs-lookup"><span data-stu-id="0f702-112">IEnumRAWINPUTDEVIC:Reset</span></span>](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-reset.md)|<span data-ttu-id="0f702-113">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="0f702-113">Resets the enumeration sequence to the beginning.</span></span>|  
|[<span data-ttu-id="0f702-114">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="0f702-114">IEnumRAWINPUTDEVIC:Clone</span></span>](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-clone.md)|<span data-ttu-id="0f702-115">Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.</span><span class="sxs-lookup"><span data-stu-id="0f702-115">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0f702-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f702-116">See Also</span></span>  
 [<span data-ttu-id="0f702-117">À propos des entrées brutes</span><span class="sxs-lookup"><span data-stu-id="0f702-117">About Raw Input</span></span>](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/aboutrawinput.asp)
