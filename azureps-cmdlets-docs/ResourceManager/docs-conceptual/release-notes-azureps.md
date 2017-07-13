---
title: "Azure PowerShell Değişiklik Günlüğü | Microsoft Docs"
description: "Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 97a23180a1fc65d96fdc9dbdffcbe3501a4c4c2a
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="c3632-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="c3632-103">Release notes</span></span>
<a id="release-notes" class="xliff"></a>

<span data-ttu-id="c3632-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c3632-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <span data-ttu-id="c3632-105">Sürüm 4.0.0</span><span class="sxs-lookup"><span data-stu-id="c3632-105">Version 4.0.0</span></span>
<a id="version-400" class="xliff"></a>

* <span data-ttu-id="c3632-106">Bu sürüm önemli değişiklikler içerir.</span><span class="sxs-lookup"><span data-stu-id="c3632-106">This release contains breaking changes.</span></span> <span data-ttu-id="c3632-107">Değişikliklerle ilgili ayrıntılar ve var olan betikler üzerindeki etkileri için lütfen [geçiş kılavuzuna](https://aka.ms/azps-migration-guide) bakın.</span><span class="sxs-lookup"><span data-stu-id="c3632-107">Please see [the migration guide](https://aka.ms/azps-migration-guide) for change details and the impact on existing scripts.</span></span>
* <span data-ttu-id="c3632-108">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c3632-108">ApiManagement</span></span>
  - <span data-ttu-id="c3632-109">New-AzureRmApiManagementGroup cmdlet'inde harici grupların yapılandırılması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="c3632-109">Added support for configuring external groups in New-AzureRmApiManagementGroup.</span></span>
* <span data-ttu-id="c3632-110">Faturalandırma</span><span class="sxs-lookup"><span data-stu-id="c3632-110">Billing</span></span>
  - <span data-ttu-id="c3632-111">Yeni Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c3632-111">New Cmdlet Get-AzureRmBillingPeriod</span></span>
    + <span data-ttu-id="c3632-112">cmdlet'i ile aboneliğin Azure faturalandırma dönemlerini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3632-112">cmdlet to retrieve azure billing periods of the subscription.</span></span>
  - <span data-ttu-id="c3632-113">Get-AzureRmBillingInvoice cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c3632-113">Update Cmdlet Get-AzureRmBillingInvoice</span></span>
  - <span data-ttu-id="c3632-114">Yeni özellik: BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="c3632-114">new property BillingPeriodNames</span></span>
  - <span data-ttu-id="c3632-115">Liste görünümünde çıktı</span><span class="sxs-lookup"><span data-stu-id="c3632-115">output in list view</span></span>
* <span data-ttu-id="c3632-116">İşlem</span><span class="sxs-lookup"><span data-stu-id="c3632-116">Compute</span></span>
  - <span data-ttu-id="c3632-117">Set-AzureRmVMAEMExtension ve Test-AzureRmVMAEMExtension cmdlet'leri Premium yönetilen diskleri destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c3632-117">Updated Set-AzureRmVMAEMExtension and Test-AzureRmVMAEMExtension cmdlets to support Premium managed disks</span></span>
  - <span data-ttu-id="c3632-118">IaaS VM'leri için şifreleme ayarlarının yedeklenmesi ve hata durumunda geri yüklenmesi</span><span class="sxs-lookup"><span data-stu-id="c3632-118">Backup encryption settings for IaaS VMs and restore on failure</span></span>
  - <span data-ttu-id="c3632-119">ChefServiceInterval seçeneğinin adı ChefDaemonInterval olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-119">ChefServiceInterval option is renamed to ChefDaemonInterval now.</span></span> <span data-ttu-id="c3632-120">Ancak eskisi de çalışmaya devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-120">Old one will continue to work however.</span></span>
  - <span data-ttu-id="c3632-121">PS VM nesnesinden yinelenen DataDiskNames ve NetworkInterfaceIDs özellikleri kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c3632-121">Remove duplicated DataDiskNames and NetworkInterfaceIDs properties from PS VM object.</span></span>
  - <span data-ttu-id="c3632-122">Remove-AzureRmVMDataDisk ve Remove-AzureRmVMNetworkInterface cmdlet'lerindeki Make DataDiskNames ve NetworkInterfaceIDs parametreleri isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-122">Make DataDiskNames and NetworkInterfaceIDs parameters optional in Remove-AzureRmVMDataDisk and Remove-AzureRmVMNetworkInterface, respectively.</span></span>
  - <span data-ttu-id="c3632-123">Get cmdlet'leri liste nesnesi döndürdüğünde karşılaşılan kanal sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-123">Fix the piping issue of Get cmdlets when the Get cmdlets return a list object.</span></span>
  - <span data-ttu-id="c3632-124">RDFE cmdlet'leriyle çakışan cmdlet'ler yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="c3632-124">Cmdlets that conflicted with RDFE cmdlets have been renamed.</span></span> <span data-ttu-id="c3632-125">Daha fazla bilgi için bkz. https://github.com/Azure/azure-powershell/issues/2917</span><span class="sxs-lookup"><span data-stu-id="c3632-125">See issue https://github.com/Azure/azure-powershell/issues/2917 for more details</span></span>
    + <span data-ttu-id="c3632-126">`New-AzureVMSqlServerAutoBackupConfig`, `New-AzureRmVMSqlServerAutoBackupConfig` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c3632-126">`New-AzureVMSqlServerAutoBackupConfig` has been renamed to `New-AzureRmVMSqlServerAutoBackupConfig`</span></span>
    + <span data-ttu-id="c3632-127">`New-AzureVMSqlServerAutoPatchingConfig`, `New-AzureRmVMSqlServerAutoPatchingConfig` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c3632-127">`New-AzureVMSqlServerAutoPatchingConfig` has been renamed to `New-AzureRmVMSqlServerAutoPatchingConfig`</span></span>
    + <span data-ttu-id="c3632-128">`New-AzureVMSqlServerKeyVaultCredentialConfig`, `New-AzureRmVMSqlServerKeyVaultCredentialConfig` olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="c3632-128">`New-AzureVMSqlServerKeyVaultCredentialConfig` has been renamed to `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span></span>
* <span data-ttu-id="c3632-129">Tüketim</span><span class="sxs-lookup"><span data-stu-id="c3632-129">Consumption</span></span>
  - <span data-ttu-id="c3632-130">Yeni cmdlet: Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c3632-130">New Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>
    + <span data-ttu-id="c3632-131">Abonelik kullanım ayrıntılarını alma cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="c3632-131">cmdlet to retrieve usage details of the subscription.</span></span>
* <span data-ttu-id="c3632-132">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3632-132">ContainerRegistry</span></span>
  - <span data-ttu-id="c3632-133">Azure Container Registry için PowerShell cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-133">Add PowerShell cmdlets for Azure Container Registry</span></span>
    + <span data-ttu-id="c3632-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3632-134">New-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c3632-135">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3632-135">Get-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c3632-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3632-136">Update-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c3632-137">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c3632-137">Remove-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c3632-138">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c3632-138">Get-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="c3632-139">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c3632-139">Update-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="c3632-140">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c3632-140">Test-AzureRmContainerRegistryNameAvailability</span></span>
* <span data-ttu-id="c3632-141">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c3632-141">DataLakeAnalytics</span></span>
  - <span data-ttu-id="c3632-142">Katalog paketleri için alma ve listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-142">Add support for catalog package get and list</span></span>
  - <span data-ttu-id="c3632-143">Aşağıdaki katalog öğeleri için daha üst öğelerden listeleme desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="c3632-143">Add support for listing the following catalog items from deeper ancestors:</span></span>
    + <span data-ttu-id="c3632-144">Tablo</span><span class="sxs-lookup"><span data-stu-id="c3632-144">Table</span></span>
    + <span data-ttu-id="c3632-145">TVF</span><span class="sxs-lookup"><span data-stu-id="c3632-145">TVF</span></span>
    + <span data-ttu-id="c3632-146">Görünüm</span><span class="sxs-lookup"><span data-stu-id="c3632-146">View</span></span>
    + <span data-ttu-id="c3632-147">İstatistikler</span><span class="sxs-lookup"><span data-stu-id="c3632-147">Statistics</span></span>
* <span data-ttu-id="c3632-148">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c3632-148">DataLakeStore</span></span>
  - <span data-ttu-id="c3632-149">Performansı artırmak için `Import-AzureRMDataLakeStoreItem` ve `Export-AzureRMDataLakeStoreItem` için izleme günlüğü varsayılan olarak devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="c3632-149">For `Import-AzureRMDataLakeStoreItem` and `Export-AzureRMDataLakeStoreItem` trace logging has been disabled by default to improve performance.</span></span> <span data-ttu-id="c3632-150">İzleme günlüğünden faydalanmak isterseniz lütfen `-DiagnosticLogLevel` ve `-DiagnosticLogPath` parametrelerini kullanın</span><span class="sxs-lookup"><span data-stu-id="c3632-150">If trace logging is desired please use the `-DiagnosticLogLevel` and `-DiagnosticLogPath` parameters</span></span>
  - <span data-ttu-id="c3632-151">Bazen ADLS'ye çok sayıda küçük dosya yüklerken PowerShell'in çökmesine neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-151">Fixed a bug that would sometimes cause PowerShell to crash when uploading lots of small file to ADLS.</span></span>
* <span data-ttu-id="c3632-152">EventHub</span><span class="sxs-lookup"><span data-stu-id="c3632-152">EventHub</span></span>
  - <span data-ttu-id="c3632-153">Hata düzeltmesi:</span><span class="sxs-lookup"><span data-stu-id="c3632-153">Bug fix :</span></span>
    + <span data-ttu-id="c3632-154">Set-AzureRmEventHubNamespace cmdlet'inin "Tier" null olamaz, "SkuName" olmalı hatası için düzeltme</span><span class="sxs-lookup"><span data-stu-id="c3632-154">Fix for Set-AzureRmEventHubNamespace cmdlet error  - 'Tier' cannot be null, where it should be 'SkuName'</span></span>
    + <span data-ttu-id="c3632-155">Set-AzureRmEventHub - EventHub güncelleştirilirken karşılaşılan "Nesne başvurusu bir nesnenin örneğine ayarlanmadı" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-155">Set-AzureRmEventHub - Fix 'Object reference not set to an instance of an object' error while updating EventHub</span></span>
* <span data-ttu-id="c3632-156">Insights</span><span class="sxs-lookup"><span data-stu-id="c3632-156">Insights</span></span>
  - <span data-ttu-id="c3632-157">Add-AzureRm*AlertRule</span><span class="sxs-lookup"><span data-stu-id="c3632-157">Add-AzureRm*AlertRule</span></span>
    + <span data-ttu-id="c3632-158">Tek bir nesne döndürür: newResource, statusCode, requestId</span><span class="sxs-lookup"><span data-stu-id="c3632-158">Returns a single object: newResource, statusCode, requestId</span></span>
  - <span data-ttu-id="c3632-159">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3632-159">Get-AzureRmAlertRule</span></span>
    + <span data-ttu-id="c3632-160">Çıktı artık tek bir nesne yerine numaralandırılmış alan şeklinde.</span><span class="sxs-lookup"><span data-stu-id="c3632-160">The output is now enumerated instead of considered a single object.</span></span> <span data-ttu-id="c3632-161">Türü değişmedi, yine bir liste.</span><span class="sxs-lookup"><span data-stu-id="c3632-161">Its type did not change, it is still a list.</span></span>
  - <span data-ttu-id="c3632-162">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3632-162">Remove-AzureRmAlertRule</span></span>
    + <span data-ttu-id="c3632-163">statusCode, istek tarafından döndürülen durum kodunu takip ediyor, önceden sürekli Tamam şeklindeydi.</span><span class="sxs-lookup"><span data-stu-id="c3632-163">The statusCode follows the status code returned by the request, before it was Ok always.</span></span>
  - <span data-ttu-id="c3632-164">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c3632-164">Add-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="c3632-165">Artık statusCode, requestId ve yeni oluşturulan/güncelleştirilen kaynağı içeren tek bir nesne (eskisi gibi liste değil) döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-165">Returns now a single object (not a list as before) containing statusCode, requestId, and the newly created/updated resource.</span></span>
    + <span data-ttu-id="c3632-166">Durum kodu istek tarafından döndürülen durumu takip ediyor, önceden sürekli Tamam şeklindeydi.</span><span class="sxs-lookup"><span data-stu-id="c3632-166">The status code follows the status returned by the request, before it was always Ok.</span></span>
  - <span data-ttu-id="c3632-167">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c3632-167">New-AzureRmAutoscaleRule</span></span>
    + <span data-ttu-id="c3632-168">ScaleActionType parametresi genişletildi, artık şu değerleri alıyor: ChangeCount, PercentChangeCount, ExactCount.</span><span class="sxs-lookup"><span data-stu-id="c3632-168">The parameter ScaleActionType has been extended, it receives the following values now: ChangeCount, PercentChangeCount, ExactCount.</span></span>
  - <span data-ttu-id="c3632-169">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c3632-169">Remove-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="c3632-170">Çıktıdaki statusCode, istek tarafından döndürülen statusCode değerini takip ediyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-170">The statusCode in the output follows the statusCode returned by the request.</span></span> <span data-ttu-id="c3632-171">Önceden sürekli Tamam şeklindeydi.</span><span class="sxs-lookup"><span data-stu-id="c3632-171">Before it was always Ok.</span></span>
  - <span data-ttu-id="c3632-172">Get-AzureRMLogProfile</span><span class="sxs-lookup"><span data-stu-id="c3632-172">Get-AzureRMLogProfile</span></span>
    + <span data-ttu-id="c3632-173">Çıktı artık numaralandırılmış alan şeklinde.</span><span class="sxs-lookup"><span data-stu-id="c3632-173">The output is now enumerated.</span></span> <span data-ttu-id="c3632-174">Önceden tek bir nesne olarak kabul ediliyordu.</span><span class="sxs-lookup"><span data-stu-id="c3632-174">Before it was considered a single object.</span></span> <span data-ttu-id="c3632-175">Çıktı türü, daha önce olduğu gibi liste olarak kalıyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-175">The type of the output remains a list as before.</span></span>
  - <span data-ttu-id="c3632-176">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c3632-176">Remove-AzureRmLogProfile</span></span>
    + <span data-ttu-id="c3632-177">PassThru paremetresi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="c3632-177">The PassThru parameter has been implemented.</span></span>
  - <span data-ttu-id="c3632-178">Ölçüm API'si</span><span class="sxs-lookup"><span data-stu-id="c3632-178">Metrics API</span></span>
    + <span data-ttu-id="c3632-179">SDK artık ölçümleri MDM'den alıyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-179">The SDK now retrieves metrics from MDM.</span></span>
  - <span data-ttu-id="c3632-180">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="c3632-180">Get-AzureRmMetricDefinition</span></span>
    + <span data-ttu-id="c3632-181">Çıktı hala bir liste, ancak liste yapısı değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-181">The output is still a list, but the structure of the list changed.</span></span>
  - <span data-ttu-id="c3632-182">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="c3632-182">Get-AzureRmMetric</span></span>
    + <span data-ttu-id="c3632-183">Çağrı değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-183">The call has changed.</span></span> <span data-ttu-id="c3632-184">Yeni sözdizimi şu şekildedir: Get-AzureRmMetric ResourceId [ÖlçümAdları [ZamanDilimi] [ToplamaTürü] [BaşlangıçZamanı] [BitişZamanı]] [AyrıntılıÇıktı]</span><span class="sxs-lookup"><span data-stu-id="c3632-184">This is the new syntax: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span></span>
    + <span data-ttu-id="c3632-185">Çıktı bir liste, ancak öğelerinin yapısı değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="c3632-185">The output is a list, and the structure of its elements has changed.</span></span>
* <span data-ttu-id="c3632-186">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c3632-186">KeyVault</span></span>
  - <span data-ttu-id="c3632-187">KeyVault gizli dizileri için yedekleme/geri yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-187">Adding backup/restore support for KeyVault secrets</span></span>
    + <span data-ttu-id="c3632-188">Gizli diziler yedeklenip geri yüklenebilir, Anahtarlar için desteklenen işlevlerle birlikte kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c3632-188">Secrets can be backed up and restored, matching the functionality currently supported for Keys</span></span>

  - <span data-ttu-id="c3632-189">Anahtarlar ve Gizli Diziler için yedekleme cmdlet'leri artık giriş parametresi için karşılık gelen bir nesneyi kabul ediyor</span><span class="sxs-lookup"><span data-stu-id="c3632-189">Backup cmdlets for Keys and Secrets now accept a corresponding object as an input parameter</span></span>
    + <span data-ttu-id="c3632-190">Çağrıda bulunan alma ve yedekleme işlemlerini bir arada kullanabilir: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c3632-190">The caller may chain retrieval and backup operations: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span></span>

  - <span data-ttu-id="c3632-191">Yedekleme cmdlet'i artık var olan bir dosyanın üzerine yazmak için -Force anahtarı kullanılmasını destekliyor</span><span class="sxs-lookup"><span data-stu-id="c3632-191">Backup cmdlets now support a -Force switch to overwrite an existing file</span></span>
    + <span data-ttu-id="c3632-192">Var olan dosyanın üzerine yazma girişiminin artık işlemi sonlandırmayacağını, kullanıcıya nasıl devam etmek istediğinin sorulacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c3632-192">Note that attempting to overwrite an existing file will no longer throw, and will instead prompt the user for a choice on how to proceed.</span></span>
* <span data-ttu-id="c3632-193">LogicApp</span><span class="sxs-lookup"><span data-stu-id="c3632-193">LogicApp</span></span>
  - <span data-ttu-id="c3632-194">Değişim Denetim Numarası olağanüstü durum kurtarma cmdlet'leri için yeni parametreler:</span><span class="sxs-lookup"><span data-stu-id="c3632-194">New parameters for Interchange Control Number disaster recovery cmdlets:</span></span>
    + <span data-ttu-id="c3632-195">İlgili kontrol numaralarını belirtmek için isteğe bağlı -AgreementType parametresi ("X12" veya "Edifact")</span><span class="sxs-lookup"><span data-stu-id="c3632-195">Optional -AgreementType parameter ("X12", or "Edifact") to specify the relevant control numbers</span></span>
* <span data-ttu-id="c3632-196">MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c3632-196">MachineLearning</span></span>
  - <span data-ttu-id="c3632-197">Yeni Azure Machine Learning .Net SDK'sı sürümü kullanılıyor ve yeni bir cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-197">Consume new version of Azure Machine Learning .Net SDK and add a new cmdlet</span></span>
    + <span data-ttu-id="c3632-198">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="c3632-198">Add-AzureRmMlWebServiceRegionalProperty</span></span>
  - <span data-ttu-id="c3632-199">Yardım metninde küçük metin düzeltmeleri yapıldı.</span><span class="sxs-lookup"><span data-stu-id="c3632-199">Minor wording fixes in help text.</span></span>
* <span data-ttu-id="c3632-200">Ağ</span><span class="sxs-lookup"><span data-stu-id="c3632-200">Network</span></span>
  - <span data-ttu-id="c3632-201">Test-AzureRmNetworkWatcherConnectivity cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-201">Added Test-AzureRmNetworkWatcherConnectivity cmdlet</span></span>
    + <span data-ttu-id="c3632-202">Belirtilen kaynak VM ve hedef için bağlantı durumu bilgilerini döndürür</span><span class="sxs-lookup"><span data-stu-id="c3632-202">Returns connectivity information for a specified source VM and a destination</span></span>
    + <span data-ttu-id="c3632-203">Kaynak ve hedef arasında bağlantı kurulamazsa cmdlet sorunla ilgili ayrıntıları döndürür</span><span class="sxs-lookup"><span data-stu-id="c3632-203">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue</span></span>
* <span data-ttu-id="c3632-204">Profil</span><span class="sxs-lookup"><span data-stu-id="c3632-204">Profile</span></span>
  - <span data-ttu-id="c3632-205">"Send-Feedback" cmdlet'i eklendi: Kullanıcının Azure PowerShell ekibine geri bildirim gönderen komut dizisi başlatmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c3632-205">Added \`Send-Feedback' cmdlet: allows a user to initiate a set of prompts which sends feedback to the Azure PowerShell team.</span></span>
  - <span data-ttu-id="c3632-206">Azure modülündeki var olan cmdlet adlarıyla çakıştığından aşağıdaki diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="c3632-206">The following aliases have been removed as they conflicted with existing cmdlet names in the Azure module:</span></span>
    + <span data-ttu-id="c3632-207">`Enable-AzureDataCollection` (destekleyen: `Enable-AzureRmDataCollection`)</span><span class="sxs-lookup"><span data-stu-id="c3632-207">`Enable-AzureDataCollection` (supported by `Enable-AzureRmDataCollection`)</span></span>
    + <span data-ttu-id="c3632-208">`Disable-AzureDataCollection` (destekleyen: `Disable-AzureRmDataCollection`)</span><span class="sxs-lookup"><span data-stu-id="c3632-208">`Disable-AzureDataCollection` (supported by `Disable-AzureRmDataCollection`)</span></span>
* <span data-ttu-id="c3632-209">Geçiş</span><span class="sxs-lookup"><span data-stu-id="c3632-209">Relay</span></span>
  - <span data-ttu-id="c3632-210">Kullanıcıların Azure Geçişi kaynakları oluşturmasını ve yönetmesini sağlayan Azure Geçişi cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="c3632-210">Adds cmdlets for the Azure Relay which allows users to create and manage all Azure Relay resources.</span></span>
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* <span data-ttu-id="c3632-211">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c3632-211">Resources</span></span>
  - <span data-ttu-id="c3632-212">New-AzureRmResourceGroupDeployment için kaynak grupları arası dağıtım desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-212">Support cross-resource-group deployments for New-AzureRmResourceGroupDeployment</span></span>
    + <span data-ttu-id="c3632-213">Kullanıcılar artık farklı kaynak gruplarında dağıtım yapmak için iç içe geçmiş dağıtımlar kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c3632-213">Users can now use nested deployments to deploy to different resource groups.</span></span>
* <span data-ttu-id="c3632-214">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c3632-214">ServiceBus</span></span>

  - <span data-ttu-id="c3632-215">Hata Düzeltmesi: ServiceBus Kuyruğu nesnesi özellik değerleri null olarak belirlenmişti, nesne Kuyruğu güncelleştirmek için Set-AzureRmServiceBusQueue cmdlet'inde giriş parametresi olarak kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="c3632-215">Bug Fix: ServiceBus Queue object property values were set to null, the object is used as input parameter in Set-AzureRmServiceBusQueue cmdlet to update Queue.</span></span>
   - <span data-ttu-id="c3632-216">Etkilenen özellikler: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount ve MessageCount</span><span class="sxs-lookup"><span data-stu-id="c3632-216">Properties affected are LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount and MessageCount</span></span>
* <span data-ttu-id="c3632-217">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c3632-217">ServiceFabric</span></span>

  - <span data-ttu-id="c3632-218">Service Fabric için cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-218">Added cmdlets for service fabric</span></span>
    + <span data-ttu-id="c3632-219">Add-AzureRmServiceFabricApplicationCertificate       Uygulama sertifikası olarak kullanılacak bir sertifika ekler</span><span class="sxs-lookup"><span data-stu-id="c3632-219">Add-AzureRmServiceFabricApplicationCertificate       Add a certificate which will be used as application certificate</span></span>
    + <span data-ttu-id="c3632-220">Add-AzureRmServiceFabricClientCertificate       Küme ayarlarına istemci kimlik doğrulaması için ortak ad veya parmak izi ekler</span><span class="sxs-lookup"><span data-stu-id="c3632-220">Add-AzureRmServiceFabricClientCertificate       Add a common name or thumbprint to the cluster settings for client authentication</span></span>
    + <span data-ttu-id="c3632-221">Add-AzureRmServiceFabricClusterCertificate       Var olan sertifikaya geçmek için kümeye ikincil küme sertifikası ekler</span><span class="sxs-lookup"><span data-stu-id="c3632-221">Add-AzureRmServiceFabricClusterCertificate       Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span>
    + <span data-ttu-id="c3632-222">Add-AzureRmServiceFabricNodes       Bir kümeye belirli bir düğüm türünde düğümler/VM'ler ekler</span><span class="sxs-lookup"><span data-stu-id="c3632-222">Add-AzureRmServiceFabricNodes       Add nodes/VMs of a specific node type to a cluster</span></span>
    + <span data-ttu-id="c3632-223">Add-AzureRmServiceFabricNodeType       Var olan bir kümeye düğüm türü/VM'ler ekler</span><span class="sxs-lookup"><span data-stu-id="c3632-223">Add-AzureRmServiceFabricNodeType       Add a node type/VMs to an existing cluster</span></span>
    + <span data-ttu-id="c3632-224">Get-AzureRmServiceFabricCluster       Küme kaynağının ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="c3632-224">Get-AzureRmServiceFabricCluster       Get the details of the cluster resource</span></span>
    + <span data-ttu-id="c3632-225">New-AzureRmServiceFabricCluster Yeni bir ServiceFabric kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3632-225">New-AzureRmServiceFabricCluster Create a new ServiceFabric cluster.</span></span> <span data-ttu-id="c3632-226">Bu komut farklı senaryoları kapsayacak şekilde kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="c3632-226">This command has many overloads to cover various scenarios</span></span>
    + <span data-ttu-id="c3632-227">Remove-AzureRmServiceFabricClientCertificate       Bir kümeye erişmek için kullanılan bir istemci sertifikasını engeller</span><span class="sxs-lookup"><span data-stu-id="c3632-227">Remove-AzureRmServiceFabricClientCertificate       Remove a client certificate from being used to access a cluster</span></span>
    + <span data-ttu-id="c3632-228">Remove-AzureRmServiceFabricClusterCertificate       Bir kümenin güvenliği için kullanılan bir küme sertifikasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c3632-228">Remove-AzureRmServiceFabricClusterCertificate       Remove a cluster certificate from being used for cluster security</span></span>
    + <span data-ttu-id="c3632-229">Remove-AzureRmServiceFabricNodes       Bir kümede yer alan belirli türdeki düğümleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="c3632-229">Remove-AzureRmServiceFabricNodes       Remove nodes from a specific node type from a cluster</span></span>
    + <span data-ttu-id="c3632-230">Remove-AzureRmServiceFabricNodeType       Bir kümedeki düğüm türünü kaldırır</span><span class="sxs-lookup"><span data-stu-id="c3632-230">Remove-AzureRmServiceFabricNodeType       Remove a node type from a cluster</span></span>
    + <span data-ttu-id="c3632-231">Remove-AzureRmServiceFabricSettings       Bir kümeden bir veya daha fazla ServiceFabric ayarını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c3632-231">Remove-AzureRmServiceFabricSettings       Remove one or more ServiceFabric settings from a cluster</span></span>
    + <span data-ttu-id="c3632-232">Set-AzureRmServiceFabricSettings       Bir kümeye bir veya daha fazla ServiceFabric ayarı ekler veya var olan ayarları güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c3632-232">Set-AzureRmServiceFabricSettings       Add or update one or more ServiceFabric settings of a cluster</span></span>
    + <span data-ttu-id="c3632-233">Set-AzureRmServiceFabricUpgradeType       Bir kümenin ServiceFabric yükseltme türünü değiştirir</span><span class="sxs-lookup"><span data-stu-id="c3632-233">Set-AzureRmServiceFabricUpgradeType       Change the ServiceFabric upgrade type of a cluster</span></span>
    + <span data-ttu-id="c3632-234">Update-AzureRmServiceFabricDurability       Bir kümenin dayanıklılık katmanını değiştirir</span><span class="sxs-lookup"><span data-stu-id="c3632-234">Update-AzureRmServiceFabricDurability       Change the durability tier of a cluster</span></span>
    + <span data-ttu-id="c3632-235">Update-AzureRmServiceFabricReliability       Bir kümenin güvenilirlik katmanını değiştirir</span><span class="sxs-lookup"><span data-stu-id="c3632-235">Update-AzureRmServiceFabricReliability       Change the reliability tier of a cluster</span></span>
* <span data-ttu-id="c3632-236">Sql</span><span class="sxs-lookup"><span data-stu-id="c3632-236">Sql</span></span>
  - <span data-ttu-id="c3632-237">New-AzureRmSqlDatabase cmdlet'ine Added -SampleName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-237">Added -SampleName parameter to New-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="c3632-238">Yük Devretme Grubu cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c3632-238">Updates to Failover Group cmdlets</span></span>
  - <span data-ttu-id="c3632-239">"Etiket" parametreleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c3632-239">Remove 'Tag' parameters</span></span>
  - <span data-ttu-id="c3632-240">Remove-AzureRmSqlDatabaseFailoverGroup cmdlet'inden "PartnerResourceGroupName" ve "PartnerServerName" parametreleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c3632-240">Remove 'PartnerResourceGroupName' and 'PartnerServerName' parameters from Remove-AzureRmSqlDatabaseFailoverGroup cmdlet</span></span>
  - <span data-ttu-id="c3632-241">New- ve Set- cmdlet'lerine "GracePeriodWithDataLossHours" paremetresi eklendi, "GracePeriodWithDataLossHour" parametresinin yerini alması planlanıyor</span><span class="sxs-lookup"><span data-stu-id="c3632-241">Add 'GracePeriodWithDataLossHours' parameter to New- and Set- cmdlets, which shall eventually replace 'GracePeriodWithDataLossHour'</span></span>
  - <span data-ttu-id="c3632-242">Belgeler gözden geçirildi ve güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="c3632-242">Documentation has been fleshed out and updated</span></span>
  - <span data-ttu-id="c3632-243">Geri döndürülen nesnelerin biçimi değiştirildi ve alanların doldurulmadığı bazı hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-243">Change formatting of returned objects and fix some bugs where fields were not always populated</span></span>
  - <span data-ttu-id="c3632-244">Yük Devretme Grubu nesnesine "DatabaseNames" ve "PartnerLocation" özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-244">Add 'DatabaseNames' and 'PartnerLocation' properties to Failover Group object</span></span>
  - <span data-ttu-id="c3632-245">Switch- cmdlet'inin işlemin tamamlanmasını beklemek yerine hemen sonuç döndürmesine neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-245">Fix bug causing Switch- cmdlet to return immediately rather than waiting for operation to complete</span></span>
  - <span data-ttu-id="c3632-246">Yüksek yetkisiz kullanım süresi değerleri kullanıldığında ortaya çıkan tamsayı taşma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-246">Fix integer overflow bug when high grace period values are used</span></span>
  - <span data-ttu-id="c3632-247">Daha düşük bir değer girildiğinde yetkisiz kullanım süresi en az 1 saat olacak şekilde ayarlandı</span><span class="sxs-lookup"><span data-stu-id="c3632-247">Adjust grace period to a minimum of 1 hour if a lower one is provided</span></span>
  - <span data-ttu-id="c3632-248">Set-AzureRmSqlDatabaseThreatDetectionPolicy ve Set-AzureRmSqlServerThreatDetectionPolicy cmdlet'lerinin "ExcludedDetectionType" parametresinin kabul edilen değerlerinden "Usage_Anomaly" kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c3632-248">Remove "Usage_Anomaly" from the accepted values for "ExcludedDetectionType" parameter of Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet and Set-AzureRmSqlServerThreatDetectionPolicy cmdlet.</span></span>
* <span data-ttu-id="c3632-249">Depolama</span><span class="sxs-lookup"><span data-stu-id="c3632-249">Storage</span></span>
  - <span data-ttu-id="c3632-250">SRP SDK'sı 6.3.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-250">Upgrade SRP SDK to 6.3.0</span></span>
  - <span data-ttu-id="c3632-251">New/Set-AzureRmStorageAccount: EnableHttpsTrafficOnly desteği için yeni bir parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-251">New/Set-AzureRmStorageAccount:Add a new parameter to support EnableHttpsTrafficOnly</span></span>
  - <span data-ttu-id="c3632-252">New/Set/Get-AzureRmStorageAccount: Döndürülen Depolama Hesabı artık yeni EnableHttpsTrafficOnly özniteliğini içeriyor</span><span class="sxs-lookup"><span data-stu-id="c3632-252">New/Set/Get-AzureRmStorageAccount: Returned Storage Account contains a new attribute EnableHttpsTrafficOnly</span></span>
* <span data-ttu-id="c3632-253">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="c3632-253">Azure.Storage</span></span>
  - <span data-ttu-id="c3632-254">Azure Depolama İstemci Kitaplığı 8.1.1 ve Azure Depolama Veri Taşıma Kitaplığı 0.5.1 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="c3632-254">Upgrade to Azure Storage Client Library 8.1.1 and Azure Storage DataMovement Library 0.5.1</span></span>
  - <span data-ttu-id="c3632-255">Blob Artımlı Kopya özelliğini desteklemek için yeni bir cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="c3632-255">Add a new cmdlet to support blob Incremental Copy feature</span></span>
