---
title: IMetaDataImport2::GetPEKind, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetPEKind
helpviewer_keywords:
- GetPEKind method [.NET Framework metadata]
- IMetaDataImport2::GetPEKind method [.NET Framework metadata]
ms.assetid: d91c3d89-8022-4a4c-a2a2-a8af2c387507
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5ad18aaca1caef242832bbdae9a1094b2ef2d7be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54572459"
---
# <a name="imetadataimport2getpekind-method"></a>IMetaDataImport2::GetPEKind, méthode
Obtient une valeur qui identifie la nature du code dans le fichier exécutable portable (PE) de fichiers, en général, un fichier DLL ou EXE, qui est défini dans la portée de métadonnées actuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPEKind (  
   [out] DWORD *pdwPEKind,  
   [out] DWORD *pdwMachine  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pdwPEKind`  
 [out] Un pointeur vers une valeur de la [CorPEKind](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md) énumération qui décrit le fichier PE.  
  
 `pdwMachine`  
 [out] Pointeur vers une valeur qui identifie l’architecture de l’ordinateur. Consultez la section suivante pour les valeurs possibles.  
  
## <a name="remarks"></a>Notes  
 La valeur référencée par le `pdwMachine` paramètre peut prendre l’une des opérations suivantes.  
  
|Value|Architecture de l’ordinateur|  
|-----------|--------------------------|  
|IMAGE_FILE_MACHINE_I386<br /><br /> 0x014C|x86|  
|IMAGE_FILE_MACHINE_IA64<br /><br /> 0x0200|Intel IPF|  
|IMAGE_FILE_MACHINE_AMD64<br /><br /> 0x8664|X64|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [CorPEKind, énumération](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md)
