---
title: 'Impossible d’écrire dans le fichier de sortie &#39; &lt;nom de fichier&gt;&#39;: &lt;erreur&gt;'
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc31019
- bc31019
helpviewer_keywords:
- BC31019
ms.assetid: 0845b245-11bb-46fd-95ca-f6cef3c318ef
caps.latest.revision: 10
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: ce97bcb2dd0de774c1a82ae75ef5b83c02467edb
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="unable-to-write-to-output-file-39ltfilenamegt39-lterrorgt"></a>Impossible d’écrire dans le fichier de sortie &#39; &lt;nom de fichier&gt;&#39;: &lt;erreur&gt;
Un problème s'est produit pendant la création du fichier.  
  
 Vous ne pouvez pas ouvrir un fichier de sortie pour écriture. Le fichier (ou le dossier qui le contient) est peut être ouvert pour un usage exclusif par un autre processus, ou a son attribut de lecture seule défini.  
  
 Les situations courantes dans lesquelles un fichier est ouvert de manière exclusive sont les suivantes :  
  
-   L'application est déjà en cours d'exécution et utilise ses fichiers. Pour résoudre ce problème, vérifiez que l'application n'est pas en cours d'exécution.  
  
-   Une autre application a ouvert le fichier. Pour résoudre ce problème, vérifiez qu'aucune autre application n'accède aux fichiers. Il n'est pas toujours évident de savoir quelle application accède à vos fichiers ; le cas échéant, le plus facile est de redémarrer l'ordinateur pour arrêter l'application.  
  
 Si au moins un des fichiers de sortie du projet est marqué en lecture seule, cette exception est levée.  
  
 **ID d’erreur :** BC31019  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Recompilez le programme pour voir si l'erreur se produit à nouveau.  
  
2.  Si l’erreur persiste, enregistrez votre travail et redémarrez Visual Studio.  
  
3.  Si l'erreur continue, redémarrez l'ordinateur.  
  
4.  Si l’erreur persiste, réinstallez Visual Basic.  
  
5.  Si l'erreur persiste après la réinstallation, avertissez les services de support technique Microsoft.  
  
### <a name="to-check-file-attributes-in-file-explorer"></a>Pour vérifier les attributs de fichier dans l'Explorateur de fichiers  
  
1.  Ouvrez le dossier qui vous intéresse.  
  
2.  Cliquez sur le **vues** icône et choisissez **détails**.  
  
3.  Cliquez sur l’en-tête de colonne, puis choisissez **attributs** dans la liste déroulante.  
  
### <a name="to-change-the-attributes-of-a-file-or-folder"></a>Pour modifier les attributs d’un fichier ou d’un dossier  
  
1.  Dans **l’Explorateur de fichiers**, cliquez sur le fichier ou dossier et choisissez **propriétés**.  
  
2.  Dans le **attributs** section de la **général** onglet, désactivez le **en lecture seule** boîte.  
  
3.  Press **OK**.  
  
## <a name="see-also"></a>Voir aussi  
 [Nous contacter](/visualstudio/ide/talk-to-us)
