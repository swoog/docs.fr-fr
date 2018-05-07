---
title: '@ServiceHost'
ms.date: 03/30/2017
ms.assetid: 96ba6967-00f2-422f-9aa7-15de4d33ebf3
ms.openlocfilehash: 5498c300ab126bbc4e08cd228e3e7b48e905932e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="servicehost"></a>@ServiceHost
Associe la fabrique utilisée pour générer l'hôte de service au service à héberger ainsi qu'à d'autres aspects de programmation requis pour compiler le code d'hébergement fourni dans le fichier .svc ou pour y accéder.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
<% @ServiceHost   
Service = "Service, ServiceNamespace"   
Factory = "Factory, FactoryNamespace"  
Debug = "Debug"  
Language = "Language"   
CodeBehind = "CodeBehind"%>  
```  
  
## <a name="attributes"></a>Attributs  
  
#### <a name="service"></a>Service  
 Nom de type CLR du service hébergé. Il doit s'agir d'un nom qualifié correspondant à un type qui implémente un ou plusieurs contacts du service.  
  
#### <a name="factory"></a>Fabrique  
 Nom de type CLR correspondant à la fabrique de l'hôte de service utilisée pour instancier l'hôte de service. Cet attribut est facultatif. S'il n'est pas spécifié, le <xref:System.ServiceModel.Activation.ServiceHostFactory> par défaut est utilisé et renvoie une instance de <xref:System.ServiceModel.ServiceHost>.  
  
#### <a name="debug"></a>Débogage  
 Indique si le service Windows Communication Foundation (WCF) doit être compilé avec les symboles de débogage. `true` Si le service WCF doit être compilé avec les symboles de débogage ; dans le cas contraire, `false`.  
  
#### <a name="language"></a>Langue  
 Spécifie le langage utilisé lors de la compilation de l'intégralité du code incorporé dans le fichier (.svc). Ces valeurs peuvent représenter tout langage pris en charge par .NET, notamment C#, VB et JS, qui font respectivement référence à C#, Visual Basic .NET et JScript .NET. Cet attribut est facultatif.  
  
#### <a name="codebehind"></a>CodeBehind  
 Spécifie le fichier source qui implémente le service web XML, lorsque la classe implémentant le service web XML ne réside pas dans le même fichier et n’a pas été compilée dans un assembly et placée dans le répertoire \Bin.  
  
## <a name="remarks"></a>Notes  
 Le <xref:System.ServiceModel.ServiceHost> utilisé pour héberger le service est un point d’extensibilité dans le modèle de programmation Windows Communication Foundation (WCF). Un modèle de fabrique est utilisé pour instancier le <xref:System.ServiceModel.ServiceHost> car il peut s'agir d'un type polymorphe ne devant pas être instancié directement par l'environnement d'hébergement.  
  
 L'implémentation par défaut utilise <xref:System.ServiceModel.Activation.ServiceHostFactory> pour créer une instance de <xref:System.ServiceModel.ServiceHost>. Mais vous pouvez fournir votre propre fabrique (celle qui retourne votre hôte dérivé) en spécifiant le nom de type CLR de l’implémentation de fabrique dans la [ @ServiceHost ](../../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md) la directive.  
  
 Pour utiliser fabrique hôte de service personnalisé propre au lieu de la fabrique par défaut, simplement fournir le nom de type dans le [ @ServiceHost ](../../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md) directive comme suit :  
  
```xml  
<% @ServiceHost Factory="DerivedFactory" Service="MyService" %>  
```  
  
 Surchargez les implémentations de fabrique le moins possible. Si vous disposez d'une importante logique personnalisée, votre code est plus facilement réutilisable si vous intégrez cette logique à votre hôte et non à la fabrique.  
  
 Par exemple, pour activer un point de terminaison compatible AJAX pour `MyService`, spécifiez la <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> pour la valeur de la `Factory` attribut, au lieu de la valeur par défaut <xref:System.ServiceModel.Activation.ServiceHostFactory>, dans le [ @ServiceHost ](../../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md) directive en tant que indiqué dans l’exemple suivant.  
  
## <a name="example"></a>Exemple  
  
```  
<% @ServiceHost   
Service="MyService"  
Language="C#"  
Debug="true"  
Factory="WebScriptServiceHostFactory"  
%>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Hôte de service personnalisé](../../../../../docs/framework/wcf/samples/custom-service-host.md)
