---
title: 'Procédure : Charger et décharger des assemblys (C#)'
ms.date: 07/20/2015
ms.assetid: 6a4f490f-3576-471f-9533-003737cad4a3
ms.openlocfilehash: eadab1d0e5ddd22fb5c0e92f45162548c9bfd76c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509348"
---
# <a name="how-to-load-and-unload-assemblies-c"></a>Procédure : Charger et décharger des assemblys (C#)
Les assemblys référencés par votre programme sont chargés automatiquement au moment de la génération, mais il est également possible de charger des assemblys spécifiques dans le domaine d’application actif au moment de l’exécution. Pour plus d'informations, voir [Procédure : Charger des assemblys dans un domaine d’application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
 Il n’existe aucun moyen de décharger un assembly spécifique sans décharger tous les domaines d’application qui le contiennent. Même si l’assembly passe hors de portée, le fichier d’assembly proprement dit restera chargé jusqu’à ce que tous les domaines d’application qui le contiennent soient déchargés.  
  
 Si vous souhaitez décharger uniquement certains assemblys, créez un domaine d’application, exécutez le code à l’intérieur de ce domaine, puis déchargez le domaine. Pour plus d'informations, voir [Procédure : Décharger un domaine d’application](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
### <a name="to-load-an-assembly-into-an-application-domain"></a>Pour charger un assembly dans un domaine d’application  
  
1.  Utilisez une des nombreuses méthodes de chargement contenues dans les classes <xref:System.AppDomain> et <xref:System.Reflection>. Pour plus d'informations, voir [Procédure : Charger des assemblys dans un domaine d’application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
### <a name="to-unload-an-application-domain"></a>Pour décharger un domaine d’application  
  
1.  Il n’existe aucun moyen de décharger un assembly spécifique sans décharger tous les domaines d’application qui le contiennent. Utilisez la méthode `Unload` de <xref:System.AppDomain> pour décharger les domaines d’application. Pour plus d'informations, voir [Procédure : Décharger un domaine d’application](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../../csharp/programming-guide/index.md)
- [Assemblys et le Global Assembly Cache (C#)](../../../../csharp/programming-guide/concepts/assemblies-gac/index.md)
- [Guide pratique pour charger des assemblys dans un domaine d’application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md)
