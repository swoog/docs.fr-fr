---
title: Traçage
ms.date: 03/30/2017
ms.assetid: 2649eae2-dbf8-421c-9cfb-cfa9e01de87f
ms.openlocfilehash: 3520d2aca07f988c45d65d5d8113d05292a37638
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64664944"
---
# <a name="tracing"></a><span data-ttu-id="ebd81-102">Traçage</span><span class="sxs-lookup"><span data-stu-id="ebd81-102">Tracing</span></span>
<span data-ttu-id="ebd81-103">Windows Communication Foundation (WCF) fournit une instrumentation de l’application et les données de diagnostic pour la surveillance des pannes et l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ebd81-103">Windows Communication Foundation (WCF) provides application instrumentation and diagnostic data for fault monitoring and analysis.</span></span> <span data-ttu-id="ebd81-104">Vous pouvez utiliser le suivi au lieu d'un débogueur pour comprendre le comportement d'une application ou la raison de sa défaillance.</span><span class="sxs-lookup"><span data-stu-id="ebd81-104">You can use tracing instead of a debugger to understand how an application is behaving, or why it faults.</span></span> <span data-ttu-id="ebd81-105">Vous pouvez également mettre en corrélation les erreurs et le traitement sur l'ensemble des composants afin de fournir une expérience de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="ebd81-105">You can also correlate faults and processing across components to provide an end-to-end experience.</span></span>  
  
 <span data-ttu-id="ebd81-106">WCF génère les données suivantes pour le suivi de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="ebd81-106">WCF outputs the following data for diagnostic tracing:</span></span>  
  
- <span data-ttu-id="ebd81-107">Suivis pour les jalons de processus sur l'ensemble des composants des applications, tels que les appels d'opération, exceptions de code, avertissements et autres événements de traitement significatifs.</span><span class="sxs-lookup"><span data-stu-id="ebd81-107">Traces for process milestones across all components of the applications, such as operation calls, code exceptions, warnings and other significant processing events."</span></span>  
  
- <span data-ttu-id="ebd81-108">Événements d’erreur Windows en cas de dysfonctionnement de la fonctionnalité de suivi.</span><span class="sxs-lookup"><span data-stu-id="ebd81-108">Windows error events when the tracing feature malfunctions.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ebd81-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ebd81-109">In This Section</span></span>  
 [<span data-ttu-id="ebd81-110">Configuration du suivi</span><span class="sxs-lookup"><span data-stu-id="ebd81-110">Configuring Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/configuring-tracing.md)  
  
 <span data-ttu-id="ebd81-111">Cette rubrique décrit comment configurer le suivi à différents niveaux en fonction de vos besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ebd81-111">This topic describes how you can configure tracing at different levels to suit your specific need.</span></span>  
  
 [<span data-ttu-id="ebd81-112">Suivi de bout en bout</span><span class="sxs-lookup"><span data-stu-id="ebd81-112">End-to-End Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/end-to-end-tracing.md)  
  
 <span data-ttu-id="ebd81-113">Cette section décrit comment utiliser le suivi et la propagation d'activité pour la corrélation de bout en bout à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="ebd81-113">This section describes how you can use Activity Tracing and Propagation for end-to-end correlation to assist debugging.</span></span>  
  
 [<span data-ttu-id="ebd81-114">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="ebd81-114">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
  
 <span data-ttu-id="ebd81-115">Cette section décrit comment utiliser le suivi pour déboguer votre application.</span><span class="sxs-lookup"><span data-stu-id="ebd81-115">This section describes how you can use tracing to debug your application.</span></span>  
  
 [<span data-ttu-id="ebd81-116">Problèmes de sécurité et conseils utiles pour le suivi</span><span class="sxs-lookup"><span data-stu-id="ebd81-116">Security Concerns and Useful Tips for Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/security-concerns-and-useful-tips-for-tracing.md)  
  
 <span data-ttu-id="ebd81-117">Cette rubrique décrit comment empêcher l'exposition des informations sensibles et fournit également des conseils utiles en cas d'utilisation de WebHost.</span><span class="sxs-lookup"><span data-stu-id="ebd81-117">This topic describes how you can protect sensitive information from being exposed, as well as useful tips when using WebHost.</span></span>  
  
 [<span data-ttu-id="ebd81-118">Informations de référence sur les suivis</span><span class="sxs-lookup"><span data-stu-id="ebd81-118">Traces Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/traces-reference.md)  
  
 <span data-ttu-id="ebd81-119">Cette rubrique répertorie tous les suivis générés par WCF.</span><span class="sxs-lookup"><span data-stu-id="ebd81-119">This topic lists all the traces generated by WCF.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebd81-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd81-120">See also</span></span>

- [<span data-ttu-id="ebd81-121">Outil Service Trace Viewer (SvcTraceViewer.exe)</span><span class="sxs-lookup"><span data-stu-id="ebd81-121">Service Trace Viewer Tool (SvcTraceViewer.exe)</span></span>](../../../../../docs/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe.md)
