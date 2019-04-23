---
title: IMetaDataImport2, interface
ms.date: 03/30/2017
api_name:
- IMetaDataImport2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2
helpviewer_keywords:
- IMetaDataImport2 interface [.NET Framework metadata]
ms.assetid: d39b2b87-ba53-4771-ae53-952a68452511
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6717c48fca14f2200f783a984594388ef3b29c15
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211924"
---
# <a name="imetadataimport2-interface"></a>IMetaDataImport2, interface
Étend la [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface pour fournir la possibilité de travailler avec les types génériques.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumGenericParamConstraints, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparamconstraints-method.md)|Obtient un énumérateur pour un tableau de contraintes de paramètre générique associé au paramètre générique représenté par le jeton spécifié.|  
|[EnumGenericParams, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparams-method.md)|Obtient un énumérateur pour un tableau de jetons de paramètre générique associé au TypeDef spécifié ou le MethodDef jeton.|  
|[EnumMethodSpecs, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enummethodspecs-method.md)|Obtient un énumérateur pour un tableau de jetons MethodSpec associé à le MethodDef ou MemberRef spécifié de jeton.|  
|[GetGenericParamConstraintProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getgenericparamconstraintprops-method.md)|Obtient les métadonnées associées à la contrainte de paramètre générique représentée par le jeton de la contrainte spécifiée.|  
|[GetGenericParamProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getgenericparamprops-method.md)|Obtient les métadonnées associées au paramètre générique représenté par le jeton spécifié.|  
|[GetMethodSpecProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getmethodspecprops-method.md)|Obtient le jeton de signature de métadonnées de la méthode référencée par le MethodSpec spécifié.|  
|[GetPEKind, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md)|Obtient une valeur qui identifie la nature du code dans un fichier exécutable portable (PE) de fichiers, en général, un fichier DLL ou EXE, défini dans la portée de métadonnées actuelle|  
|[GetVersionString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getversionstring-method.md)|Obtient le numéro de version du runtime qui a été utilisé pour générer l’assembly.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Reflection.PortableExecutableKinds>
- [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
