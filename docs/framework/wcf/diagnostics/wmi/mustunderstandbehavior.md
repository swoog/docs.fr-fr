---
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 14150a992130e9ed4734c950d4ed92f1bbd3206c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485555"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="00ae1-102">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="00ae1-102">MustUnderstandBehavior</span></span>
<span data-ttu-id="00ae1-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="00ae1-103">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00ae1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00ae1-104">Syntax</span></span>  
  
```  
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="00ae1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00ae1-105">Methods</span></span>  
 <span data-ttu-id="00ae1-106">La classe MustUnderstandBehavior ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="00ae1-106">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="00ae1-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00ae1-107">Properties</span></span>  
 <span data-ttu-id="00ae1-108">La classe MustUnderstandBehavior a la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="00ae1-108">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="00ae1-109">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="00ae1-109">ValidateMustUnderstand</span></span>  
 <span data-ttu-id="00ae1-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="00ae1-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="00ae1-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="00ae1-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="00ae1-112">Lorsque cette propriété a la valeur `true`, tous les en-têtes SOAP avec l'attribut `MustUnderstand` qui ne sont pas gérés font en sorte que le comportement lève une exception.</span><span class="sxs-lookup"><span data-stu-id="00ae1-112">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00ae1-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="00ae1-113">Requirements</span></span>  
  
|<span data-ttu-id="00ae1-114">MOF</span><span class="sxs-lookup"><span data-stu-id="00ae1-114">MOF</span></span>|<span data-ttu-id="00ae1-115">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="00ae1-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="00ae1-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00ae1-116">Namespace</span></span>|<span data-ttu-id="00ae1-117">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="00ae1-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="00ae1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ae1-118">See Also</span></span>  
 <xref:System.ServiceModel.Description.MustUnderstandBehavior>
