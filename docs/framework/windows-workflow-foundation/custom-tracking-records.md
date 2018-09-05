---
title: Enregistrements de suivi personnalisé
ms.date: 03/30/2017
ms.assetid: 24284565-c68b-40bf-b7f1-e148d151a6fc
ms.openlocfilehash: ef3c20890f33f3ffd07a9c88de863e1ebe24851f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520183"
---
# <a name="custom-tracking-records"></a><span data-ttu-id="99a7c-102">Enregistrements de suivi personnalisé</span><span class="sxs-lookup"><span data-stu-id="99a7c-102">Custom Tracking Records</span></span>
<span data-ttu-id="99a7c-103">Cette rubrique montre comment créer des enregistrements de suivi personnalisés et les remplir avec des données à émettre avec les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="99a7c-103">This topic demonstrates how to create custom tracking records and populate them with data to be emitted along with the records.</span></span>  
  
## <a name="emitting-custom-tracking-records"></a><span data-ttu-id="99a7c-104">Émission d'enregistrements de suivi personnalisé</span><span class="sxs-lookup"><span data-stu-id="99a7c-104">Emitting Custom Tracking Records</span></span>  
 <span data-ttu-id="99a7c-105">Les enregistrements de suivi personnalisés peuvent être issus d'une activité de code comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="99a7c-105">Custom tracking records can be emitted from a code activity as shown in the following example.</span></span>  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
…  
            CustomTrackingRecord customRecord = new CustomTrackingRecord("CustomEmailSentEvent");  
            customRecord.Data.Add("SendTime", sendTime);  
            context.Track(customRecord);  
}  
```  
  
 <span data-ttu-id="99a7c-106">Un <xref:System.Activities.Tracking.CustomTrackingRecord> est émis dans une activité de code en appelant la méthode <xref:System.Activities.NativeActivityContext.Track%2A> sur `ActvityContext`.</span><span class="sxs-lookup"><span data-stu-id="99a7c-106">A <xref:System.Activities.Tracking.CustomTrackingRecord> is emitted in a code activity by invoking the <xref:System.Activities.NativeActivityContext.Track%2A> method on the `ActvityContext`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99a7c-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99a7c-107">See Also</span></span>  
 [<span data-ttu-id="99a7c-108">Surveillance de Windows Server App Fabric</span><span class="sxs-lookup"><span data-stu-id="99a7c-108">Windows Server App Fabric Monitoring</span></span>](https://go.microsoft.com/fwlink/?LinkId=201273)  
 [<span data-ttu-id="99a7c-109">Surveillance des Applications avec App Fabric</span><span class="sxs-lookup"><span data-stu-id="99a7c-109">Monitoring Applications with App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkId=201275)
