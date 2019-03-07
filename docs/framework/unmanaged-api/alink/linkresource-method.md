---
title: LinkResource, méthode
ms.date: 03/30/2017
api_name:
- IALink.LinkResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- LinkResource
helpviewer_keywords:
- LinkResource method
ms.assetid: c404acb3-4c59-4100-9a4c-483cbdb1d736
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 61f82a34c287c62e1180c9c6bbe090914763afa3
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479084"
---
# <a name="linkresource-method"></a>LinkResource, méthode
Liens dans une ressource.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT LinkResource(  
    mdAssembly  AssemblyID,  
    LPCWSTR     pszFileName,  
    LPCWSTR     pszNewLocation,  
    LPCWSTR     pszResourceName,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly.  
  
 `pszFileName`  
 Nom du fichier.  
  
 `pszNewLocation`  
 Nouveau nom de fichier facultatif. Si non NULL, `pszFileName` sera copié vers pszNewLocation.  
  
 `pszResourceName`  
 Nom de la ressource.  
  
 `dwFlags`  
 Accessibilité indicateurs tels que `mrPublic` et `mrPrivate`. Ce paramètre peut être passé à [DefineManifestResource, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definemanifestresource-method.md).  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h.  
  
## <a name="see-also"></a>Voir aussi
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
