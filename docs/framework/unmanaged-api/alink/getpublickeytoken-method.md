---
title: GetPublicKeyToken, méthode
ms.date: 03/30/2017
api_name:
- IALink2.GetPublicKeyToken
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetPublicKeyToken
helpviewer_keywords:
- GetPublicKeyToken method
ms.assetid: 4a16374c-94b0-47b0-9fed-88c2b0cdccd4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 94a473d00110c07615ccdfc98bb8944e40dc30e3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405471"
---
# <a name="getpublickeytoken-method"></a><span data-ttu-id="0897b-102">GetPublicKeyToken, méthode</span><span class="sxs-lookup"><span data-stu-id="0897b-102">GetPublicKeyToken Method</span></span>
<span data-ttu-id="0897b-103">Récupère le jeton de clé publique pour un fichier ou un conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="0897b-103">Retrieves the public key token for a given keyfile or key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0897b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0897b-104">Syntax</span></span>  
  
```  
HRESULT GetPublicKeyToken(  
    LPCWSTR pszKeyFile,  
    LPCWSTR pszKeyContainer,  
    void* pvPublicKeyToken,  
    DWORD* pcbPublicKeyToken  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0897b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0897b-105">Parameters</span></span>  
 `pszKeyFile`  
 <span data-ttu-id="0897b-106">Nom de fichier de la clé.</span><span class="sxs-lookup"><span data-stu-id="0897b-106">Filename of the key.</span></span>  
  
 `pszKeyContainer`  
 <span data-ttu-id="0897b-107">Nom du conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="0897b-107">Name of the key container.</span></span>  
  
 `pvPublicKeyToken`  
 <span data-ttu-id="0897b-108">Adresse où le jeton de clé doit être stocké.</span><span class="sxs-lookup"><span data-stu-id="0897b-108">Address where key token is to be stored.</span></span>  
  
 `pcbPublicKeyToken`  
 <span data-ttu-id="0897b-109">Spécifie la taille, en octets, de la mémoire tampon indiqué par `pvPublicKeyToken`.</span><span class="sxs-lookup"><span data-stu-id="0897b-109">Specifies the size, in bytes, of the buffer indicated by `pvPublicKeyToken`.</span></span> <span data-ttu-id="0897b-110">Au retour, contient le nombre réel d’octets utilisés.</span><span class="sxs-lookup"><span data-stu-id="0897b-110">Upon return, contains actual number of bytes used.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0897b-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0897b-111">Return Value</span></span>  
 <span data-ttu-id="0897b-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0897b-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0897b-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0897b-113">Requirements</span></span>  
 <span data-ttu-id="0897b-114">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="0897b-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0897b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0897b-115">See Also</span></span>  
 [<span data-ttu-id="0897b-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0897b-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="0897b-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0897b-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="0897b-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="0897b-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
