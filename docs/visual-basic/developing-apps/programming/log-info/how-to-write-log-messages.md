---
title: 'Procédure : écrire des messages de journal (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application.Log object, writing log messages
ms.assetid: 972a3e0c-2996-4623-a7a9-d7ebc4d207f8
ms.openlocfilehash: 007d08917ed5ecae6889d03d820d48e4695c9344
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57676120"
---
# <a name="how-to-write-log-messages-visual-basic"></a><span data-ttu-id="fc715-102">Procédure : écrire des messages de journal (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fc715-102">How to: Write Log Messages (Visual Basic)</span></span>

<span data-ttu-id="fc715-103">Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur votre application.</span><span class="sxs-lookup"><span data-stu-id="fc715-103">You can use the `My.Application.Log` and `My.Log` objects to log information about your application.</span></span> <span data-ttu-id="fc715-104">Cet exemple montre comment utiliser la méthode `My.Application.Log.WriteEntry` pour enregistrer des informations de traçage.</span><span class="sxs-lookup"><span data-stu-id="fc715-104">This example shows how to use the `My.Application.Log.WriteEntry` method to log tracing information.</span></span>

<span data-ttu-id="fc715-105">Pour journaliser des informations sur les exceptions, utilisez la méthode `My.Application.Log.WriteException`. Voir [Guide pratique pour journaliser des exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="fc715-105">For logging exception information, use the `My.Application.Log.WriteException` method; see [How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md).</span></span>

## <a name="example"></a><span data-ttu-id="fc715-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc715-106">Example</span></span>

<span data-ttu-id="fc715-107">Cet exemple utilise la méthode `My.Application.Log.WriteEntry` pour écrire les informations de traçage.</span><span class="sxs-lookup"><span data-stu-id="fc715-107">This example uses the `My.Application.Log.WriteEntry` method to write out the trace information.</span></span>

[!code-vb[VbVbalrMyApplicationLog#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog/VB/Form1.vb#11)]

## <a name="net-framework-security"></a><span data-ttu-id="fc715-108">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="fc715-108">.NET Framework Security</span></span>

<span data-ttu-id="fc715-109">Vérifiez que les données que vous écrivez dans le journal n’incluent pas d’informations sensibles, comme des mots de passe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fc715-109">Make sure the data you write to the log does not include sensitive information such as user passwords.</span></span> <span data-ttu-id="fc715-110">Pour plus d’informations, consultez [Utilisation des journaux d’application](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md).</span><span class="sxs-lookup"><span data-stu-id="fc715-110">For more information, see [Working with Application Logs](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc715-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc715-111">See also</span></span>

- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [<span data-ttu-id="fc715-112">Utilisation des journaux des applications</span><span class="sxs-lookup"><span data-stu-id="fc715-112">Working with Application Logs</span></span>](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)
- [<span data-ttu-id="fc715-113">Guide pratique pour journaliser des exception</span><span class="sxs-lookup"><span data-stu-id="fc715-113">How to: Log Exceptions</span></span>](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)
- [<span data-ttu-id="fc715-114">Procédure pas à pas : Détermination de l’emplacement des informations My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="fc715-114">Walkthrough: Determining Where My.Application.Log Writes Information</span></span>](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)
- [<span data-ttu-id="fc715-115">Procédure pas à pas : Modification de l’emplacement des informations My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="fc715-115">Walkthrough: Changing Where My.Application.Log Writes Information</span></span>](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)
- [<span data-ttu-id="fc715-116">Procédure pas à pas : Filtrage de la sortie de My.Application.Log</span><span class="sxs-lookup"><span data-stu-id="fc715-116">Walkthrough: Filtering My.Application.Log Output</span></span>](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md)
