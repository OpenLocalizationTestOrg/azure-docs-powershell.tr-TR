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
ms.date: 11/14/2017
ms.openlocfilehash: cf58789ba69fd2fc157e37d0b052827b361246e5
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2017
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="20171208-version-511"></a>2017.12.08 Sürüm 5.1.1
* AnalysisServices
    - Tüm bulutların desteklenmesi için konum kümesini doğrulama, dinamik arama olarak değiştirildi.
* Otomasyon
    - Import-AzureRMAutomationRunbook güncelleştirmesi
        - Artık Python2 runbook’ları için destek sağlanmaktadır
* Batch
    - Bir kaynak grubu olmayan hesap işlemlerinin kaynak grubunu otomatik olarak algılayamadığı bir hata düzeltildi
* İşlem
    - Get-AzureRmComputeResourceSku, bölge bilgilerini gösterir.
    - https://github.com/Azure/azure-powershell/issues/5038 sorununu düzeltmek için Disable-AzureRmVmssDiskEncryption güncelleştirildi
    - Uzun süre çalışan İşlem cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
        - Etkilenen cmdlet’ler şunları içerir: Sanal Makineler ve Sanal Makine Ölçek Kümeleri için New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlet’leri
    - New-AzureRmVM cmdlet’ine akıllı varsayılanları kullanarak bir Sanal Makine ve tüm gerekli kaynakları oluşturan basitleştirilmiş parametre kümesi eklendi
* ContainerInstance
    - Azure Container Instance SDK’sı uygulama 2017-10-01
        - Kapsayıcıyı tamamlanana kadar çalıştırma desteği
        - Azure Dosya birimi bağlama desteği
        - Ortak IP için birden çok bağlantı noktası açma desteği
* ContainerRegistry
    - Coğrafi çoğaltma ve web kancaları için yeni cmdlet’ler
        - Get/New/Remove-AzureRmContainerRegistryReplication
        - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - Kimlik bilgisi şifreleme işlevi artık "Uzaktan Erişim" etkinken (Ağ Üzerinden) ve "Uzaktan Erişim" devre dışıyken (Yerel Makine) çalışır.
* DataFactoryV2
    - İki yeni cmdlet eklendi: Update-AzureRmDataFactoryV2 ve Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
    - Submit-AzureRmDataLakeAnalyticsJob’a ScriptParameter adlı bir parametre eklendi
        - ScriptParameter hakkında daha ayrıntılı bilgiye Submit-AzureRmDataLakeAnalyticsJob üzerinde Get-Help kullanarak ulaşabilirsiniz
    - New-AzureRmDataLakeAnalyticsAccount için, MaxDegreeOfParallelism parametresi MaxAnalyticsUnits olarak değiştirildi
        - MaxAnalyticsUnits parametresi için bir diğer ad eklendi: MaxDegreeOfParallelism
    - New-AzureRmDataLakeAnalyticsComputePolicy için, MaxDegreeOfParallelismPerJob parametresi MaxAnalyticsUnitsPerJob olarak değiştirildi
        - MaxAnalyticsUnitsPerJob parametresi için bir diğer ad eklendi: MaxDegreeOfParallelismPerJob
    - Set-AzureRmDataLakeAnalyticsAccount için, MaxDegreeOfParallelism parametresi MaxAnalyticsUnits olarak değiştirildi
        - MaxAnalyticsUnits parametresi için bir diğer ad eklendi: MaxDegreeOfParallelism
    - Submit-AzureRmDataLakeAnalyticsJob için, DegreeOfParallelism parametresi AnalyticsUnits olarak değiştirildi
        - AnalyticsUnits parametresi için bir diğer ad eklendi: DegreeOfParallelism
    - Update-AzureRmDataLakeAnalyticsComputePolicy için, MaxDegreeOfParallelismPerJob parametresi MaxAnalyticsUnitsPerJob olarak değiştirildi
        - MaxAnalyticsUnitsPerJob parametresi için bir diğer ad eklendi: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
    - Set-AzureRmMlOpCluster ekleme
        - Kümenin aracı sayısını veya SSL yapılandırmasını güncelleştirme
    - Orchestrator özellikleri isteğe bağlıdır
        - Bir hizmet sorumlusu sağlanmadıysa servis tarafından oluşturulur ve bu nedenle düzenleyici özellikleri artık isteğe bağlıdır
* PowerBIEmbedded
    - Power BI Embedded Kapasite cmdlet’leri için destek eklendi
    - Yeni Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesinin ayrıntılarını alır.
    - Yeni Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Yeni bir PowerBI Embedded Kapasitesi oluşturur
    - Yeni Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini siler
    - Yeni Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini sürdürür
    - Yeni Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini askıya alır
    - Yeni Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğinin varlığını test eder
    - Yeni Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini değiştirir
* Profil
    - USGovernmentActiveDirectoryEndpoint, https://login.microsoftonline.us/ olarak güncelleştirildi
        - Azure Kamu uç nokta eşlemeleri hakında daha fazla bilgi için bkz. https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - Cmdlet’ler için -AsJob desteği eklenerek seçilen cmdlet’lerin arka planda yürütülmesi ve ilerlemeyi izleyip denetlemek için bir iş döndürmesine olanak sağlandı
    - Get-AzureRmSubscription cmdlet’ine -AsJob parametresi eklendi
* RecoveryServices.Backup
    - Hata düzeltildi - Get-AzureRmRecoveryServicesBackupItem, kapsayıcı adı filtresi için büyük küçük harf duyarsız karşılaştırma yapar.
    - Hata düzeltildi - AzureVmItem, artık bir yedekleme işleminin en son gerçekleştirildiği zamanı gösteren bir özelliğe sahip: LastBackupTime.
* Kaynaklar
    - Get-AzureRMRoleAssignment’ın özel roller için roledefiniton adı olmayan atamalarla sonuçlandığı bir hata düzeltildi
        - Kullanıcılar artık rol türünden bağımsız olarak roledefinition adları olan atamalar ile Get-AzureRMRoleAssignment kullanabilir
    - Set-AzureRMRoleRoleDefinition’ın assignablescopes içinde yeni bir kapsam olduğunda RD bulunamadı hatası vermesine neden olan sorun düzeltildi
        - Kullanıcılar artık kapsamın konumundan bağımsız olarak yeni kapsamlar dahil atanabilir kapsamlar ile Set-AzureRMRoleRoleDefinition kullanabilir
    - Kapsamların "/" ile bitmesine olanak sağlandı
        - Kullanıcılar artık API ve CLI ile tutarlı olarak "/" ile biten kapsamlarda RoleDefinition ve RoleAssignment commandlet’lerini kullanabilir
    - Kullanıcıların temsilci bayrağı kullanarak RoleAssignment oluşturmasına olanak sağlandı
        - Kullanıcılar artık temsilci bayrağı ekleme seçeneğiyle New-AzureRMRoleAssignment kullanabilir
    - RoleAssignment kapsam parametresine uyacak şekilde düzeltildi
    - New-AzureRmRoleAssignment Commandlet’inde ServicePrincipalName için bir diğer ad eklendi
        - Kullanıcılar artık New-AzureRmRoleAssignment commandlet’ini kullanırken ServicePrincipalName yerine ApplicationId kullanabilir
* SiteRecovery
    - Büyük değişiklikler içeren bir sonraki sürüme hazırlık olarak bu modüldeki tüm cmdlet’ler için kullanımdan kaldırılma uyarıları eklendi.
        - Cmdlet’lerinizi AzureRM’den geçirme hakkında daha fazla bilgi için yakında sunulacak olan büyük değişikliklere ilişkin kılavuza bakın.
* Sql
    - Set-AzureRmSqlDatabase kullanarak veritabanını yeniden adlandırma özelliği eklendi
    - Sorun düzeltildi: https://github.com/Azure/azure-powershell/issues/4974
        - Denetim cmdlet’leri için geçersiz AUDIT_CHANGED_GROUP değeri sağlamak artık hata oluşturmuyor ve gelecek bir sürümde kaldırılacak.
    - Sorun düzeltildi: https://github.com/Azure/azure-powershell/issues/5046
        - Denetim cmdlet’lerinde AuditAction parametresi artık yok sayılmıyor
    - Denetim cmdlet’lerinde 'Secondary' StorageKeyType sağlandığında oluşan bir hata düzeltildi
        - Blob denetimi ayarlanırken, StorageKeyType parametresi için 'Secondary' değeri sağlandığında ikincil anahtar yerine birincil depolama hesabı anahtarı kullanılıyordu.
    - Set-AzureRmSqlServerTransparentDataEncryptionProtector onay iletisi ifadesi değiştirildi
* Azure (RDFE)
    - Tüm RemoteApp Cmdlet’leri kaldırıldı
* Azure Depolama
    - Azure Depolama İstemci Kitaplığı 8.6.0 ve Azure Depolama DataMovement Kitaplığı 0.6.5 sürümüne yükseltildi

Son sürümden sonraki değişiklikler: Son sürümden sonraki değişiklikler:  https://github.com/azure/azure-powershell/compare/v5.0.1-November2017...v5.1.1-December2017

## <a name="20171110-version-501"></a>2017.11.10 Sürüm 5.0.1
* Aşağıdaki modüller çalıştırılırken bazı cmdlet'lerin başarısız olmasına neden olan bütünleştirilmiş kod yükleme sorunu düzeltildi:
    - AzureRM.ApiManagement
    - AzureRM.Backup
    - AzureRM.Batch
    - AzureRM.Compute
    - AzureRM.DataFactories
    - AzureRM.HDInsight
    - AzureRM.KeyVault
    - AzureRM.RecoveryServices
    - AzureRM.RecoveryServices.Backup
    - AzureRM.RecoveryServices.SiteRecovery
    - AzureRM.RedisCache
    - AzureRM.SiteRecovery
    - AzureRM.Sql
    - AzureRM.Storage
    - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.8 - Sürüm 5.0.0
* Not: Bu bir önemli değişiklik yayınıdır. Sunulan önemli değişikliklerin tam listesi için lütfen geçiş kılavuzuna (https://aka.ms/azps-migration-guide) bakın.
* AzureRM’deki tüm cmdlet'ler artık çevrimiçi yardımı destekler
    - Çevrimiçi yardımı varsayılan İnternet tarayıcınızda açmak için Get-Help komutunu -Online parametresiyle birlikte çalıştırın
* AnalysisServices
    * Synchronize-AzureAsInstance komutu düzeltildi ve eşitleme için yeni AsAzure REST API’si ile çalışması sağlandı
* ApiManagement
    * Bu yayında ApiManagement’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
    * https://github.com/Azure/azure-powershell/issues/4510 sorununu düzeltmek için Get-AzureRmApiManagementUser Cmdlet’i güncelleştirildi
    * Boş Yolu olan Api oluşturmak için New-AzureRmApiManagementApi Cmdlet’i güncelleştirildi https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
    * Application Insights kaynağını alma/oluşturma/kaldırma komutları eklendi
        - Get-AzureRmApplicationInsights
        - New-AzureRmApplicationInsights
        - Remove-AzureRmApplicationInsights
    * Application Insights kaynağının fiyatlandırmasını/günlük sınırını alma/güncelleştirme komutları eklendi
        - Get-AzureRmApplicationInsights -IncludeDailyCap
        - Set-AzureRmApplicationInsightsPricingPlan
        - Set-AzureRmApplicationInsightsDailyCap
    * Application Insights kaynağının sürekli dışarı aktarma işlemini alma/oluşturma/güncelleştirme/kaldırma komutları eklendi
        - Get-AzureRmApplicationInsightsContinuousExport
        - Set-AzureRmApplicationInsightsContinuousExport
        - New-AzureRmApplicationInsightsContinuousExport
        - Remove-AzureRmApplicationInsightsContinuousExport
    * Application Insights kaynağı api anahtarlarını alma/oluşturma/kaldırma komutları eklendi
        - Get-AzureRmApplicationInsightsApiKey
        - New-AzureRmApplicationInsightsApiKey
        - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
    * `New-AzureRmBatchAccount` içine yeni parametreler eklendi.
        - `PoolAllocationMode`: Batch hesabında havuz oluşturmak için kullanılacak ayırma modu. Kullanıcının aboneliğindeki havuz düğümlerini ayıran bir Batch hesabı oluşturmak için bu ayarı `UserSubscription` olarak belirleyin.
        - `KeyVaultId`: Batch hesabıyla ilişkili Azure anahtar kasasının kaynak kimliği.
        - `KeyVaultUrl`: Batch hesabıyla ilişkili Azure anahtar kasasının URL’si.
    * Parametreler `New-AzureBatchTask` olarak güncelleştirildi.
        - `RunElevated` anahtarı kaldırıldı. `RunElevated` parametresi kaldırılıp bunun yerine `UserIdentity` parametresi eklendi. Eşdeğer bir davranış aşağıda gösterildiği gibi bir `PSUserIdentity` oluşturularak elde edilebilir:
            - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Görev", "Yönetici")
            - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
        - `AuthenticationTokenSettings` parametresi eklendi. Bu parametre Batch hizmetinden çalıştığında, göreve bir kimlik doğrulama belirteci sağlamasını istemenize olanak tanır ve Batch hizmetine istek göndermek için göreve Batch hesap anahtarlarını geçirme gereksinimini ortadan kaldırır.
        - `ContainerSettings` parametresi eklendi.
            - Bu parametre, Batch hizmetinin görevi bir kapsayıcı içinde çalıştırmasını istemenize olanak tanır.
        - `OutputFiles` parametresi eklendi.
            - Bu parametre, görevi tamamlandıktan sonra dosyaları Azure Depolama’ya yükleyecek şekilde yapılandırmanıza olanak tanır.
    * Parametreler `New-AzureBatchPool` olarak güncelleştirildi.
        - `UserAccounts` parametresi eklendi.
            - Bu parametre, havuzdaki her düğümde oluşturulan kullanıcı hesaplarını tanımlar.
        - `TargetLowPriorityComputeNodes` eklendi ve `TargetDedicated` olan ad, `TargetDedicatedComputeNodes` olarak değiştirildi.
            - `TargetDedicatedComputeNodes` parametresi için bir `TargetDedicated` diğer adı oluşturuldu.
        - `NetworkConfiguration` parametresi eklendi.
            - Bu parametre, havuz ağ ayarlarını yapılandırmanıza olanak sağlar.
    * Parametreler `New-AzureBatchCertificate` olarak güncelleştirildi.
        - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
    * Parametreler `New-AzureBatchComputeNodeUser` olarak güncelleştirildi.
        - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
    * Parametreler `Set-AzureBatchComputeNodeUser` olarak güncelleştirildi.
        - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
    * `Name` parametresi `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` ve `Remove-AzureBatchNodeFile` üzerinde `Path` olarak yeniden adlandırıldı.
        - `Path` parametresi için bir `Name` diğer adı oluşturuldu.
    * Nesnelerde yapılan değişiklikler
        - Lütfen tam liste için Batch değişiklik günlüğüne bakın
    * Azure Active Directory tabanlı kimlik doğrulaması için destek eklendi.
        - Azure Active Directory kimlik doğrulamasını kullanmak için `Get-AzureRmBatchAccount` cmdlet'ini kullanarak bir `BatchAccountContext` nesnesi alın ve bu `BatchAccountContext` değerini bir Batch hizmeti cmdlet’inin `-BatchContext` parametresine ekleyin. Azure Active Directory kimlik doğrulaması, `PoolAllocationMode = UserSubscription` özelliğine sahip hesaplar için zorunludur.
        - Mevcut hesaplar veya `PoolAllocationMode = BatchService` ile oluşturulan yeni hesaplar için, `Get-AzureRmBatchAccoutKeys` cmdlet'i ile bir `BatchAccountContext` nesnesi alarak paylaşılan anahtar kimlik doğrulamasını kullanmaya devam edebilirsiniz.
* İşlem
    * Azure Disk Şifrelemesi Uzantı Komutları
        - Yeni 'Set-AzureRmVmDiskEncryptionExtension' Parametresi olan '-EncryptFormatAll' biçim veri disklerini şifreler
        - Yeni 'Set-AzureRmVmDiskEncryptionExtension' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
        - Yeni 'Disable-AzureRmVmDiskEncryption' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
        - Yeni 'Get-AzureRmVmDiskEncryptionStatus' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
* DataLakeAnalytics
    * Bu yayında DataLakeAnalytics’te yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
    * İki Get-AzureRmDataLakeAnalyticsAccount OutputTypes seçeneğinden biri değiştirildi
        - List\<DataLakeAnalyticsAccount> - List\<PSDataLakeAnalyticsAccountBasic>
        - PSDataLakeAnalyticsAccountBasic özellikleri, DataLakeAnalyticsAccount özelliklerinin katı bir alt kümesidir
        - DataLakeAnalyticsAccount içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSDataLakeAnalyticsAccountBasic içindedir, ancak Eski olarak etiketlenir.
    * İki Get-AzureRmDataLakeAnalyticsJob OutputTypes seçeneğinden biri değiştirildi
        - List\<JobInformation> - List\<PSJobInformationBasic>
        - PSJobInformationBasic özellikleri, JobInformation özelliklerinin katı bir alt kümesidir
        - JobInformation içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSJobInformationBasic içindedir, ancak Eski olarak etiketlenir.
* DataLakeStore
    * Bu yayında DataLakeStore’da yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
    * İki Get-AzureRmDataLakeStoreAccount OutputTypes seçeneğinden biri değiştirildi
        - List\<PSDataLakeStoreAccount> - List\<PSDataLakeStoreAccountBasic>
        - PSDataLakeStoreAccountBasic özellikleri, PSDataLakeStoreAccount özelliklerinin katı bir alt kümesidir
        - PSDataLakeStoreAccount içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSDataLakeStoreAccountBasic içindedir, ancak Eski olarak etiketlenir.
* Dns
    * Azure DNS'de CAA kayıt türleri desteği
       - CAA kayıt türündeki tüm işlemleri destekler
* EventHub
    * Bu yayında EventHub’da yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Insights
    * Bu yayında Insights’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Ağ
    * Bu yayında Network’te yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
    * Belirtilen bir Azure bölgesi için kullanılabilir internet hizmet sağlayıcılarını listelemeyi sağlayan cmdlet eklendi
        - Get-AzureRmNetworkWatcherReachabilityProvidersList
    * Belirtilen bir konumdan Azure bölgelerine internet hizmet sağlayıcılarının göreli gecikme puanını almayı sağlayan cmdlet eklendi
        - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
    - Set-AzureRmDefault
        - Varsayılan kaynak grubunu ayarlamak için bu cmdlet'i kullanın.  Bunun yapılması, bazı cmdlet’ler için -ResourceGroup parametresini isteğe bağlı hale getirir ve varsayılan bir grup belirtilmediğinde varsayılan seçeneği kullanır
        - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
        - Belirtilen kaynak grubu abonelikte mevcutsa, bu kaynak grubu varsayılan olarak ayarlanır.  Aksi halde, kaynak grubu oluşturulur ve sonra varsayılan olarak ayarlanır.
    - Get-AzureRmDefault
        - Geçerli varsayılan kaynak grubunu (ve gelecekteki diğer varsayılanları) almak için bu cmdlet'i kullanın.
        - ```Get-AzureRmDefault -ResourceGroup```
    - Clear-AzureRmDefault
        - Geçerli varsayılan kaynak grubunu kaldırmak için bu cmdlet'i kullanın
        - ```Clear-AzureRmDefault -ResourceGroup```
    - Add-AzureRmEnvironment ve Set-AzureRmEnvironment
        - Batch hizmeti için kimlik doğrulama belirteçleri alırken kullanılacak Azure Batch Active Directory hedef kitlesini belirtmenize olanak tanıyan BatchAudience parametresini ekleyin.
* RecoveryServices.Backup
    * Anlık dosya kurtarmayı gerçekleştirmeyi sağlayan cmdlet'ler eklendi.
        - Get-AzureRmRecoveryServicesBackupRPMountScript
        - Disable-AzureRmRecoveryServicesBackupRPMountScript
    * RecoveryServices.Backup SDK’sı en son sürüme güncelleştirildi
    * Azure VM iş yüküne yönelik testler, test çalıştırmaları için gereken tüm ayarlar testler tarafından yapılacak şekilde güncelleştirildi.
    * Düzeltmeler https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
    * ASR VMware için Azure Site Recovery’de yapılan değişiklikler (cmdlet’ler şu anda Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure arasındaki işlemleri desteklemektedir)
        - New-AzureRmRecoveryServicesAsrPolicy
        - New-AzureRmRecoveryServicesAsrProtectedItem
        - Update-AzureRmRecoveryServicesAsrPolicy
        - Update-AzureRmRecoveryServicesAsrProtectionDirection
    * AAD tabanlı kasa desteği eklendi
    * VCenter kaynaklarını yönetmeyi sağlayan cmdlet’ler eklendi
        - Get-AzureRmRecoveryServicesAsrVCenter
        - New-AzureRmRecoveryServicesAsrVCenter
        - Remove-AzureRmRecoveryServicesAsrVCenter
        - Update-AzureRmRecoveryServicesAsrVCenter
    * Diğer cmdlet'ler eklendi
        - Get-AzureRmRecoveryServicesAsrAlertSetting
        - Get-AzureRmRecoveryServicesAsrEvent
        - New-AzureRmRecoveryServicesAsrProtectableItem
        - Set-AzureRmRecoveryServicesAsrAlertSetting
        - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
        - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
        - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
        - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
    - Bu yayında ServiceBus’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Sql
    * Veritabanındaki zaman uyumsuz updateslo işlemini listeleme ve iptal etme desteği eklendi
        - Mevcut Get-AzureRmSqlDatabaseActivity cmdlet’i DB updateslo işlem durumunu döndürecek şekilde güncelleştirildi.
        - Veritabanında zaman uyumsuz updateslo işlemini iptal etmeyi sağlayan yeni Stop-AzureRmSqlDatabaseActivity cmdlet’i eklendi.
    * Veritabanları ve elastik havuzlar için Bölge Artıklığı desteği eklendi
        - New-AzureRmSqlDatabase cmdlet’ine ZoneRedundant anahtar parametresi eklendi
        - Set-AzureRmSqlDatabase cmdlet’ine ZoneRedundant anahtar parametresi eklendi
        - New-AzureRmSqlElasticPool cmdlet’ine ZoneRedundant anahtar parametresi eklendi
        - Set-AzureRmSqlElasticPool cmdlet’ine ZoneRedundant anahtar parametresi eklendi
    * Sunucu DNS Diğer Adları için destek eklendi
        - Sunucu ve diğer ada göre sunucu dns diğer adlarını ya da bir Azure Sql Server’a ait sunucu dns diğer adlarının listesini alan Get-AzureRmSqlServerDnsAlias cmdlet’i eklendi.
        - Belirli bir Azure Sql Server için yeni sunucu dns diğer adları oluşturan New-AzureRmSqlServerDnsAlias cmdlet’i eklendi
        - Sunucu dns diğer adlarının işaret ettiği bir Azure Sql Server’ı güncelleştirmeye olanak tanıyan Set-AzurermSqlServerDnsAlias cmdlet’i eklendi
        - Azure Sql Server için sunucu dns diğer adını kaldıran Remove-AzureRmSqlServerDnsAlias cmdlet’i eklendi
* Azure Depolama
    * Azure Depolama İstemci Kitaplığı 8.5.0 ve Azure Depolama DataMovement Kitaplığı 0.6.3 sürümüne yükseltildi
    * Dosya Paylaşımı Anlık Görüntüsü Destek Özelliği eklendi
        - Get-AzureStorageShare cmdlet’ine 'SnapshotTime' parametresi eklendi
        - Remove-AzureStorageShare cmdlet’ine 'IncludeAllSnapshot' parametresi eklendi
