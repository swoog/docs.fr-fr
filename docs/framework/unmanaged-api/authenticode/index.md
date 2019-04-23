---
title: Authenticode (Informations de référence sur les API non managées)
ms.date: 03/30/2017
ms.assetid: 7e8cc303-6e77-4116-aa8b-7ea297a3a467
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408219307015d5c39cb581b3884ed9810f4c0566
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941621"
---
# <a name="authenticode-unmanaged-api-reference"></a><span data-ttu-id="87197-102">Authenticode (Informations de référence sur les API non managées)</span><span class="sxs-lookup"><span data-stu-id="87197-102">Authenticode (Unmanaged API Reference)</span></span>
<span data-ttu-id="87197-103">Prend en charge le module de création et de vérification des licences XrML Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87197-103">Supports the Authenticode XrML license creation and verification module.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="87197-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="87197-104">In This Section</span></span>  
 [<span data-ttu-id="87197-105">_AxlGetIssuerPublicKeyHash, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-105">_AxlGetIssuerPublicKeyHash Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/axlgetissuerpublickeyhash-function.md)  
 <span data-ttu-id="87197-106">Récupère le hachage SHA-1 de la clé publique associée à la clé privée utilisée pour signer le certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="87197-106">Retrieves the SHA-1 hash of the public key associated with the private key that is used to sign the specified certificate.</span></span>  
  
 [<span data-ttu-id="87197-107">_AxlPublicKeyBlobToPublicKeyToken, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-107">_AxlPublicKeyBlobToPublicKeyToken Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/axlpublickeyblobtopublickeytoken-function.md)  
 <span data-ttu-id="87197-108">Calcule le jeton de clé publique de nom fort à partir d'un format CSP PUBLICKEYBLOB.</span><span class="sxs-lookup"><span data-stu-id="87197-108">Computes the strong name public key token from a CSP PUBLICKEYBLOB format.</span></span>  
  
 [<span data-ttu-id="87197-109">_AxlRSAKeyValueToPublicKeyToken, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-109">_AxlRSAKeyValueToPublicKeyToken Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/axlrsakeyvaluetopublickeytoken-function.md)  
 <span data-ttu-id="87197-110">Convertit un modulo et un exposant en un jeton de clé publique de nom fort.</span><span class="sxs-lookup"><span data-stu-id="87197-110">Converts a Modulus and Exponent to a strong name public key token.</span></span>  
  
 [<span data-ttu-id="87197-111">CertFreeAuthenticodeSignerInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-111">CertFreeAuthenticodeSignerInfo Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodesignerinfo-function.md)  
 <span data-ttu-id="87197-112">Libère les ressources allouées pour la structure AXL_AUTHENTICODE_SIGNER_INFO.</span><span class="sxs-lookup"><span data-stu-id="87197-112">Frees resources allocated for the AXL_AUTHENTICODE_SIGNER_INFO structure.</span></span>  
  
 [<span data-ttu-id="87197-113">CertFreeAuthenticodeTimestamperInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-113">CertFreeAuthenticodeTimestamperInfo Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodetimestamperinfo-function.md)  
 <span data-ttu-id="87197-114">Libère les ressources allouées pour la structure AXL_AUTHENTICODE_TIMESTAMPER_INFO.</span><span class="sxs-lookup"><span data-stu-id="87197-114">Frees resources allocated for the AXL_AUTHENTICODE_TIMESTAMPER_INFO structure.</span></span>  
  
 [<span data-ttu-id="87197-115">CertTimestampAuthenticodeLicense, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-115">CertTimestampAuthenticodeLicense Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/certtimestampauthenticodelicense-function.md)  
 <span data-ttu-id="87197-116">Effectue un horodatage d'une licence XrML Authenticode créée par CertCreateAuthenticodeLicense.</span><span class="sxs-lookup"><span data-stu-id="87197-116">Time stamps an Authenticode XrML license created by CertCreateAuthenticodeLicense.</span></span>  
  
 [<span data-ttu-id="87197-117">CertVerifyAuthenticodeLicense, fonction</span><span class="sxs-lookup"><span data-stu-id="87197-117">CertVerifyAuthenticodeLicense Function</span></span>](../../../../docs/framework/unmanaged-api/authenticode/certverifyauthenticodelicense-function.md)  
 <span data-ttu-id="87197-118">Vérifie la validité d'une licence XrML Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87197-118">Verifies the validity of an Authenticode XrML license.</span></span>  
  
 [<span data-ttu-id="87197-119">AXL_AUTHENTICODE_SIGNER_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="87197-119">AXL_AUTHENTICODE_SIGNER_INFO Structure</span></span>](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md)  
 <span data-ttu-id="87197-120">Définit les informations du signataire Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87197-120">Defines the Authenticode signer information.</span></span>  
  
 [<span data-ttu-id="87197-121">AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="87197-121">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md)  
 <span data-ttu-id="87197-122">Définit les informations de l'horodateur Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87197-122">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87197-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87197-123">See also</span></span>

- [<span data-ttu-id="87197-124">Informations de référence sur les API non managées</span><span class="sxs-lookup"><span data-stu-id="87197-124">Unmanaged API Reference</span></span>](../../../../docs/framework/unmanaged-api/index.md)
