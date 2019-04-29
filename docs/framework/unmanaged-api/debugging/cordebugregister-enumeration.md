---
title: CorDebugRegister, énumération
ms.date: 03/30/2017
api_name:
- CorDebugRegister
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugRegister
helpviewer_keywords:
- CorDebugRegister enumeration [.NET Framework debugging]
ms.assetid: 003bb138-7960-4291-ac88-0d87e470ff70
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fab5225225d4e4a4e07961b0f967cff2c1b07321
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61599316"
---
# <a name="cordebugregister-enumeration"></a><span data-ttu-id="93b13-102">CorDebugRegister, énumération</span><span class="sxs-lookup"><span data-stu-id="93b13-102">CorDebugRegister Enumeration</span></span>
<span data-ttu-id="93b13-103">Spécifie les registres associés à une architecture de processeur donnée.</span><span class="sxs-lookup"><span data-stu-id="93b13-103">Specifies the registers associated with a given processor architecture.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93b13-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93b13-104">Syntax</span></span>  
  
```  
typedef enum CorDebugRegister {  
  
    REGISTER_INSTRUCTION_POINTER = 0,  
    REGISTER_STACK_POINTER,  
    REGISTER_FRAME_POINTER,  
  
    REGISTER_X86_EIP = 0,  
    REGISTER_X86_ESP,  
    REGISTER_X86_EBP,  
  
    REGISTER_X86_EAX,  
    REGISTER_X86_ECX,  
    REGISTER_X86_EDX,  
    REGISTER_X86_EBX,  
  
    REGISTER_X86_ESI,  
    REGISTER_X86_EDI,  
  
    REGISTER_X86_FPSTACK_0,  
    REGISTER_X86_FPSTACK_1,  
    REGISTER_X86_FPSTACK_2,  
    REGISTER_X86_FPSTACK_3,  
    REGISTER_X86_FPSTACK_4,  
    REGISTER_X86_FPSTACK_5,  
    REGISTER_X86_FPSTACK_6,  
    REGISTER_X86_FPSTACK_7,  
  
    REGISTER_AMD64_RIP = 0,  
    REGISTER_AMD64_RSP,  
    REGISTER_AMD64_RBP,  
    REGISTER_AMD64_RAX,  
    REGISTER_AMD64_RCX,  
    REGISTER_AMD64_RDX,  
    REGISTER_AMD64_RBX,  
    REGISTER_AMD64_RSI,  
    REGISTER_AMD64_RDI,  
    REGISTER_AMD64_R8,  
    REGISTER_AMD64_R9,  
    REGISTER_AMD64_R10,  
    REGISTER_AMD64_R11,  
    REGISTER_AMD64_R12,  
    REGISTER_AMD64_R13,  
    REGISTER_AMD64_R14,  
    REGISTER_AMD64_R15,  
  
    REGISTER_AMD64_XMM0,  
    REGISTER_AMD64_XMM1,  
    REGISTER_AMD64_XMM2,  
    REGISTER_AMD64_XMM3,  
    REGISTER_AMD64_XMM4,  
    REGISTER_AMD64_XMM5,  
    REGISTER_AMD64_XMM6,  
    REGISTER_AMD64_XMM7,  
    REGISTER_AMD64_XMM8,  
    REGISTER_AMD64_XMM9,  
    REGISTER_AMD64_XMM10,  
    REGISTER_AMD64_XMM11,  
    REGISTER_AMD64_XMM12,  
    REGISTER_AMD64_XMM13,  
    REGISTER_AMD64_XMM14,  
    REGISTER_AMD64_XMM15,  
  
    REGISTER_IA64_BSP = REGISTER_FRAME_POINTER,  
    REGISTER_IA64_R0  = REGISTER_IA64_BSP + 1,  
    REGISTER_IA64_F0  = REGISTER_IA64_R0  + 128,  
    REGISTER_ARM_PC = 0,  
    REGISTER_ARM_SP,  
    REGISTER_ARM_R0,  
    REGISTER_ARM_R1,  
    REGISTER_ARM_R2,  
    REGISTER_ARM_R3,  
    REGISTER_ARM_R4,  
    REGISTER_ARM_R5,  
    REGISTER_ARM_R6,  
    REGISTER_ARM_R7,  
    REGISTER_ARM_R8,  
    REGISTER_ARM_R9,  
    REGISTER_ARM_R10,  
    REGISTER_ARM_R11,  
    REGISTER_ARM_R12,  
    REGISTER_ARM_LR,  
  
} CorDebugRegister;  
```  
  
## <a name="members"></a><span data-ttu-id="93b13-105">Membres</span><span class="sxs-lookup"><span data-stu-id="93b13-105">Members</span></span>  
  
|<span data-ttu-id="93b13-106">Membre</span><span class="sxs-lookup"><span data-stu-id="93b13-106">Member</span></span>|<span data-ttu-id="93b13-107">Description</span><span class="sxs-lookup"><span data-stu-id="93b13-107">Description</span></span>|  
|------------|-----------------|  
|`REGISTER_INSTRUCTION_POINTER`|<span data-ttu-id="93b13-108">Registre de pointeur d'instruction sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="93b13-108">An instruction pointer register on any processor.</span></span>|  
|`REGISTER_STACK_POINTER`|<span data-ttu-id="93b13-109">Registre de pointeur de pile sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="93b13-109">A stack pointer register on any processor.</span></span>|  
|`REGISTER_FRAME_POINTER`|<span data-ttu-id="93b13-110">Registre de pointeur de trame sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="93b13-110">A frame pointer register on any processor.</span></span>|  
|`REGISTER_X86_EIP`|<span data-ttu-id="93b13-111">Registre de pointeur d'instruction sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-111">The instruction pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_ESP`|<span data-ttu-id="93b13-112">Registre de pointeur de pile sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-112">The stack pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_EBP`|<span data-ttu-id="93b13-113">Registre de pointeur de base sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-113">The base pointer register on the x86 processor.</span></span>|  
|`REGISTER_X86_EAX`|<span data-ttu-id="93b13-114">Registre de données A sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-114">The A data register on the x86 processor.</span></span>|  
|`REGISTER_X86_ECX`|<span data-ttu-id="93b13-115">Registre de données C sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-115">The C data register on the x86 processor.</span></span>|  
|`REGISTER_X86_EDX`|<span data-ttu-id="93b13-116">Registre de données D sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-116">The D data register on the x86 processor.</span></span>|  
|`REGISTER_X86_EBX`|<span data-ttu-id="93b13-117">Registre de données B sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-117">The B data register on the x86 processor.</span></span>|  
|`REGISTER_X86_ESI`|<span data-ttu-id="93b13-118">Registre d'index source sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-118">The source index register on the x86 processor.</span></span>|  
|`REGISTER_X86_EDI`|<span data-ttu-id="93b13-119">Registre d'index de destination sur le processeur x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-119">The destination index register on the x86 processor.</span></span>|  
|`REGISTER_X86_FPSTACK_0`|<span data-ttu-id="93b13-120">Registre de pile 0 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-120">The stack register 0 on the x86 floating-point (FP) processor.</span></span>|  
|`REGISTER_X86_FPSTACK_1`|<span data-ttu-id="93b13-121">Registre de pile n° 1 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-121">The #1 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_2`|<span data-ttu-id="93b13-122">Registre de pile n° 2 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-122">The #2 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_3`|<span data-ttu-id="93b13-123">Registre de pile n° 3 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-123">The #3 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_4`|<span data-ttu-id="93b13-124">Registre de pile n° 4 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-124">The #4 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_5`|<span data-ttu-id="93b13-125">Registre de pile n° 5 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-125">The #5 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_6`|<span data-ttu-id="93b13-126">Registre de pile n° 6 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-126">The #6 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_X86_FPSTACK_7`|<span data-ttu-id="93b13-127">Registre de pile n° 7 sur le processeur à virgule flottante x86.</span><span class="sxs-lookup"><span data-stu-id="93b13-127">The #7 stack register on the x86 FP processor.</span></span>|  
|`REGISTER_AMD64_RIP`|<span data-ttu-id="93b13-128">Registre de pointeur d'instruction sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-128">The instruction pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RSP`|<span data-ttu-id="93b13-129">Registre de pointeur de pile sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-129">The stack pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RBP`|<span data-ttu-id="93b13-130">Registre de pointeur de base sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-130">The base pointer register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RAX`|<span data-ttu-id="93b13-131">Registre de données A sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-131">The A data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RCX`|<span data-ttu-id="93b13-132">Registre de données C sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-132">The C data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RDX`|<span data-ttu-id="93b13-133">Registre de données D sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-133">The D data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RBX`|<span data-ttu-id="93b13-134">Registre de données B sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-134">The B data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RSI`|<span data-ttu-id="93b13-135">Registre d'index source sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-135">The source index register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_RDI`|<span data-ttu-id="93b13-136">Registre d'index de destination sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-136">The destination index register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R8`|<span data-ttu-id="93b13-137">Registre de données n° 8 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-137">The #8 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R9`|<span data-ttu-id="93b13-138">Registre de données n° 9 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-138">The #9 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R10`|<span data-ttu-id="93b13-139">Registre de données n° 10 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-139">The #10 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R11`|<span data-ttu-id="93b13-140">Registre de données n° 11 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-140">The #11 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R12`|<span data-ttu-id="93b13-141">Registre de données n° 12 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-141">The #12 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R13`|<span data-ttu-id="93b13-142">Registre de données n° 13 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-142">The #13 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R14`|<span data-ttu-id="93b13-143">Registre de données n° 14 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-143">The #14 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_R15`|<span data-ttu-id="93b13-144">Registre de données n° 15 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-144">The #15 data register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM0`|<span data-ttu-id="93b13-145">Registre multimédia n° 0 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-145">The #0 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM1`|<span data-ttu-id="93b13-146">Registre multimédia n° 1 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-146">The #1 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM2`|<span data-ttu-id="93b13-147">Registre multimédia n° 2 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-147">The #2 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM3`|<span data-ttu-id="93b13-148">Registre multimédia n° 3 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-148">The #3 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM4`|<span data-ttu-id="93b13-149">Registre multimédia n° 4 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-149">The #4 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM5`|<span data-ttu-id="93b13-150">Registre multimédia n° 5 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-150">The #5 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM6`|<span data-ttu-id="93b13-151">Registre multimédia n° 6 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-151">The #6 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM7`|<span data-ttu-id="93b13-152">Registre multimédia n° 7 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-152">The #7 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM8`|<span data-ttu-id="93b13-153">Registre multimédia n° 8 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-153">The #8 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM9`|<span data-ttu-id="93b13-154">Registre multimédia n° 9 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-154">The #9 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM10`|<span data-ttu-id="93b13-155">Registre multimédia n° 10 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-155">The #10 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM11`|<span data-ttu-id="93b13-156">Registre multimédia n° 11 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-156">The #11 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM12`|<span data-ttu-id="93b13-157">Registre multimédia n° 12 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-157">The #12 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM13`|<span data-ttu-id="93b13-158">Registre multimédia n° 13 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-158">The #13 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM14`|<span data-ttu-id="93b13-159">Registre multimédia n° 14 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-159">The #14 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_AMD64_XMM15`|<span data-ttu-id="93b13-160">Registre multimédia n° 15 sur le processeur AMD64.</span><span class="sxs-lookup"><span data-stu-id="93b13-160">The #15 multimedia register on the AMD64 processor.</span></span>|  
|`REGISTER_IA64_BSP`|<span data-ttu-id="93b13-161">Registre de pointeur de pile sur le processeur IA-64.</span><span class="sxs-lookup"><span data-stu-id="93b13-161">The stack pointer register on the IA-64 processor.</span></span>|  
|`REGISTER_IA64_R0`|<span data-ttu-id="93b13-162">Registre de données n° 0 sur le processeur IA-64.</span><span class="sxs-lookup"><span data-stu-id="93b13-162">The #0 data register on the IA-64 processor.</span></span>|  
|`REGISTER_IA64_F0`|<span data-ttu-id="93b13-163">Registre de données en virgule flottante n° 0 sur le processeur IA-64.</span><span class="sxs-lookup"><span data-stu-id="93b13-163">The #0 FP data register on the IA-64 processor.</span></span>|  
|`REGISTER_ARM_PC`|<span data-ttu-id="93b13-164">Registre de compteur de programme (R15) sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-164">The program counter register (R15) on the ARM processor.</span></span>|  
|`REGISTER_ARM_SP`|<span data-ttu-id="93b13-165">Registre de pointeur de pile (R13) sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-165">The stack pointer register (R13) on the ARM processor.</span></span>|  
|`REGISTER_ARM_R0`|<span data-ttu-id="93b13-166">Registre de données R0 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-166">Data register R0 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R1`|<span data-ttu-id="93b13-167">Registre de données R1 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-167">Data register R1 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R2`|<span data-ttu-id="93b13-168">Registre de données R2 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-168">Data register R2 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R3`|<span data-ttu-id="93b13-169">Registre de données R3 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-169">Data register R3 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R4`|<span data-ttu-id="93b13-170">Registre R4 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-170">Register R4 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R5`|<span data-ttu-id="93b13-171">Registre R5 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-171">Register R5 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R6`|<span data-ttu-id="93b13-172">Registre R6 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-172">Register R6 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R7`|<span data-ttu-id="93b13-173">Registre R7 (le pointeur de trame THUMB) sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-173">Register R7 (the THUMB frame pointer) on the ARM processor.</span></span>|  
|`REGISTER_ARM_R8`|<span data-ttu-id="93b13-174">Registre R8 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-174">Register R8 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R9`|<span data-ttu-id="93b13-175">Registre R9 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-175">Register R9 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R10`|<span data-ttu-id="93b13-176">Registre R10 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-176">Register R10 on the ARM processor.</span></span>|  
|`REGISTER_ARM_R11`|<span data-ttu-id="93b13-177">Pointeur de trame sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-177">The frame pointer on the ARM processor.</span></span>|  
|`REGISTER_ARM_R12`|<span data-ttu-id="93b13-178">Registre R12 sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-178">Register R12 on the ARM processor.</span></span>|  
|`REGISTER_ARM_LR`|<span data-ttu-id="93b13-179">Registre de lien (R14) sur le processeur ARM.</span><span class="sxs-lookup"><span data-stu-id="93b13-179">The link register (R14) on the ARM processor.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="93b13-180">Notes</span><span class="sxs-lookup"><span data-stu-id="93b13-180">Remarks</span></span>  
 <span data-ttu-id="93b13-181">Il existe 128 registres de données d'utilisation générale et 128 registres de données en virgule flottante sur le processeur IA-64, mais seules les valeurs `REGISTER_IA64_R0` et `REGISTER_IA64_F0` sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="93b13-181">There are 128 general-purpose data registers and 128 floating-point data registers on the IA-64 processor, but only values `REGISTER_IA64_R0` and `REGISTER_IA64_F0` are provided.</span></span> <span data-ttu-id="93b13-182">Les autres valeurs peuvent être déterminées comme suit :</span><span class="sxs-lookup"><span data-stu-id="93b13-182">The other values can be determined as follows:</span></span>  
  
- <span data-ttu-id="93b13-183">Ajoutez le numéro de registre à `REGISTER_IA64_R0` pour les valeurs allant de `REGISTER_IA64_R1` à `REGISTER_IA64_R127`, qui correspondent aux registres de données n° 1 à 127 sur le processeur IA-64.</span><span class="sxs-lookup"><span data-stu-id="93b13-183">Add the register number to `REGISTER_IA64_R0` for values `REGISTER_IA64_R1` through `REGISTER_IA64_R127`, which correspond to the #1 data register through the #127 data register on the IA-64 processor.</span></span>  
  
- <span data-ttu-id="93b13-184">Ajoutez le numéro de registre à `REGISTER_IA64_F0` pour les valeurs allant de `REGISTER_IA64_F1` à `REGISTER_IA64_F127`, qui correspondent aux registres de données en virgule flottante n° 1 à 127 sur le processeur IA-64.</span><span class="sxs-lookup"><span data-stu-id="93b13-184">Add the register number to `REGISTER_IA64_F0` for values `REGISTER_IA64_F1` through `REGISTER_IA64_F127`, which correspond to the #1 FP data register through the #127 FP data register on the IA-64 processor.</span></span>  
  
 <span data-ttu-id="93b13-185">Par exemple, si vous devez spécifier le registre de données n° 83 sur le processeur IA-64, utilisez `REGISTER_IA64_R0` + 83.</span><span class="sxs-lookup"><span data-stu-id="93b13-185">For example, if you need to specify the #83 data register on the IA-64 processor, use `REGISTER_IA64_R0` + 83.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93b13-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93b13-186">Requirements</span></span>  
 <span data-ttu-id="93b13-187">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="93b13-187">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93b13-188">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="93b13-188">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="93b13-189">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93b13-189">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93b13-190">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93b13-190">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93b13-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93b13-191">See also</span></span>

- [<span data-ttu-id="93b13-192">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="93b13-192">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
