---
title: -errorreport
ms.date: 08/14/2018
helpviewer_keywords:
- -errorreport compiler option [Visual Basic]
- /errorreport compiler option [Visual Basic]
- errorreport compiler option [Visual Basic]
ms.assetid: a7fe83a2-a6d8-460c-8dad-79a8f433f501
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d093b8ce4413a375e79eec239be37e83ac674d05
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43417647"
---
# <a name="-errorreport"></a><span data-ttu-id="e467d-102">-errorreport</span><span class="sxs-lookup"><span data-stu-id="e467d-102">-errorreport</span></span>

<span data-ttu-id="e467d-103">Spécifie comment le compilateur Visual Basic doit signaler les erreurs internes du compilateur.</span><span class="sxs-lookup"><span data-stu-id="e467d-103">Specifies how the Visual Basic compiler should report internal compiler errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e467d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e467d-104">Syntax</span></span>

```
-errorreport:{ prompt | queue | send | none }
```

## <a name="remarks"></a><span data-ttu-id="e467d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e467d-105">Remarks</span></span>

<span data-ttu-id="e467d-106">Cette option fournit un moyen pratique pour signaler une erreur interne du compilateur de Visual Basic (ICE) à l’équipe Visual Basic chez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-106">This option provides a convenient way to report a Visual Basic internal compiler error (ICE) to the Visual Basic team at Microsoft.</span></span> <span data-ttu-id="e467d-107">Par défaut, le compilateur n’envoie aucune information à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-107">By default, the compiler sends no information to Microsoft.</span></span> <span data-ttu-id="e467d-108">Toutefois, si vous rencontrez une erreur interne du compilateur, cette option permet de signaler l’erreur à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-108">However, if you do encounter an internal compiler error, this option allows you to report the error to Microsoft.</span></span> <span data-ttu-id="e467d-109">Ces informations aideront les ingénieurs Microsoft à identifier la cause et peuvent contribuer à améliorer la prochaine version de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e467d-109">That information will help Microsoft engineers identify the cause and may help improve the next release of Visual Basic.</span></span>

<span data-ttu-id="e467d-110">Capacité d’un utilisateur d’envoyer des rapports dépend des autorisations de stratégie ordinateur et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e467d-110">A user's ability to send reports depends on machine and user policy permissions.</span></span>

<span data-ttu-id="e467d-111">Le tableau suivant résume l’effet de la `-errorreport` option.</span><span class="sxs-lookup"><span data-stu-id="e467d-111">The following table summarizes the effect of the `-errorreport` option.</span></span>

|<span data-ttu-id="e467d-112">Option</span><span class="sxs-lookup"><span data-stu-id="e467d-112">Option</span></span>|<span data-ttu-id="e467d-113">Comportement</span><span class="sxs-lookup"><span data-stu-id="e467d-113">Behavior</span></span>|
|---|---|
|`prompt`|<span data-ttu-id="e467d-114">Si une erreur interne du compilateur se produit, une boîte de dialogue s’affiche afin que vous puissiez afficher les données exactes collectées par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="e467d-114">If an internal compiler error occurs, a dialog box comes up so that you can view the exact data that the compiler collected.</span></span> <span data-ttu-id="e467d-115">Vous pouvez déterminer s’il existe des informations sensibles dans le rapport d’erreurs et prendre une décision concernant s’il faut envoyer à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-115">You can determine if there is any sensitive information in the error report and make a decision on whether to send it to Microsoft.</span></span> <span data-ttu-id="e467d-116">Si vous décidez d’envoyer, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-116">If you decide to send it, and the machine and user policy settings allow it, the compiler sends the data to Microsoft.</span></span>|
|`queue`|<span data-ttu-id="e467d-117">Met le rapport d’erreurs en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="e467d-117">Queues the error report.</span></span> <span data-ttu-id="e467d-118">Lorsque vous vous connectez avec des privilèges d’administrateur, vous pouvez signaler toute défaillance depuis la dernière fois que vous étiez connecté (vous ne serez pas invité à envoyer des rapports d’échecs plus d’une fois tous les trois jours).</span><span class="sxs-lookup"><span data-stu-id="e467d-118">When you log in with administrator privileges, you can report any failures since the last time you were logged in (you will not be prompted to send reports for failures more than once every three days).</span></span> <span data-ttu-id="e467d-119">Il s’agit du comportement par défaut lors de la `-errorreport` option n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e467d-119">This is the default behavior when the `-errorreport` option is not specified.</span></span>|
|`send`|<span data-ttu-id="e467d-120">Si une erreur interne du compilateur se produit, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-120">If an internal compiler error occurs, and the machine and user policy settings allow it, the compiler sends the data to Microsoft.</span></span><br /><br /> <span data-ttu-id="e467d-121">L’option `-errorreport:send` tente d’envoyer automatiquement des informations d’erreur à Microsoft si le rapport est activé par le [rapport d’erreurs Windows](/windows/desktop/wer/windows-error-reporting) paramètres système.</span><span class="sxs-lookup"><span data-stu-id="e467d-121">The option `-errorreport:send` attempts to automatically send error information to Microsoft if reporting is enabled by the [Windows Error Reporting](/windows/desktop/wer/windows-error-reporting) system settings.</span></span> |
|`none`|<span data-ttu-id="e467d-122">Si une erreur interne du compilateur se produit, il ne sera pas être collectée ou envoyée à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-122">If an internal compiler error occurs, it will not be collected or sent to Microsoft.</span></span>|

<span data-ttu-id="e467d-123">Le compilateur envoie des données qui inclut la pile au moment de l’erreur, ce qui inclut généralement du code source.</span><span class="sxs-lookup"><span data-stu-id="e467d-123">The compiler sends data that includes the stack at the time of the error, which usually includes some source code.</span></span> <span data-ttu-id="e467d-124">Si `-errorreport` est utilisé avec le [- bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, alors le fichier source entier est envoyé.</span><span class="sxs-lookup"><span data-stu-id="e467d-124">If `-errorreport` is used with the [-bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, then the entire source file is sent.</span></span>

<span data-ttu-id="e467d-125">Cette option est mieux utilisée avec le [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, car elle permet aux ingénieurs Microsoft plus facilement reproduire l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e467d-125">This option is best used with the [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, because it allows Microsoft engineers to more easily reproduce the error.</span></span>

> [!NOTE]
> <span data-ttu-id="e467d-126">Le `-errorreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e467d-126">The `-errorreport` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>

## <a name="example"></a><span data-ttu-id="e467d-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="e467d-127">Example</span></span>

<span data-ttu-id="e467d-128">Le code suivant tente de compiler `T2.vb`, et si le compilateur rencontre une erreur interne du compilateur, il vous invite à envoyer le rapport d’erreurs à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e467d-128">The following code attempts to compile `T2.vb`, and if the compiler encounters an internal compiler error, it prompts you to send the error report to Microsoft.</span></span>

```
vbc -errorreport:prompt t2.vb
```

## <a name="see-also"></a><span data-ttu-id="e467d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e467d-129">See also</span></span>

- [<span data-ttu-id="e467d-130">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e467d-130">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="e467d-131">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="e467d-131">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="e467d-132">-bugreport</span><span class="sxs-lookup"><span data-stu-id="e467d-132">-bugreport</span></span>](../../../visual-basic/reference/command-line-compiler/bugreport.md)
