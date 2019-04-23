---
title: IMetaDataEmit, interface
ms.date: 03/30/2017
api_name:
- IMetaDataEmit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit
helpviewer_keywords:
- IMetaDataEmit interface [.NET Framework metadata]
ms.assetid: 3b48fd47-7397-4e2c-8bec-8157aa08978c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 10942541b781d367820301588656b2f1fc2fd006
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59184416"
---
# <a name="imetadataemit-interface"></a>IMetaDataEmit, interface
Fournit des méthodes pour créer, modifier et enregistrer les métadonnées relatives à l’assembly dans la portée actuellement définie. Les métadonnées peuvent être stockées en mémoire ou enregistrées sur le disque.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ApplyEditAndContinue, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-applyeditandcontinue-method.md)|Met à jour de la portée d’assembly actuelle avec les modifications apportées dans le texte spécifié `pImport`.|  
|[DefineCustomAttribute, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definecustomattribute-method.md)|Crée une définition pour un attribut personnalisé avec la signature de métadonnées spécifié, à joindre à l’objet spécifié et obtient un jeton pour cette définition d’attribut personnalisé.|  
|[DefineEvent, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineevent-method.md)|Crée une définition pour un événement avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de l’événement.|  
|[DefineField, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definefield-method.md)|Crée une définition pour un champ avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de champ.|  
|[DefineImportMember, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineimportmember-method.md)|Crée une définition pour un membre d’un type qui est défini dans un module en dehors de la portée actuelle et obtient un jeton pour cette définition de référence.|  
|[DefineImportType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineimporttype-method.md)|Crée une définition pour une référence à un type qui est défini dans un module en dehors de la portée actuelle et obtient un jeton pour cette définition de référence.|  
|[DefineMemberRef, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md)|Crée une définition pour une référence à un membre d’un module en dehors de la portée actuelle et obtient un jeton pour cette définition de référence.|  
|[DefineMethod, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md)|Crée une définition pour une méthode avec la signature spécifiée et retourne un jeton pour cette définition de méthode.|  
|[DefineMethodImpl, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethodimpl-method.md)|Crée une définition pour l’implémentation d’une méthode héritée d’une interface et retourne un jeton pour cette définition de l’implémentation de la méthode.|  
|[DefineModuleRef, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemoduleref-method.md)|Crée la signature de métadonnées pour un module portant le nom spécifié.|  
|[DefineNestedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definenestedtype-method.md)|Crée la signature de métadonnées d’une définition de type et retourne un `mdTypeDef` jeton pour ce type, en spécifiant en outre que le type défini est un membre du type référencé par `tdEncloser`.|  
|[DefineParam, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineparam-method.md)|Crée une définition de paramètre avec la signature spécifiée pour la méthode référencée par le jeton spécifié et obtient un jeton pour cette définition de paramètre.|  
|[DefinePermissionSet, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepermissionset-method.md)|Crée une définition pour un jeu d’autorisations avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de jeu d’autorisations.|  
|[DefinePinvokeMap, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md)|Définit les fonctionnalités de la signature PInvoke de la méthode référencée par le jeton spécifié.|  
|[DefineProperty, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md)|Crée une définition de propriété pour le type spécifié, avec la valeur `get` et `set` accesseurs de méthode et obtient un jeton pour cette définition de propriété.|  
|[DefineSecurityAttributeSet, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definesecurityattributeset-method.md)|Crée un jeu d’autorisations de sécurité à joindre à l’objet référencé par le jeton spécifié.|  
|[DefineTypeDef, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetypedef-method.md)|Crée une définition de type pour un type common language runtime et obtient un jeton de métadonnées pour cette définition de type.|  
|[DefineTypeRefByName, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md)|Obtient les métadonnées jeton pour un type qui est défini dans un autre module en dehors de la portée actuelle.|  
|[DefineUserString, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md)|Obtient les métadonnées jeton pour la chaîne littérale spécifiée.|  
|[DeleteClassLayout, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-deleteclasslayout-method.md)|Détruit la signature de métadonnées de disposition de classe pour le type référencé par le jeton spécifié.|  
|[DeleteFieldMarshal, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-deletefieldmarshal-method.md)|Détruit la signature de métadonnées pour l’objet référencé par le jeton spécifié de marshaling de PInvoke.|  
|[DeletePinvokeMap, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-deletepinvokemap-method.md)|Détruit les métadonnées de mappage PInvoke pour l’objet référencé par le jeton spécifié.|  
|[DeleteToken, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-deletetoken-method.md)|Supprime le jeton spécifié à partir de la portée de métadonnées actuelle.|  
|[GetSaveSize, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-getsavesize-method.md)|Obtient la taille binaire estimée de l’assembly dans la portée actuelle.|  
|[GetTokenFromSig, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromsig-method.md)|Obtient un jeton pour la signature de métadonnées spécifié.|  
|[GetTokenFromTypeSpec, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md)|Obtient les métadonnées jeton pour le type avec la signature de métadonnées spécifié.|  
|[Merge, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-merge-method.md)|Ajoute la portée importée spécifiée à la liste des étendues à fusionner.|  
|[MergeEnd, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md)|Fusionne dans la portée actuelle toutes les portées de métadonnées spécifiées par un ou plusieurs appels précédents à `IMetaDataEmit::Merge`.|  
|[Save, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-save-method.md)|Enregistre toutes les métadonnées dans la portée actuelle dans le fichier à l’adresse spécifiée.|  
|[SaveToMemory, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-savetomemory-method.md)|Enregistre toutes les métadonnées dans la portée actuelle dans la zone de mémoire spécifiée.|  
|[SaveToStream, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-savetostream-method.md)|Enregistre toutes les métadonnées dans la portée actuelle spécifié `IStream`.|  
|[SetClassLayout, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setclasslayout-method.md)|Définit ou met à jour de la signature de disposition de classe d’un type défini par un appel antérieur à `IMetaDataEmit::DefineTypeDef`.|  
|[SetCustomAttributeValue, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setcustomattributevalue-method.md)|Définit ou met à jour la valeur d’un attribut personnalisé défini par un appel antérieur à `IMetaDataEmit::DefineCustomAttribute`.|  
|[SetEventProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-seteventprops-method.md)|Définit ou met à jour de la fonctionnalité spécifiée d’un événement défini par un appel antérieur à `IMetaDataEmit::DefineEvent`.|  
|[SetFieldMarshal, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setfieldmarshal-method.md)|Définit l’informations de marshaling pour le paramètre de retour de la méthode, champ ou la méthode référencée par le jeton spécifié de PInvoke.|  
|[SetFieldProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setfieldprops-method.md)|Définit ou met à jour la valeur par défaut pour le champ référencé par le jeton de champ spécifié.|  
|[SetFieldRVA, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setfieldrva-method.md)|Définit une valeur de variable globale pour l’adresse virtuelle relative du champ référencé par le jeton spécifié.|  
|[SetHandler, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md)|Définit la méthode référencée par le `IUnknown` pointeur comme un rappel de notification pour remappages du jeton.|  
|[SetMethodImplFlags, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmethodimplflags-method.md)|Définit ou met à jour de la signature de métadonnées de l’implémentation de méthode héritée référencée par le jeton spécifié.|  
|[SetMethodProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmethodprops-method.md)|Définit ou met à jour de la fonctionnalité, stockée à l’adresse virtuelle relative spécifiée, d’une méthode définie par un appel antérieur à `IMetaDataEmit::DefineMethod`.|  
|[SetModuleProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmoduleprops-method.md)|Met à jour les références à un module défini par un appel antérieur à `IMetaDataEmit::DefineModuleRef`.|  
|[SetParamProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setparamprops-method.md)|Définit ou modifie les fonctionnalités d’un paramètre de méthode qui a été défini par un appel antérieur à `IMetaDataEmit::DefineParam`.|  
|[SetParent, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setparent-method.md)|Qui établit le membre spécifié, tel que défini par un appel antérieur à `IMetaDataEmit::DefineMemberRef`, est un membre du type spécifié, tel que défini par un appel antérieur à `IMetaDataEmit::DefineTypeDef`.|  
|[SetPermissionSetProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setpermissionsetprops-method.md)|Définit ou met à jour des fonctionnalités de la signature de métadonnées d’un jeu d’autorisations défini par un appel antérieur à `IMetaDataEmit::DefinePermissionSet`.|  
|[SetPinvokeMap, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setpinvokemap-method.md)|Définit ou modifie les fonctionnalités de la signature de PInvoke d’une méthode, comme défini par un appel antérieur à `IMetaDataEmit::DefinePinvokeMap`.|  
|[SetPropertyProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setpropertyprops-method.md)|Définit les fonctionnalités stockées dans les métadonnées pour une propriété définie par un appel antérieur à `IMetaDataEmit::DefineProperty`.|  
|[SetRVA, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setrva-method.md)|Définit l’adresse virtuelle relative de la méthode spécifiée.|  
|[SetTypeDefProps, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-settypedefprops-method.md)|Définit les fonctionnalités d’un type défini par un appel antérieur à `IMetaDataEmit::DefineTypeDef`.|  
|[TranslateSigWithScope, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-translatesigwithscope-method.md)|Importe un assembly dans la portée actuelle et obtient une nouvelle signature de métadonnées pour la portée fusionnée.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
