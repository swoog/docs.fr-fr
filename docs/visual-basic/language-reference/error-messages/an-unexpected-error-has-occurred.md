---
title: Une erreur inattendue s'est produite parce qu'une ressource de système d'exploitation requise pour le démarrage de l'instance unique ne peut pas être acquise
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_CantGetMemoryMappedFile
ms.assetid: 0d9f2a30-ff72-4355-8060-744f22339359
ms.openlocfilehash: 82b513b89d661e49853e55f26df13eb354945038
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58828590"
---
# <a name="an-unexpected-error-has-occurred-because-an-operating-system-resource-required-for-single-instance-startup-cannot-be-acquired"></a><span data-ttu-id="17557-102">Une erreur inattendue s'est produite parce qu'une ressource de système d'exploitation requise pour le démarrage de l'instance unique ne peut pas être acquise</span><span class="sxs-lookup"><span data-stu-id="17557-102">An unexpected error has occurred because an operating system resource required for single instance startup cannot be acquired</span></span>
<span data-ttu-id="17557-103">L'application n'a pas pu obtenir une ressource nécessaire du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="17557-103">The application could not acquire a necessary operating system resource.</span></span> <span data-ttu-id="17557-104">Ce problème peut avoir certaines des causes suivantes :</span><span class="sxs-lookup"><span data-stu-id="17557-104">Some of the possible causes for this problem are:</span></span>  
  
-   <span data-ttu-id="17557-105">L'application n'est pas autorisée à créer des objets de système d'exploitation nommés.</span><span class="sxs-lookup"><span data-stu-id="17557-105">The application does not have permissions to create named operating-system objects.</span></span>  
  
-   <span data-ttu-id="17557-106">Le Common Language Runtime n'est pas autorisé à créer des fichiers mappés sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="17557-106">The common language runtime does not have permissions to create memory-mapped files.</span></span>  
  
-   <span data-ttu-id="17557-107">L'application doit accéder à un objet de système d'exploitation, mais un autre processus l'utilise.</span><span class="sxs-lookup"><span data-stu-id="17557-107">The application needs to access an operating-system object, but another process is using it.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="17557-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="17557-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="17557-109">Vérifiez que l'application dispose d'autorisations suffisantes pour créer des objets de système d'exploitation nommés.</span><span class="sxs-lookup"><span data-stu-id="17557-109">Check that the application has sufficient permissions to create named operating-system objects.</span></span>  
  
2.  <span data-ttu-id="17557-110">Veillez à ce que le Common Language Runtime dispose d'autorisations suffisantes pour créer des fichiers mappés sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="17557-110">Check that the common language runtime has sufficient permissions to create memory-mapped files.</span></span>  
  
3.  <span data-ttu-id="17557-111">Redémarrez l'ordinateur pour annuler tout processus susceptible d'utiliser la ressource permettant de se connecter à l'application de l'instance d'origine.</span><span class="sxs-lookup"><span data-stu-id="17557-111">Restart the computer to clear any process that may be using the resource needed to connect to the original instance application.</span></span>  
  
4.  <span data-ttu-id="17557-112">Notez les circonstances dans lesquelles l'erreur s'est produite, puis contactez les services de support technique Microsoft</span><span class="sxs-lookup"><span data-stu-id="17557-112">Note the circumstances under which the error occurred, and call Microsoft Product Support Services</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17557-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17557-113">See also</span></span>

- [<span data-ttu-id="17557-114">Page Application, Concepteur de projets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="17557-114">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [<span data-ttu-id="17557-115">Principes de base du débogueur</span><span class="sxs-lookup"><span data-stu-id="17557-115">Debugger Basics</span></span>](/visualstudio/debugger/debugger-basics)
- [<span data-ttu-id="17557-116">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="17557-116">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
