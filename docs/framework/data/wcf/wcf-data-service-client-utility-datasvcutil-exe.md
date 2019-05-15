---
title: Utilitaire client des services de données WCF (DataSvcUtil.exe)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, generating client data classes
- WCF Data Services, client library
- WCF Data Services, consuming
ms.assetid: 9d0af606-929b-4c03-b307-3ef5f705afce
ms.openlocfilehash: bf812f45e4a4090becd8dfafe035d39d1d851860
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65583637"
---
# <a name="wcf-data-service-client-utility-datasvcutilexe"></a>Utilitaire client des services de données WCF (DataSvcUtil.exe)

DataSvcUtil.exe est un outil de ligne de commande fourni par WCF Data Services qui consomme un [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] flux et génère les classes de service de données client qui sont nécessaires pour accéder à un service de données à partir d’une application cliente .NET Framework. Cet utilitaire peut générer des classes de données à l'aide des sources de métadonnées suivantes :

- URI racine d'un service de données. L'utilitaire demande le document des métadonnées du service, qui décrit le modèle de données exposé par le service de données. Pour plus d’informations, consultez [OData : Document de métadonnées de service](https://go.microsoft.com/fwlink/?LinkId=186070).

- Un fichier de modèle de données (.csdl) défini en utilisant le langage de définition de schéma conceptuel (CSDL), tel que défini dans le [ \[MC-CSDL\]: Format de fichier de définition de schéma conceptuel](https://go.microsoft.com/fwlink/?LinkID=159072) spécification.

- Fichier .edmx créé à l'aide des outils Entity Data Model fournis avec l'Entity Framework. Pour plus d’informations, consultez le [ \[MC-EDMX\]: Entity Data Model for Data Services Packaging Format](https://go.microsoft.com/fwlink/?LinkID=178833) spécification.

Pour plus d'informations, voir [Procédure : Générer manuellement les Classes de Service de données Client](../../../../docs/framework/data/wcf/how-to-manually-generate-client-data-service-classes-wcf-data-services.md).

L’outil DataSvcUtil.exe est installé dans le répertoire .NET Framework. Dans de nombreux cas, celui-ci se trouve dans *C:\Windows\Microsoft.NET\Framework\v4.0*. Pour les systèmes 64 bits, celui-ci se trouve dans *C:\Windows\Microsoft.NET\Framework64\v4.0*. Vous pouvez également accéder à l’outil DataSvcUtil.exe à partir de l’invite de commandes développeur pour Visual Studio.

## <a name="syntax"></a>Syntaxe

```
datasvcutil /out:file [/in:file | /uri:serviceuri] [/dataservicecollection] [/language:devlang] [/nologo] [/version:ver] [/help]
```

## <a name="parameters"></a>Paramètres

|Option|Description|
|------------|-----------------|
|`/dataservicecollection`|Spécifie que le code nécessaire pour lier des objets aux contrôles est également généré.|
|`/help`<br /><br /> ou<br /><br /> `/?`|Affiche la syntaxe et les options de commande de l'outil.|
|`/in:` *\<file>*|Spécifie le fichier .csdl ou .edmx ou un répertoire qui contient le fichier.|
|`/language:`[VB&#124;CSharp]|Spécifie le langage des fichiers de code source générés. Le langage par défaut est C#.|
|`/nologo`|Supprime l'affichage du message de copyright.|
|`/out:` *\<file>*|Spécifie le nom du fichier de code source qui contient les classes de service de données client générées.|
|`/uri:` *\<string>*|L’URI du flux OData.|
|`/version:`[1.0&#124;2.0]|Spécifie la version acceptée la plus élevée d’OData. La version est déterminée selon la `DataServiceVersion` attribut de l’élément DataService dans les métadonnées de service de données retournées. Pour plus d’informations, consultez [gestion des versions du Service de données](../../../../docs/framework/data/wcf/data-service-versioning-wcf-data-services.md). Lorsque vous spécifiez le `/dataservicecollection` paramètre, vous devez également spécifier `/version:2.0` pour activer la liaison de données.|

## <a name="see-also"></a>Voir aussi

- [Génération de la bibliothèque cliente du service de données](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)
- [Guide pratique pour Ajouter une référence de Service de données](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md)
