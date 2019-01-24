---
title: IMetaDataImport::GetMemberProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberProps
helpviewer_keywords:
- IMetaDataImport::GetMemberProps method [.NET Framework metadata]
- GetMemberProps method [.NET Framework metadata]
ms.assetid: 42790918-4142-4938-b8f4-a56979a55846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98d7be5adc81cff09b121265e7d5b5f712122607
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611408"
---
# <a name="imetadataimportgetmemberprops-method"></a>IMetaDataImport::GetMemberProps, méthode
Obtient les informations de métadonnées, y compris le nom, le signature binaire et l’adresse virtuelle relative, de la <xref:System.Type> membre référencé par le jeton de métadonnées spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMemberProps (  
   [in]  mdToken           mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] DWORD             *pdwAttr,  
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] ULONG             *pulCodeRVA,   
   [out] DWORD             *pdwImplFlags,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `mb`  
 [in] Le jeton qui référence le membre pour obtenir les métadonnées associées.  
  
 `pClass`  
 [out] Pointeur vers le jeton de métadonnées qui représente la classe du membre.  
  
 `szMember`  
 [out] Le nom du membre.  
  
 `cchMember`  
 [in] La taille en caractères larges de la `szMember` mémoire tampon.  
  
 `pchMember`  
 [out] La taille en caractères larges du nom retourné.  
  
 `pdwAttr`  
 [out] Les valeurs d’indicateur appliqués au membre.  
  
 `ppvSigBlob`  
 [out] Pointeur vers la signature de métadonnées binaires du membre.  
  
 `pcbSigBlob`  
 [out] La taille en octets de `ppvSigBlob`.  
  
 `pulCodeRVA`  
 [out] Pointeur vers l’adresse virtuelle relative du membre.  
  
 `pdwImplFlags`  
 [out] Les indicateurs d’implémentation méthode associés au membre.  
  
 `pdwCPlusTypeFlag`  
 [out] Un indicateur qui marque un <xref:System.ValueType>.  
  
 `ppValue`  
 [out] Une valeur de chaîne constante retournée par ce membre.  
  
 `pcchValue`  
 [out] La taille en caractères de `ppValue`, ou zéro si `ppValue` ne contient pas de chaîne.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
