---
title: <bindings>
ms.date: 01/22/2018
ms.assetid: b62cd369-5409-4030-8490-9759a462dd3a
ms.openlocfilehash: 479941593b1abefe637525703140b02917c6692b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316789"
---
# <a name="bindings"></a>\<bindings>

Vous pouvez utiliser le `bindings` élément pour configurer une collection de liaisons standard et personnalisés pour Windows Communication Foundation (WCF). Chaque entrée est un élément de `binding` qui peut être identifié par son `name` unique. Les services utilisent les liaisons en les liant à l’aide de `name`. Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom. Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).  
  
## <a name="system-provided-bindings"></a>Liaisons fournies par le système
 
 Les liaisons fournies par le système masquent la complexité de la pile de la messagerie du WCF. Les applications qui utilisent des liaisons fournies par le système ne requièrent pas de contrôle total sur la pile. Les attributs exposés sur chaque liaison fournie par le système sont les plus appropriés pour le scénario d'utilisation des adresses de liaison.  
  
 La section de configuration de chaque liaison fournie par le système peut définir plusieurs configurations utilisées en vue de configurer la liaison. Chaque configuration est identifiée par un nom unique.  
  
 Il n’est pas possible d’ajouter des éléments ou attributs à une liaison fournie par le système. Pour ce faire, vous devez implémenter une liaison personnalisée comme décrit dans la [liaisons personnalisées](#custom-bindings) section. Il est possible de définir une liaison personnalisée qui imite une fournie par le système de liaison parfaitement et ajoute quelques paramètres de sur que l’application de l’utilisateur souhaite contrôler.  
  
 Pour obtenir la liste des liaisons fournies par le système, consultez [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).  
  
## <a name="custom-bindings"></a>Liaisons personnalisées

 Les liaisons personnalisées permettent d'exercer un contrôle total sur la pile de messagerie WCF. Une liaison individuelle définit la pile de messages en spécifiant les éléments de configuration des éléments de la pile suivant leur l'ordre d'apparition dans cette pile. Chaque élément définit et configure un élément de la pile. Il doit y avoir un seul élément de `transport` dans chaque liaison personnalisée. Sans cet élément, la pile de messagerie est incomplète.  
  
 L'ordre dans lequel les éléments apparaissent dans la pile est important car il s'agit de l'ordre dans lequel les opérations sont appliquées au message. Voici l'ordre requis des éléments de la pile :  
  
1. Transactions (facultatif)  
  
2. Fiabilité de la messagerie (facultatif)  
  
3. Sécurité (facultatif)  
  
4. Encodeur  
  
5. Transport  
  
 Les liaisons personnalisées sont identifiées par leur attribut `name`. Pour plus d’informations sur les liaisons personnalisées, consultez [liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.BindingsSection?displayProperty=nameWithType>  
- <xref:System.ServiceModel.Channels.Binding?displayProperty=nameWithType>  
- <xref:System.ServiceModel.Channels.BindingElement?displayProperty=nameWithType>  
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)  
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
- [\<binding>](../../../../../docs/framework/misc/binding.md)
