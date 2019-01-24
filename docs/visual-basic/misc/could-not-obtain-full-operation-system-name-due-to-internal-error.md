---
title: Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: df7a91ea5763c0fe4b7a1993bec29f1b1bb43fcc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723293"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a>Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne. Ceci peut être dû au fait que WMI est absent de l’ordinateur actuel.  
  
 Un appel à la propriété `My.Computer.Info.OSFullName` a échoué. WMI (Windows Management Instrumentation) n’est peut-être pas installé sur l’ordinateur actuel.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété `My.Computer.Info.OSFullName` .  
  
2.  Pour plus d’informations sur WMI et comment l’installer, accédez à et recherchez « Windows Management Instrumentation Core ».  
  
## <a name="see-also"></a>Voir aussi
- [My.Computer.Info.OSFullName](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [Gestion des exceptions et des erreurs en Visual Basic](https://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)
- [Try...Catch...Finally (instruction)](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
