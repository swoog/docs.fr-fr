---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 1ab6426875b73b400a59b7e4cf155615d7472d05
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514487"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="93a16-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="93a16-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="93a16-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="93a16-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="93a16-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="93a16-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="93a16-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="93a16-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="93a16-106">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-106">Tables</span></span>  
  
-   <span data-ttu-id="93a16-107">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-107">Columns</span></span>  
  
-   <span data-ttu-id="93a16-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-108">Procedures</span></span>  
  
-   <span data-ttu-id="93a16-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="93a16-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="93a16-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="93a16-110">Catalog</span></span>  
  
-   <span data-ttu-id="93a16-111">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="93a16-112">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-112">Tables</span></span>  
  
|<span data-ttu-id="93a16-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-113">ColumnName</span></span>|<span data-ttu-id="93a16-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-115">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-116">String</span></span>|  
|<span data-ttu-id="93a16-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-118">String</span></span>|  
|<span data-ttu-id="93a16-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-119">TABLE_NAME</span></span>|<span data-ttu-id="93a16-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-120">String</span></span>|  
|<span data-ttu-id="93a16-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-121">TABLE_TYPE</span></span>|<span data-ttu-id="93a16-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-122">String</span></span>|  
|<span data-ttu-id="93a16-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-123">TABLE_GUID</span></span>|<span data-ttu-id="93a16-124">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-124">Guid</span></span>|  
|<span data-ttu-id="93a16-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-125">DESCRIPTION</span></span>|<span data-ttu-id="93a16-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-126">String</span></span>|  
|<span data-ttu-id="93a16-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-127">TABLE_PROPID</span></span>|<span data-ttu-id="93a16-128">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-128">Int64</span></span>|  
|<span data-ttu-id="93a16-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-129">DATE_CREATED</span></span>|<span data-ttu-id="93a16-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-130">DateTime</span></span>|  
|<span data-ttu-id="93a16-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-131">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="93a16-133">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-133">Columns</span></span>  
  
|<span data-ttu-id="93a16-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-134">ColumnName</span></span>|<span data-ttu-id="93a16-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-136">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-137">String</span></span>|  
|<span data-ttu-id="93a16-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-139">String</span></span>|  
|<span data-ttu-id="93a16-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-140">TABLE_NAME</span></span>|<span data-ttu-id="93a16-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-141">String</span></span>|  
|<span data-ttu-id="93a16-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-142">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-143">String</span></span>|  
|<span data-ttu-id="93a16-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-144">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-145">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-145">Guid</span></span>|  
|<span data-ttu-id="93a16-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-146">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-147">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-147">Int64</span></span>|  
|<span data-ttu-id="93a16-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-149">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-149">Int64</span></span>|  
|<span data-ttu-id="93a16-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="93a16-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-151">Boolean</span></span>|  
|<span data-ttu-id="93a16-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="93a16-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-153">String</span></span>|  
|<span data-ttu-id="93a16-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="93a16-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="93a16-155">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-155">Int64</span></span>|  
|<span data-ttu-id="93a16-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-156">IS_NULLABLE</span></span>|<span data-ttu-id="93a16-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-157">Boolean</span></span>|  
|<span data-ttu-id="93a16-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-158">DATA_TYPE</span></span>|<span data-ttu-id="93a16-159">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-159">Int32</span></span>|  
|<span data-ttu-id="93a16-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-160">TYPE_GUID</span></span>|<span data-ttu-id="93a16-161">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-161">Guid</span></span>|  
|<span data-ttu-id="93a16-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="93a16-163">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-163">Int64</span></span>|  
|<span data-ttu-id="93a16-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="93a16-165">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-165">Int64</span></span>|  
|<span data-ttu-id="93a16-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="93a16-167">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-167">Int32</span></span>|  
|<span data-ttu-id="93a16-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="93a16-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="93a16-169">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-169">Int16</span></span>|  
|<span data-ttu-id="93a16-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="93a16-171">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-171">Int64</span></span>|  
|<span data-ttu-id="93a16-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="93a16-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-173">String</span></span>|  
|<span data-ttu-id="93a16-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="93a16-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-175">String</span></span>|  
|<span data-ttu-id="93a16-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="93a16-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-177">String</span></span>|  
|<span data-ttu-id="93a16-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="93a16-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-179">String</span></span>|  
|<span data-ttu-id="93a16-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="93a16-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-181">String</span></span>|  
|<span data-ttu-id="93a16-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-182">COLLATION_NAME</span></span>|<span data-ttu-id="93a16-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-183">String</span></span>|  
|<span data-ttu-id="93a16-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="93a16-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-185">String</span></span>|  
|<span data-ttu-id="93a16-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="93a16-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-187">String</span></span>|  
|<span data-ttu-id="93a16-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-188">DOMAIN_NAME</span></span>|<span data-ttu-id="93a16-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-189">String</span></span>|  
|<span data-ttu-id="93a16-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-190">DESCRIPTION</span></span>|<span data-ttu-id="93a16-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-191">String</span></span>|  
|<span data-ttu-id="93a16-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="93a16-192">COLUMN_LCID</span></span>|<span data-ttu-id="93a16-193">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-193">Int32</span></span>|  
|<span data-ttu-id="93a16-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="93a16-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="93a16-195">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-195">Int32</span></span>|  
|<span data-ttu-id="93a16-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="93a16-196">COLUMN_SORTID</span></span>|<span data-ttu-id="93a16-197">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-197">Int32</span></span>|  
|<span data-ttu-id="93a16-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="93a16-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="93a16-199">Byte[]</span></span>|  
|<span data-ttu-id="93a16-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="93a16-200">IS_COMPUTED</span></span>|<span data-ttu-id="93a16-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="93a16-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-202">Procedures</span></span>  
  
|<span data-ttu-id="93a16-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-203">ColumnName</span></span>|<span data-ttu-id="93a16-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="93a16-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-206">String</span></span>|  
|<span data-ttu-id="93a16-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="93a16-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-208">String</span></span>|  
|<span data-ttu-id="93a16-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="93a16-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-210">String</span></span>|  
|<span data-ttu-id="93a16-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="93a16-212">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-212">Int16</span></span>|  
|<span data-ttu-id="93a16-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="93a16-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="93a16-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-214">String</span></span>|  
|<span data-ttu-id="93a16-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-215">DESCRIPTION</span></span>|<span data-ttu-id="93a16-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-216">String</span></span>|  
|<span data-ttu-id="93a16-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-217">DATE_CREATED</span></span>|<span data-ttu-id="93a16-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-218">DateTime</span></span>|  
|<span data-ttu-id="93a16-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-219">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="93a16-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="93a16-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="93a16-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-222">ColumnName</span></span>|<span data-ttu-id="93a16-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="93a16-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-225">String</span></span>|  
|<span data-ttu-id="93a16-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="93a16-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-227">String</span></span>|  
|<span data-ttu-id="93a16-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="93a16-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-229">String</span></span>|  
|<span data-ttu-id="93a16-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-230">PARAMETER_NAME</span></span>|<span data-ttu-id="93a16-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-231">String</span></span>|  
|<span data-ttu-id="93a16-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-233">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-233">Int32</span></span>|  
|<span data-ttu-id="93a16-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="93a16-235">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-235">Int32</span></span>|  
|<span data-ttu-id="93a16-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="93a16-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-237">Boolean</span></span>|  
|<span data-ttu-id="93a16-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="93a16-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-239">String</span></span>|  
|<span data-ttu-id="93a16-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-240">IS_NULLABLE</span></span>|<span data-ttu-id="93a16-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-241">Boolean</span></span>|  
|<span data-ttu-id="93a16-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-242">DATA_TYPE</span></span>|<span data-ttu-id="93a16-243">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-243">Int32</span></span>|  
|<span data-ttu-id="93a16-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="93a16-245">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-245">Int64</span></span>|  
|<span data-ttu-id="93a16-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="93a16-247">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-247">Int64</span></span>|  
|<span data-ttu-id="93a16-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="93a16-249">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-249">Int32</span></span>|  
|<span data-ttu-id="93a16-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="93a16-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="93a16-251">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-251">Int16</span></span>|  
|<span data-ttu-id="93a16-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-252">DESCRIPTION</span></span>|<span data-ttu-id="93a16-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-253">String</span></span>|  
|<span data-ttu-id="93a16-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-254">TYPE_NAME</span></span>|<span data-ttu-id="93a16-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-255">String</span></span>|  
|<span data-ttu-id="93a16-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="93a16-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="93a16-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="93a16-258">Catalog</span></span>  
  
|<span data-ttu-id="93a16-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-259">ColumnName</span></span>|<span data-ttu-id="93a16-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-261">CATALOG_NAME</span></span>|<span data-ttu-id="93a16-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-262">String</span></span>|  
|<span data-ttu-id="93a16-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-263">DESCRIPTION</span></span>|<span data-ttu-id="93a16-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="93a16-265">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-265">Indexes</span></span>  
  
|<span data-ttu-id="93a16-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-266">ColumnName</span></span>|<span data-ttu-id="93a16-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-268">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-269">String</span></span>|  
|<span data-ttu-id="93a16-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-271">String</span></span>|  
|<span data-ttu-id="93a16-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-272">TABLE_NAME</span></span>|<span data-ttu-id="93a16-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-273">String</span></span>|  
|<span data-ttu-id="93a16-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-274">INDEX_CATALOG</span></span>|<span data-ttu-id="93a16-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-275">String</span></span>|  
|<span data-ttu-id="93a16-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="93a16-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-277">String</span></span>|  
|<span data-ttu-id="93a16-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-278">INDEX_NAME</span></span>|<span data-ttu-id="93a16-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-279">String</span></span>|  
|<span data-ttu-id="93a16-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="93a16-280">PRIMARY_KEY</span></span>|<span data-ttu-id="93a16-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-281">Boolean</span></span>|  
|<span data-ttu-id="93a16-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="93a16-282">UNIQUE</span></span>|<span data-ttu-id="93a16-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-283">Boolean</span></span>|  
|<span data-ttu-id="93a16-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="93a16-284">CLUSTERED</span></span>|<span data-ttu-id="93a16-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-285">Boolean</span></span>|  
|<span data-ttu-id="93a16-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-286">TYPE</span></span>|<span data-ttu-id="93a16-287">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-287">Int32</span></span>|  
|<span data-ttu-id="93a16-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="93a16-288">FILL_FACTOR</span></span>|<span data-ttu-id="93a16-289">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-289">Int32</span></span>|  
|<span data-ttu-id="93a16-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="93a16-290">INITIAL_SIZE</span></span>|<span data-ttu-id="93a16-291">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-291">Int32</span></span>|  
|<span data-ttu-id="93a16-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="93a16-292">NULLS</span></span>|<span data-ttu-id="93a16-293">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-293">Int32</span></span>|  
|<span data-ttu-id="93a16-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="93a16-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="93a16-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-295">Boolean</span></span>|  
|<span data-ttu-id="93a16-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="93a16-296">AUTO_UPDATE</span></span>|<span data-ttu-id="93a16-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-297">Boolean</span></span>|  
|<span data-ttu-id="93a16-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-298">NULL_COLLATION</span></span>|<span data-ttu-id="93a16-299">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-299">Int32</span></span>|  
|<span data-ttu-id="93a16-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-301">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-301">Int64</span></span>|  
|<span data-ttu-id="93a16-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-302">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-303">String</span></span>|  
|<span data-ttu-id="93a16-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-304">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-305">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-305">Guid</span></span>|  
|<span data-ttu-id="93a16-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-306">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-307">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-307">Int64</span></span>|  
|<span data-ttu-id="93a16-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-308">COLLATION</span></span>|<span data-ttu-id="93a16-309">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-309">Int16</span></span>|  
|<span data-ttu-id="93a16-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="93a16-310">CARDINALITY</span></span>|<span data-ttu-id="93a16-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="93a16-311">Decimal</span></span>|  
|<span data-ttu-id="93a16-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="93a16-312">PAGES</span></span>|<span data-ttu-id="93a16-313">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-313">Int32</span></span>|  
|<span data-ttu-id="93a16-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="93a16-314">FILTER_CONDITION</span></span>|<span data-ttu-id="93a16-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-315">String</span></span>|  
|<span data-ttu-id="93a16-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="93a16-316">INTEGRATED</span></span>|<span data-ttu-id="93a16-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="93a16-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="93a16-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="93a16-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="93a16-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="93a16-320">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-320">Tables</span></span>  
  
-   <span data-ttu-id="93a16-321">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-321">Columns</span></span>  
  
-   <span data-ttu-id="93a16-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-322">Procedures</span></span>  
  
-   <span data-ttu-id="93a16-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="93a16-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="93a16-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="93a16-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="93a16-325">Vues</span><span class="sxs-lookup"><span data-stu-id="93a16-325">Views</span></span>  
  
-   <span data-ttu-id="93a16-326">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="93a16-327">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-327">Tables</span></span>  
  
|<span data-ttu-id="93a16-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-328">ColumnName</span></span>|<span data-ttu-id="93a16-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-330">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-331">String</span></span>|  
|<span data-ttu-id="93a16-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-333">String</span></span>|  
|<span data-ttu-id="93a16-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-334">TABLE_NAME</span></span>|<span data-ttu-id="93a16-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-335">String</span></span>|  
|<span data-ttu-id="93a16-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-336">TABLE_TYPE</span></span>|<span data-ttu-id="93a16-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-337">String</span></span>|  
|<span data-ttu-id="93a16-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-338">TABLE_GUID</span></span>|<span data-ttu-id="93a16-339">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-339">Guid</span></span>|  
|<span data-ttu-id="93a16-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-340">DESCRIPTION</span></span>|<span data-ttu-id="93a16-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-341">String</span></span>|  
|<span data-ttu-id="93a16-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-342">TABLE_PROPID</span></span>|<span data-ttu-id="93a16-343">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-343">Int64</span></span>|  
|<span data-ttu-id="93a16-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-344">DATE_CREATED</span></span>|<span data-ttu-id="93a16-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-345">DateTime</span></span>|  
|<span data-ttu-id="93a16-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-346">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="93a16-348">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-348">Columns</span></span>  
  
|<span data-ttu-id="93a16-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-349">ColumnName</span></span>|<span data-ttu-id="93a16-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-351">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-352">String</span></span>|  
|<span data-ttu-id="93a16-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-354">String</span></span>|  
|<span data-ttu-id="93a16-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-355">TABLE_NAME</span></span>|<span data-ttu-id="93a16-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-356">String</span></span>|  
|<span data-ttu-id="93a16-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-357">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-358">String</span></span>|  
|<span data-ttu-id="93a16-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-359">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-360">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-360">Guid</span></span>|  
|<span data-ttu-id="93a16-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-361">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-362">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-362">Int64</span></span>|  
|<span data-ttu-id="93a16-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-364">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-364">Int64</span></span>|  
|<span data-ttu-id="93a16-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="93a16-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-366">Boolean</span></span>|  
|<span data-ttu-id="93a16-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="93a16-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-368">String</span></span>|  
|<span data-ttu-id="93a16-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="93a16-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="93a16-370">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-370">Int64</span></span>|  
|<span data-ttu-id="93a16-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-371">IS_NULLABLE</span></span>|<span data-ttu-id="93a16-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-372">Boolean</span></span>|  
|<span data-ttu-id="93a16-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-373">DATA_TYPE</span></span>|<span data-ttu-id="93a16-374">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-374">Int32</span></span>|  
|<span data-ttu-id="93a16-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-375">TYPE_GUID</span></span>|<span data-ttu-id="93a16-376">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-376">Guid</span></span>|  
|<span data-ttu-id="93a16-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="93a16-378">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-378">Int64</span></span>|  
|<span data-ttu-id="93a16-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="93a16-380">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-380">Int64</span></span>|  
|<span data-ttu-id="93a16-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="93a16-382">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-382">Int32</span></span>|  
|<span data-ttu-id="93a16-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="93a16-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="93a16-384">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-384">Int16</span></span>|  
|<span data-ttu-id="93a16-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="93a16-386">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-386">Int64</span></span>|  
|<span data-ttu-id="93a16-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="93a16-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-388">String</span></span>|  
|<span data-ttu-id="93a16-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="93a16-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-390">String</span></span>|  
|<span data-ttu-id="93a16-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="93a16-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-392">String</span></span>|  
|<span data-ttu-id="93a16-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="93a16-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-394">String</span></span>|  
|<span data-ttu-id="93a16-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="93a16-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-396">String</span></span>|  
|<span data-ttu-id="93a16-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-397">COLLATION_NAME</span></span>|<span data-ttu-id="93a16-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-398">String</span></span>|  
|<span data-ttu-id="93a16-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="93a16-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-400">String</span></span>|  
|<span data-ttu-id="93a16-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="93a16-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-402">String</span></span>|  
|<span data-ttu-id="93a16-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-403">DOMAIN_NAME</span></span>|<span data-ttu-id="93a16-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-404">String</span></span>|  
|<span data-ttu-id="93a16-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-405">DESCRIPTION</span></span>|<span data-ttu-id="93a16-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="93a16-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-407">Procedures</span></span>  
  
|<span data-ttu-id="93a16-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-408">ColumnName</span></span>|<span data-ttu-id="93a16-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="93a16-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-411">String</span></span>|  
|<span data-ttu-id="93a16-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="93a16-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-413">String</span></span>|  
|<span data-ttu-id="93a16-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="93a16-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-415">String</span></span>|  
|<span data-ttu-id="93a16-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="93a16-417">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-417">Int16</span></span>|  
|<span data-ttu-id="93a16-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="93a16-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="93a16-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-419">String</span></span>|  
|<span data-ttu-id="93a16-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-420">DESCRIPTION</span></span>|<span data-ttu-id="93a16-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-421">String</span></span>|  
|<span data-ttu-id="93a16-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-422">DATE_CREATED</span></span>|<span data-ttu-id="93a16-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-423">DateTime</span></span>|  
|<span data-ttu-id="93a16-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-424">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="93a16-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="93a16-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="93a16-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-427">ColumnName</span></span>|<span data-ttu-id="93a16-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="93a16-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-430">String</span></span>|  
|<span data-ttu-id="93a16-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="93a16-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-432">String</span></span>|  
|<span data-ttu-id="93a16-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="93a16-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-434">String</span></span>|  
|<span data-ttu-id="93a16-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-435">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-436">String</span></span>|  
|<span data-ttu-id="93a16-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-437">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-438">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-438">Guid</span></span>|  
|<span data-ttu-id="93a16-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-439">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-440">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-440">Int64</span></span>|  
|<span data-ttu-id="93a16-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="93a16-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="93a16-442">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-442">Int64</span></span>|  
|<span data-ttu-id="93a16-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-444">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-444">Int64</span></span>|  
|<span data-ttu-id="93a16-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-445">IS_NULLABLE</span></span>|<span data-ttu-id="93a16-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-446">Boolean</span></span>|  
|<span data-ttu-id="93a16-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-447">DATA_TYPE</span></span>|<span data-ttu-id="93a16-448">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-448">Int32</span></span>|  
|<span data-ttu-id="93a16-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-449">TYPE_GUID</span></span>|<span data-ttu-id="93a16-450">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-450">Guid</span></span>|  
|<span data-ttu-id="93a16-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="93a16-452">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-452">Int64</span></span>|  
|<span data-ttu-id="93a16-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="93a16-454">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-454">Int64</span></span>|  
|<span data-ttu-id="93a16-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="93a16-456">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-456">Int32</span></span>|  
|<span data-ttu-id="93a16-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="93a16-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="93a16-458">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-458">Int16</span></span>|  
|<span data-ttu-id="93a16-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-459">DESCRIPTION</span></span>|<span data-ttu-id="93a16-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-460">String</span></span>|  
|<span data-ttu-id="93a16-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="93a16-461">OVERLOAD</span></span>|<span data-ttu-id="93a16-462">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="93a16-463">Vues</span><span class="sxs-lookup"><span data-stu-id="93a16-463">Views</span></span>  
  
|<span data-ttu-id="93a16-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-464">ColumnName</span></span>|<span data-ttu-id="93a16-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-466">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-467">String</span></span>|  
|<span data-ttu-id="93a16-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-469">String</span></span>|  
|<span data-ttu-id="93a16-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-470">TABLE_NAME</span></span>|<span data-ttu-id="93a16-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-471">String</span></span>|  
|<span data-ttu-id="93a16-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="93a16-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="93a16-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-473">String</span></span>|  
|<span data-ttu-id="93a16-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-474">CHECK_OPTION</span></span>|<span data-ttu-id="93a16-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-475">Boolean</span></span>|  
|<span data-ttu-id="93a16-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-476">IS_UPDATABLE</span></span>|<span data-ttu-id="93a16-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-477">Boolean</span></span>|  
|<span data-ttu-id="93a16-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-478">DESCRIPTION</span></span>|<span data-ttu-id="93a16-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-479">String</span></span>|  
|<span data-ttu-id="93a16-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-480">DATE_CREATED</span></span>|<span data-ttu-id="93a16-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-481">DateTime</span></span>|  
|<span data-ttu-id="93a16-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-482">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="93a16-484">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-484">Indexes</span></span>  
  
|<span data-ttu-id="93a16-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-485">ColumnName</span></span>|<span data-ttu-id="93a16-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-487">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-488">String</span></span>|  
|<span data-ttu-id="93a16-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-490">String</span></span>|  
|<span data-ttu-id="93a16-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-491">TABLE_NAME</span></span>|<span data-ttu-id="93a16-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-492">String</span></span>|  
|<span data-ttu-id="93a16-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-493">INDEX_CATALOG</span></span>|<span data-ttu-id="93a16-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-494">String</span></span>|  
|<span data-ttu-id="93a16-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="93a16-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-496">String</span></span>|  
|<span data-ttu-id="93a16-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-497">INDEX_NAME</span></span>|<span data-ttu-id="93a16-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-498">String</span></span>|  
|<span data-ttu-id="93a16-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="93a16-499">PRIMARY_KEY</span></span>|<span data-ttu-id="93a16-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-500">Boolean</span></span>|  
|<span data-ttu-id="93a16-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="93a16-501">UNIQUE</span></span>|<span data-ttu-id="93a16-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-502">Boolean</span></span>|  
|<span data-ttu-id="93a16-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="93a16-503">CLUSTERED</span></span>|<span data-ttu-id="93a16-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-504">Boolean</span></span>|  
|<span data-ttu-id="93a16-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-505">TYPE</span></span>|<span data-ttu-id="93a16-506">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-506">Int32</span></span>|  
|<span data-ttu-id="93a16-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="93a16-507">FILL_FACTOR</span></span>|<span data-ttu-id="93a16-508">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-508">Int32</span></span>|  
|<span data-ttu-id="93a16-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="93a16-509">INITIAL_SIZE</span></span>|<span data-ttu-id="93a16-510">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-510">Int32</span></span>|  
|<span data-ttu-id="93a16-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="93a16-511">NULLS</span></span>|<span data-ttu-id="93a16-512">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-512">Int32</span></span>|  
|<span data-ttu-id="93a16-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="93a16-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="93a16-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-514">Boolean</span></span>|  
|<span data-ttu-id="93a16-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="93a16-515">AUTO_UPDATE</span></span>|<span data-ttu-id="93a16-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-516">Boolean</span></span>|  
|<span data-ttu-id="93a16-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-517">NULL_COLLATION</span></span>|<span data-ttu-id="93a16-518">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-518">Int32</span></span>|  
|<span data-ttu-id="93a16-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-520">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-520">Int64</span></span>|  
|<span data-ttu-id="93a16-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-521">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-522">String</span></span>|  
|<span data-ttu-id="93a16-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-523">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-524">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-524">Guid</span></span>|  
|<span data-ttu-id="93a16-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-525">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-526">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-526">Int64</span></span>|  
|<span data-ttu-id="93a16-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-527">COLLATION</span></span>|<span data-ttu-id="93a16-528">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-528">Int16</span></span>|  
|<span data-ttu-id="93a16-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="93a16-529">CARDINALITY</span></span>|<span data-ttu-id="93a16-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="93a16-530">Decimal</span></span>|  
|<span data-ttu-id="93a16-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="93a16-531">PAGES</span></span>|<span data-ttu-id="93a16-532">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-532">Int32</span></span>|  
|<span data-ttu-id="93a16-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="93a16-533">FILTER_CONDITION</span></span>|<span data-ttu-id="93a16-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-534">String</span></span>|  
|<span data-ttu-id="93a16-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="93a16-535">INTEGRATED</span></span>|<span data-ttu-id="93a16-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="93a16-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="93a16-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="93a16-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="93a16-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="93a16-539">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-539">Tables</span></span>  
  
-   <span data-ttu-id="93a16-540">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-540">Columns</span></span>  
  
-   <span data-ttu-id="93a16-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-541">Procedures</span></span>  
  
-   <span data-ttu-id="93a16-542">Vues</span><span class="sxs-lookup"><span data-stu-id="93a16-542">Views</span></span>  
  
-   <span data-ttu-id="93a16-543">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="93a16-544">Tables</span><span class="sxs-lookup"><span data-stu-id="93a16-544">Tables</span></span>  
  
|<span data-ttu-id="93a16-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-545">ColumnName</span></span>|<span data-ttu-id="93a16-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-547">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-548">String</span></span>|  
|<span data-ttu-id="93a16-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-550">String</span></span>|  
|<span data-ttu-id="93a16-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-551">TABLE_NAME</span></span>|<span data-ttu-id="93a16-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-552">String</span></span>|  
|<span data-ttu-id="93a16-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-553">TABLE_TYPE</span></span>|<span data-ttu-id="93a16-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-554">String</span></span>|  
|<span data-ttu-id="93a16-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-555">TABLE_GUID</span></span>|<span data-ttu-id="93a16-556">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-556">Guid</span></span>|  
|<span data-ttu-id="93a16-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-557">DESCRIPTION</span></span>|<span data-ttu-id="93a16-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-558">String</span></span>|  
|<span data-ttu-id="93a16-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-559">TABLE_PROPID</span></span>|<span data-ttu-id="93a16-560">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-560">Int64</span></span>|  
|<span data-ttu-id="93a16-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-561">DATE_CREATED</span></span>|<span data-ttu-id="93a16-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-562">DateTime</span></span>|  
|<span data-ttu-id="93a16-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-563">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="93a16-565">Columns</span><span class="sxs-lookup"><span data-stu-id="93a16-565">Columns</span></span>  
  
|<span data-ttu-id="93a16-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-566">ColumnName</span></span>|<span data-ttu-id="93a16-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-568">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-569">String</span></span>|  
|<span data-ttu-id="93a16-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-571">String</span></span>|  
|<span data-ttu-id="93a16-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-572">TABLE_NAME</span></span>|<span data-ttu-id="93a16-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-573">String</span></span>|  
|<span data-ttu-id="93a16-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-574">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-575">String</span></span>|  
|<span data-ttu-id="93a16-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-576">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-577">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-577">Guid</span></span>|  
|<span data-ttu-id="93a16-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-578">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-579">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-579">Int64</span></span>|  
|<span data-ttu-id="93a16-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-581">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-581">Int64</span></span>|  
|<span data-ttu-id="93a16-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="93a16-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-583">Boolean</span></span>|  
|<span data-ttu-id="93a16-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="93a16-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="93a16-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-585">String</span></span>|  
|<span data-ttu-id="93a16-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="93a16-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="93a16-587">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-587">Int64</span></span>|  
|<span data-ttu-id="93a16-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-588">IS_NULLABLE</span></span>|<span data-ttu-id="93a16-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-589">Boolean</span></span>|  
|<span data-ttu-id="93a16-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-590">DATA_TYPE</span></span>|<span data-ttu-id="93a16-591">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-591">Int32</span></span>|  
|<span data-ttu-id="93a16-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-592">TYPE_GUID</span></span>|<span data-ttu-id="93a16-593">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-593">Guid</span></span>|  
|<span data-ttu-id="93a16-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="93a16-595">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-595">Int64</span></span>|  
|<span data-ttu-id="93a16-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="93a16-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="93a16-597">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-597">Int64</span></span>|  
|<span data-ttu-id="93a16-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="93a16-599">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-599">Int32</span></span>|  
|<span data-ttu-id="93a16-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="93a16-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="93a16-601">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-601">Int16</span></span>|  
|<span data-ttu-id="93a16-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="93a16-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="93a16-603">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-603">Int64</span></span>|  
|<span data-ttu-id="93a16-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="93a16-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-605">String</span></span>|  
|<span data-ttu-id="93a16-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="93a16-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-607">String</span></span>|  
|<span data-ttu-id="93a16-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="93a16-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-609">String</span></span>|  
|<span data-ttu-id="93a16-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="93a16-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-611">String</span></span>|  
|<span data-ttu-id="93a16-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="93a16-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-613">String</span></span>|  
|<span data-ttu-id="93a16-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-614">COLLATION_NAME</span></span>|<span data-ttu-id="93a16-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-615">String</span></span>|  
|<span data-ttu-id="93a16-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="93a16-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-617">String</span></span>|  
|<span data-ttu-id="93a16-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="93a16-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-619">String</span></span>|  
|<span data-ttu-id="93a16-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-620">DOMAIN_NAME</span></span>|<span data-ttu-id="93a16-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-621">String</span></span>|  
|<span data-ttu-id="93a16-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-622">DESCRIPTION</span></span>|<span data-ttu-id="93a16-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="93a16-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="93a16-624">Procedures</span></span>  
  
|<span data-ttu-id="93a16-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-625">ColumnName</span></span>|<span data-ttu-id="93a16-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="93a16-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-628">String</span></span>|  
|<span data-ttu-id="93a16-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="93a16-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-630">String</span></span>|  
|<span data-ttu-id="93a16-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="93a16-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-632">String</span></span>|  
|<span data-ttu-id="93a16-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="93a16-634">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-634">Int16</span></span>|  
|<span data-ttu-id="93a16-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="93a16-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="93a16-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-636">String</span></span>|  
|<span data-ttu-id="93a16-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-637">DESCRIPTION</span></span>|<span data-ttu-id="93a16-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-638">String</span></span>|  
|<span data-ttu-id="93a16-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-639">DATE_CREATED</span></span>|<span data-ttu-id="93a16-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-640">DateTime</span></span>|  
|<span data-ttu-id="93a16-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-641">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="93a16-643">Vues</span><span class="sxs-lookup"><span data-stu-id="93a16-643">Views</span></span>  
  
|<span data-ttu-id="93a16-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-644">ColumnName</span></span>|<span data-ttu-id="93a16-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-646">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-647">String</span></span>|  
|<span data-ttu-id="93a16-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-649">String</span></span>|  
|<span data-ttu-id="93a16-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-650">TABLE_NAME</span></span>|<span data-ttu-id="93a16-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-651">String</span></span>|  
|<span data-ttu-id="93a16-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="93a16-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="93a16-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-653">String</span></span>|  
|<span data-ttu-id="93a16-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-654">CHECK_OPTION</span></span>|<span data-ttu-id="93a16-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-655">Boolean</span></span>|  
|<span data-ttu-id="93a16-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="93a16-656">IS_UPDATABLE</span></span>|<span data-ttu-id="93a16-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-657">Boolean</span></span>|  
|<span data-ttu-id="93a16-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93a16-658">DESCRIPTION</span></span>|<span data-ttu-id="93a16-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-659">String</span></span>|  
|<span data-ttu-id="93a16-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="93a16-660">DATE_CREATED</span></span>|<span data-ttu-id="93a16-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-661">DateTime</span></span>|  
|<span data-ttu-id="93a16-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="93a16-662">DATE_MODIFIED</span></span>|<span data-ttu-id="93a16-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="93a16-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="93a16-664">Index</span><span class="sxs-lookup"><span data-stu-id="93a16-664">Indexes</span></span>  
  
|<span data-ttu-id="93a16-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="93a16-665">ColumnName</span></span>|<span data-ttu-id="93a16-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="93a16-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="93a16-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-667">TABLE_CATALOG</span></span>|<span data-ttu-id="93a16-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-668">String</span></span>|  
|<span data-ttu-id="93a16-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="93a16-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-670">String</span></span>|  
|<span data-ttu-id="93a16-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-671">TABLE_NAME</span></span>|<span data-ttu-id="93a16-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-672">String</span></span>|  
|<span data-ttu-id="93a16-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="93a16-673">INDEX_CATALOG</span></span>|<span data-ttu-id="93a16-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-674">String</span></span>|  
|<span data-ttu-id="93a16-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="93a16-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="93a16-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-676">String</span></span>|  
|<span data-ttu-id="93a16-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-677">INDEX_NAME</span></span>|<span data-ttu-id="93a16-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-678">String</span></span>|  
|<span data-ttu-id="93a16-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="93a16-679">PRIMARY_KEY</span></span>|<span data-ttu-id="93a16-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-680">Boolean</span></span>|  
|<span data-ttu-id="93a16-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="93a16-681">UNIQUE</span></span>|<span data-ttu-id="93a16-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-682">Boolean</span></span>|  
|<span data-ttu-id="93a16-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="93a16-683">CLUSTERED</span></span>|<span data-ttu-id="93a16-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-684">Boolean</span></span>|  
|<span data-ttu-id="93a16-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="93a16-685">TYPE</span></span>|<span data-ttu-id="93a16-686">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-686">Int32</span></span>|  
|<span data-ttu-id="93a16-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="93a16-687">FILL_FACTOR</span></span>|<span data-ttu-id="93a16-688">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-688">Int32</span></span>|  
|<span data-ttu-id="93a16-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="93a16-689">INITIAL_SIZE</span></span>|<span data-ttu-id="93a16-690">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-690">Int32</span></span>|  
|<span data-ttu-id="93a16-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="93a16-691">NULLS</span></span>|<span data-ttu-id="93a16-692">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-692">Int32</span></span>|  
|<span data-ttu-id="93a16-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="93a16-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="93a16-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-694">Boolean</span></span>|  
|<span data-ttu-id="93a16-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="93a16-695">AUTO_UPDATE</span></span>|<span data-ttu-id="93a16-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="93a16-696">Boolean</span></span>|  
|<span data-ttu-id="93a16-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-697">NULL_COLLATION</span></span>|<span data-ttu-id="93a16-698">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-698">Int32</span></span>|  
|<span data-ttu-id="93a16-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="93a16-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="93a16-700">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-700">Int64</span></span>|  
|<span data-ttu-id="93a16-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="93a16-701">COLUMN_NAME</span></span>|<span data-ttu-id="93a16-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-702">String</span></span>|  
|<span data-ttu-id="93a16-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="93a16-703">COLUMN_GUID</span></span>|<span data-ttu-id="93a16-704">Guid</span><span class="sxs-lookup"><span data-stu-id="93a16-704">Guid</span></span>|  
|<span data-ttu-id="93a16-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="93a16-705">COLUMN_PROPID</span></span>|<span data-ttu-id="93a16-706">Int64</span><span class="sxs-lookup"><span data-stu-id="93a16-706">Int64</span></span>|  
|<span data-ttu-id="93a16-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="93a16-707">COLLATION</span></span>|<span data-ttu-id="93a16-708">Int16</span><span class="sxs-lookup"><span data-stu-id="93a16-708">Int16</span></span>|  
|<span data-ttu-id="93a16-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="93a16-709">CARDINALITY</span></span>|<span data-ttu-id="93a16-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="93a16-710">Decimal</span></span>|  
|<span data-ttu-id="93a16-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="93a16-711">PAGES</span></span>|<span data-ttu-id="93a16-712">Int32</span><span class="sxs-lookup"><span data-stu-id="93a16-712">Int32</span></span>|  
|<span data-ttu-id="93a16-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="93a16-713">FILTER_CONDITION</span></span>|<span data-ttu-id="93a16-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="93a16-714">String</span></span>|  
|<span data-ttu-id="93a16-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="93a16-715">INTEGRATED</span></span>|<span data-ttu-id="93a16-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="93a16-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="93a16-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93a16-717">See Also</span></span>  
 [<span data-ttu-id="93a16-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="93a16-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
