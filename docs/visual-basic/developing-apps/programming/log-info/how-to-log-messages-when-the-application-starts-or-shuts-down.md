---
title: 'Procédure : enregistrer des messages lorsque l’application démarre ou s’arrête (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- event logs, shutdown
- My.Application.Log object, logging
- Startup event [Visual Basic]
- event logs, startup
- Shutdown event [Visual Basic]
- My.Log object, logging
ms.assetid: 67624d05-cddf-48b7-8c36-5c99baa4c621
ms.openlocfilehash: 8fc7b441c6e19d70ceefa3422cf9823007280b64
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59330569"
---
# <a name="how-to-log-messages-when-the-application-starts-or-shuts-down-visual-basic"></a><span data-ttu-id="7ae1b-102">Procédure : enregistrer des messages lorsque l’application démarre ou s’arrête (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ae1b-102">How to: Log Messages When the Application Starts or Shuts Down (Visual Basic)</span></span>
<span data-ttu-id="7ae1b-103">Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur les événements qui se produisent dans votre application.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-103">You can use the `My.Application.Log` and `My.Log` objects to log information about events that occur in your application.</span></span> <span data-ttu-id="7ae1b-104">Cet exemple montre comment utiliser la méthode `My.Application.Log.WriteEntry` avec les événements `Startup` et `Shutdown` pour enregistrer des informations de traçage.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-104">This example shows how to use the `My.Application.Log.WriteEntry` method with the `Startup` and `Shutdown` events to write tracing information.</span></span>  
  
### <a name="to-access-the-applications-event-handler-code"></a><span data-ttu-id="7ae1b-105">Pour accéder au code du gestionnaire d’événements de l’application</span><span class="sxs-lookup"><span data-stu-id="7ae1b-105">To access the application's event-handler code</span></span>  
  
1. <span data-ttu-id="7ae1b-106">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-106">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="7ae1b-107">Dans le menu **Projet** , choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-107">On the **Project** menu, choose **Properties**.</span></span>  
  
2. <span data-ttu-id="7ae1b-108">Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="7ae1b-108">Click the **Application** tab.</span></span>  
  
3. <span data-ttu-id="7ae1b-109">Cliquez sur le bouton **Afficher les événements de l’application** pour ouvrir l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-109">Click the **View Application Events** button to open the Code Editor.</span></span>  
  
     <span data-ttu-id="7ae1b-110">Le fichier ApplicationEvents.vb s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-110">This opens the ApplicationEvents.vb file.</span></span>  
  
### <a name="to-log-messages-when-the-application-starts"></a><span data-ttu-id="7ae1b-111">Pour enregistrer des messages quand l’application démarre</span><span class="sxs-lookup"><span data-stu-id="7ae1b-111">To log messages when the application starts</span></span>  
  
1. <span data-ttu-id="7ae1b-112">Ouvrez le fichier ApplicationEvents.vb dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-112">Have the ApplicationEvents.vb file open in the Code Editor.</span></span> <span data-ttu-id="7ae1b-113">Dans le menu **Général** , choisissez **Événements MyApplication**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-113">On the **General** menu, choose **MyApplication Events**.</span></span>  
  
2. <span data-ttu-id="7ae1b-114">Dans le menu **Déclarations** , choisissez **Démarrage**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-114">On the **Declarations** menu, choose **Startup**.</span></span>  
  
     <span data-ttu-id="7ae1b-115">L’application déclenche l’événement <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> avant l’exécution de l’application principale.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-115">The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> event before the main application runs.</span></span>  
  
3. <span data-ttu-id="7ae1b-116">Ajoutez la méthode `My.Application.Log.WriteEntry` au gestionnaire d’événements `Startup` .</span><span class="sxs-lookup"><span data-stu-id="7ae1b-116">Add the `My.Application.Log.WriteEntry` method to the `Startup` event handler.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#1)]  
  
### <a name="to-log-messages-when-the-application-shuts-down"></a><span data-ttu-id="7ae1b-117">Pour enregistrer des messages quand l’application s’arrête</span><span class="sxs-lookup"><span data-stu-id="7ae1b-117">To log messages when the application shuts down</span></span>  
  
1. <span data-ttu-id="7ae1b-118">Ouvrez le fichier ApplicationEvents.vb dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-118">Have the ApplicationEvents.vb file open in the Code Editor.</span></span> <span data-ttu-id="7ae1b-119">Dans le menu **Général** , choisissez **Événements MyApplication**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-119">On the **General** menu, choose **MyApplication Events**.</span></span>  
  
2. <span data-ttu-id="7ae1b-120">Dans le menu **Déclarations** , choisissez **Arrêt**.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-120">On the **Declarations** menu, choose **Shutdown**.</span></span>  
  
     <span data-ttu-id="7ae1b-121">L’application déclenche l’événement <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> après l’exécution de l’application principale, mais avant qu’elle s’arrête.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-121">The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> event after the main application runs, but before it shuts down.</span></span>  
  
3. <span data-ttu-id="7ae1b-122">Ajoutez la méthode `My.Application.Log.WriteEntry` au gestionnaire d’événements `Shutdown` .</span><span class="sxs-lookup"><span data-stu-id="7ae1b-122">Add the `My.Application.Log.WriteEntry` method to the `Shutdown` event handler.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#2)]  
  
## <a name="example"></a><span data-ttu-id="7ae1b-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ae1b-123">Example</span></span>  
 <span data-ttu-id="7ae1b-124">Vous pouvez utiliser le **Concepteur de projets** pour accéder aux événements de l’application dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="7ae1b-124">You can use the **Project Designer** to access the application events in the Code Editor.</span></span> <span data-ttu-id="7ae1b-125">Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="7ae1b-125">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
 [!code-vb[VbVbalrMyApplicationLog#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/MyEventsFake.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="7ae1b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ae1b-126">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [<span data-ttu-id="7ae1b-127">Page Application, Concepteur de projets (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ae1b-127">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [<span data-ttu-id="7ae1b-128">Utilisation des journaux des applications</span><span class="sxs-lookup"><span data-stu-id="7ae1b-128">Working with Application Logs</span></span>](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)
