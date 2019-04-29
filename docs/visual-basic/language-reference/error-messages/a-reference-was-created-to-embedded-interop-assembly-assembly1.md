---
title: Une référence a été créée pour l'assembly d'interopérabilité incorporé '<assembly1>' en raison d'une référence indirecte à cet assembly à partir de l'assembly '<assembly2>'
ms.date: 07/20/2015
f1_keywords:
- vbc40059
- bc40059
helpviewer_keywords:
- VBC40059
- BC40059
ms.assetid: 520e39cb-8ab6-46f5-aa00-08afd51b4b7c
ms.openlocfilehash: c0b4f56e3d1613486dd1198976557831ce657e1b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774859"
---
# <a name="a-reference-was-created-to-embedded-interop-assembly-assembly1-because-of-an-indirect-reference-to-that-assembly-from-assembly-assembly2"></a><span data-ttu-id="e307d-102">Une référence a été créée pour l’assembly d’interopérabilité incorporé '\<assembly1 >' en raison d’une référence indirecte à cet assembly à partir de l’assembly '\<assembly2 >'</span><span class="sxs-lookup"><span data-stu-id="e307d-102">A reference was created to embedded interop assembly '\<assembly1>' because of an indirect reference to that assembly from assembly '\<assembly2>'</span></span>
<span data-ttu-id="e307d-103">Une référence a été créée pour l’assembly d’interopérabilité incorporé '\<assembly1>' en raison d’une référence indirecte à cet assembly à partir de l’assembly '\<assembly2>'.</span><span class="sxs-lookup"><span data-stu-id="e307d-103">A reference was created to embedded interop assembly '\<assembly1>' because of an indirect reference to that assembly from assembly '\<assembly2>'.</span></span> <span data-ttu-id="e307d-104">Modifiez la propriété 'Incorporer les types interop' pour l’un des assemblys.</span><span class="sxs-lookup"><span data-stu-id="e307d-104">Consider changing the 'Embed Interop Types' property on either assembly.</span></span>  
  
 <span data-ttu-id="e307d-105">Vous avez ajouté une référence à un assembly (assembly1) avec une valeur de propriété `Embed Interop Types` égale à `True`.</span><span class="sxs-lookup"><span data-stu-id="e307d-105">You have added a reference to an assembly (assembly1) that has the `Embed Interop Types` property set to `True`.</span></span> <span data-ttu-id="e307d-106">Cela indique au compilateur d’incorporer les informations de type interop à partir de cet assembly.</span><span class="sxs-lookup"><span data-stu-id="e307d-106">This instructs the compiler to embed interop type information from that assembly.</span></span> <span data-ttu-id="e307d-107">Toutefois, le compilateur ne peut pas incorporer les informations de type interop à partir de cet assembly, car un autre assembly que vous avez référencé (assembly2) fait également référence à cet assembly (assembly1) et a la propriété `Embed Interop Types` définie sur `False`.</span><span class="sxs-lookup"><span data-stu-id="e307d-107">However, the compiler cannot embed interop type information from that assembly because another assembly that you have referenced (assembly2) also references that assembly (assembly1) and has the `Embed Interop Types` property set to `False`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e307d-108">L’affectation de la valeur `True` à la propriété `Embed Interop Types` d’une référence d’assembly revient à référencer l’assembly en utilisant l’option `/link` pour le compilateur de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e307d-108">Setting the `Embed Interop Types` property on an assembly reference to `True` is equivalent to referencing the assembly by using the `/link` option for the command-line compiler.</span></span>  
  
 <span data-ttu-id="e307d-109">**ID d’erreur :** BC40059</span><span class="sxs-lookup"><span data-stu-id="e307d-109">**Error ID:** BC40059</span></span>  
  
### <a name="to-address-this-warning"></a><span data-ttu-id="e307d-110">Pour traiter cet avertissement</span><span class="sxs-lookup"><span data-stu-id="e307d-110">To address this warning</span></span>  
  
- <span data-ttu-id="e307d-111">Pour incorporer des informations de type interop pour les deux assemblys, affectez la valeur `True` à la propriété `Embed Interop Types` de toutes les références à assembly1.</span><span class="sxs-lookup"><span data-stu-id="e307d-111">To embed interop type information for both assemblies, set the `Embed Interop Types` property on all references to assembly1 to `True`.</span></span>  
  
- <span data-ttu-id="e307d-112">Pour supprimer cet avertissement, vous pouvez affecter à la propriété `Embed Interop Types` d’assembly1 la valeur `False`.</span><span class="sxs-lookup"><span data-stu-id="e307d-112">To remove the warning, you can set the `Embed Interop Types` property of assembly1 to `False`.</span></span> <span data-ttu-id="e307d-113">Dans ce cas, les informations de type interop sont fournies par un assembly d’interopérabilité primaire (PIA).</span><span class="sxs-lookup"><span data-stu-id="e307d-113">In this case, interop type information is provided by a primary interop assembly (PIA).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e307d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e307d-114">See also</span></span>

- [<span data-ttu-id="e307d-115">/link (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e307d-115">/link (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/link.md)
- [<span data-ttu-id="e307d-116">Interopération avec du code non managé</span><span class="sxs-lookup"><span data-stu-id="e307d-116">Interoperating with Unmanaged Code</span></span>](../../../framework/interop/index.md)
