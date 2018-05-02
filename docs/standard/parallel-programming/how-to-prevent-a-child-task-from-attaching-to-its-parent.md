---
title: 'Comment : empêcher une tâche enfant de s’attacher à son parent'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology: dotnet-standard
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, preventing attachments
ms.assetid: c0fb85d4-9e80-4905-9f65-29acc54201c4
caps.latest.revision: 5
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 654bfec4e8ba163c9dc9adf470c45401c0babd8b
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-prevent-a-child-task-from-attaching-to-its-parent"></a><span data-ttu-id="bd75a-102">Comment : empêcher une tâche enfant de s’attacher à son parent</span><span class="sxs-lookup"><span data-stu-id="bd75a-102">How to: Prevent a Child Task from Attaching to its Parent</span></span>
<span data-ttu-id="bd75a-103">Ce document explique comment empêcher une tâche enfant de s’attacher à la tâche parente.</span><span class="sxs-lookup"><span data-stu-id="bd75a-103">This document demonstrates how to prevent a child task from attaching to the parent task.</span></span> <span data-ttu-id="bd75a-104">Empêcher une tâche enfant de s’attacher à son parent est utile quand vous appelez un composant écrit par un tiers, qui utilise également des tâches.</span><span class="sxs-lookup"><span data-stu-id="bd75a-104">Preventing a child task from attaching to its parent is useful when you call a component that is written by a third party and that also uses tasks.</span></span> <span data-ttu-id="bd75a-105">Par exemple, un composant tiers qui utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent?displayProperty=nameWithType> pour créer un objet <xref:System.Threading.Tasks.Task> ou <xref:System.Threading.Tasks.Task%601> peut causer des problèmes dans votre code s’il est long ou s’il lève une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="bd75a-105">For example, a third-party component that uses the <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent?displayProperty=nameWithType> option to create a <xref:System.Threading.Tasks.Task> or <xref:System.Threading.Tasks.Task%601> object can cause problems in your code if it is long-running or throws an unhandled exception.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd75a-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd75a-106">Example</span></span>  
 <span data-ttu-id="bd75a-107">L’exemple suivant compare les effets d’utiliser les options par défaut à ceux d’empêcher une tâche enfant de s’attacher au parent.</span><span class="sxs-lookup"><span data-stu-id="bd75a-107">The following example compares the effects of using the default options to the effects of preventing a child task from attaching to the parent.</span></span> <span data-ttu-id="bd75a-108">L’exemple crée un objet <xref:System.Threading.Tasks.Task> qui appelle une bibliothèque tierce qui utilise également un objet <xref:System.Threading.Tasks.Task>.</span><span class="sxs-lookup"><span data-stu-id="bd75a-108">The example creates a <xref:System.Threading.Tasks.Task> object that calls into a third-party library that also uses a <xref:System.Threading.Tasks.Task> object.</span></span> <span data-ttu-id="bd75a-109">La bibliothèque tierce utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> pour créer l’objet <xref:System.Threading.Tasks.Task>.</span><span class="sxs-lookup"><span data-stu-id="bd75a-109">The third-party library uses the <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> option to create the <xref:System.Threading.Tasks.Task> object.</span></span> <span data-ttu-id="bd75a-110">L’application utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> pour créer la tâche parente.</span><span class="sxs-lookup"><span data-stu-id="bd75a-110">The application uses the <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> option to create the parent task.</span></span> <span data-ttu-id="bd75a-111">Cette option ordonne au runtime de supprimer la spécification <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> des tâches enfants.</span><span class="sxs-lookup"><span data-stu-id="bd75a-111">This option instructs the runtime to remove the <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> specification in child tasks.</span></span>  
  
 [!code-csharp[TPL_DenyChildAttach#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_denychildattach/cs/denychildattach.cs#1)]
 [!code-vb[TPL_DenyChildAttach#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_denychildattach/vb/denychildattach.vb#1)]  
  
 <span data-ttu-id="bd75a-112">Étant donné qu’une tâche parente ne se termine pas tant que toutes les tâches enfants ne sont pas achevées, une tâche enfant à exécution longue peut entraîner des performances médiocres de la part de l’application globale.</span><span class="sxs-lookup"><span data-stu-id="bd75a-112">Because a parent task does not finish until all child tasks finish, a long-running child task can cause the overall application to perform poorly.</span></span> <span data-ttu-id="bd75a-113">Dans cet exemple, quand l’application utilise les options par défaut pour créer une tâche parente, la tâche enfant doit se terminer avant la fin de la tâche parente.</span><span class="sxs-lookup"><span data-stu-id="bd75a-113">In this example, when the application uses the default options to create the parent task, the child task must finish before the parent task finishes.</span></span> <span data-ttu-id="bd75a-114">Quand l’application utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType>, l’enfant n’est pas attachée au parent.</span><span class="sxs-lookup"><span data-stu-id="bd75a-114">When the application uses the <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> option, the child is not attached to the parent.</span></span> <span data-ttu-id="bd75a-115">Par conséquent, l’application peut effectuer du travail supplémentaire dès que la tâche parente est terminée et avant qu’elle ne doive attendre la fin de la tâche enfant.</span><span class="sxs-lookup"><span data-stu-id="bd75a-115">Therefore, the application can perform additional work after the parent task finishes and before it must wait for the child task to finish.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bd75a-116">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bd75a-116">Compiling the Code</span></span>  
 <span data-ttu-id="bd75a-117">Copiez l’exemple de code et collez-le dans un projet Visual Studio, ou collez-le dans un fichier nommé `DenyChildAttach.cs` (`DenyChildAttach.vb` pour Visual Basic), puis exécutez la commande suivante dans une fenêtre d’invite de commandes Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bd75a-117">Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `DenyChildAttach.cs` (`DenyChildAttach.vb` for Visual Basic), and then run the following command in a Visual Studio Command Prompt window.</span></span>  
  
 <span data-ttu-id="bd75a-118">Visual C#</span><span class="sxs-lookup"><span data-stu-id="bd75a-118">Visual C#</span></span>  
  
 <span data-ttu-id="bd75a-119">**csc.exe DenyChildAttach.cs**</span><span class="sxs-lookup"><span data-stu-id="bd75a-119">**csc.exe DenyChildAttach.cs**</span></span>  
  
 <span data-ttu-id="bd75a-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bd75a-120">Visual Basic</span></span>  
  
 <span data-ttu-id="bd75a-121">**vbc.exe DenyChildAttach.vb**</span><span class="sxs-lookup"><span data-stu-id="bd75a-121">**vbc.exe DenyChildAttach.vb**</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="bd75a-122">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="bd75a-122">Robust Programming</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd75a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd75a-123">See Also</span></span>  
 [<span data-ttu-id="bd75a-124">Programmation asynchrone basée sur les tâches</span><span class="sxs-lookup"><span data-stu-id="bd75a-124">Task-based Asynchronous Programming</span></span>](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
