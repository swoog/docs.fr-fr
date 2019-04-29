---
title: CreateHistoryReader, fonction
ms.date: 03/30/2017
api_name:
- CreateHistoryReader
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateHistoryReader
helpviewer_keywords:
- CreateHistoryReader function [.NET Framework fusion]
ms.assetid: 66a89acf-8c32-44c0-8787-960c99c7b3ec
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e438006d6424866514e73119c05e8fd69d7ba62e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61669704"
---
# <a name="createhistoryreader-function"></a><span data-ttu-id="66952-102">CreateHistoryReader, fonction</span><span class="sxs-lookup"><span data-stu-id="66952-102">CreateHistoryReader Function</span></span>
<span data-ttu-id="66952-103">Crée un lecteur de l’historique pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="66952-103">Creates a history reader for the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66952-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66952-104">Syntax</span></span>  
  
```  
HRESULT CreateHistoryReader (  
    [in]  LPCWSTR        wzFilePath,  
    [out] IHistoryReader **ppHistoryReader  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="66952-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66952-105">Parameters</span></span>  
 `wzFilePath`  
 <span data-ttu-id="66952-106">[in] Le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="66952-106">[in] The file path.</span></span>  
  
 `ppHistoryReader`  
 <span data-ttu-id="66952-107">[out] Opération réussie, contient un pointeur vers le lecteur de l’historique.</span><span class="sxs-lookup"><span data-stu-id="66952-107">[out] On successful completion, contains a pointer to the history reader.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="66952-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="66952-108">Return Value</span></span>  
 <span data-ttu-id="66952-109">Cette méthode retourne des codes d’erreur COM standard, tel que défini dans WinError.h, en plus des valeurs décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="66952-109">This method returns standard COM error codes as defined in WinError.h, in addition to the values described in the following table.</span></span>  
  
|<span data-ttu-id="66952-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="66952-110">Return code</span></span>|<span data-ttu-id="66952-111">Description</span><span class="sxs-lookup"><span data-stu-id="66952-111">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="66952-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="66952-112">S_OK</span></span>|<span data-ttu-id="66952-113">Indique que la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="66952-113">Indicates that the method completed successfully.</span></span>|  
|<span data-ttu-id="66952-114">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="66952-114">E_INVALIDARG</span></span>|<span data-ttu-id="66952-115">Indique que `wzFilePath` ou `ppHistoryReader` sont définies sur une référence null.</span><span class="sxs-lookup"><span data-stu-id="66952-115">Indicates that `wzFilePath` or `ppHistoryReader` are set to a null reference.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="66952-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66952-116">Requirements</span></span>  
 <span data-ttu-id="66952-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="66952-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66952-118">**Bibliothèque :** Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="66952-118">**Library:** Fusion.dll</span></span>  
  
 <span data-ttu-id="66952-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66952-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66952-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66952-120">See also</span></span>

- [<span data-ttu-id="66952-121">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="66952-121">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
