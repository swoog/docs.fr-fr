---
title: Événement ETW d'exception Thrown_V1
ms.date: 03/30/2017
helpviewer_keywords:
- ExceptionThrown_V1 event [.NET Framework]
- ETW, ExceptionThrown_V1 event (CLR)
ms.assetid: 0d3da389-6b7b-40f6-a877-fac546d6019c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 865b7b16d5807bd9161855f453128a63c84eab96
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43400820"
---
# <a name="exception-thrownv1-etw-event"></a><span data-ttu-id="e4a5e-102">Événement ETW d'exception Thrown_V1</span><span class="sxs-lookup"><span data-stu-id="e4a5e-102">Exception Thrown_V1 ETW Event</span></span>
<span data-ttu-id="e4a5e-103">Cet événement capture des informations sur les exceptions levées.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-103">This event captures information about the exceptions that are thrown.</span></span>  
  
 <span data-ttu-id="e4a5e-104">Le tableau suivant affiche le mot clé sous lequel l’événement est déclenché, ainsi que le niveau de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-104">The following table shows the keyword under which the event is raised, and the level of the event.</span></span> <span data-ttu-id="e4a5e-105">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="e4a5e-105">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="e4a5e-106">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="e4a5e-106">Keyword for raising the event</span></span>|<span data-ttu-id="e4a5e-107">Niveau</span><span class="sxs-lookup"><span data-stu-id="e4a5e-107">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="e4a5e-108">`ExceptionKeyword` (0x8000)</span><span class="sxs-lookup"><span data-stu-id="e4a5e-108">`ExceptionKeyword` (0x8000)</span></span>|<span data-ttu-id="e4a5e-109">Avertissement (2)</span><span class="sxs-lookup"><span data-stu-id="e4a5e-109">Warning (2)</span></span>|  
  
 <span data-ttu-id="e4a5e-110">Le tableau suivant affiche des informations sur les événements.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-110">The following table shows event information.</span></span>  
  
|<span data-ttu-id="e4a5e-111">Événement</span><span class="sxs-lookup"><span data-stu-id="e4a5e-111">Event</span></span>|<span data-ttu-id="e4a5e-112">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="e4a5e-112">Event ID</span></span>|<span data-ttu-id="e4a5e-113">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="e4a5e-113">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ExceptionThrown_V1`|<span data-ttu-id="e4a5e-114">80</span><span class="sxs-lookup"><span data-stu-id="e4a5e-114">80</span></span>|<span data-ttu-id="e4a5e-115">Une exception managée est levée.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-115">A managed exception is thrown.</span></span>|  
  
 <span data-ttu-id="e4a5e-116">Le tableau suivant affiche des données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-116">The following table shows event data.</span></span>  
  
|<span data-ttu-id="e4a5e-117">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="e4a5e-117">Field name</span></span>|<span data-ttu-id="e4a5e-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="e4a5e-118">Data type</span></span>|<span data-ttu-id="e4a5e-119">Description</span><span class="sxs-lookup"><span data-stu-id="e4a5e-119">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="e4a5e-120">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="e4a5e-120">Exception Type</span></span>|<span data-ttu-id="e4a5e-121">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="e4a5e-121">win:UnicodeString</span></span>|<span data-ttu-id="e4a5e-122">Type de l’exception, par exemple `System.NullReferenceException`.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-122">Type of the exception; for example, `System.NullReferenceException`.</span></span>|  
|<span data-ttu-id="e4a5e-123">Message d’exception</span><span class="sxs-lookup"><span data-stu-id="e4a5e-123">Exception Message</span></span>|<span data-ttu-id="e4a5e-124">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="e4a5e-124">win:UnicodeString</span></span>|<span data-ttu-id="e4a5e-125">Message d’exception réel.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-125">Actual exception message.</span></span>|  
|<span data-ttu-id="e4a5e-126">EIPCodeThrow</span><span class="sxs-lookup"><span data-stu-id="e4a5e-126">EIPCodeThrow</span></span>|<span data-ttu-id="e4a5e-127">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="e4a5e-127">win:Pointer</span></span>|<span data-ttu-id="e4a5e-128">Pointeur d’instruction où l’exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-128">Instruction pointer where exception occurred.</span></span>|  
|<span data-ttu-id="e4a5e-129">ExceptionHR</span><span class="sxs-lookup"><span data-stu-id="e4a5e-129">ExceptionHR</span></span>|<span data-ttu-id="e4a5e-130">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="e4a5e-130">win:UInt32</span></span>|<span data-ttu-id="e4a5e-131">Exception [HRESULT](https://go.microsoft.com/fwlink/?LinkId=179679).</span><span class="sxs-lookup"><span data-stu-id="e4a5e-131">Exception [HRESULT](https://go.microsoft.com/fwlink/?LinkId=179679).</span></span>|  
|<span data-ttu-id="e4a5e-132">ExceptionFlags</span><span class="sxs-lookup"><span data-stu-id="e4a5e-132">ExceptionFlags</span></span>|<span data-ttu-id="e4a5e-133">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="e4a5e-133">win:UInt16</span></span>|<span data-ttu-id="e4a5e-134">0x01 : HasInnerException (consultez [Événements ETW du CLR](../../../docs/framework/performance/clr-etw-events.md) dans la documentation Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="e4a5e-134">0x01: HasInnerException (see [CLR ETW Events](../../../docs/framework/performance/clr-etw-events.md) in the Visual Basic documentation).</span></span><br /><br /> <span data-ttu-id="e4a5e-135">0x02 : IsNestedException.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-135">0x02: IsNestedException.</span></span><br /><br /> <span data-ttu-id="e4a5e-136">0x04 : IsRethrownException.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-136">0x04: IsRethrownException.</span></span><br /><br /> <span data-ttu-id="e4a5e-137">0x08 : IsCorruptedStateException (indique que l’état du processus est endommagé ; consultez [Gestion des exceptions dans un état endommagé](https://go.microsoft.com/fwlink/?LinkId=179681) sur MSDN).</span><span class="sxs-lookup"><span data-stu-id="e4a5e-137">0x08: IsCorruptedStateException (indicates that the process state is corrupt; see [Handling Corrupted State Exceptions](https://go.microsoft.com/fwlink/?LinkId=179681) on MSDN).</span></span><br /><br /> <span data-ttu-id="e4a5e-138">0x10 : IsCLSCompliant (une exception qui dérive d’<xref:System.Exception> est conforme CLS ; sinon elle n’est pas conforme CLS).</span><span class="sxs-lookup"><span data-stu-id="e4a5e-138">0x10: IsCLSCompliant (an exception that derives from <xref:System.Exception> is CLS-compliant; otherwise, it is not CLS-compliant).</span></span>|  
|<span data-ttu-id="e4a5e-139">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="e4a5e-139">ClrInstanceID</span></span>|<span data-ttu-id="e4a5e-140">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="e4a5e-140">win:UInt16</span></span>|<span data-ttu-id="e4a5e-141">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="e4a5e-141">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e4a5e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4a5e-142">See Also</span></span>  
 [<span data-ttu-id="e4a5e-143">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="e4a5e-143">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
