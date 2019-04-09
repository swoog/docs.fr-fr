---
title: IMetaDataTables, interface
ms.date: 03/30/2017
api_name:
- IMetaDataTables
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables
helpviewer_keywords:
- IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 31272cce-506a-4f18-bcbf-01ee45e36356
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2b2298e2d67e8a50e11d53d864f0e78f3b549e45
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59131415"
---
# <a name="imetadatatables-interface"></a><span data-ttu-id="bc93b-102">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="bc93b-102">IMetaDataTables Interface</span></span>
<span data-ttu-id="bc93b-103">Fournit des méthodes pour le stockage et la récupération d'informations de métadonnées dans des tables.</span><span class="sxs-lookup"><span data-stu-id="bc93b-103">Provides methods for the storage and retrieval of metadata information in tables.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bc93b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bc93b-104">Methods</span></span>  
  
|<span data-ttu-id="bc93b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-105">Method</span></span>|<span data-ttu-id="bc93b-106">Description</span><span class="sxs-lookup"><span data-stu-id="bc93b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bc93b-107">GetBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-107">GetBlob Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getblob-method.md)|<span data-ttu-id="bc93b-108">Obtient un pointeur vers l’objet binaire volumineux (BLOB) à l’index de colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc93b-108">Gets a pointer to the binary large object (BLOB) at the specified column index.</span></span>|  
|[<span data-ttu-id="bc93b-109">GetBlobHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-109">GetBlobHeapSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getblobheapsize-method.md)|<span data-ttu-id="bc93b-110">Obtient la taille, en octets, du tas de BLOB.</span><span class="sxs-lookup"><span data-stu-id="bc93b-110">Gets the size, in bytes, of the BLOB heap.</span></span>|  
|[<span data-ttu-id="bc93b-111">GetCodedTokenInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-111">GetCodedTokenInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcodedtokeninfo-method.md)|<span data-ttu-id="bc93b-112">Obtient un pointeur vers un tableau de jetons associé à l’index de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc93b-112">Gets a pointer to an array of tokens associated with the specified row index.</span></span>|  
|[<span data-ttu-id="bc93b-113">GetColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-113">GetColumn Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcolumn-method.md)|<span data-ttu-id="bc93b-114">Obtient un pointeur vers les valeurs contenues dans la colonne à l’index de colonne spécifié dans la table à l’index de la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc93b-114">Gets a pointer to the values contained in the column at the specified column index, in the table at the specified table index.</span></span>|  
|[<span data-ttu-id="bc93b-115">GetColumnInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-115">GetColumnInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcolumninfo-method.md)|<span data-ttu-id="bc93b-116">Obtient les données relatives à la colonne spécifiée dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc93b-116">Gets data about the specified column in the specified table.</span></span>|  
|[<span data-ttu-id="bc93b-117">GetGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-117">GetGuid Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getguid-method.md)|<span data-ttu-id="bc93b-118">Obtient un GUID à partir de la ligne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc93b-118">Gets a GUID from the row at the specified index.</span></span>|  
|[<span data-ttu-id="bc93b-119">GetGuidHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-119">GetGuidHeapSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getguidheapsize-method.md)|<span data-ttu-id="bc93b-120">Obtient la taille, en octets, du tas GUID.</span><span class="sxs-lookup"><span data-stu-id="bc93b-120">Gets the size, in bytes, of the GUID heap.</span></span>|  
|[<span data-ttu-id="bc93b-121">GetNextBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-121">GetNextBlob Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextblob-method.md)|<span data-ttu-id="bc93b-122">Obtient l’index de l’objet BLOB suivant dans la table.</span><span class="sxs-lookup"><span data-stu-id="bc93b-122">Gets the index of the next BLOB in the table.</span></span>|  
|[<span data-ttu-id="bc93b-123">GetNextGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-123">GetNextGuid Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextguid-method.md)|<span data-ttu-id="bc93b-124">Obtient l’index de la valeur GUID suivante dans la colonne de table actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc93b-124">Gets the index of the next GUID value in the current table column.</span></span>|  
|[<span data-ttu-id="bc93b-125">GetNextString, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-125">GetNextString Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextstring-method.md)|<span data-ttu-id="bc93b-126">Obtient l’index de la chaîne suivante dans la colonne de table actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc93b-126">Gets the index of the next string in the current table column.</span></span>|  
|[<span data-ttu-id="bc93b-127">GetNextUserString, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-127">GetNextUserString Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextuserstring-method.md)|<span data-ttu-id="bc93b-128">Obtient l’index de la ligne qui contient la chaîne codée en dur suivante dans la colonne de table actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc93b-128">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>|  
|[<span data-ttu-id="bc93b-129">GetNumTables, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-129">GetNumTables Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnumtables-method.md)|<span data-ttu-id="bc93b-130">Obtient le nombre de tables dans la portée du cours `IMetaDataTables` instance.</span><span class="sxs-lookup"><span data-stu-id="bc93b-130">Gets the number of tables in the scope of the current `IMetaDataTables` instance.</span></span>|  
|[<span data-ttu-id="bc93b-131">GetRow, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-131">GetRow Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getrow-method.md)|<span data-ttu-id="bc93b-132">Obtient la ligne à l’index de la ligne spécifiée, dans la table à l’index de la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc93b-132">Gets the row at the specified row index, in the table at the specified table index.</span></span>|  
|[<span data-ttu-id="bc93b-133">GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-133">GetString Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getstring-method.md)|<span data-ttu-id="bc93b-134">Obtient la chaîne à l’index spécifié à partir de la colonne de table dans l’étendue actuelle de la référence.</span><span class="sxs-lookup"><span data-stu-id="bc93b-134">Gets the string at the specified index from the table column in the current reference scope.</span></span>|  
|[<span data-ttu-id="bc93b-135">GetStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-135">GetStringHeapSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getstringheapsize-method.md)|<span data-ttu-id="bc93b-136">Obtient la taille, en octets, du tas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bc93b-136">Gets the size, in bytes, of the string heap.</span></span>|  
|[<span data-ttu-id="bc93b-137">GetTableIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-137">GetTableIndex Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-gettableindex-method.md)|<span data-ttu-id="bc93b-138">Obtient l’index pour la table référencée par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc93b-138">Gets the index for the table referenced by the specified token.</span></span>|  
|[<span data-ttu-id="bc93b-139">GetTableInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-139">GetTableInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-gettableinfo-method.md)|<span data-ttu-id="bc93b-140">Obtient le nom, la taille de ligne, le nombre de lignes, le nombre de colonnes et index de colonne clé de la table à l’index de la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bc93b-140">Gets the name, row size, number of rows, number of columns, and key column index of the table at the specified table index.</span></span>|  
|[<span data-ttu-id="bc93b-141">GetUserString, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-141">GetUserString Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getuserstring-method.md)|<span data-ttu-id="bc93b-142">Obtient la chaîne codée en dur à l’index spécifié dans la colonne de chaîne dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc93b-142">Gets the hard-coded string at the specified index in the string column in the current scope.</span></span>|  
|[<span data-ttu-id="bc93b-143">GetUserStringHeapSize, méthode</span><span class="sxs-lookup"><span data-stu-id="bc93b-143">GetUserStringHeapSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getuserstringheapsize-method.md)|<span data-ttu-id="bc93b-144">Obtient la taille, en octets, du tas de chaîne utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc93b-144">Gets the size, in bytes, of the user string heap.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bc93b-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc93b-145">Requirements</span></span>  
 <span data-ttu-id="bc93b-146">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bc93b-146">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc93b-147">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bc93b-147">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bc93b-148">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bc93b-148">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="bc93b-149">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bc93b-149">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bc93b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc93b-150">See also</span></span>

- [<span data-ttu-id="bc93b-151">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="bc93b-151">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="bc93b-152">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="bc93b-152">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
