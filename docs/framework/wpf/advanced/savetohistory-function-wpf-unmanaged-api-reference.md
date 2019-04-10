---
title: Fonction SaveToHistory (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- SaveToHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: 6dd101a3-44ad-4143-b228-772156f9b8ff
ms.openlocfilehash: 3f6413558ff1f259e497c6a1c31eb2664f70cc48
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213714"
---
# <a name="savetohistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="adaa1-102">Fonction SaveToHistory (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="adaa1-102">SaveToHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="adaa1-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="adaa1-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="adaa1-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="adaa1-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adaa1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adaa1-105">Syntax</span></span>  
  
```cpp  
HRESULT SaveToHistory(  
   __in_ecount(1) IStream* pHistoryStream  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="adaa1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adaa1-106">Parameters</span></span>  
 <span data-ttu-id="adaa1-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="adaa1-107">pHistoryStream</span></span>  
 <span data-ttu-id="adaa1-108">Un pointeur vers le flux de l’historique.</span><span class="sxs-lookup"><span data-stu-id="adaa1-108">A pointer to the history stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="adaa1-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adaa1-109">Requirements</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="adaa1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adaa1-110">Requirements</span></span>  
 <span data-ttu-id="adaa1-111">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="adaa1-111">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 **<span data-ttu-id="adaa1-112">DLL :</span><span class="sxs-lookup"><span data-stu-id="adaa1-112">DLL:</span></span>**  
  
 <span data-ttu-id="adaa1-113">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="adaa1-113">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="adaa1-114">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="adaa1-114">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 **<span data-ttu-id="adaa1-115">Version du .NET framework :</span><span class="sxs-lookup"><span data-stu-id="adaa1-115">.NET Framework Version:</span></span>** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="adaa1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adaa1-116">See also</span></span>

- [<span data-ttu-id="adaa1-117">Informations de référence sur les API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="adaa1-117">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
