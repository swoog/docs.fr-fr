---
title: 'Procédure : écrire des messages de journal (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application.Log object, writing log messags
ms.assetid: 972a3e0c-2996-4623-a7a9-d7ebc4d207f8
ms.openlocfilehash: 4b4210983aa5bd57f1b0a89f2f06f089e98670f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594949"
---
# <a name="how-to-write-log-messages-visual-basic"></a>Procédure : écrire des messages de journal (Visual Basic)
Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur votre application. Cet exemple montre comment utiliser la méthode `My.Application.Log.WriteEntry` pour enregistrer des informations de traçage.  
  
 Pour journaliser des informations sur les exceptions, utilisez la méthode `My.Application.Log.WriteException`. Voir [Guide pratique pour journaliser des exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md).  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise la méthode `My.Application.Log.WriteEntry` pour écrire les informations de traçage.  
  
 [!code-vb[VbVbalrMyApplicationLog#11](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-write-log-messages_1.vb)]  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Vérifiez que les données que vous écrivez dans le journal n’incluent pas d’informations sensibles, comme des mots de passe utilisateur. Pour plus d’informations, consultez [Utilisation des journaux d’application](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [Utilisation des journaux des applications](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)
- [Guide pratique pour journaliser des exception](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)
- [Procédure pas à pas : Détermination de l’emplacement des informations My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)
- [Procédure pas à pas : Modification de l’emplacement des informations My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)
- [Procédure pas à pas : Filtrage de la sortie de My.Application.Log](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md)
