---
title: "Comment : empêcher une tâche enfant de s’attacher à son parent"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, preventing attachments
ms.assetid: c0fb85d4-9e80-4905-9f65-29acc54201c4
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 2cab2fb9c26a8ddaa868cafebac718e5dfd6baa0
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-prevent-a-child-task-from-attaching-to-its-parent"></a>Comment : empêcher une tâche enfant de s’attacher à son parent
Ce document explique comment empêcher une tâche enfant de s’attacher à la tâche parente. Empêcher une tâche enfant de s’attacher à son parent est utile quand vous appelez un composant écrit par un tiers, qui utilise également des tâches. Par exemple, un composant tiers qui utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent?displayProperty=nameWithType> pour créer un objet <xref:System.Threading.Tasks.Task> ou <xref:System.Threading.Tasks.Task%601> peut causer des problèmes dans votre code s’il est long ou s’il lève une exception non gérée.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant compare les effets d’utiliser les options par défaut à ceux d’empêcher une tâche enfant de s’attacher au parent. L’exemple crée un objet <xref:System.Threading.Tasks.Task> qui appelle une bibliothèque tierce qui utilise également un objet <xref:System.Threading.Tasks.Task>. La bibliothèque tierce utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> pour créer l’objet <xref:System.Threading.Tasks.Task>. L’application utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> pour créer la tâche parente. Cette option ordonne au runtime de supprimer la spécification <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> des tâches enfants.  
  
 [!code-csharp[TPL_DenyChildAttach#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_denychildattach/cs/denychildattach.cs#1)]
 [!code-vb[TPL_DenyChildAttach#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_denychildattach/vb/denychildattach.vb#1)]  
  
 Étant donné qu’une tâche parente ne se termine pas tant que toutes les tâches enfants ne sont pas achevées, une tâche enfant à exécution longue peut entraîner des performances médiocres de la part de l’application globale. Dans cet exemple, quand l’application utilise les options par défaut pour créer une tâche parente, la tâche enfant doit se terminer avant la fin de la tâche parente. Quand l’application utilise l’option <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType>, l’enfant n’est pas attachée au parent. Par conséquent, l’application peut effectuer du travail supplémentaire dès que la tâche parente est terminée et avant qu’elle ne doive attendre la fin de la tâche enfant.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Copiez l’exemple de code et collez-le dans un projet Visual Studio, ou collez-le dans un fichier nommé `DenyChildAttach.cs` (`DenyChildAttach.vb` pour [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]), puis exécutez la commande suivante dans une fenêtre d’invite de commandes Visual Studio.  
  
 [!INCLUDE[csprcs](../../../includes/csprcs-md.md)]  
  
 **csc.exe DenyChildAttach.cs**  
  
 [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)]  
  
 **vbc.exe DenyChildAttach.vb**  
  
## <a name="robust-programming"></a>Programmation fiable  
  
## <a name="see-also"></a>Voir aussi  
 [Programmation asynchrone basée sur les tâches](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
