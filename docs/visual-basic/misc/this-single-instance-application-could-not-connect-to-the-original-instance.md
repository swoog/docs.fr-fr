---
title: Impossible de connecter cette application à instance unique à l’instance d’origine
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_SingleInstanceCantConnect
ms.assetid: 7c2c0cee-02a1-4157-be03-39d18e18408f
ms.openlocfilehash: 7ffa9b185e16cfdf8223ce84e77d1a0e1fa67f65
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942609"
---
# <a name="this-single-instance-application-could-not-connect-to-the-original-instance"></a><span data-ttu-id="b7980-102">Impossible de connecter cette application à instance unique à l’instance d’origine</span><span class="sxs-lookup"><span data-stu-id="b7980-102">This single-instance application could not connect to the original instance</span></span>
<span data-ttu-id="b7980-103">Impossible de connecter cette application à instance unique à l'instance d'origine.</span><span class="sxs-lookup"><span data-stu-id="b7980-103">This single-instance application could not connect to the original instance.</span></span> <span data-ttu-id="b7980-104">Ce problème peut avoir les causes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7980-104">Some of the possible causes for this problem are as follows:</span></span>  
  
- <span data-ttu-id="b7980-105">L'instance d'origine a cessé de répondre.</span><span class="sxs-lookup"><span data-stu-id="b7980-105">The original instance stopped responding.</span></span>  
  
- <span data-ttu-id="b7980-106">L'application n'a pas l'autorisation de créer des objets du noyau.</span><span class="sxs-lookup"><span data-stu-id="b7980-106">The application does not have permissions to create kernel objects.</span></span> <span data-ttu-id="b7980-107">Pour plus d’informations sur les objets du noyau, consultez [mutex](../../standard/threading/mutexes.md).</span><span class="sxs-lookup"><span data-stu-id="b7980-107">For more information about kernel objects, see [Mutexes](../../standard/threading/mutexes.md).</span></span>  
  
     <span data-ttu-id="b7980-108">Le nom de base des objets du noyau est une concaténation entre le GUID de l'assembly, le numéro de la version principale et le numéro de la version secondaire.</span><span class="sxs-lookup"><span data-stu-id="b7980-108">The base name for the kernel objects comes from concatenating the assembly's GUID, major version number, and minor version number.</span></span> <span data-ttu-id="b7980-109">Le nom de base pourrait être, par exemple, `3639f15d-9547-43da-8145-60da347829915.1`.</span><span class="sxs-lookup"><span data-stu-id="b7980-109">For example, the base name could be `3639f15d-9547-43da-8145-60da347829915.1`.</span></span>  
  
## <a name="to-correct-this-error-when-developing-the-application"></a><span data-ttu-id="b7980-110">Pour corriger cette erreur lors du développement d’une application</span><span class="sxs-lookup"><span data-stu-id="b7980-110">To correct this error when developing the application</span></span>  
  
1. <span data-ttu-id="b7980-111">Vérifiez que l’application continue de répondre.</span><span class="sxs-lookup"><span data-stu-id="b7980-111">Check that the application does not go into an unresponsive state.</span></span>  
  
2. <span data-ttu-id="b7980-112">Vérifiez que l’application dispose d’autorisations suffisantes pour créer des objets noyaux.</span><span class="sxs-lookup"><span data-stu-id="b7980-112">Check that the application has sufficient permissions to create kernel objects.</span></span>  
  
3. <span data-ttu-id="b7980-113">Redémarrez l’instance d’origine de l’application.</span><span class="sxs-lookup"><span data-stu-id="b7980-113">Restart the original instance of the application.</span></span>  
  
4. <span data-ttu-id="b7980-114">Redémarrez l’ordinateur pour annuler tout processus susceptible d’utiliser la ressource permettant de se connecter à l’application de l’instance d’origine.</span><span class="sxs-lookup"><span data-stu-id="b7980-114">Restart the computer to clear any process that may be using the resource that is required to connect to the original instance application.</span></span>  
  
5. <span data-ttu-id="b7980-115">Notez les circonstances dans lesquelles l’erreur s’est produite, puis contactez les services de support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7980-115">Note the circumstances under which the error occurred, and telephone Microsoft Product Support Services.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7980-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7980-116">See also</span></span>

- [<span data-ttu-id="b7980-117">Principes de base du débogueur</span><span class="sxs-lookup"><span data-stu-id="b7980-117">Debugger Basics</span></span>](/visualstudio/debugger/debugger-basics)
