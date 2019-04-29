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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645177"
---
# <a name="imetadatatables-interface"></a>IMetaDataTables, interface
Fournit des méthodes pour le stockage et la récupération d'informations de métadonnées dans des tables.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetBlob, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getblob-method.md)|Obtient un pointeur vers l’objet binaire volumineux (BLOB) à l’index de colonne spécifiée.|  
|[GetBlobHeapSize, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getblobheapsize-method.md)|Obtient la taille, en octets, du tas de BLOB.|  
|[GetCodedTokenInfo, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcodedtokeninfo-method.md)|Obtient un pointeur vers un tableau de jetons associé à l’index de ligne spécifié.|  
|[GetColumn, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcolumn-method.md)|Obtient un pointeur vers les valeurs contenues dans la colonne à l’index de colonne spécifié dans la table à l’index de la table spécifiée.|  
|[GetColumnInfo, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getcolumninfo-method.md)|Obtient les données relatives à la colonne spécifiée dans la table spécifiée.|  
|[GetGuid, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getguid-method.md)|Obtient un GUID à partir de la ligne à l’index spécifié.|  
|[GetGuidHeapSize, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getguidheapsize-method.md)|Obtient la taille, en octets, du tas GUID.|  
|[GetNextBlob, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextblob-method.md)|Obtient l’index de l’objet BLOB suivant dans la table.|  
|[GetNextGuid, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextguid-method.md)|Obtient l’index de la valeur GUID suivante dans la colonne de table actuelle.|  
|[GetNextString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextstring-method.md)|Obtient l’index de la chaîne suivante dans la colonne de table actuelle.|  
|[GetNextUserString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnextuserstring-method.md)|Obtient l’index de la ligne qui contient la chaîne codée en dur suivante dans la colonne de table actuelle.|  
|[GetNumTables, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getnumtables-method.md)|Obtient le nombre de tables dans la portée du cours `IMetaDataTables` instance.|  
|[GetRow, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getrow-method.md)|Obtient la ligne à l’index de la ligne spécifiée, dans la table à l’index de la table spécifiée.|  
|[GetString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getstring-method.md)|Obtient la chaîne à l’index spécifié à partir de la colonne de table dans l’étendue actuelle de la référence.|  
|[GetStringHeapSize, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getstringheapsize-method.md)|Obtient la taille, en octets, du tas de chaîne.|  
|[GetTableIndex, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-gettableindex-method.md)|Obtient l’index pour la table référencée par le jeton spécifié.|  
|[GetTableInfo, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-gettableinfo-method.md)|Obtient le nom, la taille de ligne, le nombre de lignes, le nombre de colonnes et index de colonne clé de la table à l’index de la table spécifiée.|  
|[GetUserString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getuserstring-method.md)|Obtient la chaîne codée en dur à l’index spécifié dans la colonne de chaîne dans la portée actuelle.|  
|[GetUserStringHeapSize, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-getuserstringheapsize-method.md)|Obtient la taille, en octets, du tas de chaîne utilisateur.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [IMetaDataTables2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
