---
title: Validation du registre des noms d'émetteurs
ms.date: 03/30/2017
ms.assetid: c4644dd1-dead-48ff-abeb-7bffae69a6ac
ms.openlocfilehash: aa6a71ced0f9bf969eb6c8800739f629810dd63f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645901"
---
# <a name="validating-issuer-name-registry"></a>Validation du registre des noms d'émetteurs
Le Registre de validation de nom d'émetteur (VINR) pour Windows Identity Foundation permet aux applications d'une architecture mutualisée de garantir qu'un jeton entrant a été publié par un locataire et un fournisseur d'identité approuvés. Cette fonctionnalité est particulièrement utile pour les applications partagée qui utilisent Microsoft Azure Active Directory car tous les jetons publiés par Microsoft Azure AD sont archivés avec le même certificat. Pour différencier les demandes de plusieurs locataires qui utilisent le même certificat, et par conséquent disposent de la même empreinte numérique, votre application doit rendre persistant le nom de l'émetteur pour chaque locataire pour exécuter la logique de validation. Le VINR fournit cette fonctionnalité, et il vous permet également d’ajouter une logique de validation personnalisée ou de stocker les données de Registre de l’émetteur dans les emplacements autres que le fichier de configuration. L’extension peut être ajoutée au pipeline WIF de votre application ou elle peut être utilisée de manière indépendante.  
  
 Le VINR est disponible sous forme de package NuGet. Pour plus d’informations, consultez [Téléchargement du package de validation du registre des noms d’émetteurs](../../../docs/framework/security/downloading-the-validating-issuer-name-registry-package.md).  
  
## <a name="scenarios"></a>Scénarios  
 Le VINR active le scénario principal suivant :  
  
- **Valider un jeton dans une Application mutualisée**: Dans ce scénario, une société nommée Litware a développé une application mutualisée qui utilise un fournisseur d’identité tels que Windows Azure AD. Cette application sert deux clients : Contoso et Fabrikam. Lorsqu'un utilisateur de Fabrikam s'authentifie auprès de l'application Litware, le jeton résultant de Microsoft Azure AD est signé avec son certificat standard et la demande est émise par Fabrikam. L'application doit vérifier que le nom de l'émetteur et le jeton sont valides, et doit différencier les requêtes de Contoso qui sont signées avec le même certificat de Microsoft Azure AD. Le VINR permet à une application de Litware de différencier et de valider plus facilement les demandes de plusieurs locataires tels que Contoso et Fabrikam.  
  
## <a name="features"></a>Fonctionnalités  
 La bibliothèque VINR offre les fonctionnalités suivantes :  
  
- **Nom de l’émetteur et Validation du jeton pour les Applications mutualisées**: Valide le jeton entrant en vérifiant le nom de l’émetteur (locataire) et si le jeton a été signé à l’aide d’un certificat valide du fournisseur d’identité.  
  
- **Extensibilité pour la logique de Validation personnalisée et de magasins de données**: Fournit l’extensibilité d’injecter votre propre logique de validation et spécifier un magasin de données autre que le fichier de configuration par défaut.
