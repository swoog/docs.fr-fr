---
title: Déploiement d’applications faisant référencent au composant PrintForm (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- PrintForm component [Visual Basic], deploying
ms.assetid: b595ea44-a712-4625-a761-190c64f59bbe
ms.openlocfilehash: 3dd7c348c4dc36a7ff64e76a93c05ddb24837079
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33584694"
---
# <a name="deploying-applications-that-reference-the-printform-component-visual-basic"></a>Déploiement d’applications faisant référencent au composant PrintForm (Visual Basic)
Si vous voulez déployer une application qui fait référence au composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> , le composant doit être installé sur l’ordinateur de destination.  
  
 Les contrôles PowerPack ne sont plus inclus dans Visual Studio, mais vous pouvez les télécharger à partir du [Centre de téléchargement](http://www.microsoft.com/en-us/download/details.aspx?id=25169).  
  
## <a name="installing-the-printform-as-a-prerequisite"></a>Installation de PrintForm comme composant requis  
 Pour déployer une application, vous devez également déployer tous les composants qui sont référencés par l’application. Le processus d’installation des composants prérequis est connu sous le nom d’ *amorçage*.  
  
 Lorsque le <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> composant est installé sur votre ordinateur de développement, un package de programme d’amorçage Microsoft Visual Basic Power Packs est ajouté au répertoire du programme d’amorçage Visual Studio. Ce package est alors disponible quand vous suivez les procédures d’ajout des composants prérequis pour le déploiement de [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] ou de Windows Installer.  
  
 Par défaut, les composants d’amorçage sont déployés à partir du même emplacement que le package d’installation. Vous pouvez également déployer les composants à partir d’une URL ou d’un emplacement de partage de fichiers, à partir duquel les utilisateurs peuvent les télécharger si nécessaire.  
  
> [!NOTE]
>  Pour installer les composants d’amorçage, l’utilisateur peut avoir besoin d’autorisations d’administration ou d’autorisations similaires sur l’ordinateur. Pour les applications [!INCLUDE[ndptecclick](~/includes/ndptecclick-md.md)] , cela signifie que l’utilisateur a besoin d’autorisations d’administration pour installer l’application, quel que soit le niveau de sécurité spécifié par celle-ci. Une fois l’application installée, l’utilisateur peut exécuter l’application sans autorisations d’administration.  
  
 Lors de l’installation, les utilisateurs sont invités à installer le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> s’il n’est pas présent sur l’ordinateur de destination.  
  
 À la place de l’amorçage, vous pouvez prédéployer le composant <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> à l’aide d’un système électronique de distribution de logiciels, par exemple Microsoft Systems Management Server (SMS).  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour installer des composants prérequis avec une application ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application)  
 [PrintForm, composant](../../../visual-basic/developing-apps/printing/printform-component.md)
