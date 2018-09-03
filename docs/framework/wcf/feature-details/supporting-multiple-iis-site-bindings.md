---
title: Prise en charge de plusieurs liaisons de site IIS
ms.date: 03/30/2017
ms.assetid: 40440495-254d-45c8-a8c6-b29f364892ba
ms.openlocfilehash: 2c42ba7cf3713e5d165d10ce7049df8200d612fb
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482205"
---
# <a name="supporting-multiple-iis-site-bindings"></a>Prise en charge de plusieurs liaisons de site IIS
Lorsque vous hébergez un service Windows Communication Foundation (WCF) sous Internet Information Services (IIS) 7.0, vous souhaiterez fournir plusieurs adresses de base qui utilisent le même protocole sur le même site. Cela permet au même service de répondre à plusieurs URI différents. Cela est utile lorsque vous souhaitez héberger un service qui écoute sur http://www.contoso.com et http://contoso.com. Il est également utile de créer un service qui a une adresse de base pour les utilisateurs internes et une autre adresse de base pour les utilisateurs externes. Par exemple : http://internal.contoso.com et http://www.contoso.com.  
  
> [!NOTE]
>  Ces fonctionnalités ne sont disponibles qu'en utilisant le protocole HTTP.  
  
## <a name="multiple-base-addresses"></a>Plusieurs adresses de base  
 Cette fonctionnalité est uniquement disponible pour les services WCF hébergés sous IIS. Cette fonctionnalité n’est pas activée par défaut. Pour l’activer, vous devez ajouter le `multipleSiteBindingsEnabled` d’attribut à la <`serviceHostingEnvironment`> élément dans votre fichier Web.config de fichiers et affectez-lui la valeur `true`, comme illustré dans l’exemple suivant.  
  
```xml  
<serviceHostingEnvironment multipleSiteBindingsEnabled="true"/>  
```  
  
 Lorsque vous hébergez un service WCF dans IIS, IIS crée une adresse de base en fonction de l’URI vers le répertoire virtuel qui contient l’application. Vous pouvez ajouter des adresses de base supplémentaires utilisant le même protocole, à l’aide du gestionnaire des services IIS pour ajouter une ou plusieurs liaisons à votre site web. Pour chaque liaison, spécifiez un protocole (HTTP ou HTTPS), une adresse IP, un port et un nom d’hôte. Pour plus d’informations sur l’utilisation du Gestionnaire des Services Internet, consultez [Gestionnaire des services Internet (IIS 7)](https://go.microsoft.com/fwlink/?LinkId=164057). Pour plus d’informations sur l’ajout de liaisons à un site, consultez [créer un Site Web (IIS 7)](https://go.microsoft.com/fwlink/?LinkId=164060)  
  
 Spécification de plusieurs adresses de base pour le même site affecte le contenu de la page d’aide WCF, importation de schéma et les informations WSDL/MEX générées par le service. La page d’aide WCF affiche la ligne de commande à utiliser pour générer un client WCF qui peut communiquer avec le service. Cette ligne de commande contient uniquement la première adresse spécifiée dans la liaison IIS pour le site web. De même, lors de l'importation du schéma, seule la première adresse de base spécifiée dans la liaison IIS est utilisée. Les données WSDL et MEX contiennent toutes les adresses de base spécifiées dans les liaisons IIS.  
  
> [!WARNING]
>  Cela signifie que si un service possède deux adresses de base, une pour les utilisateurs internes et l'autre pour les utilisateurs externes, les deux sont spécifiées dans les informations WSDL/MEX générées par le service.
