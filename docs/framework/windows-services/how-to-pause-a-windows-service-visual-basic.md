---
title: 'Procédure : interrompre un service Windows (Visual Basic)'
ms.date: 03/30/2017
dev_langs:
- vb
f1_keywords:
- ServiceController.Pause
helpviewer_keywords:
- Windows Service applications, pausing
- pausing Windows Service applications
ms.assetid: eddb9409-942b-46b6-a2ce-fbd4c65f2790
author: ghogen
ms.openlocfilehash: 8d378aba5ad09a38d24359fda8b50de072c58035
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612721"
---
# <a name="how-to-pause-a-windows-service-visual-basic"></a><span data-ttu-id="9b73b-102">Procédure : interrompre un service Windows (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9b73b-102">How to: Pause a Windows Service (Visual Basic)</span></span>
<span data-ttu-id="9b73b-103">Cet exemple utilise le composant <xref:System.ServiceProcess.ServiceController> pour interrompre le service d’administration IIS sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9b73b-103">This example uses the <xref:System.ServiceProcess.ServiceController> component to pause the IIS Admin service on the local computer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9b73b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9b73b-104">Example</span></span>  
 [!code-vb[VbRadconService#11](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#11)]  
[!code-vb[VbRadconService#12](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#12)]  
  
 <span data-ttu-id="9b73b-105">Cet exemple de code est également disponible sous la forme d’un extrait de code IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="9b73b-105">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="9b73b-106">Dans le sélecteur d’extraits de code, il se trouve dans **Système d’exploitation Windows > Services Windows**.</span><span class="sxs-lookup"><span data-stu-id="9b73b-106">In the code snippet picker, it is located in **Windows Operating System > Windows Services**.</span></span> <span data-ttu-id="9b73b-107">Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).</span><span class="sxs-lookup"><span data-stu-id="9b73b-107">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9b73b-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9b73b-108">Compiling the Code</span></span>  
 <span data-ttu-id="9b73b-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="9b73b-109">This example requires:</span></span>  
  
-   <span data-ttu-id="9b73b-110">Une référence de projet à System.serviceprocess.dll.</span><span class="sxs-lookup"><span data-stu-id="9b73b-110">A project reference to System.serviceprocess.dll.</span></span>  
  
-   <span data-ttu-id="9b73b-111">Un accès aux membres de l’espace de noms <xref:System.ServiceProcess>.</span><span class="sxs-lookup"><span data-stu-id="9b73b-111">Access to the members of the <xref:System.ServiceProcess> namespace.</span></span> <span data-ttu-id="9b73b-112">Ajoutez une instruction `Imports` si vous n’utilisez pas de noms de membres qualifiés complets dans votre code.</span><span class="sxs-lookup"><span data-stu-id="9b73b-112">Add an `Imports` statement if you are not fully qualifying member names in your code.</span></span> <span data-ttu-id="9b73b-113">Pour plus d’informations, consultez [Instruction Imports (espace de noms et type .NET)](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span><span class="sxs-lookup"><span data-stu-id="9b73b-113">For more information, see [Imports Statement (.NET Namespace and Type)](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="9b73b-114">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="9b73b-114">Robust Programming</span></span>  
 <span data-ttu-id="9b73b-115">La propriété <xref:System.ServiceProcess.ServiceController.MachineName%2A> de la classe <xref:System.ServiceProcess.ServiceController> est l’ordinateur local par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b73b-115">The <xref:System.ServiceProcess.ServiceController.MachineName%2A> property of the <xref:System.ServiceProcess.ServiceController> class is the local computer by default.</span></span> <span data-ttu-id="9b73b-116">Pour référencer des services Windows sur un autre ordinateur, remplacez la propriété <xref:System.ServiceProcess.ServiceController.MachineName%2A> par le nom de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9b73b-116">To reference Windows services on another computer, change the <xref:System.ServiceProcess.ServiceController.MachineName%2A> property to the name of that computer.</span></span>  
  
 <span data-ttu-id="9b73b-117">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="9b73b-117">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="9b73b-118">Le service ne peut pas être suspendu.</span><span class="sxs-lookup"><span data-stu-id="9b73b-118">The service cannot be paused.</span></span> <span data-ttu-id="9b73b-119">(<xref:System.InvalidOperationException>)</span><span class="sxs-lookup"><span data-stu-id="9b73b-119">(<xref:System.InvalidOperationException>)</span></span>  
  
-   <span data-ttu-id="9b73b-120">Une erreur s'est produite lors de l'accès à une API système.</span><span class="sxs-lookup"><span data-stu-id="9b73b-120">An error occurred when accessing a system API.</span></span> <span data-ttu-id="9b73b-121">(<xref:System.ComponentModel.Win32Exception>)</span><span class="sxs-lookup"><span data-stu-id="9b73b-121">(<xref:System.ComponentModel.Win32Exception>)</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="9b73b-122">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="9b73b-122">.NET Framework Security</span></span>  
 <span data-ttu-id="9b73b-123">Vous pouvez restreindre le contrôle des services sur l’ordinateur à l’aide de <xref:System.ServiceProcess.ServiceControllerPermissionAccess>, qui permet de définir des autorisations dans <xref:System.ServiceProcess.ServiceControllerPermission>.</span><span class="sxs-lookup"><span data-stu-id="9b73b-123">Control of services on the computer may be restricted by using the <xref:System.ServiceProcess.ServiceControllerPermissionAccess> to set permissions in the <xref:System.ServiceProcess.ServiceControllerPermission>.</span></span>  
  
 <span data-ttu-id="9b73b-124">Vous pouvez restreindre l’accès aux informations de service à l’aide de <xref:System.Security.Permissions.PermissionState>, qui permet de définir des autorisations dans <xref:System.Security.Permissions.SecurityPermission>.</span><span class="sxs-lookup"><span data-stu-id="9b73b-124">Access to service information may be restricted by using the <xref:System.Security.Permissions.PermissionState> to set permissions in the <xref:System.Security.Permissions.SecurityPermission>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b73b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b73b-125">See also</span></span>
- <xref:System.ServiceProcess.ServiceController>
- <xref:System.ServiceProcess.ServiceControllerStatus>
- <xref:System.ServiceProcess.ServiceController.WaitForStatus%2A>
- [<span data-ttu-id="9b73b-126">Guide pratique pour poursuivre un service Windows (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9b73b-126">How to: Continue a Windows Service (Visual Basic)</span></span>](../../../docs/framework/windows-services/how-to-continue-a-windows-service-visual-basic.md)
