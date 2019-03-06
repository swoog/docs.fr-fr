---
title: IMetaDataTables::GetUserString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetUserString
helpviewer_keywords:
- IMetaDataTables::GetUserString method [.NET Framework metadata]
- GetUserString method, IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 35b8f0d6-9aba-4714-adb2-62020a38fb7e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0fefbab6b2ea9fbbfd90e03c41578a924f99c7a0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364162"
---
# <a name="imetadatatablesgetuserstring-method"></a><span data-ttu-id="5036f-102">IMetaDataTables::GetUserString, méthode</span><span class="sxs-lookup"><span data-stu-id="5036f-102">IMetaDataTables::GetUserString Method</span></span>

<span data-ttu-id="5036f-103">Obtient la chaîne codée en dur à l’index spécifié dans la colonne de chaîne dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="5036f-103">Gets the hard-coded string at the specified index in the string column in the current scope.</span></span>

## <a name="syntax"></a><span data-ttu-id="5036f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5036f-104">Syntax</span></span>

```cpp
HRESULT GetUserString (
    [in]  ULONG       ixUserString,
    [out] ULONG       *pcbData,
    [out] const void  **ppData
);
```

## <a name="parameters"></a><span data-ttu-id="5036f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5036f-105">Parameters</span></span>

`ixUserString`\
<span data-ttu-id="5036f-106">[in] La valeur d’index à partir de laquelle la chaîne codée en dur est récupérée.</span><span class="sxs-lookup"><span data-stu-id="5036f-106">[in] The index value from which the hard-coded string will be retrieved.</span></span>

`pcbData`\
<span data-ttu-id="5036f-107">[out] Un pointeur vers la taille de `ppData`.</span><span class="sxs-lookup"><span data-stu-id="5036f-107">[out] A pointer to the size of `ppData`.</span></span>

`ppData`\
<span data-ttu-id="5036f-108">[out] Pointeur vers un pointeur vers la chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="5036f-108">[out] A pointer to a pointer to the returned string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5036f-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5036f-109">Requirements</span></span>

<span data-ttu-id="5036f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5036f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="5036f-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5036f-111">**Header:** Cor.h</span></span>

<span data-ttu-id="5036f-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5036f-112">**Library:** Used as a resource in MsCorEE.dll</span></span>

<span data-ttu-id="5036f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5036f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="5036f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5036f-114">See also</span></span>

- [<span data-ttu-id="5036f-115">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="5036f-115">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="5036f-116">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="5036f-116">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)