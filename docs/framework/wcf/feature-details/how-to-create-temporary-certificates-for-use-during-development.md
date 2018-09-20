---
title: 'Comment : créer des certificats temporaires à utiliser au cours du développement'
ms.date: 03/30/2017
helpviewer_keywords:
- certificates [WCF], creating temporary certificates
- temporary certificates [WCF]
ms.assetid: bc5f6637-5513-4d27-99bb-51aad7741e4a
ms.openlocfilehash: 2d0301b040d0fd9865eaf5c3f96fe320ccfd8488
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46485309"
---
# <a name="how-to-create-temporary-certificates-for-use-during-development"></a><span data-ttu-id="7cc56-102">Comment : créer des certificats temporaires à utiliser au cours du développement</span><span class="sxs-lookup"><span data-stu-id="7cc56-102">How to: Create Temporary Certificates for Use During Development</span></span>

<span data-ttu-id="7cc56-103">Lorsque vous développez un service sécurisé ou un client à l’aide de Windows Communication Foundation (WCF), il est souvent nécessaire de fournir un certificat X.509 à utiliser comme informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="7cc56-103">When developing a secure service or client using Windows Communication Foundation (WCF), it is often necessary to supply an X.509 certificate to be used as a credential.</span></span> <span data-ttu-id="7cc56-104">Le certificat fait en général partie d'une chaîne de certificats dont l'autorité racine est présente dans le magasin d'Autorités de certification racines de confiance de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cc56-104">The certificate typically is part of a chain of certificates with a root authority found in the Trusted Root Certification Authorities store of the computer.</span></span> <span data-ttu-id="7cc56-105">Une chaîne de certificats vous permet de définir la portée d'un jeu de certificats où en général l'autorité racine provient de votre organisation ou votre division.</span><span class="sxs-lookup"><span data-stu-id="7cc56-105">Having a certificate chain enables you to scope a set of certificates where typically the root authority is from your organization or business unit.</span></span> <span data-ttu-id="7cc56-106">Pour émuler ce scénario au moment du développement, vous pouvez créer deux certificats pour satisfaire les conditions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7cc56-106">To emulate this at development time, you can create two certificates to satisfy the security requirements.</span></span> <span data-ttu-id="7cc56-107">Le premier est un certificat auto-signé placé dans le magasin d'Autorités de certification racines de confiance. Le deuxième certificat est créé à partir du premier et placé dans le magasin personnel de l'emplacement de l'ordinateur local ou dans le magasin personnel de l'emplacement de l'utilisateur actif.</span><span class="sxs-lookup"><span data-stu-id="7cc56-107">The first is a self-signed certificate that is placed in the Trusted Root Certification Authorities store, and the second certificate is created from the first and is placed in either the Personal store of the Local Machine location, or the Personal store of the Current User location.</span></span> <span data-ttu-id="7cc56-108">Cette rubrique décrit les étapes pour créer ces deux certificats à l’aide de la commande Powershell [New-SelfSignedCertificate)](/powershell/module/pkiclient/new-selfsignedcertificate) applet de commande.</span><span class="sxs-lookup"><span data-stu-id="7cc56-108">This topic walks through the steps to create these two certificates using the Powershell [New-SelfSignedCertificate)](/powershell/module/pkiclient/new-selfsignedcertificate) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7cc56-109">Les certificats qui génère l’applet de commande New-SelfSignedCertificate sont fournis uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="7cc56-109">The certificates that the New-SelfSignedCertificate cmdlet generates are provided for testing purposes only.</span></span> <span data-ttu-id="7cc56-110">Lorsque vous déployez un service ou un client, veillez à utiliser un certificat approprié fourni par une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="7cc56-110">When deploying a service or client, be sure to use an appropriate certificate provided by a certification authority.</span></span> <span data-ttu-id="7cc56-111">Cela peut provenir d’un serveur de certificats Windows Server dans votre organisation ou un tiers.</span><span class="sxs-lookup"><span data-stu-id="7cc56-111">This could either be from a Windows Server certificate server in your organization or a third party.</span></span>
>
> <span data-ttu-id="7cc56-112">Par défaut, le [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate) applet de commande crée des certificats auto-signés et ces certificats ne sont pas sécurisés.</span><span class="sxs-lookup"><span data-stu-id="7cc56-112">By default, the [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate) cmdlet creates certificates that are self-signed and these certificates are insecure.</span></span> <span data-ttu-id="7cc56-113">Placer les certificats auto-signés dans Trusted Root Certification Authorities store vous permet de créer un environnement de développement plus fidèlement votre environnement de déploiement.</span><span class="sxs-lookup"><span data-stu-id="7cc56-113">Placing the self-signed certificates in the Trusted Root Certification Authorities store enables you to create a development environment that more closely simulates your deployment environment.</span></span>

 <span data-ttu-id="7cc56-114">Pour plus d’informations sur la création et l’utilisation de certificats, consultez [utilisation des certificats](working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-114">For more information about creating and using certificates, see [Working with Certificates](working-with-certificates.md).</span></span> <span data-ttu-id="7cc56-115">Pour plus d’informations sur l’utilisation d’un certificat comme information d’identification, consultez [Securing Services and Clients](securing-services-and-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-115">For more information about using a certificate as a credential, see [Securing Services and Clients](securing-services-and-clients.md).</span></span> <span data-ttu-id="7cc56-116">Pour obtenir un didacticiel sur l’utilisation de la technologie Authenticode de Microsoft, consultez [Authenticode Overviews and Tutorials](https://go.microsoft.com/fwlink/?LinkId=88919).</span><span class="sxs-lookup"><span data-stu-id="7cc56-116">For a tutorial about using Microsoft Authenticode technology, see [Authenticode Overviews and Tutorials](https://go.microsoft.com/fwlink/?LinkId=88919).</span></span>

## <a name="to-create-a-self-signed-root-authority-certificate-and-export-the-private-key"></a><span data-ttu-id="7cc56-117">Pour créer un certificat d'autorité racine auto-signé et exporter la clé privée</span><span class="sxs-lookup"><span data-stu-id="7cc56-117">To create a self-signed root authority certificate and export the private key</span></span>

<span data-ttu-id="7cc56-118">La commande suivante crée un certificat auto-signé avec le nom du sujet du « RootCA » dans le magasin utilisateur actuel personnel.</span><span class="sxs-lookup"><span data-stu-id="7cc56-118">The following command creates a self-signed certificate with a subject name of "RootCA" in the Current User Personal store.</span></span>

```powershell
PS $rootCert = New-SelfSignedCertificate -CertStoreLocation cert:\CurrentUser\My -DnsName "RootCA" -TextExtension @("1.3.6.1.4.1.311.21.10={text}1.3.6.1.5.5.7.3.1,1.3.6.1.5.5.7.3.2")
```

<span data-ttu-id="7cc56-119">Nous avons besoin d’exporter le certificat vers un fichier PFX afin qu’il puisse être importé à là où cela est nécessaire dans une étape ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7cc56-119">We need to export the certificate to a PFX file so that it can be imported to where it's needed in a later step.</span></span> <span data-ttu-id="7cc56-120">Lorsque vous exportez un certificat avec la clé privée, un mot de passe est nécessaire pour les protéger.</span><span class="sxs-lookup"><span data-stu-id="7cc56-120">When exporting a certificate with the private key, a password is needed to protect it.</span></span> <span data-ttu-id="7cc56-121">Nous enregistrons le mot de passe dans un `SecureString` et utiliser le [Export-PfxCertificate](/powershell/module/pkiclient/export-pfxcertificate) applet de commande pour exporter le certificat avec la clé privée associée à un fichier PFX.</span><span class="sxs-lookup"><span data-stu-id="7cc56-121">We save the password in a `SecureString` and use the [Export-PfxCertificate](/powershell/module/pkiclient/export-pfxcertificate) cmdlet to export the certificate with the associated private key to a PFX file.</span></span> <span data-ttu-id="7cc56-122">Nous enregistrons également simplement le certificat public dans un fichier de bibliothèque CRT, en utilisant le [Export-Certificate](/powershell/module/pkiclient/export-certificate) applet de commande.</span><span class="sxs-lookup"><span data-stu-id="7cc56-122">We also save just the public certificate into a CRT file using the [Export-Certificate](/powershell/module/pkiclient/export-certificate) cmdlet.</span></span>

```powershell
PS [System.Security.SecureString]$rootcertPassword = ConvertTo-SecureString -String "password" -Force -AsPlainText
PS [String]$rootCertPath = Join-Path -Path 'cert:\CurrentUser\My\' -ChildPath "$($rootcert.Thumbprint)"
PS Export-PfxCertificate -Cert $rootCertPath -FilePath 'RootCA.pfx' -Password $rootcertPassword
PS Export-Certificate -Cert $rootCertPath -FilePath 'RootCA.crt'
```

## <a name="to-create-a-new-certificate-signed-by-a-root-authority-certificate"></a><span data-ttu-id="7cc56-123">Pour créer un nouveau certificat signé par un certificat d'autorité racine</span><span class="sxs-lookup"><span data-stu-id="7cc56-123">To create a new certificate signed by a root authority certificate</span></span>

<span data-ttu-id="7cc56-124">La commande suivante crée un certificat signé par le `RootCA` avec un nom de sujet de « SignedByRootCA » à l’aide de la clé privée de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="7cc56-124">The following command creates a certificate signed by the `RootCA` with a subject name of "SignedByRootCA" using the private key of the issuer.</span></span>

```powershell
PS $testCert = New-SelfSignedCertificate -CertStoreLocation Cert:\LocalMachine\My -DnsName "SignedByRootCA" -KeyExportPolicy Exportable -KeyLength 2048 -KeyUsage DigitalSignature,KeyEncipherment -Signer $rootCert
```

<span data-ttu-id="7cc56-125">De même, nous enregistrons le certificat signé avec la clé privée dans un fichier PFX et uniquement la clé publique dans un fichier de bibliothèque CRT.</span><span class="sxs-lookup"><span data-stu-id="7cc56-125">Similarly, we save the signed certificate with private key into a PFX file and just the public key into a CRT file.</span></span>

```powershell
PS [String]$testCertPath = Join-Path -Path 'cert:\LocalMachine\My\' -ChildPath "$($testCert.Thumbprint)"
PS Export-PfxCertificate -Cert $testCertPath -FilePath testcert.pfx -Password $rootcertPassword
PS Export-Certificate -Cert $testCertPath -FilePath testcert.crt
```

## <a name="installing-a-certificate-in-the-trusted-root-certification-authorities-store"></a><span data-ttu-id="7cc56-126">Installation d'un certificat dans le magasin d'Autorités de certification racines de confiance</span><span class="sxs-lookup"><span data-stu-id="7cc56-126">Installing a Certificate in the Trusted Root Certification Authorities Store</span></span>

<span data-ttu-id="7cc56-127">Une fois qu'un certificat auto-signé est créé, vous pouvez l'installer dans le magasin d'Autorités de certification racines de confiance.</span><span class="sxs-lookup"><span data-stu-id="7cc56-127">Once a self-signed certificate is created, you can install it in the Trusted Root Certification Authorities store.</span></span> <span data-ttu-id="7cc56-128">Tous les certificats signés à ce stade avec le certificat sont approuvés par l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cc56-128">Any certificates that are signed with the certificate at this point are trusted by the computer.</span></span> <span data-ttu-id="7cc56-129">Pour cette raison, supprimez le certificat du magasin dès que vous n'en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="7cc56-129">For this reason, delete the certificate from the store as soon as you no longer need it.</span></span> <span data-ttu-id="7cc56-130">Lorsque vous supprimez ce certificat d'autorité racine, tous les autres certificats ayant signé à l'aide de ce dernier ne sont plus autorisés.</span><span class="sxs-lookup"><span data-stu-id="7cc56-130">When you delete this root authority certificate, all other certificates that signed with it become unauthorized.</span></span> <span data-ttu-id="7cc56-131">Les certificats d'autorité racines sont un simple mécanisme qui permet de définir la portée d'un groupe de certificats selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="7cc56-131">Root authority certificates are simply a mechanism whereby a group of certificates can be scoped as necessary.</span></span> <span data-ttu-id="7cc56-132">Par exemple, dans les applications d'égal à égal, l'autorité racine n'est pas nécessaire le plus souvent dans la mesure où l'identité d'un individu est garantie par le certificat qu'il fournit.</span><span class="sxs-lookup"><span data-stu-id="7cc56-132">For example, in peer-to-peer applications, there is typically no need for a root authority because you simply trust the identity of an individual by its supplied certificate.</span></span>

### <a name="to-install-a-self-signed-certificate-in-the-trusted-root-certification-authorities"></a><span data-ttu-id="7cc56-133">Pour installer un certificat auto-signé dans les Autorités de certification racines de confiance</span><span class="sxs-lookup"><span data-stu-id="7cc56-133">To install a self-signed certificate in the Trusted Root Certification Authorities</span></span>

1. <span data-ttu-id="7cc56-134">Ouvrez le composant logiciel enfichable Certificat.</span><span class="sxs-lookup"><span data-stu-id="7cc56-134">Open the certificate snap-in.</span></span> <span data-ttu-id="7cc56-135">Pour plus d’informations, consultez [Guide pratique pour afficher des certificats à l’aide du composant logiciel enfichable MMC](how-to-view-certificates-with-the-mmc-snap-in.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-135">For more information, see [How to: View Certificates with the MMC Snap-in](how-to-view-certificates-with-the-mmc-snap-in.md).</span></span>

2. <span data-ttu-id="7cc56-136">Ouvrez le dossier pour stocker le certificat, soit **Ordinateur local** , soit **Utilisateur actuel**.</span><span class="sxs-lookup"><span data-stu-id="7cc56-136">Open the folder to store the certificate, either the **Local Computer** or the **Current User**.</span></span>

3. <span data-ttu-id="7cc56-137">Ouvrez le dossier **Autorités de certification racines de confiance** .</span><span class="sxs-lookup"><span data-stu-id="7cc56-137">Open the **Trusted Root Certification Authorities** folder.</span></span>

4. <span data-ttu-id="7cc56-138">Cliquez avec le bouton droit sur le dossier **Certificats** et cliquez sur **Toutes les tâches**, puis cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="7cc56-138">Right-click the **Certificates** folder and click **All Tasks**, then click **Import**.</span></span>

5. <span data-ttu-id="7cc56-139">Suivez les instructions de l'Assistant à l'écran pour importer TempCa.cer dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="7cc56-139">Follow the on-screen wizard instructions to import the TempCa.cer into the store.</span></span>

## <a name="using-certificates-with-wcf"></a><span data-ttu-id="7cc56-140">L’utilisation de certificats avec WCF</span><span class="sxs-lookup"><span data-stu-id="7cc56-140">Using certificates With WCF</span></span>

<span data-ttu-id="7cc56-141">Une fois que vous avez configuré les certificats temporaires, vous pouvez les utiliser pour développer des solutions WCF qui spécifient des certificats comme un type d'informations d'identification du client.</span><span class="sxs-lookup"><span data-stu-id="7cc56-141">Once you have set up the temporary certificates, you can use them to develop WCF solutions that specify certificates as a client credential type.</span></span> <span data-ttu-id="7cc56-142">Par exemple, la configuration XML suivante spécifie la sécurité du message et un certificat comme type d'informations d'identification du client.</span><span class="sxs-lookup"><span data-stu-id="7cc56-142">For example, the following XML configuration specifies message security and a certificate as the client credential type.</span></span>

### <a name="to-specify-a-certificate-as-the-client-credential-type"></a><span data-ttu-id="7cc56-143">Pour spécifier un certificat comme type d'informations d'identification du client</span><span class="sxs-lookup"><span data-stu-id="7cc56-143">To specify a certificate as the client credential type</span></span>

- <span data-ttu-id="7cc56-144">Dans le fichier de configuration d'un service, utilisez le XML suivant pour affecter au mode de sécurité la valeur Message, et au type d'informations d'identification du client la valeur Certificat.</span><span class="sxs-lookup"><span data-stu-id="7cc56-144">In the configuration file for a service, use the following XML to set the security mode to message, and the client credential type to certificate.</span></span>

    ```xml
    <bindings>
      <wsHttpBinding>
        <binding name="CertificateForClient">
          <security>
            <message clientCredentialType="Certificate" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    ```

<span data-ttu-id="7cc56-145">Dans le fichier de configuration pour un client, utilisez le code XML suivant pour spécifier que le certificat est trouvé dans le magasin de l’utilisateur et peut être trouvé en recherchant le champ SubjectName pour la valeur « CohoWinery ».</span><span class="sxs-lookup"><span data-stu-id="7cc56-145">In the configuration file for a client, use the following XML to specify that the certificate is found in the user’s store, and can be found by searching the SubjectName field for the value "CohoWinery."</span></span>

```xml
<behaviors>
  <endpointBehaviors>
    <behavior name="CertForClient">
      <clientCredentials>
        <clientCertificate findValue="CohoWinery" x509FindType="FindBySubjectName" />
       </clientCredentials>
     </behavior>
   </endpointBehaviors>
</behaviors>
```

<span data-ttu-id="7cc56-146">Pour plus d’informations sur l’utilisation de certificats dans WCF, consultez [utilisation des certificats](working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="7cc56-146">For more information about using certificates in WCF, see [Working with Certificates](working-with-certificates.md).</span></span>

## <a name="net-framework-security"></a><span data-ttu-id="7cc56-147">sécurité du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7cc56-147">.NET Framework security</span></span>

<span data-ttu-id="7cc56-148">Veillez à supprimer tous les certificats d'autorité racines temporaires des dossiers **Autorités de certification racines de confiance** et **Personnel** en cliquant avec le bouton droit sur le certificat, en cliquant sur ensuite **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="7cc56-148">Be sure to delete any temporary root authority certificates from the **Trusted Root Certification Authorities** and **Personal** folders by right-clicking the certificate, then clicking **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cc56-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc56-149">See also</span></span>

- [<span data-ttu-id="7cc56-150">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="7cc56-150">Working with Certificates</span></span>](working-with-certificates.md)
- [<span data-ttu-id="7cc56-151">Guide pratique pour afficher des certificats à l’aide du composant logiciel enfichable MMC</span><span class="sxs-lookup"><span data-stu-id="7cc56-151">How to: View Certificates with the MMC Snap-in</span></span>](how-to-view-certificates-with-the-mmc-snap-in.md)
- [<span data-ttu-id="7cc56-152">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="7cc56-152">Securing Services and Clients</span></span>](securing-services-and-clients.md)