---
title: 'Comment : obtenir un certificat (WCF)'
ms.date: 03/30/2017
helpviewer_keywords:
- certificates [WCF], obtaining
ms.assetid: d53762fd-15ea-42dc-b0ea-6a6597aa23f7
ms.openlocfilehash: 368401d91aa2a83110631d583660d6ccebf8d4fc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491505"
---
# <a name="how-to-obtain-a-certificate-wcf"></a><span data-ttu-id="2fb61-102">Comment : obtenir un certificat (WCF)</span><span class="sxs-lookup"><span data-stu-id="2fb61-102">How to: Obtain a Certificate (WCF)</span></span>
<span data-ttu-id="2fb61-103">Utilisation de Windows Communication Foundation (WCF) fonctionnalités de qui utilisent des certificats X.509, vous devez d’abord obtenez des certificats.</span><span class="sxs-lookup"><span data-stu-id="2fb61-103">To use any of the Windows Communication Foundation (WCF) features of that use X.509 certificates, you just first obtain certificates.</span></span>  
  
### <a name="to-obtain-an-x509-certificate"></a><span data-ttu-id="2fb61-104">Pour obtenir un certificat X.509</span><span class="sxs-lookup"><span data-stu-id="2fb61-104">To obtain an X.509 certificate</span></span>  
  
1.  <span data-ttu-id="2fb61-105">Choisissez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fb61-105">Choose one of the following:</span></span>  
  
    -   <span data-ttu-id="2fb61-106">Achetez un certificat auprès d'une autorité de certification, telle que VeriSign, Inc.</span><span class="sxs-lookup"><span data-stu-id="2fb61-106">Purchase a certificate from a certification authority, such as VeriSign, Inc.</span></span>  
  
    -   <span data-ttu-id="2fb61-107">Installez votre propre service de certificats et faites en sorte qu'une autorité de certification signe les certificats.</span><span class="sxs-lookup"><span data-stu-id="2fb61-107">Set up your own certificate service and have a certification authority sign the certificates.</span></span> [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)]<span data-ttu-id="2fb61-108">, Windows 2000 Server, Windows 2000 Server Datacenter et Windows 2000 Datacenter Server incluent tous des services de certificat qui prennent en charge l'infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="2fb61-108">, Windows 2000 Server, Windows 2000 Server Datacenter, and Windows 2000 Datacenter Server all include certificate services that support public key infrastructure (PKI).</span></span> <span data-ttu-id="2fb61-109">Dans Windows Server 2008, utilisez le [Active Directory Certificate Services](http://go.microsoft.com/fwlink/?LinkID=153483) rôle pour gérer une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="2fb61-109">In Windows Server 2008, use the [Active Directory Certificate Services](http://go.microsoft.com/fwlink/?LinkID=153483) role to manage a certification authority.</span></span>  
  
    -   <span data-ttu-id="2fb61-110">Installez votre propre service de certificats et ne faites pas signer les certificats.</span><span class="sxs-lookup"><span data-stu-id="2fb61-110">Set up your own certificate service and do not have the certificates signed.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="2fb61-111">Quelle que soit la méthode adoptée, le destinataire de la demande SOAP contenant le certificat X.509 doit approuver ce dernier.</span><span class="sxs-lookup"><span data-stu-id="2fb61-111">Whichever approach you take, the recipient of the SOAP request that contains the X.509 certificate must trust the X.509 certificate.</span></span> <span data-ttu-id="2fb61-112">Cela signifie que le certificat X.509 ou un émetteur dans la chaîne de certificats se trouve dans le magasin de certificats Personnes de confiance et que le certificat X.509 ne se trouve pas dans le magasin de certificats non fiables.</span><span class="sxs-lookup"><span data-stu-id="2fb61-112">This means that the X.509 certificate or an issuer in the certificate chain is in the Trusted People certificate store and that the X.509 certificate is not in the Untrusted Certificates store.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2fb61-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fb61-113">See Also</span></span>  
 [<span data-ttu-id="2fb61-114">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="2fb61-114">Working with Certificates</span></span>](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="2fb61-115">Guide pratique pour créer des certificats temporaires à utiliser au cours du développement</span><span class="sxs-lookup"><span data-stu-id="2fb61-115">How to: Create Temporary Certificates for Use During Development</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development.md)
