---
title: ICorDebugILFrame2::EnumerateTypeParameters, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2.EnumerateTypeParameters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2::EnumerateTypeParameters
helpviewer_keywords:
- EnumerateTypeParameters method, ICorDebugILFrame2 interface [.NET Framework debugging]
- ICorDebugILFrame2::EnumerateTypeParameters method [.NET Framework debugging]
ms.assetid: 722d0d74-e0df-491f-98c4-62d501dfaf6f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0a0c23c066a6f704c4dfcfbe254e91ab3bc5817e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416239"
---
# <a name="icordebugilframe2enumeratetypeparameters-method"></a><span data-ttu-id="32719-102">ICorDebugILFrame2::EnumerateTypeParameters, méthode</span><span class="sxs-lookup"><span data-stu-id="32719-102">ICorDebugILFrame2::EnumerateTypeParameters Method</span></span>
<span data-ttu-id="32719-103">Obtient un objet du ICorDebugTypeEnum qui contient le <xref:System.Type> paramètres dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="32719-103">Gets an ICorDebugTypeEnum object that contains the <xref:System.Type> parameters in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32719-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32719-104">Syntax</span></span>  
  
```  
HRESULT EnumerateTypeParameters (  
    [out] ICorDebugTypeEnum    **ppTyParEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="32719-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32719-105">Parameters</span></span>  
 `ppTyParEnum`  
 <span data-ttu-id="32719-106">Pointeur vers l’adresse d’un objet d’interface ICorDebugTypeEnum qui permet l’énumération des paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="32719-106">A pointer to the address of a ICorDebugTypeEnum interface object that allows enumeration of type parameters.</span></span>  
  
 <span data-ttu-id="32719-107">La liste des paramètres de type inclut les paramètres de type classe (le cas échéant) suivis par les paramètres de type (méthode) (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="32719-107">The list of type parameters include the class type parameters (if any) followed by the method type parameters (if any).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="32719-108">Notes</span><span class="sxs-lookup"><span data-stu-id="32719-108">Remarks</span></span>  
 <span data-ttu-id="32719-109">Utilisez le [IMetaDataImport2::EnumGenericParams](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparams-method.md) méthode pour déterminer le nombre de paramètres de type de classe et de méthode de cette liste contient les paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="32719-109">Use the [IMetaDataImport2::EnumGenericParams](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparams-method.md) method to determine how many class type parameters and method type parameters this list contains.</span></span>  
  
 <span data-ttu-id="32719-110">Les paramètres de type ne sont pas toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="32719-110">The type parameters are not always available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32719-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32719-111">Requirements</span></span>  
 <span data-ttu-id="32719-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="32719-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="32719-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="32719-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="32719-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="32719-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="32719-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="32719-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
