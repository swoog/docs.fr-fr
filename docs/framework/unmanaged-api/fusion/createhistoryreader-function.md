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
ms.openlocfilehash: f3a3cc21dbbcfa99ddcecb534bd2e337da005597
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431176"
---
# <a name="createhistoryreader-function"></a><span data-ttu-id="28e7c-102">CreateHistoryReader, fonction</span><span class="sxs-lookup"><span data-stu-id="28e7c-102">CreateHistoryReader Function</span></span>
<span data-ttu-id="28e7c-103">Crée un lecteur de l’historique pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="28e7c-103">Creates a history reader for the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28e7c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28e7c-104">Syntax</span></span>  
  
```  
HRESULT CreateHistoryReader (  
    [in]  LPCWSTR        wzFilePath,  
    [out] IHistoryReader **ppHistoryReader  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="28e7c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28e7c-105">Parameters</span></span>  
 `wzFilePath`  
 <span data-ttu-id="28e7c-106">[in] Le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="28e7c-106">[in] The file path.</span></span>  
  
 `ppHistoryReader`  
 <span data-ttu-id="28e7c-107">[out] Opération réussie, contient un pointeur vers le lecteur de l’historique.</span><span class="sxs-lookup"><span data-stu-id="28e7c-107">[out] On successful completion, contains a pointer to the history reader.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="28e7c-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="28e7c-108">Return Value</span></span>  
 <span data-ttu-id="28e7c-109">Cette méthode retourne des codes d’erreur COM standard, tel que défini dans WinError.h, en plus des valeurs décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="28e7c-109">This method returns standard COM error codes as defined in WinError.h, in addition to the values described in the following table.</span></span>  
  
|<span data-ttu-id="28e7c-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="28e7c-110">Return code</span></span>|<span data-ttu-id="28e7c-111">Description</span><span class="sxs-lookup"><span data-stu-id="28e7c-111">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="28e7c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="28e7c-112">S_OK</span></span>|<span data-ttu-id="28e7c-113">Indique que la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="28e7c-113">Indicates that the method completed successfully.</span></span>|  
|<span data-ttu-id="28e7c-114">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="28e7c-114">E_INVALIDARG</span></span>|<span data-ttu-id="28e7c-115">Indique que `wzFilePath` ou `ppHistoryReader` sont définies sur une référence null.</span><span class="sxs-lookup"><span data-stu-id="28e7c-115">Indicates that `wzFilePath` or `ppHistoryReader` are set to a null reference.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="28e7c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28e7c-116">Requirements</span></span>  
 <span data-ttu-id="28e7c-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="28e7c-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28e7c-118">**Bibliothèque :** Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="28e7c-118">**Library:** Fusion.dll</span></span>  
  
 <span data-ttu-id="28e7c-119">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28e7c-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28e7c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28e7c-120">See Also</span></span>  
 [<span data-ttu-id="28e7c-121">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="28e7c-121">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
