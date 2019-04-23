---
title: 'Procédure : Afficher les certificats avec le composant logiciel enfichable MMC'
ms.date: 02/25/2019
helpviewer_keywords:
- certificates [WCF], viewing with the MMC snap-in
ms.assetid: 2b8782aa-ebb4-4ee7-974b-90299e356dc5
ms.openlocfilehash: 69f79b64250ff46524e7b4720d13351774875a3f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59167503"
---
# <a name="how-to-view-certificates-with-the-mmc-snap-in"></a><span data-ttu-id="e730a-102">Procédure : Afficher les certificats avec le composant logiciel enfichable MMC</span><span class="sxs-lookup"><span data-stu-id="e730a-102">How to: View certificates with the MMC snap-in</span></span>
<span data-ttu-id="e730a-103">Lorsque vous créez un client sécurisé ou un service, vous pouvez utiliser un [certificat](working-with-certificates.md) en tant que les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="e730a-103">When you create a secure client or service, you can use a [certificate](working-with-certificates.md) as the credential.</span></span> <span data-ttu-id="e730a-104">Par exemple, un type commun des informations d’identification est le certificat X.509, que vous créez avec le <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="e730a-104">For example, a common type of credential is the X.509 certificate, which you create with the <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A?displayProperty=nameWithType> method.</span></span> 

<span data-ttu-id="e730a-105">Il existe trois types différents de magasins de certificats que vous pouvez examiner avec la Console MMC (Microsoft Management) sur les systèmes de Windows :</span><span class="sxs-lookup"><span data-stu-id="e730a-105">There are three different types of certificate stores that you can examine with the Microsoft Management Console (MMC) on Windows systems:</span></span>

- <span data-ttu-id="e730a-106">Ordinateur local : Le magasin est local sur l’appareil et pour tous les utilisateurs sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e730a-106">Local computer: The store is local to the device and global to all users on the device.</span></span>

- <span data-ttu-id="e730a-107">Utilisateur actuel : Le magasin est local pour le compte d’utilisateur actuel sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e730a-107">Current user: The store is local to the current user account on the device.</span></span>

- <span data-ttu-id="e730a-108">Compte de service : Le magasin est local à un service particulier sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e730a-108">Service account: The store is local to a particular service on the device.</span></span>

## <a name="view-certificates-in-the-mmc-snap-in"></a><span data-ttu-id="e730a-109">Afficher les certificats dans le composant logiciel enfichable MMC</span><span class="sxs-lookup"><span data-stu-id="e730a-109">View certificates in the MMC snap-in</span></span> 

<span data-ttu-id="e730a-110">La procédure suivante montre comment les magasins sur votre appareil local pour rechercher un certificat approprié :</span><span class="sxs-lookup"><span data-stu-id="e730a-110">The following procedure demonstrates how to examine the stores on your local device to find an appropriate certificate:</span></span> 
  
1. <span data-ttu-id="e730a-111">Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *mmc*.</span><span class="sxs-lookup"><span data-stu-id="e730a-111">Select **Run** from the **Start** menu, and then enter *mmc*.</span></span> 

    <span data-ttu-id="e730a-112">La console MMC s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e730a-112">The MMC appears.</span></span> 
  
2. <span data-ttu-id="e730a-113">À partir de la **fichier** menu, sélectionnez **ajouter/supprimer un composant logiciel enfichable**.</span><span class="sxs-lookup"><span data-stu-id="e730a-113">From the **File** menu, select **Add/Remove Snap In**.</span></span> 
    
    <span data-ttu-id="e730a-114">Le **ajouter ou supprimer des composants logiciel enfichables** fenêtre s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e730a-114">The **Add or Remove Snap-ins** window appears.</span></span>
  
3. <span data-ttu-id="e730a-115">À partir de la **des composants logiciels enfichables disponibles** , choisissez **certificats**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e730a-115">From the **Available snap-ins** list, choose **Certificates**, then select **Add**.</span></span>  

    ![Ajouter le composant logiciel enfichable Certificats](./media/mmc-add-certificate-snap-in.png)
  
4. <span data-ttu-id="e730a-117">Dans le **enfichable Certificats** fenêtre, sélectionnez **compte d’ordinateur**, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e730a-117">In the **Certificates snap-in** window, select **Computer account**, and then select **Next**.</span></span> 
  
    <span data-ttu-id="e730a-118">Si vous le souhaitez, vous pouvez sélectionner **mon compte d’utilisateur** pour l’utilisateur actuel ou **compte de Service** pour un service particulier.</span><span class="sxs-lookup"><span data-stu-id="e730a-118">Optionally, you can select **My user account** for the current user or **Service account** for a particular service.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e730a-119">Si vous n’êtes pas un administrateur pour votre appareil, vous pouvez gérer des certificats uniquement pour votre compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e730a-119">If you're not an administrator for your device, you can manage certificates only for your user account.</span></span>
  
5. <span data-ttu-id="e730a-120">Dans le **sélectionner un ordinateur** fenêtre, laissez le champ **ordinateur Local** sélectionné, puis sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e730a-120">In the **Select Computer** window, leave **Local computer** selected, and then select **Finish**.</span></span>  
  
6. <span data-ttu-id="e730a-121">Dans le **ajouter ou supprimer des Snap-in** fenêtre, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="e730a-121">In the **Add or Remove Snap-in** window, select **OK**.</span></span>  
  
    ![Ajouter le composant logiciel enfichable Certificats](./media/mmc-certificate-snap-in-selected.png)

7. <span data-ttu-id="e730a-123">Facultatif : À partir de la **fichier** menu, sélectionnez **enregistrer** ou **Enregistrer sous** pour enregistrer le fichier de la console MMC pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e730a-123">Optional: From the **File** menu, select **Save** or **Save As** to save the MMC console file for later use.</span></span>  

8. <span data-ttu-id="e730a-124">Pour afficher vos certificats dans le composant logiciel enfichable MMC, sélectionnez **racine de la Console** dans le volet gauche, puis développez **certificats (ordinateur Local)**.</span><span class="sxs-lookup"><span data-stu-id="e730a-124">To view your certificates in the MMC snap-in, select **Console Root** in the left pane, then expand **Certificates (Local Computer)**.</span></span>

    <span data-ttu-id="e730a-125">Une liste de répertoires pour chaque type de certificat s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e730a-125">A list of directories for each type of certificate appears.</span></span> <span data-ttu-id="e730a-126">À partir de chaque répertoire du certificat, vous pouvez afficher, exporter, importer et supprimer ses certificats.</span><span class="sxs-lookup"><span data-stu-id="e730a-126">From each certificate directory, you can view, export, import, and delete its certificates.</span></span>

## <a name="view-certificates-with-the-certificate-manager-tool"></a><span data-ttu-id="e730a-127">Afficher les certificats avec l’outil Certificate Manager</span><span class="sxs-lookup"><span data-stu-id="e730a-127">View certificates with the Certificate Manager tool</span></span>

<span data-ttu-id="e730a-128">Vous pouvez également afficher, exporter, importer et supprimer des certificats à l’aide de l’outil Certificate Manager.</span><span class="sxs-lookup"><span data-stu-id="e730a-128">You can also view, export, import, and delete certificates by using the Certificate Manager tool.</span></span>

### <a name="to-view-certificates-for-the-local-device"></a><span data-ttu-id="e730a-129">Pour afficher les certificats de l’appareil local</span><span class="sxs-lookup"><span data-stu-id="e730a-129">To view certificates for the local device</span></span>

1. <span data-ttu-id="e730a-130">Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *certlm.msc*.</span><span class="sxs-lookup"><span data-stu-id="e730a-130">Select **Run** from the **Start** menu, and then enter *certlm.msc*.</span></span> 

    <span data-ttu-id="e730a-131">L’outil Gestionnaire de certificats pour l’appareil local s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e730a-131">The Certificate Manager tool for the local device appears.</span></span> 
  
2. <span data-ttu-id="e730a-132">Pour afficher vos certificats, sous **certificats - ordinateur Local** dans le volet gauche, développez le répertoire pour le type de certificat que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="e730a-132">To view your certificates, under **Certificates - Local Computer** in the left pane, expand the directory for the type of certificate you want to view.</span></span>

### <a name="to-view-certificates-for-the-current-user"></a><span data-ttu-id="e730a-133">Pour afficher des certificats pour l’utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="e730a-133">To view certificates for the current user</span></span>

1. <span data-ttu-id="e730a-134">Sélectionnez **exécuter** à partir de la **Démarrer** menu, puis entrez *certmgr.msc*.</span><span class="sxs-lookup"><span data-stu-id="e730a-134">Select **Run** from the **Start** menu, and then enter *certmgr.msc*.</span></span> 

    <span data-ttu-id="e730a-135">L’outil Gestionnaire de certificats pour l’utilisateur actuel s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e730a-135">The Certificate Manager tool for the current user appears.</span></span> 
  
2. <span data-ttu-id="e730a-136">Pour afficher vos certificats, sous **certificats - utilisateur actuel** dans le volet gauche, développez le répertoire pour le type de certificat que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="e730a-136">To view your certificates, under **Certificates - Current User** in the left pane, expand the directory for the type of certificate you want to view.</span></span>

## <a name="see-also"></a><span data-ttu-id="e730a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e730a-137">See also</span></span>

- [<span data-ttu-id="e730a-138">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="e730a-138">Working with certificates</span></span>](working-with-certificates.md)
- [<span data-ttu-id="e730a-139">Guide pratique pour Créer des certificats temporaires à utiliser pendant le développement</span><span class="sxs-lookup"><span data-stu-id="e730a-139">How to: Create temporary certificates for use during development</span></span>](how-to-create-temporary-certificates-for-use-during-development.md)
- [<span data-ttu-id="e730a-140">Guide pratique pour Récupérer l’empreinte numérique d’un certificat</span><span class="sxs-lookup"><span data-stu-id="e730a-140">How to: Retrieve the thumbprint of a certificate</span></span>](how-to-retrieve-the-thumbprint-of-a-certificate.md)
