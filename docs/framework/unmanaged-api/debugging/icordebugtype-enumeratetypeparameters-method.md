---
title: ICorDebugType::EnumerateTypeParameters, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugType.EnumerateTypeParameters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::EnumerateTypeParameters
helpviewer_keywords:
- EnumerateTypeParameters method, ICorDebugType interface [.NET Framework debugging]
- ICorDebugType::EnumerateTypeParameters method [.NET Framework debugging]
ms.assetid: 1ee1f6e6-1bd7-4ebb-83b8-ff9a08ca03de
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8fa39a54437e60737aa052c495f58422bc0d3fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946235"
---
# <a name="icordebugtypeenumeratetypeparameters-method"></a><span data-ttu-id="54b5d-102">ICorDebugType::EnumerateTypeParameters, méthode</span><span class="sxs-lookup"><span data-stu-id="54b5d-102">ICorDebugType::EnumerateTypeParameters Method</span></span>
<span data-ttu-id="54b5d-103">Obtient un pointeur d’interface ICorDebugTypeEnum qui contient le <xref:System.Type> paramètres de la classe référencée par ICorDebugType.</span><span class="sxs-lookup"><span data-stu-id="54b5d-103">Gets an interface pointer to an ICorDebugTypeEnum that contains the <xref:System.Type> parameters of the class referenced by this ICorDebugType.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54b5d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54b5d-104">Syntax</span></span>  
  
```  
HRESULT EnumerateTypeParameters (  
    [out] ICorDebugTypeEnum   **ppTyParEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54b5d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54b5d-105">Parameters</span></span>  
 `ppTyParEnum`  
 <span data-ttu-id="54b5d-106">[out] Un pointeur vers l’adresse d’un `ICorDebugTypeEnum` qui contient les paramètres du type.</span><span class="sxs-lookup"><span data-stu-id="54b5d-106">[out] A pointer to the address of an `ICorDebugTypeEnum` that contains the parameters of the type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54b5d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="54b5d-107">Remarks</span></span>  
 <span data-ttu-id="54b5d-108">Vous pouvez utiliser `EnumerateTypeParameters` si la valeur CorElementType retournée par [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) est ELEMENT_TYPE_CLASS, ELEMENT_TYPE_VALUETYPE, ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, ELEMENT_TYPE_ PTR, ou ELEMENT_TYPE_FNPTR.</span><span class="sxs-lookup"><span data-stu-id="54b5d-108">You can use `EnumerateTypeParameters` if the CorElementType value returned by [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) is ELEMENT_TYPE_CLASS, ELEMENT_TYPE_VALUETYPE, ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, ELEMENT_TYPE_PTR, or ELEMENT_TYPE_FNPTR.</span></span> <span data-ttu-id="54b5d-109">Le nombre de paramètres et leur ordre varie selon le type :</span><span class="sxs-lookup"><span data-stu-id="54b5d-109">The number of parameters and their order depends on the type:</span></span>  
  
- <span data-ttu-id="54b5d-110">ELEMENT_TYPE_CLASS ou ELEMENT_TYPE_VALUETYPE : Le nombre de paramètres de type contenues dans le `ICorDebugTypeEnum` que cette méthode est retournée, varient selon le nombre de paramètres de type formel pour la classe correspondante.</span><span class="sxs-lookup"><span data-stu-id="54b5d-110">ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE: The number of type parameters contained in the `ICorDebugTypeEnum` that this method returns, will depend on the number of formal type parameters for the corresponding class.</span></span> <span data-ttu-id="54b5d-111">Par exemple, si le type est `class Dict<String,int32>`, puis `EnumerateTypeParameters` retournera un `ICorDebugTypeEnum` qui contient des objets représentant `String` et `int32` dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="54b5d-111">For example, if the type is `class Dict<String,int32>`, then `EnumerateTypeParameters` will return an `ICorDebugTypeEnum` that contains objects representing `String` and `int32` in sequence.</span></span>  
  
- <span data-ttu-id="54b5d-112">ELEMENT_TYPE_FNPTR : Le nombre de paramètres de type contenues dans le `ICorDebugTypeEnum` sera supérieur au nombre d’arguments acceptés par la fonction.</span><span class="sxs-lookup"><span data-stu-id="54b5d-112">ELEMENT_TYPE_FNPTR: The number of type parameters contained in the `ICorDebugTypeEnum` will be one greater than the number of arguments accepted by the function.</span></span> <span data-ttu-id="54b5d-113">Le premier paramètre de type contenu dans le `ICorDebugTypeEnum` est le type de retour pour la fonction, et les paramètres de type suivants sont les paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="54b5d-113">The first type parameter contained in the `ICorDebugTypeEnum` is the return type for the function, and the subsequent type parameters are the function's parameters.</span></span>  
  
- <span data-ttu-id="54b5d-114">ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF ou ELEMENT_TYPE_PTR : Un paramètre de type est retourné.</span><span class="sxs-lookup"><span data-stu-id="54b5d-114">ELEMENT_TYPE_ARRAY, ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF, or ELEMENT_TYPE_PTR: One type parameter will be returned.</span></span> <span data-ttu-id="54b5d-115">Par exemple, si le type est un type tableau tel que `int32[]`,`EnumerateTypeParameters` retournera un `ICorDebugTypeEnum` qui contient un objet représentant `int32`.</span><span class="sxs-lookup"><span data-stu-id="54b5d-115">For example, if the type is an array type such as `int32[]`,`EnumerateTypeParameters` will return an `ICorDebugTypeEnum` that contains an object representing `int32`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54b5d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54b5d-116">Requirements</span></span>  
 <span data-ttu-id="54b5d-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="54b5d-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54b5d-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="54b5d-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="54b5d-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="54b5d-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="54b5d-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54b5d-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
