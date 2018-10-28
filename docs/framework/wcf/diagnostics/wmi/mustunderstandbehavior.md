---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 0f3efc446104a1afff507f6e7d2cd8c01c4ed417
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452597"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="02694-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="02694-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="02694-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="02694-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02694-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02694-104">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="02694-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02694-105">Methods</span></span>  
 <span data-ttu-id="02694-106">La classe MustUnderstandBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="02694-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="02694-107">Properties</span><span class="sxs-lookup"><span data-stu-id="02694-107">Properties</span></span>  
 <span data-ttu-id="02694-108">La classe MustUnderstandBehavior a la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="02694-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="02694-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="02694-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="02694-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="02694-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="02694-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="02694-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="02694-112">Lorsque cette propriété a la valeur `true`, tous les en-têtes SOAP avec l'attribut `MustUnderstand` qui ne sont pas gérés font en sorte que le comportement lève une exception.</span><span class="sxs-lookup"><span data-stu-id="02694-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02694-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02694-113">Requirements</span></span>  
  
|<span data-ttu-id="02694-114">MOF</span><span class="sxs-lookup"><span data-stu-id="02694-114">MOF</span></span>|<span data-ttu-id="02694-115">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="02694-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="02694-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02694-116">Namespace</span></span>|<span data-ttu-id="02694-117">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="02694-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="02694-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02694-118">See Also</span></span>  
 <xref:System.ServiceModel.Description.MustUnderstandBehavior>
