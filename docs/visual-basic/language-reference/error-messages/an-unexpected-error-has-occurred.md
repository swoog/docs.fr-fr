---
title: Une erreur inattendue s'est produite parce qu'une ressource de système d'exploitation requise pour le démarrage de l'instance unique ne peut pas être acquise
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_CantGetMemoryMappedFile
ms.assetid: 0d9f2a30-ff72-4355-8060-744f22339359
ms.openlocfilehash: 9aa7ba0babe0a89942e320a76e07c05162b31700
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61751616"
---
# <a name="an-unexpected-error-has-occurred-because-an-operating-system-resource-required-for-single-instance-startup-cannot-be-acquired"></a>Une erreur inattendue s'est produite parce qu'une ressource de système d'exploitation requise pour le démarrage de l'instance unique ne peut pas être acquise
L'application n'a pas pu obtenir une ressource nécessaire du système d'exploitation. Ce problème peut avoir certaines des causes suivantes :  
  
- L'application n'est pas autorisée à créer des objets de système d'exploitation nommés.  
  
- Le Common Language Runtime n'est pas autorisé à créer des fichiers mappés sur la mémoire.  
  
- L'application doit accéder à un objet de système d'exploitation, mais un autre processus l'utilise.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez que l'application dispose d'autorisations suffisantes pour créer des objets de système d'exploitation nommés.  
  
2. Veillez à ce que le Common Language Runtime dispose d'autorisations suffisantes pour créer des fichiers mappés sur la mémoire.  
  
3. Redémarrez l'ordinateur pour annuler tout processus susceptible d'utiliser la ressource permettant de se connecter à l'application de l'instance d'origine.  
  
4. Notez les circonstances dans lesquelles l'erreur s'est produite, puis contactez les services de support technique Microsoft  
  
## <a name="see-also"></a>Voir aussi

- [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [Principes de base du débogueur](/visualstudio/debugger/debugger-basics)
- [Nous contacter](/visualstudio/ide/talk-to-us)
