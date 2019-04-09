---
title: IMetaDataImport::GetFieldProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetFieldProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetFieldProps
helpviewer_keywords:
- IMetaDataImport::GetFieldProps method [.NET Framework metadata]
- GetFieldProps method [.NET Framework metadata]
ms.assetid: 7b0e9b10-8cef-4ba6-8432-40bf63e65ab1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d7f8cccf8d583645982eb37f6afcb553914679ad
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075659"
---
# <a name="imetadataimportgetfieldprops-method"></a><span data-ttu-id="a8cef-102">IMetaDataImport::GetFieldProps, méthode</span><span class="sxs-lookup"><span data-stu-id="a8cef-102">IMetaDataImport::GetFieldProps Method</span></span>
<span data-ttu-id="a8cef-103">Obtient les métadonnées associées au champ référencé par le jeton FieldDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8cef-103">Gets metadata associated with the field referenced by the specified FieldDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8cef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8cef-104">Syntax</span></span>  
  
```  
HRESULT GetFieldProps (  
   [in]  mdFieldDef        mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szField,  
   [in]  ULONG             cchField,   
   [out] ULONG             *pchField,  
   [out] DWORD             *pdwAttr,  
   [in]  PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a8cef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8cef-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="a8cef-106">[in] Jeton FieldDef qui représente le champ pour obtenir les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="a8cef-106">[in] A FieldDef token that represents the field to get associated metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="a8cef-107">[out] Pointeur vers un jeton TypeDef qui représente le type de la classe à laquelle appartient le champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-107">[out] A pointer to a TypeDef token that represents the type of the class that the field belongs to.</span></span>  
  
 `szField`  
 <span data-ttu-id="a8cef-108">[out] Le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-108">[out] The name of the field.</span></span>  
  
 `cchField`  
 <span data-ttu-id="a8cef-109">[in] La taille en caractères larges de la mémoire tampon pour *szField*.</span><span class="sxs-lookup"><span data-stu-id="a8cef-109">[in] The size in wide characters of the buffer for *szField*.</span></span>  
  
 `pchField`  
 <span data-ttu-id="a8cef-110">[out] La taille réelle de la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="a8cef-110">[out] The actual size of the returned buffer.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="a8cef-111">[out] Indicateurs associés aux métadonnées du champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-111">[out] Flags associated with the field's metadata.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="a8cef-112">[in] Pointeur vers la valeur de métadonnées binaires qui décrit le champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-112">[in] A pointer to the binary metadata value that describes the field.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="a8cef-113">[out] La taille en octets de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="a8cef-113">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="a8cef-114">[out] Un indicateur qui spécifie le type de valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-114">[out] A flag that specifies the value type of the field.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="a8cef-115">[out] Une valeur constante pour le champ.</span><span class="sxs-lookup"><span data-stu-id="a8cef-115">[out] A constant value for the field.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="a8cef-116">[out] La taille en caractères de `ppValue`, ou zéro si aucune chaîne n’existe.</span><span class="sxs-lookup"><span data-stu-id="a8cef-116">[out] The size in chars of `ppValue`, or zero if no string exists.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8cef-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8cef-117">Requirements</span></span>  
 <span data-ttu-id="a8cef-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8cef-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8cef-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a8cef-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a8cef-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a8cef-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="a8cef-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a8cef-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a8cef-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8cef-122">See also</span></span>

- [<span data-ttu-id="a8cef-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="a8cef-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="a8cef-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="a8cef-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
