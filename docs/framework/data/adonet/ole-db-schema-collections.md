---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: f1cb5e1fe967088b44fa4045dfe50c1c57d963eb
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32766931"
---
# <a name="ole-db-schema-collections"></a><span data-ttu-id="dea8b-102">Collections de schémas OLE DB</span><span class="sxs-lookup"><span data-stu-id="dea8b-102">OLE DB Schema Collections</span></span>
<span data-ttu-id="dea8b-103">Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="dea8b-103">This section discusses schema collection support for the OLE DB providers for Microsoft SQL Server, Oracle, and Microsoft Jet.</span></span>  
  
## <a name="microsoft-sql-server-ole-db-provider"></a><span data-ttu-id="dea8b-104">Fournisseur Microsoft SQL Server OLE DB</span><span class="sxs-lookup"><span data-stu-id="dea8b-104">Microsoft SQL Server OLE DB Provider</span></span>  
 <span data-ttu-id="dea8b-105">Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dea8b-105">The Microsoft SQL Server OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="dea8b-106">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-106">Tables</span></span>  
  
-   <span data-ttu-id="dea8b-107">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-107">Columns</span></span>  
  
-   <span data-ttu-id="dea8b-108">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-108">Procedures</span></span>  
  
-   <span data-ttu-id="dea8b-109">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dea8b-109">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="dea8b-110">Catalogue</span><span class="sxs-lookup"><span data-stu-id="dea8b-110">Catalog</span></span>  
  
-   <span data-ttu-id="dea8b-111">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-111">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dea8b-112">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-112">Tables</span></span>  
  
|<span data-ttu-id="dea8b-113">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-113">ColumnName</span></span>|<span data-ttu-id="dea8b-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-114">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-115">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-115">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-116">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-116">String</span></span>|  
|<span data-ttu-id="dea8b-117">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-117">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-118">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-118">String</span></span>|  
|<span data-ttu-id="dea8b-119">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-119">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-120">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-120">String</span></span>|  
|<span data-ttu-id="dea8b-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-121">TABLE_TYPE</span></span>|<span data-ttu-id="dea8b-122">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-122">String</span></span>|  
|<span data-ttu-id="dea8b-123">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-123">TABLE_GUID</span></span>|<span data-ttu-id="dea8b-124">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-124">Guid</span></span>|  
|<span data-ttu-id="dea8b-125">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-125">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-126">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-126">String</span></span>|  
|<span data-ttu-id="dea8b-127">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-127">TABLE_PROPID</span></span>|<span data-ttu-id="dea8b-128">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-128">Int64</span></span>|  
|<span data-ttu-id="dea8b-129">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-129">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-130">DateTime</span></span>|  
|<span data-ttu-id="dea8b-131">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-131">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-132">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-132">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dea8b-133">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-133">Columns</span></span>  
  
|<span data-ttu-id="dea8b-134">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-134">ColumnName</span></span>|<span data-ttu-id="dea8b-135">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-135">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-136">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-136">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-137">String</span></span>|  
|<span data-ttu-id="dea8b-138">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-138">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-139">String</span></span>|  
|<span data-ttu-id="dea8b-140">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-140">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-141">String</span></span>|  
|<span data-ttu-id="dea8b-142">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-142">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-143">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-143">String</span></span>|  
|<span data-ttu-id="dea8b-144">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-144">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-145">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-145">Guid</span></span>|  
|<span data-ttu-id="dea8b-146">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-146">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-147">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-147">Int64</span></span>|  
|<span data-ttu-id="dea8b-148">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-148">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-149">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-149">Int64</span></span>|  
|<span data-ttu-id="dea8b-150">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-150">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dea8b-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-151">Boolean</span></span>|  
|<span data-ttu-id="dea8b-152">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-152">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dea8b-153">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-153">String</span></span>|  
|<span data-ttu-id="dea8b-154">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dea8b-154">COLUMN_FLAGS</span></span>|<span data-ttu-id="dea8b-155">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-155">Int64</span></span>|  
|<span data-ttu-id="dea8b-156">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-156">IS_NULLABLE</span></span>|<span data-ttu-id="dea8b-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-157">Boolean</span></span>|  
|<span data-ttu-id="dea8b-158">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-158">DATA_TYPE</span></span>|<span data-ttu-id="dea8b-159">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-159">Int32</span></span>|  
|<span data-ttu-id="dea8b-160">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-160">TYPE_GUID</span></span>|<span data-ttu-id="dea8b-161">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-161">Guid</span></span>|  
|<span data-ttu-id="dea8b-162">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-162">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dea8b-163">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-163">Int64</span></span>|  
|<span data-ttu-id="dea8b-164">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-164">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dea8b-165">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-165">Int64</span></span>|  
|<span data-ttu-id="dea8b-166">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-166">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dea8b-167">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-167">Int32</span></span>|  
|<span data-ttu-id="dea8b-168">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dea8b-168">NUMERIC_SCALE</span></span>|<span data-ttu-id="dea8b-169">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-169">Int16</span></span>|  
|<span data-ttu-id="dea8b-170">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-170">DATETIME_PRECISION</span></span>|<span data-ttu-id="dea8b-171">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-171">Int64</span></span>|  
|<span data-ttu-id="dea8b-172">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-172">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dea8b-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-173">String</span></span>|  
|<span data-ttu-id="dea8b-174">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-174">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dea8b-175">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-175">String</span></span>|  
|<span data-ttu-id="dea8b-176">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-176">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dea8b-177">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-177">String</span></span>|  
|<span data-ttu-id="dea8b-178">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-178">COLLATION_CATALOG</span></span>|<span data-ttu-id="dea8b-179">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-179">String</span></span>|  
|<span data-ttu-id="dea8b-180">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-180">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dea8b-181">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-181">String</span></span>|  
|<span data-ttu-id="dea8b-182">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-182">COLLATION_NAME</span></span>|<span data-ttu-id="dea8b-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-183">String</span></span>|  
|<span data-ttu-id="dea8b-184">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-184">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dea8b-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-185">String</span></span>|  
|<span data-ttu-id="dea8b-186">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-186">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dea8b-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-187">String</span></span>|  
|<span data-ttu-id="dea8b-188">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-188">DOMAIN_NAME</span></span>|<span data-ttu-id="dea8b-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-189">String</span></span>|  
|<span data-ttu-id="dea8b-190">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-190">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-191">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-191">String</span></span>|  
|<span data-ttu-id="dea8b-192">COLUMN_LCID</span><span class="sxs-lookup"><span data-stu-id="dea8b-192">COLUMN_LCID</span></span>|<span data-ttu-id="dea8b-193">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-193">Int32</span></span>|  
|<span data-ttu-id="dea8b-194">COLUMN_COMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="dea8b-194">COLUMN_COMPFLAGS</span></span>|<span data-ttu-id="dea8b-195">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-195">Int32</span></span>|  
|<span data-ttu-id="dea8b-196">COLUMN_SORTID</span><span class="sxs-lookup"><span data-stu-id="dea8b-196">COLUMN_SORTID</span></span>|<span data-ttu-id="dea8b-197">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-197">Int32</span></span>|  
|<span data-ttu-id="dea8b-198">COLUMN_TDSCOLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-198">COLUMN_TDSCOLLATION</span></span>|<span data-ttu-id="dea8b-199">Byte[]</span><span class="sxs-lookup"><span data-stu-id="dea8b-199">Byte[]</span></span>|  
|<span data-ttu-id="dea8b-200">IS_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="dea8b-200">IS_COMPUTED</span></span>|<span data-ttu-id="dea8b-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-201">Boolean</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dea8b-202">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-202">Procedures</span></span>  
  
|<span data-ttu-id="dea8b-203">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-203">ColumnName</span></span>|<span data-ttu-id="dea8b-204">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-204">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-205">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-205">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dea8b-206">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-206">String</span></span>|  
|<span data-ttu-id="dea8b-207">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-207">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dea8b-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-208">String</span></span>|  
|<span data-ttu-id="dea8b-209">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-209">PROCEDURE_NAME</span></span>|<span data-ttu-id="dea8b-210">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-210">String</span></span>|  
|<span data-ttu-id="dea8b-211">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-211">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dea8b-212">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-212">Int16</span></span>|  
|<span data-ttu-id="dea8b-213">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-213">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dea8b-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-214">String</span></span>|  
|<span data-ttu-id="dea8b-215">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-215">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-216">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-216">String</span></span>|  
|<span data-ttu-id="dea8b-217">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-217">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-218">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-218">DateTime</span></span>|  
|<span data-ttu-id="dea8b-219">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-219">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-220">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-220">DateTime</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="dea8b-221">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dea8b-221">ProcedureParameters</span></span>  
  
|<span data-ttu-id="dea8b-222">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-222">ColumnName</span></span>|<span data-ttu-id="dea8b-223">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-223">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-224">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-224">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dea8b-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-225">String</span></span>|  
|<span data-ttu-id="dea8b-226">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-226">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dea8b-227">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-227">String</span></span>|  
|<span data-ttu-id="dea8b-228">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-228">PROCEDURE_NAME</span></span>|<span data-ttu-id="dea8b-229">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-229">String</span></span>|  
|<span data-ttu-id="dea8b-230">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-230">PARAMETER_NAME</span></span>|<span data-ttu-id="dea8b-231">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-231">String</span></span>|  
|<span data-ttu-id="dea8b-232">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-232">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-233">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-233">Int32</span></span>|  
|<span data-ttu-id="dea8b-234">PARAMETER_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-234">PARAMETER_TYPE</span></span>|<span data-ttu-id="dea8b-235">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-235">Int32</span></span>|  
|<span data-ttu-id="dea8b-236">PARAMETER_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-236">PARAMETER_HASDEFAULT</span></span>|<span data-ttu-id="dea8b-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-237">Boolean</span></span>|  
|<span data-ttu-id="dea8b-238">PARAMETER_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-238">PARAMETER_DEFAULT</span></span>|<span data-ttu-id="dea8b-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-239">String</span></span>|  
|<span data-ttu-id="dea8b-240">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-240">IS_NULLABLE</span></span>|<span data-ttu-id="dea8b-241">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-241">Boolean</span></span>|  
|<span data-ttu-id="dea8b-242">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-242">DATA_TYPE</span></span>|<span data-ttu-id="dea8b-243">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-243">Int32</span></span>|  
|<span data-ttu-id="dea8b-244">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-244">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dea8b-245">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-245">Int64</span></span>|  
|<span data-ttu-id="dea8b-246">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-246">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dea8b-247">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-247">Int64</span></span>|  
|<span data-ttu-id="dea8b-248">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-248">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dea8b-249">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-249">Int32</span></span>|  
|<span data-ttu-id="dea8b-250">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dea8b-250">NUMERIC_SCALE</span></span>|<span data-ttu-id="dea8b-251">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-251">Int16</span></span>|  
|<span data-ttu-id="dea8b-252">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-252">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-253">String</span></span>|  
|<span data-ttu-id="dea8b-254">TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-254">TYPE_NAME</span></span>|<span data-ttu-id="dea8b-255">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-255">String</span></span>|  
|<span data-ttu-id="dea8b-256">LOCAL_TYPE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-256">LOCAL_TYPE_NAME</span></span>|<span data-ttu-id="dea8b-257">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-257">String</span></span>|  
  
### <a name="catalog"></a><span data-ttu-id="dea8b-258">Catalogue</span><span class="sxs-lookup"><span data-stu-id="dea8b-258">Catalog</span></span>  
  
|<span data-ttu-id="dea8b-259">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-259">ColumnName</span></span>|<span data-ttu-id="dea8b-260">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-260">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-261">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-261">CATALOG_NAME</span></span>|<span data-ttu-id="dea8b-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-262">String</span></span>|  
|<span data-ttu-id="dea8b-263">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-263">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-264">String</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dea8b-265">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-265">Indexes</span></span>  
  
|<span data-ttu-id="dea8b-266">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-266">ColumnName</span></span>|<span data-ttu-id="dea8b-267">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-267">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-268">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-268">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-269">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-269">String</span></span>|  
|<span data-ttu-id="dea8b-270">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-270">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-271">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-271">String</span></span>|  
|<span data-ttu-id="dea8b-272">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-272">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-273">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-273">String</span></span>|  
|<span data-ttu-id="dea8b-274">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-274">INDEX_CATALOG</span></span>|<span data-ttu-id="dea8b-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-275">String</span></span>|  
|<span data-ttu-id="dea8b-276">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-276">INDEX_SCHEMA</span></span>|<span data-ttu-id="dea8b-277">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-277">String</span></span>|  
|<span data-ttu-id="dea8b-278">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-278">INDEX_NAME</span></span>|<span data-ttu-id="dea8b-279">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-279">String</span></span>|  
|<span data-ttu-id="dea8b-280">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dea8b-280">PRIMARY_KEY</span></span>|<span data-ttu-id="dea8b-281">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-281">Boolean</span></span>|  
|<span data-ttu-id="dea8b-282">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dea8b-282">UNIQUE</span></span>|<span data-ttu-id="dea8b-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-283">Boolean</span></span>|  
|<span data-ttu-id="dea8b-284">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dea8b-284">CLUSTERED</span></span>|<span data-ttu-id="dea8b-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-285">Boolean</span></span>|  
|<span data-ttu-id="dea8b-286">TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-286">TYPE</span></span>|<span data-ttu-id="dea8b-287">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-287">Int32</span></span>|  
|<span data-ttu-id="dea8b-288">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dea8b-288">FILL_FACTOR</span></span>|<span data-ttu-id="dea8b-289">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-289">Int32</span></span>|  
|<span data-ttu-id="dea8b-290">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dea8b-290">INITIAL_SIZE</span></span>|<span data-ttu-id="dea8b-291">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-291">Int32</span></span>|  
|<span data-ttu-id="dea8b-292">NULLS</span><span class="sxs-lookup"><span data-stu-id="dea8b-292">NULLS</span></span>|<span data-ttu-id="dea8b-293">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-293">Int32</span></span>|  
|<span data-ttu-id="dea8b-294">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dea8b-294">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dea8b-295">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-295">Boolean</span></span>|  
|<span data-ttu-id="dea8b-296">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dea8b-296">AUTO_UPDATE</span></span>|<span data-ttu-id="dea8b-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-297">Boolean</span></span>|  
|<span data-ttu-id="dea8b-298">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-298">NULL_COLLATION</span></span>|<span data-ttu-id="dea8b-299">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-299">Int32</span></span>|  
|<span data-ttu-id="dea8b-300">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-300">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-301">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-301">Int64</span></span>|  
|<span data-ttu-id="dea8b-302">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-302">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-303">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-303">String</span></span>|  
|<span data-ttu-id="dea8b-304">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-304">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-305">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-305">Guid</span></span>|  
|<span data-ttu-id="dea8b-306">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-306">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-307">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-307">Int64</span></span>|  
|<span data-ttu-id="dea8b-308">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-308">COLLATION</span></span>|<span data-ttu-id="dea8b-309">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-309">Int16</span></span>|  
|<span data-ttu-id="dea8b-310">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dea8b-310">CARDINALITY</span></span>|<span data-ttu-id="dea8b-311">Decimal</span><span class="sxs-lookup"><span data-stu-id="dea8b-311">Decimal</span></span>|  
|<span data-ttu-id="dea8b-312">PAGES</span><span class="sxs-lookup"><span data-stu-id="dea8b-312">PAGES</span></span>|<span data-ttu-id="dea8b-313">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-313">Int32</span></span>|  
|<span data-ttu-id="dea8b-314">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-314">FILTER_CONDITION</span></span>|<span data-ttu-id="dea8b-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-315">String</span></span>|  
|<span data-ttu-id="dea8b-316">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-316">INTEGRATED</span></span>|<span data-ttu-id="dea8b-317">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-317">Boolean</span></span>|  
  
## <a name="microsoft-oracle-ole-db-provider"></a><span data-ttu-id="dea8b-318">Fournisseur Microsoft Oracle OLE DB</span><span class="sxs-lookup"><span data-stu-id="dea8b-318">Microsoft Oracle OLE DB Provider</span></span>  
 <span data-ttu-id="dea8b-319">Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dea8b-319">The Microsoft Oracle OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="dea8b-320">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-320">Tables</span></span>  
  
-   <span data-ttu-id="dea8b-321">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-321">Columns</span></span>  
  
-   <span data-ttu-id="dea8b-322">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-322">Procedures</span></span>  
  
-   <span data-ttu-id="dea8b-323">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="dea8b-323">ProcedureColumns</span></span>  
  
-   <span data-ttu-id="dea8b-324">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="dea8b-324">ProcedureParameters</span></span>  
  
-   <span data-ttu-id="dea8b-325">Vues</span><span class="sxs-lookup"><span data-stu-id="dea8b-325">Views</span></span>  
  
-   <span data-ttu-id="dea8b-326">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-326">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dea8b-327">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-327">Tables</span></span>  
  
|<span data-ttu-id="dea8b-328">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-328">ColumnName</span></span>|<span data-ttu-id="dea8b-329">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-329">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-330">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-330">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-331">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-331">String</span></span>|  
|<span data-ttu-id="dea8b-332">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-332">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-333">String</span></span>|  
|<span data-ttu-id="dea8b-334">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-334">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-335">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-335">String</span></span>|  
|<span data-ttu-id="dea8b-336">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-336">TABLE_TYPE</span></span>|<span data-ttu-id="dea8b-337">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-337">String</span></span>|  
|<span data-ttu-id="dea8b-338">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-338">TABLE_GUID</span></span>|<span data-ttu-id="dea8b-339">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-339">Guid</span></span>|  
|<span data-ttu-id="dea8b-340">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-340">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-341">String</span></span>|  
|<span data-ttu-id="dea8b-342">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-342">TABLE_PROPID</span></span>|<span data-ttu-id="dea8b-343">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-343">Int64</span></span>|  
|<span data-ttu-id="dea8b-344">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-344">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-345">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-345">DateTime</span></span>|  
|<span data-ttu-id="dea8b-346">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-346">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-347">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-347">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dea8b-348">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-348">Columns</span></span>  
  
|<span data-ttu-id="dea8b-349">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-349">ColumnName</span></span>|<span data-ttu-id="dea8b-350">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-350">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-351">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-351">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-352">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-352">String</span></span>|  
|<span data-ttu-id="dea8b-353">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-353">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-354">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-354">String</span></span>|  
|<span data-ttu-id="dea8b-355">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-355">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-356">String</span></span>|  
|<span data-ttu-id="dea8b-357">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-357">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-358">String</span></span>|  
|<span data-ttu-id="dea8b-359">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-359">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-360">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-360">Guid</span></span>|  
|<span data-ttu-id="dea8b-361">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-361">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-362">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-362">Int64</span></span>|  
|<span data-ttu-id="dea8b-363">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-363">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-364">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-364">Int64</span></span>|  
|<span data-ttu-id="dea8b-365">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-365">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dea8b-366">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-366">Boolean</span></span>|  
|<span data-ttu-id="dea8b-367">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-367">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dea8b-368">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-368">String</span></span>|  
|<span data-ttu-id="dea8b-369">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dea8b-369">COLUMN_FLAGS</span></span>|<span data-ttu-id="dea8b-370">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-370">Int64</span></span>|  
|<span data-ttu-id="dea8b-371">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-371">IS_NULLABLE</span></span>|<span data-ttu-id="dea8b-372">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-372">Boolean</span></span>|  
|<span data-ttu-id="dea8b-373">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-373">DATA_TYPE</span></span>|<span data-ttu-id="dea8b-374">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-374">Int32</span></span>|  
|<span data-ttu-id="dea8b-375">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-375">TYPE_GUID</span></span>|<span data-ttu-id="dea8b-376">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-376">Guid</span></span>|  
|<span data-ttu-id="dea8b-377">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-377">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dea8b-378">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-378">Int64</span></span>|  
|<span data-ttu-id="dea8b-379">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-379">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dea8b-380">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-380">Int64</span></span>|  
|<span data-ttu-id="dea8b-381">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-381">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dea8b-382">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-382">Int32</span></span>|  
|<span data-ttu-id="dea8b-383">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dea8b-383">NUMERIC_SCALE</span></span>|<span data-ttu-id="dea8b-384">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-384">Int16</span></span>|  
|<span data-ttu-id="dea8b-385">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-385">DATETIME_PRECISION</span></span>|<span data-ttu-id="dea8b-386">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-386">Int64</span></span>|  
|<span data-ttu-id="dea8b-387">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-387">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dea8b-388">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-388">String</span></span>|  
|<span data-ttu-id="dea8b-389">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-389">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dea8b-390">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-390">String</span></span>|  
|<span data-ttu-id="dea8b-391">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-391">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dea8b-392">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-392">String</span></span>|  
|<span data-ttu-id="dea8b-393">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-393">COLLATION_CATALOG</span></span>|<span data-ttu-id="dea8b-394">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-394">String</span></span>|  
|<span data-ttu-id="dea8b-395">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-395">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dea8b-396">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-396">String</span></span>|  
|<span data-ttu-id="dea8b-397">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-397">COLLATION_NAME</span></span>|<span data-ttu-id="dea8b-398">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-398">String</span></span>|  
|<span data-ttu-id="dea8b-399">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-399">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dea8b-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-400">String</span></span>|  
|<span data-ttu-id="dea8b-401">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-401">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dea8b-402">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-402">String</span></span>|  
|<span data-ttu-id="dea8b-403">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-403">DOMAIN_NAME</span></span>|<span data-ttu-id="dea8b-404">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-404">String</span></span>|  
|<span data-ttu-id="dea8b-405">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-405">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-406">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-406">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dea8b-407">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-407">Procedures</span></span>  
  
|<span data-ttu-id="dea8b-408">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-408">ColumnName</span></span>|<span data-ttu-id="dea8b-409">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-409">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-410">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-410">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dea8b-411">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-411">String</span></span>|  
|<span data-ttu-id="dea8b-412">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-412">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dea8b-413">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-413">String</span></span>|  
|<span data-ttu-id="dea8b-414">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-414">PROCEDURE_NAME</span></span>|<span data-ttu-id="dea8b-415">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-415">String</span></span>|  
|<span data-ttu-id="dea8b-416">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-416">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dea8b-417">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-417">Int16</span></span>|  
|<span data-ttu-id="dea8b-418">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-418">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dea8b-419">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-419">String</span></span>|  
|<span data-ttu-id="dea8b-420">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-420">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-421">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-421">String</span></span>|  
|<span data-ttu-id="dea8b-422">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-422">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-423">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-423">DateTime</span></span>|  
|<span data-ttu-id="dea8b-424">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-424">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-425">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-425">DateTime</span></span>|  
  
### <a name="procedurecolumns"></a><span data-ttu-id="dea8b-426">ProcedureColumns</span><span class="sxs-lookup"><span data-stu-id="dea8b-426">ProcedureColumns</span></span>  
  
|<span data-ttu-id="dea8b-427">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-427">ColumnName</span></span>|<span data-ttu-id="dea8b-428">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-428">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-429">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-429">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dea8b-430">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-430">String</span></span>|  
|<span data-ttu-id="dea8b-431">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-431">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dea8b-432">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-432">String</span></span>|  
|<span data-ttu-id="dea8b-433">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-433">PROCEDURE_NAME</span></span>|<span data-ttu-id="dea8b-434">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-434">String</span></span>|  
|<span data-ttu-id="dea8b-435">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-435">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-436">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-436">String</span></span>|  
|<span data-ttu-id="dea8b-437">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-437">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-438">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-438">Guid</span></span>|  
|<span data-ttu-id="dea8b-439">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-439">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-440">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-440">Int64</span></span>|  
|<span data-ttu-id="dea8b-441">ROWSET_NUMBER</span><span class="sxs-lookup"><span data-stu-id="dea8b-441">ROWSET_NUMBER</span></span>|<span data-ttu-id="dea8b-442">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-442">Int64</span></span>|  
|<span data-ttu-id="dea8b-443">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-443">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-444">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-444">Int64</span></span>|  
|<span data-ttu-id="dea8b-445">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-445">IS_NULLABLE</span></span>|<span data-ttu-id="dea8b-446">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-446">Boolean</span></span>|  
|<span data-ttu-id="dea8b-447">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-447">DATA_TYPE</span></span>|<span data-ttu-id="dea8b-448">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-448">Int32</span></span>|  
|<span data-ttu-id="dea8b-449">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-449">TYPE_GUID</span></span>|<span data-ttu-id="dea8b-450">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-450">Guid</span></span>|  
|<span data-ttu-id="dea8b-451">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-451">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dea8b-452">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-452">Int64</span></span>|  
|<span data-ttu-id="dea8b-453">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-453">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dea8b-454">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-454">Int64</span></span>|  
|<span data-ttu-id="dea8b-455">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-455">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dea8b-456">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-456">Int32</span></span>|  
|<span data-ttu-id="dea8b-457">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dea8b-457">NUMERIC_SCALE</span></span>|<span data-ttu-id="dea8b-458">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-458">Int16</span></span>|  
|<span data-ttu-id="dea8b-459">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-459">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-460">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-460">String</span></span>|  
|<span data-ttu-id="dea8b-461">OVERLOAD</span><span class="sxs-lookup"><span data-stu-id="dea8b-461">OVERLOAD</span></span>|<span data-ttu-id="dea8b-462">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-462">Int16</span></span>|  
  
### <a name="views"></a><span data-ttu-id="dea8b-463">Vues</span><span class="sxs-lookup"><span data-stu-id="dea8b-463">Views</span></span>  
  
|<span data-ttu-id="dea8b-464">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-464">ColumnName</span></span>|<span data-ttu-id="dea8b-465">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-465">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-466">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-466">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-467">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-467">String</span></span>|  
|<span data-ttu-id="dea8b-468">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-468">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-469">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-469">String</span></span>|  
|<span data-ttu-id="dea8b-470">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-470">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-471">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-471">String</span></span>|  
|<span data-ttu-id="dea8b-472">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-472">VIEW_DEFINITION</span></span>|<span data-ttu-id="dea8b-473">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-473">String</span></span>|  
|<span data-ttu-id="dea8b-474">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-474">CHECK_OPTION</span></span>|<span data-ttu-id="dea8b-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-475">Boolean</span></span>|  
|<span data-ttu-id="dea8b-476">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-476">IS_UPDATABLE</span></span>|<span data-ttu-id="dea8b-477">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-477">Boolean</span></span>|  
|<span data-ttu-id="dea8b-478">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-478">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-479">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-479">String</span></span>|  
|<span data-ttu-id="dea8b-480">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-480">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-481">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-481">DateTime</span></span>|  
|<span data-ttu-id="dea8b-482">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-482">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-483">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-483">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dea8b-484">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-484">Indexes</span></span>  
  
|<span data-ttu-id="dea8b-485">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-485">ColumnName</span></span>|<span data-ttu-id="dea8b-486">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-486">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-487">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-487">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-488">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-488">String</span></span>|  
|<span data-ttu-id="dea8b-489">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-489">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-490">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-490">String</span></span>|  
|<span data-ttu-id="dea8b-491">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-491">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-492">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-492">String</span></span>|  
|<span data-ttu-id="dea8b-493">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-493">INDEX_CATALOG</span></span>|<span data-ttu-id="dea8b-494">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-494">String</span></span>|  
|<span data-ttu-id="dea8b-495">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-495">INDEX_SCHEMA</span></span>|<span data-ttu-id="dea8b-496">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-496">String</span></span>|  
|<span data-ttu-id="dea8b-497">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-497">INDEX_NAME</span></span>|<span data-ttu-id="dea8b-498">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-498">String</span></span>|  
|<span data-ttu-id="dea8b-499">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dea8b-499">PRIMARY_KEY</span></span>|<span data-ttu-id="dea8b-500">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-500">Boolean</span></span>|  
|<span data-ttu-id="dea8b-501">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dea8b-501">UNIQUE</span></span>|<span data-ttu-id="dea8b-502">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-502">Boolean</span></span>|  
|<span data-ttu-id="dea8b-503">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dea8b-503">CLUSTERED</span></span>|<span data-ttu-id="dea8b-504">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-504">Boolean</span></span>|  
|<span data-ttu-id="dea8b-505">TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-505">TYPE</span></span>|<span data-ttu-id="dea8b-506">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-506">Int32</span></span>|  
|<span data-ttu-id="dea8b-507">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dea8b-507">FILL_FACTOR</span></span>|<span data-ttu-id="dea8b-508">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-508">Int32</span></span>|  
|<span data-ttu-id="dea8b-509">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dea8b-509">INITIAL_SIZE</span></span>|<span data-ttu-id="dea8b-510">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-510">Int32</span></span>|  
|<span data-ttu-id="dea8b-511">NULLS</span><span class="sxs-lookup"><span data-stu-id="dea8b-511">NULLS</span></span>|<span data-ttu-id="dea8b-512">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-512">Int32</span></span>|  
|<span data-ttu-id="dea8b-513">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dea8b-513">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dea8b-514">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-514">Boolean</span></span>|  
|<span data-ttu-id="dea8b-515">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dea8b-515">AUTO_UPDATE</span></span>|<span data-ttu-id="dea8b-516">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-516">Boolean</span></span>|  
|<span data-ttu-id="dea8b-517">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-517">NULL_COLLATION</span></span>|<span data-ttu-id="dea8b-518">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-518">Int32</span></span>|  
|<span data-ttu-id="dea8b-519">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-519">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-520">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-520">Int64</span></span>|  
|<span data-ttu-id="dea8b-521">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-521">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-522">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-522">String</span></span>|  
|<span data-ttu-id="dea8b-523">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-523">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-524">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-524">Guid</span></span>|  
|<span data-ttu-id="dea8b-525">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-525">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-526">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-526">Int64</span></span>|  
|<span data-ttu-id="dea8b-527">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-527">COLLATION</span></span>|<span data-ttu-id="dea8b-528">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-528">Int16</span></span>|  
|<span data-ttu-id="dea8b-529">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dea8b-529">CARDINALITY</span></span>|<span data-ttu-id="dea8b-530">Decimal</span><span class="sxs-lookup"><span data-stu-id="dea8b-530">Decimal</span></span>|  
|<span data-ttu-id="dea8b-531">PAGES</span><span class="sxs-lookup"><span data-stu-id="dea8b-531">PAGES</span></span>|<span data-ttu-id="dea8b-532">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-532">Int32</span></span>|  
|<span data-ttu-id="dea8b-533">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-533">FILTER_CONDITION</span></span>|<span data-ttu-id="dea8b-534">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-534">String</span></span>|  
|<span data-ttu-id="dea8b-535">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-535">INTEGRATED</span></span>|<span data-ttu-id="dea8b-536">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-536">Boolean</span></span>|  
  
## <a name="microsoft-jet-ole-db-provider"></a><span data-ttu-id="dea8b-537">Fournisseur Microsoft Jet OLE DB</span><span class="sxs-lookup"><span data-stu-id="dea8b-537">Microsoft Jet OLE DB Provider</span></span>  
 <span data-ttu-id="dea8b-538">Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :</span><span class="sxs-lookup"><span data-stu-id="dea8b-538">The Microsoft Jet OLE DB Driver supports the following specific schema collections in addition to the common schema collections:</span></span>  
  
-   <span data-ttu-id="dea8b-539">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-539">Tables</span></span>  
  
-   <span data-ttu-id="dea8b-540">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-540">Columns</span></span>  
  
-   <span data-ttu-id="dea8b-541">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-541">Procedures</span></span>  
  
-   <span data-ttu-id="dea8b-542">Vues</span><span class="sxs-lookup"><span data-stu-id="dea8b-542">Views</span></span>  
  
-   <span data-ttu-id="dea8b-543">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-543">Indexes</span></span>  
  
### <a name="tables"></a><span data-ttu-id="dea8b-544">Tables</span><span class="sxs-lookup"><span data-stu-id="dea8b-544">Tables</span></span>  
  
|<span data-ttu-id="dea8b-545">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-545">ColumnName</span></span>|<span data-ttu-id="dea8b-546">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-546">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-547">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-547">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-548">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-548">String</span></span>|  
|<span data-ttu-id="dea8b-549">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-549">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-550">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-550">String</span></span>|  
|<span data-ttu-id="dea8b-551">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-551">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-552">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-552">String</span></span>|  
|<span data-ttu-id="dea8b-553">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-553">TABLE_TYPE</span></span>|<span data-ttu-id="dea8b-554">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-554">String</span></span>|  
|<span data-ttu-id="dea8b-555">TABLE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-555">TABLE_GUID</span></span>|<span data-ttu-id="dea8b-556">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-556">Guid</span></span>|  
|<span data-ttu-id="dea8b-557">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-557">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-558">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-558">String</span></span>|  
|<span data-ttu-id="dea8b-559">TABLE_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-559">TABLE_PROPID</span></span>|<span data-ttu-id="dea8b-560">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-560">Int64</span></span>|  
|<span data-ttu-id="dea8b-561">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-561">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-562">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-562">DateTime</span></span>|  
|<span data-ttu-id="dea8b-563">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-563">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-564">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-564">DateTime</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="dea8b-565">Columns</span><span class="sxs-lookup"><span data-stu-id="dea8b-565">Columns</span></span>  
  
|<span data-ttu-id="dea8b-566">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-566">ColumnName</span></span>|<span data-ttu-id="dea8b-567">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-567">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-568">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-568">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-569">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-569">String</span></span>|  
|<span data-ttu-id="dea8b-570">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-570">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-571">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-571">String</span></span>|  
|<span data-ttu-id="dea8b-572">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-572">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-573">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-573">String</span></span>|  
|<span data-ttu-id="dea8b-574">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-574">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-575">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-575">String</span></span>|  
|<span data-ttu-id="dea8b-576">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-576">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-577">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-577">Guid</span></span>|  
|<span data-ttu-id="dea8b-578">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-578">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-579">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-579">Int64</span></span>|  
|<span data-ttu-id="dea8b-580">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-580">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-581">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-581">Int64</span></span>|  
|<span data-ttu-id="dea8b-582">COLUMN_HASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-582">COLUMN_HASDEFAULT</span></span>|<span data-ttu-id="dea8b-583">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-583">Boolean</span></span>|  
|<span data-ttu-id="dea8b-584">COLUMN_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dea8b-584">COLUMN_DEFAULT</span></span>|<span data-ttu-id="dea8b-585">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-585">String</span></span>|  
|<span data-ttu-id="dea8b-586">COLUMN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dea8b-586">COLUMN_FLAGS</span></span>|<span data-ttu-id="dea8b-587">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-587">Int64</span></span>|  
|<span data-ttu-id="dea8b-588">IS_NULLABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-588">IS_NULLABLE</span></span>|<span data-ttu-id="dea8b-589">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-589">Boolean</span></span>|  
|<span data-ttu-id="dea8b-590">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-590">DATA_TYPE</span></span>|<span data-ttu-id="dea8b-591">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-591">Int32</span></span>|  
|<span data-ttu-id="dea8b-592">TYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-592">TYPE_GUID</span></span>|<span data-ttu-id="dea8b-593">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-593">Guid</span></span>|  
|<span data-ttu-id="dea8b-594">CHARACTER_MAXIMUM_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-594">CHARACTER_MAXIMUM_LENGTH</span></span>|<span data-ttu-id="dea8b-595">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-595">Int64</span></span>|  
|<span data-ttu-id="dea8b-596">CHARACTER_OCTET_LENGTH</span><span class="sxs-lookup"><span data-stu-id="dea8b-596">CHARACTER_OCTET_LENGTH</span></span>|<span data-ttu-id="dea8b-597">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-597">Int64</span></span>|  
|<span data-ttu-id="dea8b-598">NUMERIC_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-598">NUMERIC_PRECISION</span></span>|<span data-ttu-id="dea8b-599">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-599">Int32</span></span>|  
|<span data-ttu-id="dea8b-600">NUMERIC_SCALE</span><span class="sxs-lookup"><span data-stu-id="dea8b-600">NUMERIC_SCALE</span></span>|<span data-ttu-id="dea8b-601">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-601">Int16</span></span>|  
|<span data-ttu-id="dea8b-602">DATETIME_PRECISION</span><span class="sxs-lookup"><span data-stu-id="dea8b-602">DATETIME_PRECISION</span></span>|<span data-ttu-id="dea8b-603">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-603">Int64</span></span>|  
|<span data-ttu-id="dea8b-604">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-604">CHARACTER_SET_CATALOG</span></span>|<span data-ttu-id="dea8b-605">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-605">String</span></span>|  
|<span data-ttu-id="dea8b-606">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-606">CHARACTER_SET_SCHEMA</span></span>|<span data-ttu-id="dea8b-607">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-607">String</span></span>|  
|<span data-ttu-id="dea8b-608">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-608">CHARACTER_SET_NAME</span></span>|<span data-ttu-id="dea8b-609">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-609">String</span></span>|  
|<span data-ttu-id="dea8b-610">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-610">COLLATION_CATALOG</span></span>|<span data-ttu-id="dea8b-611">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-611">String</span></span>|  
|<span data-ttu-id="dea8b-612">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-612">COLLATION_SCHEMA</span></span>|<span data-ttu-id="dea8b-613">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-613">String</span></span>|  
|<span data-ttu-id="dea8b-614">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-614">COLLATION_NAME</span></span>|<span data-ttu-id="dea8b-615">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-615">String</span></span>|  
|<span data-ttu-id="dea8b-616">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-616">DOMAIN_CATALOG</span></span>|<span data-ttu-id="dea8b-617">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-617">String</span></span>|  
|<span data-ttu-id="dea8b-618">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-618">DOMAIN_SCHEMA</span></span>|<span data-ttu-id="dea8b-619">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-619">String</span></span>|  
|<span data-ttu-id="dea8b-620">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-620">DOMAIN_NAME</span></span>|<span data-ttu-id="dea8b-621">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-621">String</span></span>|  
|<span data-ttu-id="dea8b-622">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-622">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-623">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-623">String</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="dea8b-624">Procédures</span><span class="sxs-lookup"><span data-stu-id="dea8b-624">Procedures</span></span>  
  
|<span data-ttu-id="dea8b-625">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-625">ColumnName</span></span>|<span data-ttu-id="dea8b-626">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-626">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-627">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-627">PROCEDURE_CATALOG</span></span>|<span data-ttu-id="dea8b-628">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-628">String</span></span>|  
|<span data-ttu-id="dea8b-629">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-629">PROCEDURE_SCHEMA</span></span>|<span data-ttu-id="dea8b-630">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-630">String</span></span>|  
|<span data-ttu-id="dea8b-631">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-631">PROCEDURE_NAME</span></span>|<span data-ttu-id="dea8b-632">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-632">String</span></span>|  
|<span data-ttu-id="dea8b-633">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-633">PROCEDURE_TYPE</span></span>|<span data-ttu-id="dea8b-634">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-634">Int16</span></span>|  
|<span data-ttu-id="dea8b-635">PROCEDURE_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-635">PROCEDURE_DEFINITION</span></span>|<span data-ttu-id="dea8b-636">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-636">String</span></span>|  
|<span data-ttu-id="dea8b-637">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-637">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-638">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-638">String</span></span>|  
|<span data-ttu-id="dea8b-639">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-639">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-640">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-640">DateTime</span></span>|  
|<span data-ttu-id="dea8b-641">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-641">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-642">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-642">DateTime</span></span>|  
  
### <a name="views"></a><span data-ttu-id="dea8b-643">Vues</span><span class="sxs-lookup"><span data-stu-id="dea8b-643">Views</span></span>  
  
|<span data-ttu-id="dea8b-644">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-644">ColumnName</span></span>|<span data-ttu-id="dea8b-645">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-645">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-646">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-646">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-647">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-647">String</span></span>|  
|<span data-ttu-id="dea8b-648">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-648">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-649">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-649">String</span></span>|  
|<span data-ttu-id="dea8b-650">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-650">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-651">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-651">String</span></span>|  
|<span data-ttu-id="dea8b-652">VIEW_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-652">VIEW_DEFINITION</span></span>|<span data-ttu-id="dea8b-653">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-653">String</span></span>|  
|<span data-ttu-id="dea8b-654">CHECK_OPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-654">CHECK_OPTION</span></span>|<span data-ttu-id="dea8b-655">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-655">Boolean</span></span>|  
|<span data-ttu-id="dea8b-656">IS_UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="dea8b-656">IS_UPDATABLE</span></span>|<span data-ttu-id="dea8b-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-657">Boolean</span></span>|  
|<span data-ttu-id="dea8b-658">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dea8b-658">DESCRIPTION</span></span>|<span data-ttu-id="dea8b-659">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-659">String</span></span>|  
|<span data-ttu-id="dea8b-660">DATE_CREATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-660">DATE_CREATED</span></span>|<span data-ttu-id="dea8b-661">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-661">DateTime</span></span>|  
|<span data-ttu-id="dea8b-662">DATE_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="dea8b-662">DATE_MODIFIED</span></span>|<span data-ttu-id="dea8b-663">DateTime</span><span class="sxs-lookup"><span data-stu-id="dea8b-663">DateTime</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="dea8b-664">Index</span><span class="sxs-lookup"><span data-stu-id="dea8b-664">Indexes</span></span>  
  
|<span data-ttu-id="dea8b-665">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="dea8b-665">ColumnName</span></span>|<span data-ttu-id="dea8b-666">Type de données</span><span class="sxs-lookup"><span data-stu-id="dea8b-666">DataType</span></span>|  
|----------------|--------------|  
|<span data-ttu-id="dea8b-667">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-667">TABLE_CATALOG</span></span>|<span data-ttu-id="dea8b-668">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-668">String</span></span>|  
|<span data-ttu-id="dea8b-669">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-669">TABLE_SCHEMA</span></span>|<span data-ttu-id="dea8b-670">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-670">String</span></span>|  
|<span data-ttu-id="dea8b-671">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-671">TABLE_NAME</span></span>|<span data-ttu-id="dea8b-672">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-672">String</span></span>|  
|<span data-ttu-id="dea8b-673">INDEX_CATALOG</span><span class="sxs-lookup"><span data-stu-id="dea8b-673">INDEX_CATALOG</span></span>|<span data-ttu-id="dea8b-674">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-674">String</span></span>|  
|<span data-ttu-id="dea8b-675">INDEX_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="dea8b-675">INDEX_SCHEMA</span></span>|<span data-ttu-id="dea8b-676">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-676">String</span></span>|  
|<span data-ttu-id="dea8b-677">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-677">INDEX_NAME</span></span>|<span data-ttu-id="dea8b-678">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-678">String</span></span>|  
|<span data-ttu-id="dea8b-679">PRIMARY_KEY</span><span class="sxs-lookup"><span data-stu-id="dea8b-679">PRIMARY_KEY</span></span>|<span data-ttu-id="dea8b-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-680">Boolean</span></span>|  
|<span data-ttu-id="dea8b-681">UNIQUE</span><span class="sxs-lookup"><span data-stu-id="dea8b-681">UNIQUE</span></span>|<span data-ttu-id="dea8b-682">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-682">Boolean</span></span>|  
|<span data-ttu-id="dea8b-683">CLUSTERED</span><span class="sxs-lookup"><span data-stu-id="dea8b-683">CLUSTERED</span></span>|<span data-ttu-id="dea8b-684">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-684">Boolean</span></span>|  
|<span data-ttu-id="dea8b-685">TYPE</span><span class="sxs-lookup"><span data-stu-id="dea8b-685">TYPE</span></span>|<span data-ttu-id="dea8b-686">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-686">Int32</span></span>|  
|<span data-ttu-id="dea8b-687">FILL_FACTOR</span><span class="sxs-lookup"><span data-stu-id="dea8b-687">FILL_FACTOR</span></span>|<span data-ttu-id="dea8b-688">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-688">Int32</span></span>|  
|<span data-ttu-id="dea8b-689">INITIAL_SIZE</span><span class="sxs-lookup"><span data-stu-id="dea8b-689">INITIAL_SIZE</span></span>|<span data-ttu-id="dea8b-690">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-690">Int32</span></span>|  
|<span data-ttu-id="dea8b-691">NULLS</span><span class="sxs-lookup"><span data-stu-id="dea8b-691">NULLS</span></span>|<span data-ttu-id="dea8b-692">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-692">Int32</span></span>|  
|<span data-ttu-id="dea8b-693">SORT_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="dea8b-693">SORT_BOOKMARKS</span></span>|<span data-ttu-id="dea8b-694">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-694">Boolean</span></span>|  
|<span data-ttu-id="dea8b-695">AUTO_UPDATE</span><span class="sxs-lookup"><span data-stu-id="dea8b-695">AUTO_UPDATE</span></span>|<span data-ttu-id="dea8b-696">Boolean</span><span class="sxs-lookup"><span data-stu-id="dea8b-696">Boolean</span></span>|  
|<span data-ttu-id="dea8b-697">NULL_COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-697">NULL_COLLATION</span></span>|<span data-ttu-id="dea8b-698">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-698">Int32</span></span>|  
|<span data-ttu-id="dea8b-699">ORDINAL_POSITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-699">ORDINAL_POSITION</span></span>|<span data-ttu-id="dea8b-700">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-700">Int64</span></span>|  
|<span data-ttu-id="dea8b-701">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="dea8b-701">COLUMN_NAME</span></span>|<span data-ttu-id="dea8b-702">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-702">String</span></span>|  
|<span data-ttu-id="dea8b-703">COLUMN_GUID</span><span class="sxs-lookup"><span data-stu-id="dea8b-703">COLUMN_GUID</span></span>|<span data-ttu-id="dea8b-704">Guid</span><span class="sxs-lookup"><span data-stu-id="dea8b-704">Guid</span></span>|  
|<span data-ttu-id="dea8b-705">COLUMN_PROPID</span><span class="sxs-lookup"><span data-stu-id="dea8b-705">COLUMN_PROPID</span></span>|<span data-ttu-id="dea8b-706">Int64</span><span class="sxs-lookup"><span data-stu-id="dea8b-706">Int64</span></span>|  
|<span data-ttu-id="dea8b-707">COLLATION</span><span class="sxs-lookup"><span data-stu-id="dea8b-707">COLLATION</span></span>|<span data-ttu-id="dea8b-708">Int16</span><span class="sxs-lookup"><span data-stu-id="dea8b-708">Int16</span></span>|  
|<span data-ttu-id="dea8b-709">CARDINALITY</span><span class="sxs-lookup"><span data-stu-id="dea8b-709">CARDINALITY</span></span>|<span data-ttu-id="dea8b-710">Decimal</span><span class="sxs-lookup"><span data-stu-id="dea8b-710">Decimal</span></span>|  
|<span data-ttu-id="dea8b-711">PAGES</span><span class="sxs-lookup"><span data-stu-id="dea8b-711">PAGES</span></span>|<span data-ttu-id="dea8b-712">Int32</span><span class="sxs-lookup"><span data-stu-id="dea8b-712">Int32</span></span>|  
|<span data-ttu-id="dea8b-713">FILTER_CONDITION</span><span class="sxs-lookup"><span data-stu-id="dea8b-713">FILTER_CONDITION</span></span>|<span data-ttu-id="dea8b-714">Chaîne</span><span class="sxs-lookup"><span data-stu-id="dea8b-714">String</span></span>|  
|<span data-ttu-id="dea8b-715">INTEGRATED</span><span class="sxs-lookup"><span data-stu-id="dea8b-715">INTEGRATED</span></span>|<span data-ttu-id="dea8b-716">Booléen</span><span class="sxs-lookup"><span data-stu-id="dea8b-716">Boolean</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dea8b-717">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea8b-717">See Also</span></span>  
 [<span data-ttu-id="dea8b-718">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="dea8b-718">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
