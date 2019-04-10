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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211924"
---
# <a name="imetadataimport2-interface"></a><span data-ttu-id="c0963-102">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="c0963-102">IMetaDataImport2 Interface</span></span>
<span data-ttu-id="c0963-103">Étend la [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface pour fournir la possibilité de travailler avec les types génériques.</span><span class="sxs-lookup"><span data-stu-id="c0963-103">Extends the [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface to provide the capability of working with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c0963-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0963-104">Methods</span></span>  
  
|<span data-ttu-id="c0963-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-105">Method</span></span>|<span data-ttu-id="c0963-106">Description</span><span class="sxs-lookup"><span data-stu-id="c0963-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c0963-107">EnumGenericParamConstraints, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-107">EnumGenericParamConstraints Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparamconstraints-method.md)|<span data-ttu-id="c0963-108">Obtient un énumérateur pour un tableau de contraintes de paramètre générique associé au paramètre générique représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0963-108">Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.</span></span>|  
|[<span data-ttu-id="c0963-109">EnumGenericParams, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-109">EnumGenericParams Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enumgenericparams-method.md)|<span data-ttu-id="c0963-110">Obtient un énumérateur pour un tableau de jetons de paramètre générique associé au TypeDef spécifié ou le MethodDef jeton.</span><span class="sxs-lookup"><span data-stu-id="c0963-110">Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.</span></span>|  
|[<span data-ttu-id="c0963-111">EnumMethodSpecs, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-111">EnumMethodSpecs Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-enummethodspecs-method.md)|<span data-ttu-id="c0963-112">Obtient un énumérateur pour un tableau de jetons MethodSpec associé à le MethodDef ou MemberRef spécifié de jeton.</span><span class="sxs-lookup"><span data-stu-id="c0963-112">Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.</span></span>|  
|[<span data-ttu-id="c0963-113">GetGenericParamConstraintProps, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-113">GetGenericParamConstraintProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getgenericparamconstraintprops-method.md)|<span data-ttu-id="c0963-114">Obtient les métadonnées associées à la contrainte de paramètre générique représentée par le jeton de la contrainte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c0963-114">Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.</span></span>|  
|[<span data-ttu-id="c0963-115">GetGenericParamProps, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-115">GetGenericParamProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getgenericparamprops-method.md)|<span data-ttu-id="c0963-116">Obtient les métadonnées associées au paramètre générique représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0963-116">Gets the metadata associated with the generic parameter represented by the specified token.</span></span>|  
|[<span data-ttu-id="c0963-117">GetMethodSpecProps, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-117">GetMethodSpecProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getmethodspecprops-method.md)|<span data-ttu-id="c0963-118">Obtient le jeton de signature de métadonnées de la méthode référencée par le MethodSpec spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0963-118">Gets the metadata signature of the method referenced by the specified MethodSpec token.</span></span>|  
|[<span data-ttu-id="c0963-119">GetPEKind, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-119">GetPEKind Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md)|<span data-ttu-id="c0963-120">Obtient une valeur qui identifie la nature du code dans un fichier exécutable portable (PE) de fichiers, en général, un fichier DLL ou EXE, défini dans la portée de métadonnées actuelle</span><span class="sxs-lookup"><span data-stu-id="c0963-120">Gets a value identifying the nature of the code in a portable executable (PE) file, typically a DLL or EXE file, defined in the current metadata scope</span></span>|  
|[<span data-ttu-id="c0963-121">GetVersionString, méthode</span><span class="sxs-lookup"><span data-stu-id="c0963-121">GetVersionString Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getversionstring-method.md)|<span data-ttu-id="c0963-122">Obtient le numéro de version du runtime qui a été utilisé pour générer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c0963-122">Gets the version number of the runtime that was used to build the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c0963-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0963-123">Requirements</span></span>  
 <span data-ttu-id="c0963-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0963-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0963-125">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c0963-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c0963-126">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0963-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="c0963-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c0963-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c0963-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0963-128">See also</span></span>

- <xref:System.Reflection.PortableExecutableKinds>
- [<span data-ttu-id="c0963-129">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="c0963-129">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="c0963-130">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="c0963-130">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
