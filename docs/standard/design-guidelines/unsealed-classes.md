---
title: Classes unsealed
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 672d36c6b888ee9a89a76d5d417a7a7e92dd8f36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571659"
---
# <a name="unsealed-classes"></a>Classes unsealed
Classes sealed ne peut pas être héritées, et empêchent d’extensibilité. En revanche, les classes qui peuvent être héritées sont appelées classes unsealed.  
  
 **✓ Envisagez** à l’aide des classes unsealed sans aucune ajouté des membres virtuels ou protégés comme un excellent moyen de fournir un peu coûteux encore apprécié extensibilité à une infrastructure.  
  
 Les développeurs souhaitent souvent héritent des classes unsealed afin d’ajouter des membres de commodité telles que les constructeurs personnalisés, les nouvelles méthodes ou les surcharges de méthode. Par exemple, `System.Messaging.MessageQueue` est non scellé, et permet ainsi aux utilisateurs de créer des files d’attente personnalisées cette valeur par défaut pour un chemin d’accès de la file d’attente particulière ou ajouter des méthodes personnalisées qui simplifient l’API pour des scénarios spécifiques.  
  
 Classes sont non scellés par défaut dans les langages de programmation plus, et c’est également la valeur par défaut recommandée pour la plupart des classes dans les infrastructures. L’extensibilité offerte par les types unsealed est bien appréciés par les utilisateurs de l’infrastructure et relativement peu coûteux fournir des coûts relativement faible de test associées aux types unsealed.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
 [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
 [Scellement](../../../docs/standard/design-guidelines/sealing.md)
