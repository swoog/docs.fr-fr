---
title: Déploiement d’applications faisant référence aux contrôles Power Packs (Visual Studio)
ms.date: 07/20/2015
helpviewer_keywords:
- Power Packs, deploying
ms.assetid: f2230f53-a745-4731-89e6-033943faa209
ms.openlocfilehash: 3fd46a6e8aad61d2f8ce5a230c856470f913d0bd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54551772"
---
# <a name="deploying-applications-that-reference-power-packs-controls-visual-studio"></a>Déploiement d’applications faisant référence aux contrôles Power Packs (Visual Studio)
Si vous souhaitez déployer une application qui référence les contrôles Power Packs (<xref:Microsoft.VisualBasic.PowerPacks.LineShape>, <xref:Microsoft.VisualBasic.PowerPacks.OvalShape>, <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape>, ou <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>), les contrôles doivent être installés sur l’ordinateur de destination.  
  
## <a name="installing-the-power-packs-controls-as-a-prerequisite"></a>Installer les contrôles Power Packs comme condition préalable  
 Pour déployer une application, vous devez également déployer tous les composants qui sont référencés par l’application. Le processus d’installation des composants prérequis est connu sous le nom d’ *amorçage*.  
  
 Lorsque Visual Studio est installé sur votre ordinateur de développement, un package de programme d’amorçage de Power Packs est ajouté dans le répertoire du programme d’amorçage de Visual Studio. Ce package est alors disponible quand vous suivez les procédures d’ajout des composants prérequis pour le déploiement de [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] ou de Windows Installer.  
  
 Par défaut, les composants d’amorçage sont déployés à partir du même emplacement que le package d’installation. Vous pouvez également déployer les composants à partir d’une URL ou d’un emplacement de partage de fichiers, à partir duquel les utilisateurs peuvent les télécharger si nécessaire.  
  
> [!NOTE]
>  Pour installer les composants d’amorçage, l’utilisateur peut avoir besoin d’autorisations d’administration ou d’autorisations similaires sur l’ordinateur. Pour les applications [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] , cela signifie que l’utilisateur a besoin d’autorisations d’administration pour installer l’application, quel que soit le niveau de sécurité spécifié par celle-ci. Une fois l’application installée, l’utilisateur peut exécuter l’application sans autorisations d’administration.  
  
 Pendant l’installation, les utilisateurs seront être invités à installer les contrôles Power Packs s’ils ne sont pas présents sur l’ordinateur de destination.  
  
 Comme alternative à l’amorçage, vous pouvez prédéployer les contrôles Power Packs à l’aide d’un système de distribution électronique de logiciels tel que Microsoft Systems Management Server.  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour installer des prérequis avec une application ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application)
- [Contrôles Visual Basic Power Packs](../../../visual-basic/developing-apps/windows-forms/power-packs-controls.md)
