---
title: Sécurité des Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- designer access security [Windows Forms]
- permissions [Windows Forms], Windows Forms
- Windows Forms, security
- security [Windows Forms]
- access control [Windows Forms], Windows Forms
- security policy [Windows Forms], Windows Forms
ms.assetid: 932d438a-5285-46d8-a958-8c93d0ad6cae
ms.openlocfilehash: 75016e9e04cf47782add18c87f7c677931743a4e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865642"
---
# <a name="windows-forms-security"></a><span data-ttu-id="d65ab-102">Sécurité des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d65ab-102">Windows Forms Security</span></span>
<span data-ttu-id="d65ab-103">Windows Forms propose un modèle de sécurité est basée sur le code (niveaux de sécurité sont définis pour le code, quel que soit l’utilisateur qui exécute le code).</span><span class="sxs-lookup"><span data-stu-id="d65ab-103">Windows Forms features a security model that is code-based (security levels are set for code, regardless of the user running the code).</span></span> <span data-ttu-id="d65ab-104">Cela s’ajoute tous les schémas de sécurité qui peuvent être déjà en place sur votre système informatique.</span><span class="sxs-lookup"><span data-stu-id="d65ab-104">This is in addition to any security schemas that may be in place already on your computer system.</span></span> <span data-ttu-id="d65ab-105">Celles-ci peuvent inclure celles figurant dans le navigateur (par exemple, la sécurité par zone disponible dans Internet Explorer) ou le système d’exploitation (par exemple, la sécurité basée sur les informations d’identification de Windows NT).</span><span class="sxs-lookup"><span data-stu-id="d65ab-105">These can include those in the browser (such as the zone-based security available in Internet Explorer) or the operating system (such as the credential-based security of Windows NT).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d65ab-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d65ab-106">In This Section</span></span>  
 [<span data-ttu-id="d65ab-107">Vue d’ensemble de la sécurité dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d65ab-107">Security in Windows Forms Overview</span></span>](../../../docs/framework/winforms/security-in-windows-forms-overview.md)  
 <span data-ttu-id="d65ab-108">Présente brièvement le modèle de sécurité .NET Framework et les étapes de base nécessaires pour assurer les formulaires Windows dans votre application.</span><span class="sxs-lookup"><span data-stu-id="d65ab-108">Briefly explains the .NET Framework security model and the basic steps necessary to ensure the Windows Forms in your application are secure.</span></span>  
  
 [<span data-ttu-id="d65ab-109">Accès plus sécurisé aux fichiers et aux données dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d65ab-109">More Secure File and Data Access in Windows Forms</span></span>](../../../docs/framework/winforms/more-secure-file-and-data-access-in-windows-forms.md)  
 <span data-ttu-id="d65ab-110">Décrit comment accéder aux fichiers et des données dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="d65ab-110">Describes how to access files and data in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="d65ab-111">Impression plus sécurisée dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d65ab-111">More Secure Printing in Windows Forms</span></span>](../../../docs/framework/winforms/more-secure-printing-in-windows-forms.md)  
 <span data-ttu-id="d65ab-112">Décrit comment accéder aux fonctionnalités d’impression dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="d65ab-112">Describes how to access printing features in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="d65ab-113">Considérations supplémentaires sur la sécurité des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d65ab-113">Additional Security Considerations in Windows Forms</span></span>](../../../docs/framework/winforms/additional-security-considerations-in-windows-forms.md)  
 <span data-ttu-id="d65ab-114">Décrit comment manipuler des fenêtres, l’utilisation du Presse-papiers et effectuer des appels au code non managé dans un environnement de confiance partiel.</span><span class="sxs-lookup"><span data-stu-id="d65ab-114">Describes performing window manipulation, using the Clipboard, and making calls to unmanaged code in a semi-trusted environment.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="d65ab-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d65ab-115">Related Sections</span></span>  
 [<span data-ttu-id="d65ab-116">NIB : Stratégie de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="d65ab-116">NIB: Default Security Policy</span></span>](https://msdn.microsoft.com/library/2c086873-0894-4f4d-8f7e-47427c1a3b55)  
 <span data-ttu-id="d65ab-117">Répertorie les autorisations par défaut accordées dans les jeux d’autorisations confiance totale, Intranet Local et Internet.</span><span class="sxs-lookup"><span data-stu-id="d65ab-117">Lists the default permissions granted in the Full Trust, Local Intranet, and Internet permission sets.</span></span>  
  
 [<span data-ttu-id="d65ab-118">NIB : Administration de stratégie de sécurité général</span><span class="sxs-lookup"><span data-stu-id="d65ab-118">NIB: General Security Policy Administration</span></span>](https://msdn.microsoft.com/library/5121fe35-f0e3-402c-94ab-4f35b0a87b4b)  
 <span data-ttu-id="d65ab-119">Fournit des informations sur l’administration de la stratégie de sécurité .NET Framework et l’élévation d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="d65ab-119">Gives information about the administering the .NET Framework security policy and elevating permissions.</span></span>  
  
 [<span data-ttu-id="d65ab-120">Autorisations dangereuses et Administration de stratégie</span><span class="sxs-lookup"><span data-stu-id="d65ab-120">Dangerous Permissions and Policy Administration</span></span>](../../../docs/framework/misc/dangerous-permissions-and-policy-administration.md)  
 <span data-ttu-id="d65ab-121">Traite de certaines autorisations du.NET Framework susceptibles de permettre le contournement du système de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d65ab-121">Discusses some of the.NET Framework permissions that can potentially allow the security system to be circumvented.</span></span>  
  
 [<span data-ttu-id="d65ab-122">Instructions de codage sécurisé</span><span class="sxs-lookup"><span data-stu-id="d65ab-122">Secure Coding Guidelines</span></span>](../../../docs/standard/security/secure-coding-guidelines.md)  
 <span data-ttu-id="d65ab-123">Liens vers des rubriques qui expliquent les meilleures pratiques pour l’écriture en toute sécurité de code par rapport à .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d65ab-123">Links to topics that explain the best practices for securely writing code against the .NET Framework.</span></span>  
  
 [<span data-ttu-id="d65ab-124">NIB : Demande d’autorisations</span><span class="sxs-lookup"><span data-stu-id="d65ab-124">NIB: Requesting Permissions</span></span>](https://msdn.microsoft.com/library/0447c49d-8cba-45e4-862c-ff0b59bebdc2)  
 <span data-ttu-id="d65ab-125">Décrit l’utilisation d’attributs pour informer le runtime les autorisations que votre code doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="d65ab-125">Discusses the use of attributes to let the runtime know what permissions your code needs to run.</span></span>  
  
 [<span data-ttu-id="d65ab-126">Concepts fondamentaux sur la sécurité</span><span class="sxs-lookup"><span data-stu-id="d65ab-126">Key Security Concepts</span></span>](../../../docs/standard/security/key-security-concepts.md)  
 <span data-ttu-id="d65ab-127">Liens vers des rubriques qui couvrent les aspects de sécurité du code base.</span><span class="sxs-lookup"><span data-stu-id="d65ab-127">Links to topics that cover the basic aspects of code security.</span></span>  
  
 [<span data-ttu-id="d65ab-128">Notions fondamentales de la sécurité d’accès du code</span><span class="sxs-lookup"><span data-stu-id="d65ab-128">Code Access Security Basics</span></span>](../../../docs/framework/misc/code-access-security-basics.md)  
 <span data-ttu-id="d65ab-129">Explique les principes fondamentaux de l’utilisation de la stratégie de sécurité du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d65ab-129">Discusses the basics of working with the .NET Framework run time security policy.</span></span>  
  
 [<span data-ttu-id="d65ab-130">NIB : Détermination des cas modifier la stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="d65ab-130">NIB: Determining When to Modify Security Policy</span></span>](https://msdn.microsoft.com/library/af749b17-e461-409d-84b9-a3d44789db16)  
 <span data-ttu-id="d65ab-131">Explique comment déterminer quand vos applications doivent diverger de la stratégie de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="d65ab-131">Explains how to determine when your applications need to diverge from the default security policy.</span></span>  
  
 [<span data-ttu-id="d65ab-132">NIB : Déploiement de stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="d65ab-132">NIB: Deploying Security Policy</span></span>](https://msdn.microsoft.com/library/f936c1e5-033b-4bd9-a3bd-a39ba733a681)  
 <span data-ttu-id="d65ab-133">Décrit la méthode la mieux adaptée pour déployer les modifications de stratégie de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d65ab-133">Discusses the best manner for deploying security policy changes.</span></span>
