---
title: 'Procédure : Spécifiez la chaîne de certificat d’autorité de certification utilisée pour vérifier les Signatures (WCF)'
ms.date: 03/30/2017
helpviewer_keywords:
- certificates [WCF], specifying the certificate authority certificate chain
- certificates [WCF], verifying signatures
ms.assetid: 7c719355-aa41-4567-80d0-5115a8cf73fd
ms.openlocfilehash: 8d44e9f9278a212813fca5e77ebfca72734c60d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648782"
---
# <a name="how-to-specify-the-certificate-authority-certificate-chain-used-to-verify-signatures-wcf"></a>Procédure : Spécifiez la chaîne de certificat d’autorité de certification utilisée pour vérifier les Signatures (WCF)
Lorsque Windows Communication Foundation (WCF) reçoit un message SOAP signé à l’aide d’un certificat X.509, par défaut il vérifie que le certificat X.509 a été émis par une autorité de certification approuvée. Il consulte pour cela un magasin de certificats et détermine si le certificat de cette autorité de certification a été désigné comme approuvé. Dans l’ordre pour WCF effectuer cette détermination, la chaîne de certificat de l’autorité de certification doit être installée dans le magasin de certificats correct.  
  
### <a name="to-install-a-certification-authority-certificate-chain"></a>Pour installer une chaîne de certificats d'autorité de certification  
  
-   Pour chaque autorité de certification qu’un destinataire de message SOAP prévoit d’approuver les certificats X.509 émis à partir, installer la chaîne de certificat de l’autorité de certification dans le magasin de certificats que WCF est configuré pour récupérer des certificats X.509 à partir.  
  
     Par exemple, si un destinataire de message SOAP prévoit d’approuver des certificats X.509 publiés par Microsoft, chaîne de certificat de l’autorité de certification pour Microsoft doit être installée dans le magasin de certificats WCF est configuré pour rechercher des certificats X.509. Le magasin de certificats dans lequel WCF recherche de certificats X.509 peut être spécifié dans le code ou de configuration. Par exemple, cela peut être spécifié dans le code à l’aide du <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A> méthode ou dans la configuration de plusieurs manières, y compris le [ \<serviceCertificate >](../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-clientcredentials-element.md) .  
  
     Windows étant fourni avec un ensemble de chaînes de certificats par défaut pour les autorités de certification approuvées, il ne sera peut-être pas nécessaire d'installer la chaîne de certificats pour toutes les autorités de certification.  
  
    1.  Exportez la chaîne de certificats d'autorité de certification.  
  
         La procédure exacte dépend de l'autorité de certification. Si l’autorité de certification est en cours d’exécution des Services de certificats Microsoft, sélectionnez **télécharger un certificat autorité de certification, chaîne de certificats ou la liste de révocation**, puis choisissez **certificat d’autorité de certification télécharger**.  
  
    2.  Importez la chaîne de certificats d'autorité de certification.  
  
         Dans la console MMC (Microsoft Management Console), ouvrez le composant logiciel enfichable Certificats. Pour le magasin de certificats que WCF est configuré pour récupérer des certificats X.509 dans, sélectionnez le **racine de confiance** **autorités de Certification** dossier. Sous le **Trusted Root Certification Authorities** dossier, avec le bouton droit le **certificats** dossier, pointez sur **toutes les tâches**, puis cliquez sur **importation** . Fournissez le fichier exporté à l'étape a.  
  
         Pour plus d’informations sur l’utilisation du composant logiciel enfichable certificats avec MMC, consultez [Comment : Afficher les certificats avec le composant logiciel enfichable MMC](../../../../docs/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in.md).  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation des certificats](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
