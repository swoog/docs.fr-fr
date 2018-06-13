---
title: Guide pratique pour enregistrer des exceptions en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- exceptions, logging
- exceptions, tracking
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
ms.openlocfilehash: b8ec45f43438f8181d9e045cdf43c81db34e4242
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588524"
---
# <a name="how-to-log-exceptions-in-visual-basic"></a><span data-ttu-id="f265f-102">Guide pratique pour enregistrer des exceptions en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f265f-102">How to: Log Exceptions in Visual Basic</span></span>
<span data-ttu-id="f265f-103">Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur les exceptions qui se produisent dans votre application.</span><span class="sxs-lookup"><span data-stu-id="f265f-103">You can use the `My.Application.Log` and `My.Log` objects to log information about exceptions that occur in your application.</span></span> <span data-ttu-id="f265f-104">Ces exemples montrent comment utiliser la méthode `My.Application.Log.WriteException` pour enregistrer des exceptions que vous interceptez explicitement et des exceptions qui ne sont pas gérées.</span><span class="sxs-lookup"><span data-stu-id="f265f-104">These examples show how to use the `My.Application.Log.WriteException` method to log exceptions that you catch explicitly and exceptions that are unhandled.</span></span>  
  
 <span data-ttu-id="f265f-105">Pour enregistrer des informations de traçage, utilisez la méthode `My.Application.Log.WriteEntry`.</span><span class="sxs-lookup"><span data-stu-id="f265f-105">For logging tracing information, use the `My.Application.Log.WriteEntry` method.</span></span> <span data-ttu-id="f265f-106">Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A></span><span class="sxs-lookup"><span data-stu-id="f265f-106">For more information, see <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A></span></span>  
  
### <a name="to-log-a-handled-exception"></a><span data-ttu-id="f265f-107">Pour enregistrer une exception gérée</span><span class="sxs-lookup"><span data-stu-id="f265f-107">To log a handled exception</span></span>  
  
1.  <span data-ttu-id="f265f-108">Créez la méthode qui génère les informations sur l’exception.</span><span class="sxs-lookup"><span data-stu-id="f265f-108">Create the method that will generate the exception information.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#9](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_1.vb)]  
  
2.  <span data-ttu-id="f265f-109">Utilisez un bloc `Try...Catch` pour intercepter l’exception.</span><span class="sxs-lookup"><span data-stu-id="f265f-109">Use a `Try...Catch` block to catch the exception.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#6](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_2.vb)]  
  
3.  <span data-ttu-id="f265f-110">Placez le code susceptible de générer une exception dans le bloc `Try`.</span><span class="sxs-lookup"><span data-stu-id="f265f-110">Put the code that could generate an exception in the `Try` block.</span></span>  
  
     <span data-ttu-id="f265f-111">Supprimez les commentaires des lignes `Dim` et `MsgBox` pour déclencher une exception <xref:System.NullReferenceException>.</span><span class="sxs-lookup"><span data-stu-id="f265f-111">Uncomment the `Dim` and `MsgBox` lines to cause a <xref:System.NullReferenceException> exception.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#7](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_3.vb)]  
  
4.  <span data-ttu-id="f265f-112">Dans le bloc `Catch`, utilisez la méthode `My.Application.Log.WriteException` pour écrire les informations sur l’exception.</span><span class="sxs-lookup"><span data-stu-id="f265f-112">In the `Catch` block, use the `My.Application.Log.WriteException` method to write the exception information.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#8](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_4.vb)]  
  
     <span data-ttu-id="f265f-113">L’exemple suivant montre le code complet permettant d’enregistrer une exception gérée.</span><span class="sxs-lookup"><span data-stu-id="f265f-113">The following example shows the complete code for logging a handled exception.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#10](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_5.vb)]  
  
### <a name="to-log-an-unhandled-exception"></a><span data-ttu-id="f265f-114">Pour enregistrer une exception non gérée</span><span class="sxs-lookup"><span data-stu-id="f265f-114">To log an unhandled exception</span></span>  
  
1.  <span data-ttu-id="f265f-115">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="f265f-115">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="f265f-116">Dans le menu **Projet** , choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f265f-116">On the **Project** menu, choose **Properties**.</span></span>  
  
2.  <span data-ttu-id="f265f-117">Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="f265f-117">Click the **Application** tab.</span></span>  
  
3.  <span data-ttu-id="f265f-118">Cliquez sur le bouton **Afficher les événements de l’application** pour ouvrir l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="f265f-118">Click the **View Application Events** button to open the Code Editor.</span></span>  
  
     <span data-ttu-id="f265f-119">Le fichier ApplicationEvents.vb s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f265f-119">This opens the ApplicationEvents.vb file.</span></span>  
  
4.  <span data-ttu-id="f265f-120">Ouvrez le fichier ApplicationEvents.vb dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="f265f-120">Have the ApplicationEvents.vb file open in the Code Editor.</span></span> <span data-ttu-id="f265f-121">Dans le menu **Général** , choisissez **Événements MyApplication**.</span><span class="sxs-lookup"><span data-stu-id="f265f-121">On the **General** menu, choose **MyApplication Events**.</span></span>  
  
5.  <span data-ttu-id="f265f-122">Dans le menu **Déclarations**, choisissez **UnhandledException**.</span><span class="sxs-lookup"><span data-stu-id="f265f-122">On the **Declarations** menu, choose **UnhandledException**.</span></span>  
  
     <span data-ttu-id="f265f-123">L’application déclenche l’événement <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> avant l’exécution de l’application principale.</span><span class="sxs-lookup"><span data-stu-id="f265f-123">The application raises the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> event before the main application runs.</span></span>  
  
6.  <span data-ttu-id="f265f-124">Ajoutez la méthode `My.Application.Log.WriteException` au gestionnaire d’événements `UnhandledException` .</span><span class="sxs-lookup"><span data-stu-id="f265f-124">Add the `My.Application.Log.WriteException` method to the `UnhandledException` event handler.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#4](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_6.vb)]  
  
     <span data-ttu-id="f265f-125">L’exemple suivant montre le code complet permettant d’enregistrer une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="f265f-125">The following example shows the complete code for logging an unhandled exception.</span></span>  
  
     [!code-vb[VbVbalrMyApplicationLog#5](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-exceptions_7.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="f265f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f265f-126">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>  
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>  
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>  
 [<span data-ttu-id="f265f-127">Utilisation des journaux des applications</span><span class="sxs-lookup"><span data-stu-id="f265f-127">Working with Application Logs</span></span>](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)  
 [<span data-ttu-id="f265f-128">Guide pratique : écrire des messages de journal</span><span class="sxs-lookup"><span data-stu-id="f265f-128">How to: Write Log Messages</span></span>](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)  
 [<span data-ttu-id="f265f-129">Procédure pas à pas : détermination de l’emplacement des informations My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="f265f-129">Walkthrough: Determining Where My.Application.Log Writes Information</span></span>](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)  
 [<span data-ttu-id="f265f-130">Procédure pas à pas : modification de l’emplacement des informations My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="f265f-130">Walkthrough: Changing Where My.Application.Log Writes Information</span></span>](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)
