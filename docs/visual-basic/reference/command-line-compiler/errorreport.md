---
title: -errorreport
ms.date: 03/10/2018
helpviewer_keywords:
- -errorreport compiler option [Visual Basic]
- /errorreport compiler option [Visual Basic]
- errorreport compiler option [Visual Basic]
ms.assetid: a7fe83a2-a6d8-460c-8dad-79a8f433f501
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8c6a81d3491f4876cfbca80aa8fda6640187176
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33650931"
---
# <a name="-errorreport"></a><span data-ttu-id="70b47-102">-errorreport</span><span class="sxs-lookup"><span data-stu-id="70b47-102">-errorreport</span></span>
<span data-ttu-id="70b47-103">Spécifie comment le compilateur Visual Basic doit signaler les erreurs internes du compilateur.</span><span class="sxs-lookup"><span data-stu-id="70b47-103">Specifies how the Visual Basic compiler should report internal compiler errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70b47-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70b47-104">Syntax</span></span>  
  
```  
-errorreport:{ prompt | queue | send | none }  
```  
  
## <a name="remarks"></a><span data-ttu-id="70b47-105">Notes</span><span class="sxs-lookup"><span data-stu-id="70b47-105">Remarks</span></span>  
 <span data-ttu-id="70b47-106">Cette option offre un moyen pratique de signaler une erreur interne du compilateur de Visual Basic (ICE) à l’équipe Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="70b47-106">This option provides a convenient way to report a Visual Basic internal compiler error (ICE) to the Visual Basic team at Microsoft.</span></span> <span data-ttu-id="70b47-107">Par défaut, le compilateur n’envoie aucune information à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-107">By default, the compiler sends no information to Microsoft.</span></span> <span data-ttu-id="70b47-108">Toutefois, si vous rencontrez une erreur interne du compilateur, cette option vous permet de signaler l’erreur à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-108">However, if you do encounter an internal compiler error, this option allows you to report the error to Microsoft.</span></span> <span data-ttu-id="70b47-109">Ces informations aideront les ingénieurs de Microsoft à identifier la cause et peuvent aider à améliorer la prochaine version de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="70b47-109">That information will help Microsoft engineers identify the cause and may help improve the next release of Visual Basic.</span></span>  
  
 <span data-ttu-id="70b47-110">Capacité d’un utilisateur d’envoyer des rapports dépend des autorisations de stratégie ordinateur et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="70b47-110">A user's ability to send reports depends on machine and user policy permissions.</span></span>  
  
 <span data-ttu-id="70b47-111">Le tableau suivant résume l’effet de la `-errorreport` option.</span><span class="sxs-lookup"><span data-stu-id="70b47-111">The following table summarizes the effect of the `-errorreport` option.</span></span>  
  
|<span data-ttu-id="70b47-112">Option</span><span class="sxs-lookup"><span data-stu-id="70b47-112">Option</span></span>|<span data-ttu-id="70b47-113">Comportement</span><span class="sxs-lookup"><span data-stu-id="70b47-113">Behavior</span></span>|  
|---|---|  
|`prompt`|<span data-ttu-id="70b47-114">Si une erreur interne du compilateur se produit, une boîte de dialogue s’affiche afin que vous puissiez afficher les données collectées par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="70b47-114">If an internal compiler error occurs, a dialog box comes up so that you can view the exact data that the compiler collected.</span></span> <span data-ttu-id="70b47-115">Vous pouvez déterminer s’il existe des informations sensibles dans le rapport d’erreurs et prendre une décision quant à envoyer à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-115">You can determine if there is any sensitive information in the error report and make a decision on whether to send it to Microsoft.</span></span> <span data-ttu-id="70b47-116">Si vous décidez d’envoyer, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-116">If you decide to send it, and the machine and user policy settings allow it, the compiler sends the data to Microsoft.</span></span>|  
|`queue`|<span data-ttu-id="70b47-117">Met le rapport d’erreurs en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="70b47-117">Queues the error report.</span></span> <span data-ttu-id="70b47-118">Lorsque vous vous connectez avec des privilèges d’administrateur, vous pouvez signaler les erreurs depuis la dernière fois que vous étiez connecté (vous ne serez pas invité à envoyer des rapports pour les échecs de plus d’une fois tous les trois jours).</span><span class="sxs-lookup"><span data-stu-id="70b47-118">When you log in with administrator privileges, you can report any failures since the last time you were logged in (you will not be prompted to send reports for failures more than once every three days).</span></span> <span data-ttu-id="70b47-119">Il s’agit du comportement par défaut lors de la `-errorreport` option n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="70b47-119">This is the default behavior when the `-errorreport` option is not specified.</span></span>|  
|`send`|<span data-ttu-id="70b47-120">Si une erreur interne du compilateur se produit et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-120">If an internal compiler error occurs, and the machine and user policy settings allow it, the compiler sends the data to Microsoft.</span></span><br /><br /> <span data-ttu-id="70b47-121">L’option `-errorreport:send` tente d’envoyer automatiquement les informations d’erreur à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-121">The option `-errorreport:send` attempts to automatically send error information to Microsoft.</span></span> <span data-ttu-id="70b47-122">Cette option dépend du Registre.</span><span class="sxs-lookup"><span data-stu-id="70b47-122">This option depends on the registry.</span></span> <span data-ttu-id="70b47-123">Pour plus d’informations sur les valeurs appropriées dans le Registre, consultez [comment activer le rapport d’erreurs automatique dans les outils de ligne de commande de Visual Studio 2008](http://go.microsoft.com/fwlink/?LinkID=184695).</span><span class="sxs-lookup"><span data-stu-id="70b47-123">For more information about setting the appropriate values in the registry, see [How to Turn on Automatic Error Reporting in Visual Studio 2008 Command-line Tools](http://go.microsoft.com/fwlink/?LinkID=184695).</span></span>|  
|`none`|<span data-ttu-id="70b47-124">Si une erreur interne du compilateur se produit, il ne sera pas collectée ou envoyée à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-124">If an internal compiler error occurs, it will not be collected or sent to Microsoft.</span></span>|  
  
 <span data-ttu-id="70b47-125">Le compilateur envoie les données qui comprend la pile au moment de l’erreur, qui inclut généralement du code source.</span><span class="sxs-lookup"><span data-stu-id="70b47-125">The compiler sends data that includes the stack at the time of the error, which usually includes some source code.</span></span> <span data-ttu-id="70b47-126">Si `-errorreport` est utilisé avec le [- /bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, l’intégralité du fichier source est envoyé.</span><span class="sxs-lookup"><span data-stu-id="70b47-126">If `-errorreport` is used with the [-bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, then the entire source file is sent.</span></span>  
  
 <span data-ttu-id="70b47-127">Il est préférable d’utiliser cette option avec la [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, car elle permet aux ingénieurs Microsoft plus facilement de reproduire l’erreur.</span><span class="sxs-lookup"><span data-stu-id="70b47-127">This option is best used with the [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, because it allows Microsoft engineers to more easily reproduce the error.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="70b47-128">Le `-errorreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="70b47-128">The `-errorreport` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="70b47-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="70b47-129">Example</span></span>  
 <span data-ttu-id="70b47-130">Le code suivant tente de compiler `T2.vb`, et si le compilateur rencontre une erreur interne du compilateur, il vous invite à envoyer le rapport d’erreurs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70b47-130">The following code attempts to compile `T2.vb`, and if the compiler encounters an internal compiler error, it prompts you to send the error report to Microsoft.</span></span>  
  
```  
vbc -errorreport:prompt t2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="70b47-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70b47-131">See Also</span></span>  
 [<span data-ttu-id="70b47-132">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="70b47-132">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="70b47-133">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="70b47-133">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [<span data-ttu-id="70b47-134">-bugreport</span><span class="sxs-lookup"><span data-stu-id="70b47-134">-bugreport</span></span>](../../../visual-basic/reference/command-line-compiler/bugreport.md)
