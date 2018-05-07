---
title: 'Comment : charger et décharger des assemblys (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: bbc84236-04b6-4c1b-9672-52773f65a5dc
ms.openlocfilehash: 1cec7a7e15843874b65cf5d2f3a23b8e644a26d6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-load-and-unload-assemblies-visual-basic"></a>Comment : charger et décharger des assemblys (Visual Basic)
Les assemblys référencés par votre programme sont chargés automatiquement au moment de la génération, mais il est également possible de charger des assemblys spécifiques dans le domaine d’application actif au moment de l’exécution. Pour plus d’informations, consultez [Guide pratique pour charger des assemblys dans un domaine d’Application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
 Il n’existe aucun moyen de décharger un assembly spécifique sans décharger tous les domaines d’application qui le contiennent. Même si l’assembly passe hors de portée, le fichier d’assembly proprement dit restera chargé jusqu’à ce que tous les domaines d’application qui le contiennent soient déchargés.  
  
 Si vous souhaitez décharger uniquement certains assemblys, créez un domaine d’application, exécutez le code à l’intérieur de ce domaine, puis déchargez le domaine. Pour plus d’informations, consultez [Guide pratique pour décharger un domaine d’Application](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
### <a name="to-load-an-assembly-into-an-application-domain"></a>Pour charger un assembly dans un domaine d’application  
  
1.  Utilisez une des nombreuses méthodes de chargement contenues dans les classes <xref:System.AppDomain> et <xref:System.Reflection>. Pour plus d’informations, consultez [Guide pratique pour charger des assemblys dans un domaine d’Application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
### <a name="to-unload-an-application-domain"></a>Pour décharger un domaine d’application  
  
1.  Il n’existe aucun moyen de décharger un assembly spécifique sans décharger tous les domaines d’application qui le contiennent. Utilisez la méthode `Unload` de <xref:System.AppDomain> pour décharger les domaines d’application. Pour plus d’informations, consultez [Guide pratique pour décharger un domaine d’Application](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Concepts de programmation](../../../../visual-basic/programming-guide/concepts/index.md)  
 [Assemblys et le Global Assembly Cache (Visual Basic)](../../../../visual-basic/programming-guide/concepts/assemblies-gac/index.md)  
 [Guide pratique pour charger des assemblys dans un domaine d’application](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md)
