---
title: Conception en vue de l'extensibilité
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 68419fe293dd25936aa3c1e3def10bbe8852e175
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571382"
---
# <a name="designing-for-extensibility"></a>Conception en vue de l'extensibilité
Un aspect important de la conception d’une infrastructure consiste à s’assurer de que l’extensibilité de l’infrastructure a été examinée avec soin. Cela nécessite que vous comprenez les coûts et les avantages associés à différents mécanismes d’extensibilité. Ce chapitre vous aide à décider des mécanismes d’extensibilité : sous-classement, les événements, les membres virtuels, les rappels et ainsi de suite, peuvent mieux les exigences de votre infrastructure.  
  
 Il existe de nombreuses façons pour permettre d’extensibilité dans les infrastructures. Elles vont de moins puissants mais moins coûteux à très puissante, mais il est coûteux. Pour tous les besoins d’extensibilité donné, vous devez choisir le mécanisme d’extensibilité moins coûteux qui répond aux exigences. Gardez à l’esprit qu’il est généralement possible d’ajouter plus d’extensibilité ultérieurement, mais prennent immédiatement sans introduire de modifications avec rupture jamais.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Classes unsealed](../../../docs/standard/design-guidelines/unsealed-classes.md)  
 [Membres protégés](../../../docs/standard/design-guidelines/protected-members.md)  
 [Événements et rappels](../../../docs/standard/design-guidelines/events-and-callbacks.md)  
 [Membres virtuels](../../../docs/standard/design-guidelines/virtual-members.md)  
 [Abstractions (types et interfaces abstraits)](../../../docs/standard/design-guidelines/abstractions-abstract-types-and-interfaces.md)  
 [Classes de base pour l’implémentation d’abstractions](../../../docs/standard/design-guidelines/base-classes-for-implementing-abstractions.md)  
 [Scellement](../../../docs/standard/design-guidelines/sealing.md)  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
