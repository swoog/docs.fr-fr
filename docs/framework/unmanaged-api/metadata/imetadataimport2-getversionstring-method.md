---
title: IMetaDataImport2::GetVersionString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetVersionString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetVersionString
helpviewer_keywords:
- GetVersionString method, IMetaDataImport2 interface [.NET Framework metadata]
- IMetaDataImport2::GetVersionString method [.NET Framework metadata]
ms.assetid: 308183ee-fd44-4432-9d86-ef00d181b49b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a01b4203145f6ffee4e3a11a3526f0b83e3dc741
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154620"
---
# <a name="imetadataimport2getversionstring-method"></a>IMetaDataImport2::GetVersionString, méthode
Obtient le numéro de version du runtime qui a été utilisé pour générer l’assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetVersionString (  
   [out] LPWSTR      pwzBuf,  
   [in]  DWORD       ccBufSize,  
   [out] DWORD       *pccBufSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pwzBuf`  
 [out] Un tableau pour stocker la chaîne qui spécifie la version.  
  
 `ccBufSize`  
 [in] La taille, en caractères larges, de la `pwzBuf` tableau.  
  
 `pccBufSize`  
 [out] Le nombre de caractères larges, y compris une marque de fin null, retournés dans le `pwzBuf` tableau.  
  
## <a name="remarks"></a>Notes  
 Le `GetVersionString` méthode obtient la version propre à la portée de métadonnées actuelle. Si l’étendue n’a jamais été enregistré, il n’aura pas d’une version propre à, et une chaîne vide est retournée.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
