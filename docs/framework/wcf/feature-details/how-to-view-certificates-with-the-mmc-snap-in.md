---
title: 'Procédure : Afficher les certificats avec le composant logiciel enfichable MMC'
ms.date: 02/25/2019
helpviewer_keywords:
- certificates [WCF], viewing with the MMC snap-in
ms.assetid: 2b8782aa-ebb4-4ee7-974b-90299e356dc5
ms.openlocfilehash: 69f79b64250ff46524e7b4720d13351774875a3f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972718"
---
# <a name="how-to-view-certificates-with-the-mmc-snap-in"></a>Procédure : Afficher les certificats avec le composant logiciel enfichable MMC
Lorsque vous créez un client sécurisé ou un service, vous pouvez utiliser un [certificat](working-with-certificates.md) en tant que les informations d’identification. Par exemple, un type commun des informations d’identification est le certificat X.509, que vous créez avec le <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A?displayProperty=nameWithType> (méthode). 

Il existe trois types différents de magasins de certificats que vous pouvez examiner avec la Console MMC (Microsoft Management) sur les systèmes de Windows :

- Ordinateur local : Le magasin est local sur l’appareil et pour tous les utilisateurs sur l’appareil.

- Utilisateur actuel : Le magasin est local pour le compte d’utilisateur actuel sur l’appareil.

- Compte de service : Le magasin est local à un service particulier sur l’appareil.

## <a name="view-certificates-in-the-mmc-snap-in"></a>Afficher les certificats dans le composant logiciel enfichable MMC 

La procédure suivante montre comment les magasins sur votre appareil local pour rechercher un certificat approprié : 
  
1. Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *mmc*. 

    La console MMC s’affiche. 
  
2. À partir de la **fichier** menu, sélectionnez **ajouter/supprimer un composant logiciel enfichable**. 
    
    Le **ajouter ou supprimer des composants logiciel enfichables** fenêtre s’affiche.
  
3. À partir de la **des composants logiciels enfichables disponibles** , choisissez **certificats**, puis sélectionnez **ajouter**.  

    ![Ajouter le composant logiciel enfichable Certificats](./media/mmc-add-certificate-snap-in.png)
  
4. Dans le **enfichable Certificats** fenêtre, sélectionnez **compte d’ordinateur**, puis sélectionnez **suivant**. 
  
    Si vous le souhaitez, vous pouvez sélectionner **mon compte d’utilisateur** pour l’utilisateur actuel ou **compte de Service** pour un service particulier. 

    > [!NOTE]
    > Si vous n’êtes pas un administrateur pour votre appareil, vous pouvez gérer des certificats uniquement pour votre compte d’utilisateur.
  
5. Dans le **sélectionner un ordinateur** fenêtre, laissez le champ **ordinateur Local** sélectionné, puis sélectionnez **Terminer**.  
  
6. Dans le **ajouter ou supprimer des Snap-in** fenêtre, sélectionnez **OK**.  
  
    ![Ajouter le composant logiciel enfichable Certificats](./media/mmc-certificate-snap-in-selected.png)

7. Facultatif : À partir de la **fichier** menu, sélectionnez **enregistrer** ou **Enregistrer sous** pour enregistrer le fichier de la console MMC pour une utilisation ultérieure.  

8. Pour afficher vos certificats dans le composant logiciel enfichable MMC, sélectionnez **racine de la Console** dans le volet gauche, puis développez **certificats (ordinateur Local)**.

    Une liste de répertoires pour chaque type de certificat s’affiche. À partir de chaque répertoire du certificat, vous pouvez afficher, exporter, importer et supprimer ses certificats.

## <a name="view-certificates-with-the-certificate-manager-tool"></a>Afficher les certificats avec l’outil Certificate Manager

Vous pouvez également afficher, exporter, importer et supprimer des certificats à l’aide de l’outil Certificate Manager.

### <a name="to-view-certificates-for-the-local-device"></a>Pour afficher les certificats de l’appareil local

1. Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *certlm.msc*. 

    L’outil Gestionnaire de certificats pour l’appareil local s’affiche. 
  
2. Pour afficher vos certificats, sous **certificats - ordinateur Local** dans le volet gauche, développez le répertoire pour le type de certificat que vous souhaitez afficher.

### <a name="to-view-certificates-for-the-current-user"></a>Pour afficher des certificats pour l’utilisateur actuel

1. Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *certmgr.msc*. 

    L’outil Gestionnaire de certificats pour l’utilisateur actuel s’affiche. 
  
2. Pour afficher vos certificats, sous **certificats - utilisateur actuel** dans le volet gauche, développez le répertoire pour le type de certificat que vous souhaitez afficher.

## <a name="see-also"></a>Voir aussi

- [Utilisation des certificats](working-with-certificates.md)
- [Guide pratique pour Créer des certificats temporaires à utiliser pendant le développement](how-to-create-temporary-certificates-for-use-during-development.md)
- [Guide pratique pour Récupérer l’empreinte numérique d’un certificat](how-to-retrieve-the-thumbprint-of-a-certificate.md)
