---
title: 'Procédure : accéder au modèle objet de document HTML managé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- HTML DOM [Windows Forms], accessing
- managed HTML DOM [Windows Forms], accessing
ms.assetid: 40fa5cd5-1ed8-42f6-a93f-9ac01608bbeb
ms.openlocfilehash: 04d5f9e6f128d9b4ed3f07a5faebe06ae4ffdebf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59315190"
---
# <a name="how-to-access-the-managed-html-document-object-model"></a><span data-ttu-id="f2f07-102">Procédure : accéder au modèle objet de document HTML managé</span><span class="sxs-lookup"><span data-stu-id="f2f07-102">How to: Access the Managed HTML Document Object Model</span></span>
<span data-ttu-id="f2f07-103">Vous pouvez accéder au modèle DOM (Document Object Model) HTML géré à partir de deux types d'applications :</span><span class="sxs-lookup"><span data-stu-id="f2f07-103">You can access the managed HTML Document Object Model (DOM) from two types of applications:</span></span>  
  
-   <span data-ttu-id="f2f07-104">l’application Windows Forms (.exe) qui a hébergé le contrôle <xref:System.Windows.Forms.WebBrowser> géré.</span><span class="sxs-lookup"><span data-stu-id="f2f07-104">A Windows Forms application (.exe) that hosted the managed <xref:System.Windows.Forms.WebBrowser> control.</span></span> <span data-ttu-id="f2f07-105">Ces deux technologies se complètent mutuellement, avec le contrôle <xref:System.Windows.Forms.WebBrowser> qui affiche la page pour l'utilisateur et le modèle DOM HTML qui représente la structure logique du document ;</span><span class="sxs-lookup"><span data-stu-id="f2f07-105">These two technologies complement one another, with the <xref:System.Windows.Forms.WebBrowser> control displaying the page to the user and the HTML DOM representing the document's logical structure.</span></span>  
  
-   <span data-ttu-id="f2f07-106">l'<xref:System.Windows.Forms.UserControl> Windows Forms hébergé dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f2f07-106">A Windows Forms <xref:System.Windows.Forms.UserControl> hosted within Internet Explorer.</span></span> <span data-ttu-id="f2f07-107">Vous pouvez accéder au modèle DOM HTML qui représente la page sur laquelle votre <xref:System.Windows.Forms.UserControl> est hébergé pour modifier la structure du document ou ouvrir des boîtes de dialogue modales, entre autres possibilités.</span><span class="sxs-lookup"><span data-stu-id="f2f07-107">You can access the HTML DOM representing the page on which your <xref:System.Windows.Forms.UserControl> is hosted in order to change the document's structure or open modal dialog boxes, among many other possibilities.</span></span>  
  
### <a name="to-access-dom-from-a-windows-forms-application"></a><span data-ttu-id="f2f07-108">Pour accéder au modèle DOM à partir d’une application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f2f07-108">To access DOM from a Windows Forms application</span></span>  
  
1. <span data-ttu-id="f2f07-109">Hébergez un contrôle <xref:System.Windows.Forms.WebBrowser> dans votre application Windows Forms et surveillez l'événement <xref:System.Windows.Forms.WebBrowser.DocumentCompleted>.</span><span class="sxs-lookup"><span data-stu-id="f2f07-109">Host a <xref:System.Windows.Forms.WebBrowser> control within your Windows Forms application and monitor for the <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event.</span></span> <span data-ttu-id="f2f07-110">Pour plus d’informations sur l’hébergement de contrôles et la surveillance d’événements, consultez [Événements](../../../standard/events/index.md).</span><span class="sxs-lookup"><span data-stu-id="f2f07-110">For details on hosting controls and monitoring for events, see [Events](../../../standard/events/index.md).</span></span>  
  
2. <span data-ttu-id="f2f07-111">Récupérez <xref:System.Windows.Forms.HtmlDocument> pour la page actuelle en accédant à la propriété <xref:System.Windows.Forms.WebBrowser.Document%2A> du contrôle <xref:System.Windows.Forms.WebBrowser>.</span><span class="sxs-lookup"><span data-stu-id="f2f07-111">Retrieve the <xref:System.Windows.Forms.HtmlDocument> for the current page by accessing the <xref:System.Windows.Forms.WebBrowser.Document%2A> property of the <xref:System.Windows.Forms.WebBrowser> control.</span></span>  

### <a name="to-access-dom-from-a-usercontrol-hosted-in-internet-explorer"></a><span data-ttu-id="f2f07-112">Pour accéder au modèle DOM à partir d'un UserControl hébergé dans Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f2f07-112">To access DOM from a UserControl hosted in Internet Explorer</span></span>  
  
1. <span data-ttu-id="f2f07-113">Créez votre propre classe personnalisée dérivée de la classe <xref:System.Windows.Forms.UserControl>.</span><span class="sxs-lookup"><span data-stu-id="f2f07-113">Create your own custom derived class of the <xref:System.Windows.Forms.UserControl> class.</span></span> <span data-ttu-id="f2f07-114">Pour plus d'informations, voir [Procédure : Créer des contrôles composites](how-to-author-composite-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f2f07-114">For more information, see [How to: Author Composite Controls](how-to-author-composite-controls.md).</span></span>  
  
2. <span data-ttu-id="f2f07-115">Placez le code suivant dans votre gestionnaire d'événements Load pour <xref:System.Windows.Forms.UserControl> :</span><span class="sxs-lookup"><span data-stu-id="f2f07-115">Place the following code inside of your Load event handler for your <xref:System.Windows.Forms.UserControl>:</span></span>  
  
 [!code-csharp[AccessHTMLDOMControl#1](~/samples/snippets/csharp/VS_Snippets_Winforms/AccessHTMLDOMControl/cs/UserControl1.cs#1)]
 [!code-vb[AccessHTMLDOMControl#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/AccessHTMLDOMControl/vb/UserControl1.vb#1)]  
  
## <a name="robust-programming"></a><span data-ttu-id="f2f07-116">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="f2f07-116">Robust Programming</span></span>  
  
1. <span data-ttu-id="f2f07-117">Quand vous utilisez le modèle DOM via le contrôle <xref:System.Windows.Forms.WebBrowser>, vous devez systématiquement attendre que l'événement <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> se produise avant de tenter d'accéder à la propriété <xref:System.Windows.Forms.WebBrowser.Document%2A> du contrôle <xref:System.Windows.Forms.WebBrowser>.</span><span class="sxs-lookup"><span data-stu-id="f2f07-117">When using the DOM through the <xref:System.Windows.Forms.WebBrowser> control, you should always wait until the <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event occurs before attempting to access the <xref:System.Windows.Forms.WebBrowser.Document%2A> property of the <xref:System.Windows.Forms.WebBrowser> control.</span></span> <span data-ttu-id="f2f07-118">L'événement <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> est déclenché une fois que le document entier a été chargé. Si vous utilisez le modèle DOM avant, cela risque de provoquer une exception au moment de l'exécution dans votre application.</span><span class="sxs-lookup"><span data-stu-id="f2f07-118">The <xref:System.Windows.Forms.WebBrowser.DocumentCompleted> event is raised after the entire document has loaded; if you use the DOM before then, you risk causing a run-time exception in your application.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="f2f07-119">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f2f07-119">.NET Framework Security</span></span>  
  
1. <span data-ttu-id="f2f07-120">Votre application ou <xref:System.Windows.Forms.UserControl> nécessite la confiance totale pour accéder au modèle DOM HTML géré.</span><span class="sxs-lookup"><span data-stu-id="f2f07-120">Your application or <xref:System.Windows.Forms.UserControl> will require full trust in order to access the managed HTML DOM.</span></span> <span data-ttu-id="f2f07-121">Si vous déployez une application Windows Forms à l’aide de [!INCLUDE[ndptecclick](../../../../includes/ndptecclick-md.md)], vous pouvez demander une confiance totale en utilisant les options d’élévation d’autorisations ou de déploiement d’application approuvée. Pour plus d’informations, consultez [Sécurisation des applications ClickOnce](/visualstudio/deployment/securing-clickonce-applications).</span><span class="sxs-lookup"><span data-stu-id="f2f07-121">If you are deploying a Windows Forms application using [!INCLUDE[ndptecclick](../../../../includes/ndptecclick-md.md)], you can request full trust using either Permission Elevation or Trusted Application Deployment; see [Securing ClickOnce Applications](/visualstudio/deployment/securing-clickonce-applications) for details.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2f07-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2f07-122">See also</span></span>

- [<span data-ttu-id="f2f07-123">Utilisation du modèle DOM HTML managé</span><span class="sxs-lookup"><span data-stu-id="f2f07-123">Using the Managed HTML Document Object Model</span></span>](using-the-managed-html-document-object-model.md)
