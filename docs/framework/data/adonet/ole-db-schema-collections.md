---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 6dc187b0a876d9e167a74f2381db156dde2764fe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59164682"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="7bfc0-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="7bfc0-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="7bfc0-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="7bfc0-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="7bfc0-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="7bfc0-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="7bfc0-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="7bfc0-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="7bfc0-106">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-106">Tables</span></span>  
  
-   <span data-ttu-id="7bfc0-107">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-107">Columns</span></span>  
  
-   <span data-ttu-id="7bfc0-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-108">Procedures</span></span>  
  
-   <span data-ttu-id="7bfc0-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="7bfc0-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="7bfc0-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="7bfc0-110">Catalog</span></span>  
  
-   <span data-ttu-id="7bfc0-111">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="7bfc0-112">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-112">Tables</span></span>  
  
|<span data-ttu-id="7bfc0-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-113">ColumnName</span></span>|<span data-ttu-id="7bfc0-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-115">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-116">String</span></span>|  
|<span data-ttu-id="7bfc0-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-118">String</span></span>|  
|<span data-ttu-id="7bfc0-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-119">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-120">String</span></span>|  
|<span data-ttu-id="7bfc0-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-121">TABLE_TYPE</span></span>|<span data-ttu-id="7bfc0-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-122">String</span></span>|  
|<span data-ttu-id="7bfc0-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-123">TABLE_GUID</span></span>|<span data-ttu-id="7bfc0-124">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-124">Guid</span></span>|  
|<span data-ttu-id="7bfc0-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-125">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-126">String</span></span>|  
|<span data-ttu-id="7bfc0-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-127">TABLE_PROPID</span></span>|<span data-ttu-id="7bfc0-128">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-128">Int64</span></span>|  
|<span data-ttu-id="7bfc0-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-129">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-130">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-131">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="7bfc0-133">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-133">Columns</span></span>  
  
|<span data-ttu-id="7bfc0-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-134">ColumnName</span></span>|<span data-ttu-id="7bfc0-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-136">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-137">String</span></span>|  
|<span data-ttu-id="7bfc0-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-139">String</span></span>|  
|<span data-ttu-id="7bfc0-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-140">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-141">String</span></span>|  
|<span data-ttu-id="7bfc0-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-142">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-143">String</span></span>|  
|<span data-ttu-id="7bfc0-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-144">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-145">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-145">Guid</span></span>|  
|<span data-ttu-id="7bfc0-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-146">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-147">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-147">Int64</span></span>|  
|<span data-ttu-id="7bfc0-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-149">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-149">Int64</span></span>|  
|<span data-ttu-id="7bfc0-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="7bfc0-151">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-151">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="7bfc0-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-153">String</span></span>|  
|<span data-ttu-id="7bfc0-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="7bfc0-155">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-155">Int64</span></span>|  
|<span data-ttu-id="7bfc0-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-156">IS_NULLABLE</span></span>|<span data-ttu-id="7bfc0-157">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-157">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-158">DATA_TYPE</span></span>|<span data-ttu-id="7bfc0-159">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-159">Int32</span></span>|  
|<span data-ttu-id="7bfc0-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-160">TYPE_GUID</span></span>|<span data-ttu-id="7bfc0-161">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-161">Guid</span></span>|  
|<span data-ttu-id="7bfc0-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="7bfc0-163">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-163">Int64</span></span>|  
|<span data-ttu-id="7bfc0-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="7bfc0-165">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-165">Int64</span></span>|  
|<span data-ttu-id="7bfc0-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="7bfc0-167">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-167">Int32</span></span>|  
|<span data-ttu-id="7bfc0-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="7bfc0-169">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-169">Int16</span></span>|  
|<span data-ttu-id="7bfc0-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="7bfc0-171">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-171">Int64</span></span>|  
|<span data-ttu-id="7bfc0-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="7bfc0-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-173">String</span></span>|  
|<span data-ttu-id="7bfc0-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="7bfc0-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-175">String</span></span>|  
|<span data-ttu-id="7bfc0-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="7bfc0-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-177">String</span></span>|  
|<span data-ttu-id="7bfc0-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="7bfc0-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-179">String</span></span>|  
|<span data-ttu-id="7bfc0-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="7bfc0-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-181">String</span></span>|  
|<span data-ttu-id="7bfc0-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-182">COLLATION_NAME</span></span>|<span data-ttu-id="7bfc0-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-183">String</span></span>|  
|<span data-ttu-id="7bfc0-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="7bfc0-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-185">String</span></span>|  
|<span data-ttu-id="7bfc0-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="7bfc0-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-187">String</span></span>|  
|<span data-ttu-id="7bfc0-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-188">DOMAIN_NAME</span></span>|<span data-ttu-id="7bfc0-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-189">String</span></span>|  
|<span data-ttu-id="7bfc0-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-190">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-191">String</span></span>|  
|<span data-ttu-id="7bfc0-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-192">COLUMN_LCID</span></span>|<span data-ttu-id="7bfc0-193">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-193">Int32</span></span>|  
|<span data-ttu-id="7bfc0-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="7bfc0-195">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-195">Int32</span></span>|  
|<span data-ttu-id="7bfc0-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-196">COLUMN_SORTID</span></span>|<span data-ttu-id="7bfc0-197">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-197">Int32</span></span>|  
|<span data-ttu-id="7bfc0-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="7bfc0-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="7bfc0-199">Byte[]</span></span>|  
|<span data-ttu-id="7bfc0-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-200">IS_COMPUTED</span></span>|<span data-ttu-id="7bfc0-201">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="7bfc0-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-202">Procedures</span></span>  
  
|<span data-ttu-id="7bfc0-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-203">ColumnName</span></span>|<span data-ttu-id="7bfc0-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="7bfc0-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-206">String</span></span>|  
|<span data-ttu-id="7bfc0-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-208">String</span></span>|  
|<span data-ttu-id="7bfc0-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="7bfc0-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-210">String</span></span>|  
|<span data-ttu-id="7bfc0-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="7bfc0-212">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-212">Int16</span></span>|  
|<span data-ttu-id="7bfc0-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="7bfc0-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-214">String</span></span>|  
|<span data-ttu-id="7bfc0-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-215">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-216">String</span></span>|  
|<span data-ttu-id="7bfc0-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-217">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-218">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-219">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="7bfc0-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="7bfc0-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="7bfc0-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-222">ColumnName</span></span>|<span data-ttu-id="7bfc0-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="7bfc0-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-225">String</span></span>|  
|<span data-ttu-id="7bfc0-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-227">String</span></span>|  
|<span data-ttu-id="7bfc0-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="7bfc0-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-229">String</span></span>|  
|<span data-ttu-id="7bfc0-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-230">PARAMETER_NAME</span></span>|<span data-ttu-id="7bfc0-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-231">String</span></span>|  
|<span data-ttu-id="7bfc0-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-233">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-233">Int32</span></span>|  
|<span data-ttu-id="7bfc0-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="7bfc0-235">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-235">Int32</span></span>|  
|<span data-ttu-id="7bfc0-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="7bfc0-237">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-237">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="7bfc0-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-239">String</span></span>|  
|<span data-ttu-id="7bfc0-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-240">IS_NULLABLE</span></span>|<span data-ttu-id="7bfc0-241">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-241">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-242">DATA_TYPE</span></span>|<span data-ttu-id="7bfc0-243">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-243">Int32</span></span>|  
|<span data-ttu-id="7bfc0-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="7bfc0-245">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-245">Int64</span></span>|  
|<span data-ttu-id="7bfc0-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="7bfc0-247">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-247">Int64</span></span>|  
|<span data-ttu-id="7bfc0-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="7bfc0-249">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-249">Int32</span></span>|  
|<span data-ttu-id="7bfc0-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="7bfc0-251">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-251">Int16</span></span>|  
|<span data-ttu-id="7bfc0-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-252">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-253">String</span></span>|  
|<span data-ttu-id="7bfc0-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-254">TYPE_NAME</span></span>|<span data-ttu-id="7bfc0-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-255">String</span></span>|  
|<span data-ttu-id="7bfc0-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="7bfc0-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="7bfc0-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="7bfc0-258">Catalog</span></span>  
  
|<span data-ttu-id="7bfc0-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-259">ColumnName</span></span>|<span data-ttu-id="7bfc0-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-261">CATALOG_NAME</span></span>|<span data-ttu-id="7bfc0-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-262">String</span></span>|  
|<span data-ttu-id="7bfc0-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-263">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="7bfc0-265">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-265">Indexes</span></span>  
  
|<span data-ttu-id="7bfc0-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-266">ColumnName</span></span>|<span data-ttu-id="7bfc0-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-268">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-269">String</span></span>|  
|<span data-ttu-id="7bfc0-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-271">String</span></span>|  
|<span data-ttu-id="7bfc0-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-272">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-273">String</span></span>|  
|<span data-ttu-id="7bfc0-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-274">INDEX_CATALOG</span></span>|<span data-ttu-id="7bfc0-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-275">String</span></span>|  
|<span data-ttu-id="7bfc0-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="7bfc0-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-277">String</span></span>|  
|<span data-ttu-id="7bfc0-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-278">INDEX_NAME</span></span>|<span data-ttu-id="7bfc0-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-279">String</span></span>|  
|<span data-ttu-id="7bfc0-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-280">PRIMARY_KEY</span></span>|<span data-ttu-id="7bfc0-281">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-281">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-282">UNIQUE</span></span>|<span data-ttu-id="7bfc0-283">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-283">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-284">CLUSTERED</span></span>|<span data-ttu-id="7bfc0-285">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-285">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-286">TYPE</span></span>|<span data-ttu-id="7bfc0-287">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-287">Int32</span></span>|  
|<span data-ttu-id="7bfc0-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="7bfc0-288">FILL_FACTOR</span></span>|<span data-ttu-id="7bfc0-289">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-289">Int32</span></span>|  
|<span data-ttu-id="7bfc0-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-290">INITIAL_SIZE</span></span>|<span data-ttu-id="7bfc0-291">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-291">Int32</span></span>|  
|<span data-ttu-id="7bfc0-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-292">NULLS</span></span>|<span data-ttu-id="7bfc0-293">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-293">Int32</span></span>|  
|<span data-ttu-id="7bfc0-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="7bfc0-295">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-295">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-296">AUTO_UPDATE</span></span>|<span data-ttu-id="7bfc0-297">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-297">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-298">NULL_COLLATION</span></span>|<span data-ttu-id="7bfc0-299">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-299">Int32</span></span>|  
|<span data-ttu-id="7bfc0-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-301">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-301">Int64</span></span>|  
|<span data-ttu-id="7bfc0-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-302">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-303">String</span></span>|  
|<span data-ttu-id="7bfc0-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-304">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-305">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-305">Guid</span></span>|  
|<span data-ttu-id="7bfc0-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-306">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-307">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-307">Int64</span></span>|  
|<span data-ttu-id="7bfc0-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-308">COLLATION</span></span>|<span data-ttu-id="7bfc0-309">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-309">Int16</span></span>|  
|<span data-ttu-id="7bfc0-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-310">CARDINALITY</span></span>|<span data-ttu-id="7bfc0-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="7bfc0-311">Decimal</span></span>|  
|<span data-ttu-id="7bfc0-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="7bfc0-312">PAGES</span></span>|<span data-ttu-id="7bfc0-313">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-313">Int32</span></span>|  
|<span data-ttu-id="7bfc0-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-314">FILTER_CONDITION</span></span>|<span data-ttu-id="7bfc0-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-315">String</span></span>|  
|<span data-ttu-id="7bfc0-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-316">INTEGRATED</span></span>|<span data-ttu-id="7bfc0-317">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="7bfc0-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="7bfc0-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="7bfc0-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="7bfc0-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="7bfc0-320">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-320">Tables</span></span>  
  
-   <span data-ttu-id="7bfc0-321">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-321">Columns</span></span>  
  
-   <span data-ttu-id="7bfc0-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-322">Procedures</span></span>  
  
-   <span data-ttu-id="7bfc0-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="7bfc0-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="7bfc0-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="7bfc0-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="7bfc0-325">Affichages</span><span class="sxs-lookup"><span data-stu-id="7bfc0-325">Views</span></span>  
  
-   <span data-ttu-id="7bfc0-326">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="7bfc0-327">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-327">Tables</span></span>  
  
|<span data-ttu-id="7bfc0-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-328">ColumnName</span></span>|<span data-ttu-id="7bfc0-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-330">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-331">String</span></span>|  
|<span data-ttu-id="7bfc0-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-333">String</span></span>|  
|<span data-ttu-id="7bfc0-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-334">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-335">String</span></span>|  
|<span data-ttu-id="7bfc0-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-336">TABLE_TYPE</span></span>|<span data-ttu-id="7bfc0-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-337">String</span></span>|  
|<span data-ttu-id="7bfc0-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-338">TABLE_GUID</span></span>|<span data-ttu-id="7bfc0-339">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-339">Guid</span></span>|  
|<span data-ttu-id="7bfc0-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-340">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-341">String</span></span>|  
|<span data-ttu-id="7bfc0-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-342">TABLE_PROPID</span></span>|<span data-ttu-id="7bfc0-343">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-343">Int64</span></span>|  
|<span data-ttu-id="7bfc0-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-344">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-345">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-346">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="7bfc0-348">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-348">Columns</span></span>  
  
|<span data-ttu-id="7bfc0-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-349">ColumnName</span></span>|<span data-ttu-id="7bfc0-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-351">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-352">String</span></span>|  
|<span data-ttu-id="7bfc0-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-354">String</span></span>|  
|<span data-ttu-id="7bfc0-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-355">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-356">String</span></span>|  
|<span data-ttu-id="7bfc0-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-357">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-358">String</span></span>|  
|<span data-ttu-id="7bfc0-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-359">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-360">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-360">Guid</span></span>|  
|<span data-ttu-id="7bfc0-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-361">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-362">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-362">Int64</span></span>|  
|<span data-ttu-id="7bfc0-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-364">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-364">Int64</span></span>|  
|<span data-ttu-id="7bfc0-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="7bfc0-366">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-366">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="7bfc0-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-368">String</span></span>|  
|<span data-ttu-id="7bfc0-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="7bfc0-370">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-370">Int64</span></span>|  
|<span data-ttu-id="7bfc0-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-371">IS_NULLABLE</span></span>|<span data-ttu-id="7bfc0-372">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-372">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-373">DATA_TYPE</span></span>|<span data-ttu-id="7bfc0-374">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-374">Int32</span></span>|  
|<span data-ttu-id="7bfc0-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-375">TYPE_GUID</span></span>|<span data-ttu-id="7bfc0-376">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-376">Guid</span></span>|  
|<span data-ttu-id="7bfc0-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="7bfc0-378">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-378">Int64</span></span>|  
|<span data-ttu-id="7bfc0-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="7bfc0-380">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-380">Int64</span></span>|  
|<span data-ttu-id="7bfc0-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="7bfc0-382">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-382">Int32</span></span>|  
|<span data-ttu-id="7bfc0-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="7bfc0-384">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-384">Int16</span></span>|  
|<span data-ttu-id="7bfc0-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="7bfc0-386">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-386">Int64</span></span>|  
|<span data-ttu-id="7bfc0-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="7bfc0-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-388">String</span></span>|  
|<span data-ttu-id="7bfc0-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="7bfc0-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-390">String</span></span>|  
|<span data-ttu-id="7bfc0-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="7bfc0-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-392">String</span></span>|  
|<span data-ttu-id="7bfc0-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="7bfc0-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-394">String</span></span>|  
|<span data-ttu-id="7bfc0-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="7bfc0-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-396">String</span></span>|  
|<span data-ttu-id="7bfc0-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-397">COLLATION_NAME</span></span>|<span data-ttu-id="7bfc0-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-398">String</span></span>|  
|<span data-ttu-id="7bfc0-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="7bfc0-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-400">String</span></span>|  
|<span data-ttu-id="7bfc0-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="7bfc0-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-402">String</span></span>|  
|<span data-ttu-id="7bfc0-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-403">DOMAIN_NAME</span></span>|<span data-ttu-id="7bfc0-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-404">String</span></span>|  
|<span data-ttu-id="7bfc0-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-405">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="7bfc0-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-407">Procedures</span></span>  
  
|<span data-ttu-id="7bfc0-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-408">ColumnName</span></span>|<span data-ttu-id="7bfc0-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="7bfc0-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-411">String</span></span>|  
|<span data-ttu-id="7bfc0-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-413">String</span></span>|  
|<span data-ttu-id="7bfc0-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="7bfc0-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-415">String</span></span>|  
|<span data-ttu-id="7bfc0-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="7bfc0-417">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-417">Int16</span></span>|  
|<span data-ttu-id="7bfc0-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="7bfc0-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-419">String</span></span>|  
|<span data-ttu-id="7bfc0-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-420">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-421">String</span></span>|  
|<span data-ttu-id="7bfc0-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-422">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-423">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-424">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="7bfc0-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="7bfc0-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="7bfc0-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-427">ColumnName</span></span>|<span data-ttu-id="7bfc0-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="7bfc0-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-430">String</span></span>|  
|<span data-ttu-id="7bfc0-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-432">String</span></span>|  
|<span data-ttu-id="7bfc0-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="7bfc0-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-434">String</span></span>|  
|<span data-ttu-id="7bfc0-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-435">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-436">String</span></span>|  
|<span data-ttu-id="7bfc0-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-437">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-438">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-438">Guid</span></span>|  
|<span data-ttu-id="7bfc0-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-439">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-440">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-440">Int64</span></span>|  
|<span data-ttu-id="7bfc0-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="7bfc0-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="7bfc0-442">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-442">Int64</span></span>|  
|<span data-ttu-id="7bfc0-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-444">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-444">Int64</span></span>|  
|<span data-ttu-id="7bfc0-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-445">IS_NULLABLE</span></span>|<span data-ttu-id="7bfc0-446">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-446">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-447">DATA_TYPE</span></span>|<span data-ttu-id="7bfc0-448">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-448">Int32</span></span>|  
|<span data-ttu-id="7bfc0-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-449">TYPE_GUID</span></span>|<span data-ttu-id="7bfc0-450">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-450">Guid</span></span>|  
|<span data-ttu-id="7bfc0-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="7bfc0-452">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-452">Int64</span></span>|  
|<span data-ttu-id="7bfc0-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="7bfc0-454">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-454">Int64</span></span>|  
|<span data-ttu-id="7bfc0-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="7bfc0-456">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-456">Int32</span></span>|  
|<span data-ttu-id="7bfc0-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="7bfc0-458">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-458">Int16</span></span>|  
|<span data-ttu-id="7bfc0-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-459">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-460">String</span></span>|  
|<span data-ttu-id="7bfc0-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="7bfc0-461">OVERLOAD</span></span>|<span data-ttu-id="7bfc0-462">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="7bfc0-463">Affichages</span><span class="sxs-lookup"><span data-stu-id="7bfc0-463">Views</span></span>  
  
|<span data-ttu-id="7bfc0-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-464">ColumnName</span></span>|<span data-ttu-id="7bfc0-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-466">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-467">String</span></span>|  
|<span data-ttu-id="7bfc0-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-469">String</span></span>|  
|<span data-ttu-id="7bfc0-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-470">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-471">String</span></span>|  
|<span data-ttu-id="7bfc0-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="7bfc0-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-473">String</span></span>|  
|<span data-ttu-id="7bfc0-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-474">CHECK_OPTION</span></span>|<span data-ttu-id="7bfc0-475">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-475">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-476">IS_UPDATABLE</span></span>|<span data-ttu-id="7bfc0-477">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-477">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-478">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-479">String</span></span>|  
|<span data-ttu-id="7bfc0-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-480">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-481">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-482">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="7bfc0-484">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-484">Indexes</span></span>  
  
|<span data-ttu-id="7bfc0-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-485">ColumnName</span></span>|<span data-ttu-id="7bfc0-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-487">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-488">String</span></span>|  
|<span data-ttu-id="7bfc0-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-490">String</span></span>|  
|<span data-ttu-id="7bfc0-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-491">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-492">String</span></span>|  
|<span data-ttu-id="7bfc0-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-493">INDEX_CATALOG</span></span>|<span data-ttu-id="7bfc0-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-494">String</span></span>|  
|<span data-ttu-id="7bfc0-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="7bfc0-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-496">String</span></span>|  
|<span data-ttu-id="7bfc0-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-497">INDEX_NAME</span></span>|<span data-ttu-id="7bfc0-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-498">String</span></span>|  
|<span data-ttu-id="7bfc0-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-499">PRIMARY_KEY</span></span>|<span data-ttu-id="7bfc0-500">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-500">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-501">UNIQUE</span></span>|<span data-ttu-id="7bfc0-502">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-502">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-503">CLUSTERED</span></span>|<span data-ttu-id="7bfc0-504">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-504">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-505">TYPE</span></span>|<span data-ttu-id="7bfc0-506">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-506">Int32</span></span>|  
|<span data-ttu-id="7bfc0-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="7bfc0-507">FILL_FACTOR</span></span>|<span data-ttu-id="7bfc0-508">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-508">Int32</span></span>|  
|<span data-ttu-id="7bfc0-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-509">INITIAL_SIZE</span></span>|<span data-ttu-id="7bfc0-510">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-510">Int32</span></span>|  
|<span data-ttu-id="7bfc0-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-511">NULLS</span></span>|<span data-ttu-id="7bfc0-512">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-512">Int32</span></span>|  
|<span data-ttu-id="7bfc0-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="7bfc0-514">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-514">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-515">AUTO_UPDATE</span></span>|<span data-ttu-id="7bfc0-516">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-516">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-517">NULL_COLLATION</span></span>|<span data-ttu-id="7bfc0-518">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-518">Int32</span></span>|  
|<span data-ttu-id="7bfc0-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-520">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-520">Int64</span></span>|  
|<span data-ttu-id="7bfc0-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-521">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-522">String</span></span>|  
|<span data-ttu-id="7bfc0-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-523">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-524">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-524">Guid</span></span>|  
|<span data-ttu-id="7bfc0-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-525">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-526">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-526">Int64</span></span>|  
|<span data-ttu-id="7bfc0-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-527">COLLATION</span></span>|<span data-ttu-id="7bfc0-528">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-528">Int16</span></span>|  
|<span data-ttu-id="7bfc0-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-529">CARDINALITY</span></span>|<span data-ttu-id="7bfc0-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="7bfc0-530">Decimal</span></span>|  
|<span data-ttu-id="7bfc0-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="7bfc0-531">PAGES</span></span>|<span data-ttu-id="7bfc0-532">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-532">Int32</span></span>|  
|<span data-ttu-id="7bfc0-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-533">FILTER_CONDITION</span></span>|<span data-ttu-id="7bfc0-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-534">String</span></span>|  
|<span data-ttu-id="7bfc0-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-535">INTEGRATED</span></span>|<span data-ttu-id="7bfc0-536">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="7bfc0-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="7bfc0-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="7bfc0-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="7bfc0-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="7bfc0-539">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-539">Tables</span></span>  
  
-   <span data-ttu-id="7bfc0-540">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-540">Columns</span></span>  
  
-   <span data-ttu-id="7bfc0-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-541">Procedures</span></span>  
  
-   <span data-ttu-id="7bfc0-542">Affichages</span><span class="sxs-lookup"><span data-stu-id="7bfc0-542">Views</span></span>  
  
-   <span data-ttu-id="7bfc0-543">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="7bfc0-544">Tables</span><span class="sxs-lookup"><span data-stu-id="7bfc0-544">Tables</span></span>  
  
|<span data-ttu-id="7bfc0-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-545">ColumnName</span></span>|<span data-ttu-id="7bfc0-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-547">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-548">String</span></span>|  
|<span data-ttu-id="7bfc0-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-550">String</span></span>|  
|<span data-ttu-id="7bfc0-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-551">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-552">String</span></span>|  
|<span data-ttu-id="7bfc0-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-553">TABLE_TYPE</span></span>|<span data-ttu-id="7bfc0-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-554">String</span></span>|  
|<span data-ttu-id="7bfc0-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-555">TABLE_GUID</span></span>|<span data-ttu-id="7bfc0-556">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-556">Guid</span></span>|  
|<span data-ttu-id="7bfc0-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-557">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-558">String</span></span>|  
|<span data-ttu-id="7bfc0-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-559">TABLE_PROPID</span></span>|<span data-ttu-id="7bfc0-560">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-560">Int64</span></span>|  
|<span data-ttu-id="7bfc0-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-561">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-562">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-563">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="7bfc0-565">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7bfc0-565">Columns</span></span>  
  
|<span data-ttu-id="7bfc0-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-566">ColumnName</span></span>|<span data-ttu-id="7bfc0-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-568">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-569">String</span></span>|  
|<span data-ttu-id="7bfc0-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-571">String</span></span>|  
|<span data-ttu-id="7bfc0-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-572">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-573">String</span></span>|  
|<span data-ttu-id="7bfc0-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-574">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-575">String</span></span>|  
|<span data-ttu-id="7bfc0-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-576">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-577">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-577">Guid</span></span>|  
|<span data-ttu-id="7bfc0-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-578">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-579">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-579">Int64</span></span>|  
|<span data-ttu-id="7bfc0-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-581">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-581">Int64</span></span>|  
|<span data-ttu-id="7bfc0-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="7bfc0-583">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-583">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="7bfc0-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="7bfc0-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-585">String</span></span>|  
|<span data-ttu-id="7bfc0-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="7bfc0-587">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-587">Int64</span></span>|  
|<span data-ttu-id="7bfc0-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-588">IS_NULLABLE</span></span>|<span data-ttu-id="7bfc0-589">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-589">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-590">DATA_TYPE</span></span>|<span data-ttu-id="7bfc0-591">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-591">Int32</span></span>|  
|<span data-ttu-id="7bfc0-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-592">TYPE_GUID</span></span>|<span data-ttu-id="7bfc0-593">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-593">Guid</span></span>|  
|<span data-ttu-id="7bfc0-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="7bfc0-595">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-595">Int64</span></span>|  
|<span data-ttu-id="7bfc0-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="7bfc0-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="7bfc0-597">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-597">Int64</span></span>|  
|<span data-ttu-id="7bfc0-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="7bfc0-599">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-599">Int32</span></span>|  
|<span data-ttu-id="7bfc0-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="7bfc0-601">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-601">Int16</span></span>|  
|<span data-ttu-id="7bfc0-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="7bfc0-603">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-603">Int64</span></span>|  
|<span data-ttu-id="7bfc0-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="7bfc0-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-605">String</span></span>|  
|<span data-ttu-id="7bfc0-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="7bfc0-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-607">String</span></span>|  
|<span data-ttu-id="7bfc0-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="7bfc0-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-609">String</span></span>|  
|<span data-ttu-id="7bfc0-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="7bfc0-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-611">String</span></span>|  
|<span data-ttu-id="7bfc0-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="7bfc0-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-613">String</span></span>|  
|<span data-ttu-id="7bfc0-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-614">COLLATION_NAME</span></span>|<span data-ttu-id="7bfc0-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-615">String</span></span>|  
|<span data-ttu-id="7bfc0-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="7bfc0-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-617">String</span></span>|  
|<span data-ttu-id="7bfc0-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="7bfc0-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-619">String</span></span>|  
|<span data-ttu-id="7bfc0-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-620">DOMAIN_NAME</span></span>|<span data-ttu-id="7bfc0-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-621">String</span></span>|  
|<span data-ttu-id="7bfc0-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-622">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="7bfc0-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="7bfc0-624">Procedures</span></span>  
  
|<span data-ttu-id="7bfc0-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-625">ColumnName</span></span>|<span data-ttu-id="7bfc0-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="7bfc0-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-628">String</span></span>|  
|<span data-ttu-id="7bfc0-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-630">String</span></span>|  
|<span data-ttu-id="7bfc0-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="7bfc0-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-632">String</span></span>|  
|<span data-ttu-id="7bfc0-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="7bfc0-634">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-634">Int16</span></span>|  
|<span data-ttu-id="7bfc0-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="7bfc0-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-636">String</span></span>|  
|<span data-ttu-id="7bfc0-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-637">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-638">String</span></span>|  
|<span data-ttu-id="7bfc0-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-639">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-640">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-641">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="7bfc0-643">Affichages</span><span class="sxs-lookup"><span data-stu-id="7bfc0-643">Views</span></span>  
  
|<span data-ttu-id="7bfc0-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-644">ColumnName</span></span>|<span data-ttu-id="7bfc0-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-646">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-647">String</span></span>|  
|<span data-ttu-id="7bfc0-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-649">String</span></span>|  
|<span data-ttu-id="7bfc0-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-650">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-651">String</span></span>|  
|<span data-ttu-id="7bfc0-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="7bfc0-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-653">String</span></span>|  
|<span data-ttu-id="7bfc0-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-654">CHECK_OPTION</span></span>|<span data-ttu-id="7bfc0-655">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-655">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-656">IS_UPDATABLE</span></span>|<span data-ttu-id="7bfc0-657">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-657">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-658">DESCRIPTION</span></span>|<span data-ttu-id="7bfc0-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-659">String</span></span>|  
|<span data-ttu-id="7bfc0-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-660">DATE_CREATED</span></span>|<span data-ttu-id="7bfc0-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-661">DateTime</span></span>|  
|<span data-ttu-id="7bfc0-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-662">DATE_MODIFIED</span></span>|<span data-ttu-id="7bfc0-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="7bfc0-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="7bfc0-664">Index</span><span class="sxs-lookup"><span data-stu-id="7bfc0-664">Indexes</span></span>  
  
|<span data-ttu-id="7bfc0-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-665">ColumnName</span></span>|<span data-ttu-id="7bfc0-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="7bfc0-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="7bfc0-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-667">TABLE_CATALOG</span></span>|<span data-ttu-id="7bfc0-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-668">String</span></span>|  
|<span data-ttu-id="7bfc0-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="7bfc0-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-670">String</span></span>|  
|<span data-ttu-id="7bfc0-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-671">TABLE_NAME</span></span>|<span data-ttu-id="7bfc0-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-672">String</span></span>|  
|<span data-ttu-id="7bfc0-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="7bfc0-673">INDEX_CATALOG</span></span>|<span data-ttu-id="7bfc0-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-674">String</span></span>|  
|<span data-ttu-id="7bfc0-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="7bfc0-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="7bfc0-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-676">String</span></span>|  
|<span data-ttu-id="7bfc0-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-677">INDEX_NAME</span></span>|<span data-ttu-id="7bfc0-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-678">String</span></span>|  
|<span data-ttu-id="7bfc0-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-679">PRIMARY_KEY</span></span>|<span data-ttu-id="7bfc0-680">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-680">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-681">UNIQUE</span></span>|<span data-ttu-id="7bfc0-682">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-682">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-683">CLUSTERED</span></span>|<span data-ttu-id="7bfc0-684">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-684">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-685">TYPE</span></span>|<span data-ttu-id="7bfc0-686">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-686">Int32</span></span>|  
|<span data-ttu-id="7bfc0-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="7bfc0-687">FILL_FACTOR</span></span>|<span data-ttu-id="7bfc0-688">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-688">Int32</span></span>|  
|<span data-ttu-id="7bfc0-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-689">INITIAL_SIZE</span></span>|<span data-ttu-id="7bfc0-690">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-690">Int32</span></span>|  
|<span data-ttu-id="7bfc0-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-691">NULLS</span></span>|<span data-ttu-id="7bfc0-692">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-692">Int32</span></span>|  
|<span data-ttu-id="7bfc0-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="7bfc0-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="7bfc0-694">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-694">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7bfc0-695">AUTO_UPDATE</span></span>|<span data-ttu-id="7bfc0-696">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-696">Boolean</span></span>|  
|<span data-ttu-id="7bfc0-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-697">NULL_COLLATION</span></span>|<span data-ttu-id="7bfc0-698">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-698">Int32</span></span>|  
|<span data-ttu-id="7bfc0-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="7bfc0-700">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-700">Int64</span></span>|  
|<span data-ttu-id="7bfc0-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="7bfc0-701">COLUMN_NAME</span></span>|<span data-ttu-id="7bfc0-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-702">String</span></span>|  
|<span data-ttu-id="7bfc0-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-703">COLUMN_GUID</span></span>|<span data-ttu-id="7bfc0-704">GUID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-704">Guid</span></span>|  
|<span data-ttu-id="7bfc0-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="7bfc0-705">COLUMN_PROPID</span></span>|<span data-ttu-id="7bfc0-706">Int64</span><span class="sxs-lookup"><span data-stu-id="7bfc0-706">Int64</span></span>|  
|<span data-ttu-id="7bfc0-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-707">COLLATION</span></span>|<span data-ttu-id="7bfc0-708">Int16</span><span class="sxs-lookup"><span data-stu-id="7bfc0-708">Int16</span></span>|  
|<span data-ttu-id="7bfc0-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="7bfc0-709">CARDINALITY</span></span>|<span data-ttu-id="7bfc0-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="7bfc0-710">Decimal</span></span>|  
|<span data-ttu-id="7bfc0-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="7bfc0-711">PAGES</span></span>|<span data-ttu-id="7bfc0-712">Int32</span><span class="sxs-lookup"><span data-stu-id="7bfc0-712">Int32</span></span>|  
|<span data-ttu-id="7bfc0-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="7bfc0-713">FILTER_CONDITION</span></span>|<span data-ttu-id="7bfc0-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7bfc0-714">String</span></span>|  
|<span data-ttu-id="7bfc0-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="7bfc0-715">INTEGRATED</span></span>|<span data-ttu-id="7bfc0-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="7bfc0-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7bfc0-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bfc0-717">See also</span></span>

- [<span data-ttu-id="7bfc0-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="7bfc0-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
