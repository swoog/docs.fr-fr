---
title: Fonction LoadFromHistory (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: a4480d54390aea2771e2939b0a0825f6c49c3564
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59084957"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="1ce46-102">Fonction LoadFromHistory (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="1ce46-102">LoadFromHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="1ce46-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="1ce46-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="1ce46-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="1ce46-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ce46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ce46-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,   
        IBindCtx* pBindCtx  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="1ce46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ce46-106">Parameters</span></span>  
 <span data-ttu-id="1ce46-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="1ce46-107">pHistoryStream</span></span>  
 <span data-ttu-id="1ce46-108">Pointeur vers un flux d’informations d’historique.</span><span class="sxs-lookup"><span data-stu-id="1ce46-108">A pointer to a stream of history information.</span></span>  
  
 <span data-ttu-id="1ce46-109">pBindCtx</span><span class="sxs-lookup"><span data-stu-id="1ce46-109">pBindCtx</span></span>  
 <span data-ttu-id="1ce46-110">Pointeur vers un contexte de liaison.</span><span class="sxs-lookup"><span data-stu-id="1ce46-110">A pointer to a bind context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ce46-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ce46-111">Requirements</span></span>  
 <span data-ttu-id="1ce46-112">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ce46-112">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 **<span data-ttu-id="1ce46-113">DLL :</span><span class="sxs-lookup"><span data-stu-id="1ce46-113">DLL:</span></span>**  
  
 <span data-ttu-id="1ce46-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="1ce46-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="1ce46-115">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="1ce46-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 **<span data-ttu-id="1ce46-116">Version du .NET framework :</span><span class="sxs-lookup"><span data-stu-id="1ce46-116">.NET Framework Version:</span></span>** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1ce46-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ce46-117">See also</span></span>

- [<span data-ttu-id="1ce46-118">Informations de référence sur les API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="1ce46-118">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
