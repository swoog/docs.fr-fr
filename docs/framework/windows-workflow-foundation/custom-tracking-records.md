---
title: Enregistrements de suivi personnalisé
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: 7f866713b5d6f6c82dff80864f2eccb5d2f6cb30
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54529828"
---
# <a name="custom-tracking-records"></a>Enregistrements de suivi personnalisé
Cette rubrique montre comment créer des enregistrements de suivi personnalisés et les remplir avec des données à émettre avec les enregistrements.  
  
## <a name="emitting-custom-tracking-records"></a>Émission d'enregistrements de suivi personnalisé  
 Les enregistrements de suivi personnalisés peuvent être issus d'une activité de code comme indiqué dans l'exemple suivant.  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
…  
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");  
            customRecord.Data.Add("SendTime", sendTime);  
            context.Track(customRecord);  
}  
```  
  
 Un <xref:System.Activities.Tracking.CustomTrackingRecord> est émis dans une activité de code en appelant la méthode <xref:System.Activities.NativeActivityContext.Track%2A> sur `ActvityContext`.  
  
## <a name="see-also"></a>Voir aussi
- [Surveillance de Windows Server App Fabric](https://go.microsoft.com/fwlink/?LinkId=201273)
- [Surveillance des Applications avec App Fabric](https://go.microsoft.com/fwlink/?LinkId=201275)
