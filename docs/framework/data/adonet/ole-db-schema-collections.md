---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: f753f35aab0a0200da5de463a73abb9813253d11
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658453"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="13313-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="13313-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="13313-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="13313-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="13313-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="13313-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="13313-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="13313-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="13313-106">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-106">Tables</span></span>  
  
-   <span data-ttu-id="13313-107">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-107">Columns</span></span>  
  
-   <span data-ttu-id="13313-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-108">Procedures</span></span>  
  
-   <span data-ttu-id="13313-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="13313-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="13313-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="13313-110">Catalog</span></span>  
  
-   <span data-ttu-id="13313-111">Index</span><span class="sxs-lookup"><span data-stu-id="13313-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="13313-112">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-112">Tables</span></span>  
  
|<span data-ttu-id="13313-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-113">ColumnName</span></span>|<span data-ttu-id="13313-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-115">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-116">String</span></span>|  
|<span data-ttu-id="13313-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-118">String</span></span>|  
|<span data-ttu-id="13313-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-119">TABLE_NAME</span></span>|<span data-ttu-id="13313-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-120">String</span></span>|  
|<span data-ttu-id="13313-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-121">TABLE_TYPE</span></span>|<span data-ttu-id="13313-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-122">String</span></span>|  
|<span data-ttu-id="13313-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-123">TABLE_GUID</span></span>|<span data-ttu-id="13313-124">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-124">Guid</span></span>|  
|<span data-ttu-id="13313-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-125">DESCRIPTION</span></span>|<span data-ttu-id="13313-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-126">String</span></span>|  
|<span data-ttu-id="13313-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-127">TABLE_PROPID</span></span>|<span data-ttu-id="13313-128">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-128">Int64</span></span>|  
|<span data-ttu-id="13313-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-129">DATE_CREATED</span></span>|<span data-ttu-id="13313-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-130">DateTime</span></span>|  
|<span data-ttu-id="13313-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-131">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="13313-133">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-133">Columns</span></span>  
  
|<span data-ttu-id="13313-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-134">ColumnName</span></span>|<span data-ttu-id="13313-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-136">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-137">String</span></span>|  
|<span data-ttu-id="13313-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-139">String</span></span>|  
|<span data-ttu-id="13313-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-140">TABLE_NAME</span></span>|<span data-ttu-id="13313-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-141">String</span></span>|  
|<span data-ttu-id="13313-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-142">COLUMN_NAME</span></span>|<span data-ttu-id="13313-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-143">String</span></span>|  
|<span data-ttu-id="13313-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-144">COLUMN_GUID</span></span>|<span data-ttu-id="13313-145">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-145">Guid</span></span>|  
|<span data-ttu-id="13313-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-146">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-147">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-147">Int64</span></span>|  
|<span data-ttu-id="13313-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-149">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-149">Int64</span></span>|  
|<span data-ttu-id="13313-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="13313-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-151">Boolean</span></span>|  
|<span data-ttu-id="13313-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="13313-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-153">String</span></span>|  
|<span data-ttu-id="13313-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="13313-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="13313-155">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-155">Int64</span></span>|  
|<span data-ttu-id="13313-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="13313-156">IS_NULLABLE</span></span>|<span data-ttu-id="13313-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-157">Boolean</span></span>|  
|<span data-ttu-id="13313-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-158">DATA_TYPE</span></span>|<span data-ttu-id="13313-159">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-159">Int32</span></span>|  
|<span data-ttu-id="13313-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-160">TYPE_GUID</span></span>|<span data-ttu-id="13313-161">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-161">Guid</span></span>|  
|<span data-ttu-id="13313-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="13313-163">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-163">Int64</span></span>|  
|<span data-ttu-id="13313-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="13313-165">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-165">Int64</span></span>|  
|<span data-ttu-id="13313-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="13313-167">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-167">Int32</span></span>|  
|<span data-ttu-id="13313-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="13313-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="13313-169">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-169">Int16</span></span>|  
|<span data-ttu-id="13313-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="13313-171">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-171">Int64</span></span>|  
|<span data-ttu-id="13313-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="13313-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-173">String</span></span>|  
|<span data-ttu-id="13313-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="13313-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-175">String</span></span>|  
|<span data-ttu-id="13313-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="13313-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-177">String</span></span>|  
|<span data-ttu-id="13313-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="13313-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-179">String</span></span>|  
|<span data-ttu-id="13313-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="13313-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-181">String</span></span>|  
|<span data-ttu-id="13313-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-182">COLLATION_NAME</span></span>|<span data-ttu-id="13313-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-183">String</span></span>|  
|<span data-ttu-id="13313-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="13313-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-185">String</span></span>|  
|<span data-ttu-id="13313-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="13313-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-187">String</span></span>|  
|<span data-ttu-id="13313-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-188">DOMAIN_NAME</span></span>|<span data-ttu-id="13313-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-189">String</span></span>|  
|<span data-ttu-id="13313-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-190">DESCRIPTION</span></span>|<span data-ttu-id="13313-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-191">String</span></span>|  
|<span data-ttu-id="13313-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="13313-192">COLUMN_LCID</span></span>|<span data-ttu-id="13313-193">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-193">Int32</span></span>|  
|<span data-ttu-id="13313-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="13313-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="13313-195">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-195">Int32</span></span>|  
|<span data-ttu-id="13313-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="13313-196">COLUMN_SORTID</span></span>|<span data-ttu-id="13313-197">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-197">Int32</span></span>|  
|<span data-ttu-id="13313-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="13313-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="13313-199">Byte[]</span></span>|  
|<span data-ttu-id="13313-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="13313-200">IS_COMPUTED</span></span>|<span data-ttu-id="13313-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="13313-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-202">Procedures</span></span>  
  
|<span data-ttu-id="13313-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-203">ColumnName</span></span>|<span data-ttu-id="13313-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="13313-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-206">String</span></span>|  
|<span data-ttu-id="13313-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="13313-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-208">String</span></span>|  
|<span data-ttu-id="13313-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="13313-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-210">String</span></span>|  
|<span data-ttu-id="13313-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="13313-212">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-212">Int16</span></span>|  
|<span data-ttu-id="13313-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="13313-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="13313-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-214">String</span></span>|  
|<span data-ttu-id="13313-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-215">DESCRIPTION</span></span>|<span data-ttu-id="13313-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-216">String</span></span>|  
|<span data-ttu-id="13313-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-217">DATE_CREATED</span></span>|<span data-ttu-id="13313-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-218">DateTime</span></span>|  
|<span data-ttu-id="13313-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-219">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="13313-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="13313-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="13313-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-222">ColumnName</span></span>|<span data-ttu-id="13313-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="13313-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-225">String</span></span>|  
|<span data-ttu-id="13313-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="13313-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-227">String</span></span>|  
|<span data-ttu-id="13313-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="13313-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-229">String</span></span>|  
|<span data-ttu-id="13313-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-230">PARAMETER_NAME</span></span>|<span data-ttu-id="13313-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-231">String</span></span>|  
|<span data-ttu-id="13313-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-233">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-233">Int32</span></span>|  
|<span data-ttu-id="13313-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="13313-235">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-235">Int32</span></span>|  
|<span data-ttu-id="13313-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="13313-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-237">Boolean</span></span>|  
|<span data-ttu-id="13313-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="13313-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-239">String</span></span>|  
|<span data-ttu-id="13313-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="13313-240">IS_NULLABLE</span></span>|<span data-ttu-id="13313-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-241">Boolean</span></span>|  
|<span data-ttu-id="13313-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-242">DATA_TYPE</span></span>|<span data-ttu-id="13313-243">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-243">Int32</span></span>|  
|<span data-ttu-id="13313-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="13313-245">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-245">Int64</span></span>|  
|<span data-ttu-id="13313-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="13313-247">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-247">Int64</span></span>|  
|<span data-ttu-id="13313-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="13313-249">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-249">Int32</span></span>|  
|<span data-ttu-id="13313-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="13313-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="13313-251">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-251">Int16</span></span>|  
|<span data-ttu-id="13313-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-252">DESCRIPTION</span></span>|<span data-ttu-id="13313-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-253">String</span></span>|  
|<span data-ttu-id="13313-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-254">TYPE_NAME</span></span>|<span data-ttu-id="13313-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-255">String</span></span>|  
|<span data-ttu-id="13313-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="13313-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="13313-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="13313-258">Catalog</span></span>  
  
|<span data-ttu-id="13313-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-259">ColumnName</span></span>|<span data-ttu-id="13313-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-261">CATALOG_NAME</span></span>|<span data-ttu-id="13313-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-262">String</span></span>|  
|<span data-ttu-id="13313-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-263">DESCRIPTION</span></span>|<span data-ttu-id="13313-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="13313-265">Index</span><span class="sxs-lookup"><span data-stu-id="13313-265">Indexes</span></span>  
  
|<span data-ttu-id="13313-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-266">ColumnName</span></span>|<span data-ttu-id="13313-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-268">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-269">String</span></span>|  
|<span data-ttu-id="13313-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-271">String</span></span>|  
|<span data-ttu-id="13313-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-272">TABLE_NAME</span></span>|<span data-ttu-id="13313-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-273">String</span></span>|  
|<span data-ttu-id="13313-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-274">INDEX_CATALOG</span></span>|<span data-ttu-id="13313-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-275">String</span></span>|  
|<span data-ttu-id="13313-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="13313-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-277">String</span></span>|  
|<span data-ttu-id="13313-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-278">INDEX_NAME</span></span>|<span data-ttu-id="13313-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-279">String</span></span>|  
|<span data-ttu-id="13313-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="13313-280">PRIMARY_KEY</span></span>|<span data-ttu-id="13313-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-281">Boolean</span></span>|  
|<span data-ttu-id="13313-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="13313-282">UNIQUE</span></span>|<span data-ttu-id="13313-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-283">Boolean</span></span>|  
|<span data-ttu-id="13313-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="13313-284">CLUSTERED</span></span>|<span data-ttu-id="13313-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-285">Boolean</span></span>|  
|<span data-ttu-id="13313-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-286">TYPE</span></span>|<span data-ttu-id="13313-287">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-287">Int32</span></span>|  
|<span data-ttu-id="13313-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="13313-288">FILL_FACTOR</span></span>|<span data-ttu-id="13313-289">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-289">Int32</span></span>|  
|<span data-ttu-id="13313-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="13313-290">INITIAL_SIZE</span></span>|<span data-ttu-id="13313-291">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-291">Int32</span></span>|  
|<span data-ttu-id="13313-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="13313-292">NULLS</span></span>|<span data-ttu-id="13313-293">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-293">Int32</span></span>|  
|<span data-ttu-id="13313-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="13313-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="13313-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-295">Boolean</span></span>|  
|<span data-ttu-id="13313-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="13313-296">AUTO_UPDATE</span></span>|<span data-ttu-id="13313-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-297">Boolean</span></span>|  
|<span data-ttu-id="13313-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-298">NULL_COLLATION</span></span>|<span data-ttu-id="13313-299">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-299">Int32</span></span>|  
|<span data-ttu-id="13313-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-301">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-301">Int64</span></span>|  
|<span data-ttu-id="13313-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-302">COLUMN_NAME</span></span>|<span data-ttu-id="13313-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-303">String</span></span>|  
|<span data-ttu-id="13313-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-304">COLUMN_GUID</span></span>|<span data-ttu-id="13313-305">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-305">Guid</span></span>|  
|<span data-ttu-id="13313-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-306">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-307">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-307">Int64</span></span>|  
|<span data-ttu-id="13313-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-308">COLLATION</span></span>|<span data-ttu-id="13313-309">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-309">Int16</span></span>|  
|<span data-ttu-id="13313-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="13313-310">CARDINALITY</span></span>|<span data-ttu-id="13313-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="13313-311">Decimal</span></span>|  
|<span data-ttu-id="13313-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="13313-312">PAGES</span></span>|<span data-ttu-id="13313-313">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-313">Int32</span></span>|  
|<span data-ttu-id="13313-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="13313-314">FILTER_CONDITION</span></span>|<span data-ttu-id="13313-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-315">String</span></span>|  
|<span data-ttu-id="13313-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="13313-316">INTEGRATED</span></span>|<span data-ttu-id="13313-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="13313-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="13313-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="13313-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="13313-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="13313-320">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-320">Tables</span></span>  
  
-   <span data-ttu-id="13313-321">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-321">Columns</span></span>  
  
-   <span data-ttu-id="13313-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-322">Procedures</span></span>  
  
-   <span data-ttu-id="13313-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="13313-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="13313-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="13313-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="13313-325">Vues</span><span class="sxs-lookup"><span data-stu-id="13313-325">Views</span></span>  
  
-   <span data-ttu-id="13313-326">Index</span><span class="sxs-lookup"><span data-stu-id="13313-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="13313-327">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-327">Tables</span></span>  
  
|<span data-ttu-id="13313-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-328">ColumnName</span></span>|<span data-ttu-id="13313-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-330">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-331">String</span></span>|  
|<span data-ttu-id="13313-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-333">String</span></span>|  
|<span data-ttu-id="13313-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-334">TABLE_NAME</span></span>|<span data-ttu-id="13313-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-335">String</span></span>|  
|<span data-ttu-id="13313-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-336">TABLE_TYPE</span></span>|<span data-ttu-id="13313-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-337">String</span></span>|  
|<span data-ttu-id="13313-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-338">TABLE_GUID</span></span>|<span data-ttu-id="13313-339">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-339">Guid</span></span>|  
|<span data-ttu-id="13313-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-340">DESCRIPTION</span></span>|<span data-ttu-id="13313-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-341">String</span></span>|  
|<span data-ttu-id="13313-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-342">TABLE_PROPID</span></span>|<span data-ttu-id="13313-343">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-343">Int64</span></span>|  
|<span data-ttu-id="13313-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-344">DATE_CREATED</span></span>|<span data-ttu-id="13313-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-345">DateTime</span></span>|  
|<span data-ttu-id="13313-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-346">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="13313-348">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-348">Columns</span></span>  
  
|<span data-ttu-id="13313-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-349">ColumnName</span></span>|<span data-ttu-id="13313-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-351">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-352">String</span></span>|  
|<span data-ttu-id="13313-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-354">String</span></span>|  
|<span data-ttu-id="13313-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-355">TABLE_NAME</span></span>|<span data-ttu-id="13313-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-356">String</span></span>|  
|<span data-ttu-id="13313-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-357">COLUMN_NAME</span></span>|<span data-ttu-id="13313-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-358">String</span></span>|  
|<span data-ttu-id="13313-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-359">COLUMN_GUID</span></span>|<span data-ttu-id="13313-360">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-360">Guid</span></span>|  
|<span data-ttu-id="13313-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-361">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-362">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-362">Int64</span></span>|  
|<span data-ttu-id="13313-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-364">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-364">Int64</span></span>|  
|<span data-ttu-id="13313-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="13313-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-366">Boolean</span></span>|  
|<span data-ttu-id="13313-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="13313-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-368">String</span></span>|  
|<span data-ttu-id="13313-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="13313-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="13313-370">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-370">Int64</span></span>|  
|<span data-ttu-id="13313-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="13313-371">IS_NULLABLE</span></span>|<span data-ttu-id="13313-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-372">Boolean</span></span>|  
|<span data-ttu-id="13313-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-373">DATA_TYPE</span></span>|<span data-ttu-id="13313-374">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-374">Int32</span></span>|  
|<span data-ttu-id="13313-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-375">TYPE_GUID</span></span>|<span data-ttu-id="13313-376">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-376">Guid</span></span>|  
|<span data-ttu-id="13313-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="13313-378">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-378">Int64</span></span>|  
|<span data-ttu-id="13313-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="13313-380">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-380">Int64</span></span>|  
|<span data-ttu-id="13313-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="13313-382">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-382">Int32</span></span>|  
|<span data-ttu-id="13313-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="13313-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="13313-384">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-384">Int16</span></span>|  
|<span data-ttu-id="13313-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="13313-386">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-386">Int64</span></span>|  
|<span data-ttu-id="13313-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="13313-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-388">String</span></span>|  
|<span data-ttu-id="13313-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="13313-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-390">String</span></span>|  
|<span data-ttu-id="13313-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="13313-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-392">String</span></span>|  
|<span data-ttu-id="13313-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="13313-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-394">String</span></span>|  
|<span data-ttu-id="13313-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="13313-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-396">String</span></span>|  
|<span data-ttu-id="13313-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-397">COLLATION_NAME</span></span>|<span data-ttu-id="13313-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-398">String</span></span>|  
|<span data-ttu-id="13313-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="13313-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-400">String</span></span>|  
|<span data-ttu-id="13313-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="13313-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-402">String</span></span>|  
|<span data-ttu-id="13313-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-403">DOMAIN_NAME</span></span>|<span data-ttu-id="13313-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-404">String</span></span>|  
|<span data-ttu-id="13313-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-405">DESCRIPTION</span></span>|<span data-ttu-id="13313-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="13313-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-407">Procedures</span></span>  
  
|<span data-ttu-id="13313-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-408">ColumnName</span></span>|<span data-ttu-id="13313-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="13313-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-411">String</span></span>|  
|<span data-ttu-id="13313-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="13313-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-413">String</span></span>|  
|<span data-ttu-id="13313-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="13313-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-415">String</span></span>|  
|<span data-ttu-id="13313-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="13313-417">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-417">Int16</span></span>|  
|<span data-ttu-id="13313-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="13313-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="13313-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-419">String</span></span>|  
|<span data-ttu-id="13313-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-420">DESCRIPTION</span></span>|<span data-ttu-id="13313-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-421">String</span></span>|  
|<span data-ttu-id="13313-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-422">DATE_CREATED</span></span>|<span data-ttu-id="13313-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-423">DateTime</span></span>|  
|<span data-ttu-id="13313-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-424">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="13313-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="13313-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="13313-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-427">ColumnName</span></span>|<span data-ttu-id="13313-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="13313-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-430">String</span></span>|  
|<span data-ttu-id="13313-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="13313-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-432">String</span></span>|  
|<span data-ttu-id="13313-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="13313-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-434">String</span></span>|  
|<span data-ttu-id="13313-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-435">COLUMN_NAME</span></span>|<span data-ttu-id="13313-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-436">String</span></span>|  
|<span data-ttu-id="13313-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-437">COLUMN_GUID</span></span>|<span data-ttu-id="13313-438">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-438">Guid</span></span>|  
|<span data-ttu-id="13313-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-439">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-440">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-440">Int64</span></span>|  
|<span data-ttu-id="13313-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="13313-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="13313-442">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-442">Int64</span></span>|  
|<span data-ttu-id="13313-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-444">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-444">Int64</span></span>|  
|<span data-ttu-id="13313-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="13313-445">IS_NULLABLE</span></span>|<span data-ttu-id="13313-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-446">Boolean</span></span>|  
|<span data-ttu-id="13313-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-447">DATA_TYPE</span></span>|<span data-ttu-id="13313-448">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-448">Int32</span></span>|  
|<span data-ttu-id="13313-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-449">TYPE_GUID</span></span>|<span data-ttu-id="13313-450">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-450">Guid</span></span>|  
|<span data-ttu-id="13313-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="13313-452">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-452">Int64</span></span>|  
|<span data-ttu-id="13313-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="13313-454">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-454">Int64</span></span>|  
|<span data-ttu-id="13313-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="13313-456">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-456">Int32</span></span>|  
|<span data-ttu-id="13313-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="13313-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="13313-458">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-458">Int16</span></span>|  
|<span data-ttu-id="13313-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-459">DESCRIPTION</span></span>|<span data-ttu-id="13313-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-460">String</span></span>|  
|<span data-ttu-id="13313-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="13313-461">OVERLOAD</span></span>|<span data-ttu-id="13313-462">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="13313-463">Vues</span><span class="sxs-lookup"><span data-stu-id="13313-463">Views</span></span>  
  
|<span data-ttu-id="13313-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-464">ColumnName</span></span>|<span data-ttu-id="13313-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-466">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-467">String</span></span>|  
|<span data-ttu-id="13313-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-469">String</span></span>|  
|<span data-ttu-id="13313-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-470">TABLE_NAME</span></span>|<span data-ttu-id="13313-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-471">String</span></span>|  
|<span data-ttu-id="13313-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="13313-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="13313-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-473">String</span></span>|  
|<span data-ttu-id="13313-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="13313-474">CHECK_OPTION</span></span>|<span data-ttu-id="13313-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-475">Boolean</span></span>|  
|<span data-ttu-id="13313-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="13313-476">IS_UPDATABLE</span></span>|<span data-ttu-id="13313-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-477">Boolean</span></span>|  
|<span data-ttu-id="13313-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-478">DESCRIPTION</span></span>|<span data-ttu-id="13313-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-479">String</span></span>|  
|<span data-ttu-id="13313-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-480">DATE_CREATED</span></span>|<span data-ttu-id="13313-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-481">DateTime</span></span>|  
|<span data-ttu-id="13313-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-482">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="13313-484">Index</span><span class="sxs-lookup"><span data-stu-id="13313-484">Indexes</span></span>  
  
|<span data-ttu-id="13313-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-485">ColumnName</span></span>|<span data-ttu-id="13313-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-487">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-488">String</span></span>|  
|<span data-ttu-id="13313-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-490">String</span></span>|  
|<span data-ttu-id="13313-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-491">TABLE_NAME</span></span>|<span data-ttu-id="13313-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-492">String</span></span>|  
|<span data-ttu-id="13313-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-493">INDEX_CATALOG</span></span>|<span data-ttu-id="13313-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-494">String</span></span>|  
|<span data-ttu-id="13313-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="13313-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-496">String</span></span>|  
|<span data-ttu-id="13313-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-497">INDEX_NAME</span></span>|<span data-ttu-id="13313-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-498">String</span></span>|  
|<span data-ttu-id="13313-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="13313-499">PRIMARY_KEY</span></span>|<span data-ttu-id="13313-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-500">Boolean</span></span>|  
|<span data-ttu-id="13313-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="13313-501">UNIQUE</span></span>|<span data-ttu-id="13313-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-502">Boolean</span></span>|  
|<span data-ttu-id="13313-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="13313-503">CLUSTERED</span></span>|<span data-ttu-id="13313-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-504">Boolean</span></span>|  
|<span data-ttu-id="13313-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-505">TYPE</span></span>|<span data-ttu-id="13313-506">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-506">Int32</span></span>|  
|<span data-ttu-id="13313-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="13313-507">FILL_FACTOR</span></span>|<span data-ttu-id="13313-508">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-508">Int32</span></span>|  
|<span data-ttu-id="13313-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="13313-509">INITIAL_SIZE</span></span>|<span data-ttu-id="13313-510">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-510">Int32</span></span>|  
|<span data-ttu-id="13313-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="13313-511">NULLS</span></span>|<span data-ttu-id="13313-512">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-512">Int32</span></span>|  
|<span data-ttu-id="13313-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="13313-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="13313-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-514">Boolean</span></span>|  
|<span data-ttu-id="13313-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="13313-515">AUTO_UPDATE</span></span>|<span data-ttu-id="13313-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-516">Boolean</span></span>|  
|<span data-ttu-id="13313-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-517">NULL_COLLATION</span></span>|<span data-ttu-id="13313-518">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-518">Int32</span></span>|  
|<span data-ttu-id="13313-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-520">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-520">Int64</span></span>|  
|<span data-ttu-id="13313-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-521">COLUMN_NAME</span></span>|<span data-ttu-id="13313-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-522">String</span></span>|  
|<span data-ttu-id="13313-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-523">COLUMN_GUID</span></span>|<span data-ttu-id="13313-524">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-524">Guid</span></span>|  
|<span data-ttu-id="13313-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-525">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-526">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-526">Int64</span></span>|  
|<span data-ttu-id="13313-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-527">COLLATION</span></span>|<span data-ttu-id="13313-528">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-528">Int16</span></span>|  
|<span data-ttu-id="13313-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="13313-529">CARDINALITY</span></span>|<span data-ttu-id="13313-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="13313-530">Decimal</span></span>|  
|<span data-ttu-id="13313-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="13313-531">PAGES</span></span>|<span data-ttu-id="13313-532">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-532">Int32</span></span>|  
|<span data-ttu-id="13313-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="13313-533">FILTER_CONDITION</span></span>|<span data-ttu-id="13313-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-534">String</span></span>|  
|<span data-ttu-id="13313-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="13313-535">INTEGRATED</span></span>|<span data-ttu-id="13313-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="13313-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="13313-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="13313-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="13313-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="13313-539">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-539">Tables</span></span>  
  
-   <span data-ttu-id="13313-540">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-540">Columns</span></span>  
  
-   <span data-ttu-id="13313-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-541">Procedures</span></span>  
  
-   <span data-ttu-id="13313-542">Vues</span><span class="sxs-lookup"><span data-stu-id="13313-542">Views</span></span>  
  
-   <span data-ttu-id="13313-543">Index</span><span class="sxs-lookup"><span data-stu-id="13313-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="13313-544">Tables</span><span class="sxs-lookup"><span data-stu-id="13313-544">Tables</span></span>  
  
|<span data-ttu-id="13313-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-545">ColumnName</span></span>|<span data-ttu-id="13313-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-547">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-548">String</span></span>|  
|<span data-ttu-id="13313-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-550">String</span></span>|  
|<span data-ttu-id="13313-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-551">TABLE_NAME</span></span>|<span data-ttu-id="13313-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-552">String</span></span>|  
|<span data-ttu-id="13313-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-553">TABLE_TYPE</span></span>|<span data-ttu-id="13313-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-554">String</span></span>|  
|<span data-ttu-id="13313-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-555">TABLE_GUID</span></span>|<span data-ttu-id="13313-556">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-556">Guid</span></span>|  
|<span data-ttu-id="13313-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-557">DESCRIPTION</span></span>|<span data-ttu-id="13313-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-558">String</span></span>|  
|<span data-ttu-id="13313-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-559">TABLE_PROPID</span></span>|<span data-ttu-id="13313-560">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-560">Int64</span></span>|  
|<span data-ttu-id="13313-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-561">DATE_CREATED</span></span>|<span data-ttu-id="13313-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-562">DateTime</span></span>|  
|<span data-ttu-id="13313-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-563">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="13313-565">Columns</span><span class="sxs-lookup"><span data-stu-id="13313-565">Columns</span></span>  
  
|<span data-ttu-id="13313-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-566">ColumnName</span></span>|<span data-ttu-id="13313-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-568">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-569">String</span></span>|  
|<span data-ttu-id="13313-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-571">String</span></span>|  
|<span data-ttu-id="13313-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-572">TABLE_NAME</span></span>|<span data-ttu-id="13313-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-573">String</span></span>|  
|<span data-ttu-id="13313-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-574">COLUMN_NAME</span></span>|<span data-ttu-id="13313-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-575">String</span></span>|  
|<span data-ttu-id="13313-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-576">COLUMN_GUID</span></span>|<span data-ttu-id="13313-577">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-577">Guid</span></span>|  
|<span data-ttu-id="13313-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-578">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-579">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-579">Int64</span></span>|  
|<span data-ttu-id="13313-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-581">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-581">Int64</span></span>|  
|<span data-ttu-id="13313-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="13313-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-583">Boolean</span></span>|  
|<span data-ttu-id="13313-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="13313-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="13313-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-585">String</span></span>|  
|<span data-ttu-id="13313-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="13313-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="13313-587">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-587">Int64</span></span>|  
|<span data-ttu-id="13313-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="13313-588">IS_NULLABLE</span></span>|<span data-ttu-id="13313-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-589">Boolean</span></span>|  
|<span data-ttu-id="13313-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-590">DATA_TYPE</span></span>|<span data-ttu-id="13313-591">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-591">Int32</span></span>|  
|<span data-ttu-id="13313-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-592">TYPE_GUID</span></span>|<span data-ttu-id="13313-593">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-593">Guid</span></span>|  
|<span data-ttu-id="13313-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="13313-595">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-595">Int64</span></span>|  
|<span data-ttu-id="13313-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="13313-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="13313-597">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-597">Int64</span></span>|  
|<span data-ttu-id="13313-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="13313-599">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-599">Int32</span></span>|  
|<span data-ttu-id="13313-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="13313-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="13313-601">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-601">Int16</span></span>|  
|<span data-ttu-id="13313-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="13313-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="13313-603">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-603">Int64</span></span>|  
|<span data-ttu-id="13313-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="13313-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-605">String</span></span>|  
|<span data-ttu-id="13313-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="13313-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-607">String</span></span>|  
|<span data-ttu-id="13313-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="13313-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-609">String</span></span>|  
|<span data-ttu-id="13313-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="13313-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-611">String</span></span>|  
|<span data-ttu-id="13313-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="13313-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-613">String</span></span>|  
|<span data-ttu-id="13313-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-614">COLLATION_NAME</span></span>|<span data-ttu-id="13313-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-615">String</span></span>|  
|<span data-ttu-id="13313-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="13313-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-617">String</span></span>|  
|<span data-ttu-id="13313-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="13313-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-619">String</span></span>|  
|<span data-ttu-id="13313-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-620">DOMAIN_NAME</span></span>|<span data-ttu-id="13313-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-621">String</span></span>|  
|<span data-ttu-id="13313-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-622">DESCRIPTION</span></span>|<span data-ttu-id="13313-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="13313-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="13313-624">Procedures</span></span>  
  
|<span data-ttu-id="13313-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-625">ColumnName</span></span>|<span data-ttu-id="13313-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="13313-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-628">String</span></span>|  
|<span data-ttu-id="13313-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="13313-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-630">String</span></span>|  
|<span data-ttu-id="13313-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="13313-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-632">String</span></span>|  
|<span data-ttu-id="13313-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="13313-634">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-634">Int16</span></span>|  
|<span data-ttu-id="13313-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="13313-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="13313-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-636">String</span></span>|  
|<span data-ttu-id="13313-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-637">DESCRIPTION</span></span>|<span data-ttu-id="13313-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-638">String</span></span>|  
|<span data-ttu-id="13313-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-639">DATE_CREATED</span></span>|<span data-ttu-id="13313-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-640">DateTime</span></span>|  
|<span data-ttu-id="13313-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-641">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="13313-643">Vues</span><span class="sxs-lookup"><span data-stu-id="13313-643">Views</span></span>  
  
|<span data-ttu-id="13313-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-644">ColumnName</span></span>|<span data-ttu-id="13313-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-646">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-647">String</span></span>|  
|<span data-ttu-id="13313-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-649">String</span></span>|  
|<span data-ttu-id="13313-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-650">TABLE_NAME</span></span>|<span data-ttu-id="13313-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-651">String</span></span>|  
|<span data-ttu-id="13313-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="13313-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="13313-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-653">String</span></span>|  
|<span data-ttu-id="13313-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="13313-654">CHECK_OPTION</span></span>|<span data-ttu-id="13313-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-655">Boolean</span></span>|  
|<span data-ttu-id="13313-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="13313-656">IS_UPDATABLE</span></span>|<span data-ttu-id="13313-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-657">Boolean</span></span>|  
|<span data-ttu-id="13313-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13313-658">DESCRIPTION</span></span>|<span data-ttu-id="13313-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-659">String</span></span>|  
|<span data-ttu-id="13313-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="13313-660">DATE_CREATED</span></span>|<span data-ttu-id="13313-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-661">DateTime</span></span>|  
|<span data-ttu-id="13313-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="13313-662">DATE_MODIFIED</span></span>|<span data-ttu-id="13313-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="13313-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="13313-664">Index</span><span class="sxs-lookup"><span data-stu-id="13313-664">Indexes</span></span>  
  
|<span data-ttu-id="13313-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="13313-665">ColumnName</span></span>|<span data-ttu-id="13313-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="13313-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="13313-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-667">TABLE_CATALOG</span></span>|<span data-ttu-id="13313-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-668">String</span></span>|  
|<span data-ttu-id="13313-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="13313-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-670">String</span></span>|  
|<span data-ttu-id="13313-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-671">TABLE_NAME</span></span>|<span data-ttu-id="13313-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-672">String</span></span>|  
|<span data-ttu-id="13313-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="13313-673">INDEX_CATALOG</span></span>|<span data-ttu-id="13313-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-674">String</span></span>|  
|<span data-ttu-id="13313-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="13313-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="13313-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-676">String</span></span>|  
|<span data-ttu-id="13313-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-677">INDEX_NAME</span></span>|<span data-ttu-id="13313-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-678">String</span></span>|  
|<span data-ttu-id="13313-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="13313-679">PRIMARY_KEY</span></span>|<span data-ttu-id="13313-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-680">Boolean</span></span>|  
|<span data-ttu-id="13313-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="13313-681">UNIQUE</span></span>|<span data-ttu-id="13313-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-682">Boolean</span></span>|  
|<span data-ttu-id="13313-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="13313-683">CLUSTERED</span></span>|<span data-ttu-id="13313-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-684">Boolean</span></span>|  
|<span data-ttu-id="13313-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="13313-685">TYPE</span></span>|<span data-ttu-id="13313-686">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-686">Int32</span></span>|  
|<span data-ttu-id="13313-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="13313-687">FILL_FACTOR</span></span>|<span data-ttu-id="13313-688">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-688">Int32</span></span>|  
|<span data-ttu-id="13313-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="13313-689">INITIAL_SIZE</span></span>|<span data-ttu-id="13313-690">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-690">Int32</span></span>|  
|<span data-ttu-id="13313-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="13313-691">NULLS</span></span>|<span data-ttu-id="13313-692">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-692">Int32</span></span>|  
|<span data-ttu-id="13313-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="13313-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="13313-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-694">Boolean</span></span>|  
|<span data-ttu-id="13313-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="13313-695">AUTO_UPDATE</span></span>|<span data-ttu-id="13313-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="13313-696">Boolean</span></span>|  
|<span data-ttu-id="13313-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-697">NULL_COLLATION</span></span>|<span data-ttu-id="13313-698">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-698">Int32</span></span>|  
|<span data-ttu-id="13313-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="13313-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="13313-700">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-700">Int64</span></span>|  
|<span data-ttu-id="13313-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="13313-701">COLUMN_NAME</span></span>|<span data-ttu-id="13313-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-702">String</span></span>|  
|<span data-ttu-id="13313-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="13313-703">COLUMN_GUID</span></span>|<span data-ttu-id="13313-704">Guid</span><span class="sxs-lookup"><span data-stu-id="13313-704">Guid</span></span>|  
|<span data-ttu-id="13313-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="13313-705">COLUMN_PROPID</span></span>|<span data-ttu-id="13313-706">Int64</span><span class="sxs-lookup"><span data-stu-id="13313-706">Int64</span></span>|  
|<span data-ttu-id="13313-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="13313-707">COLLATION</span></span>|<span data-ttu-id="13313-708">Int16</span><span class="sxs-lookup"><span data-stu-id="13313-708">Int16</span></span>|  
|<span data-ttu-id="13313-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="13313-709">CARDINALITY</span></span>|<span data-ttu-id="13313-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="13313-710">Decimal</span></span>|  
|<span data-ttu-id="13313-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="13313-711">PAGES</span></span>|<span data-ttu-id="13313-712">Int32</span><span class="sxs-lookup"><span data-stu-id="13313-712">Int32</span></span>|  
|<span data-ttu-id="13313-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="13313-713">FILTER_CONDITION</span></span>|<span data-ttu-id="13313-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="13313-714">String</span></span>|  
|<span data-ttu-id="13313-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="13313-715">INTEGRATED</span></span>|<span data-ttu-id="13313-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="13313-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="13313-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13313-717">See also</span></span>
- [<span data-ttu-id="13313-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="13313-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
