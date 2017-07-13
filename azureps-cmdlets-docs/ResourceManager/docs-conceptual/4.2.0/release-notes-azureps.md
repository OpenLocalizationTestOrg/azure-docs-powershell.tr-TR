---
title: "Azure PowerShell Değişiklik Günlüğü | Microsoft Docs"
description: "Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-resource-manager
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5c8fa2a5a8f94cd24b66f42c237749a7b89af3b3
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="version-400"></a>Sürüm 4.0.0

* Bu sürüm önemli değişiklikler içerir. Değişikliklerle ilgili ayrıntılar ve var olan betikler üzerindeki etkileri için lütfen [geçiş kılavuzuna](https://aka.ms/azps-migration-guide) bakın.
* ApiManagement
  - New-AzureRmApiManagementGroup cmdlet'inde harici grupların yapılandırılması için destek eklendi.
* Faturalandırma
  - Yeni Get-AzureRmBillingPeriod
    + cmdlet'i ile aboneliğin Azure faturalandırma dönemlerini alabilirsiniz.
  - Get-AzureRmBillingInvoice cmdlet'i güncelleştirildi
  - Yeni özellik: BillingPeriodNames
  - Liste görünümünde çıktı
* İşlem
  - Set-AzureRmVMAEMExtension ve Test-AzureRmVMAEMExtension cmdlet'leri Premium yönetilen diskleri destekleyecek şekilde güncelleştirildi
  - IaaS VM'leri için şifreleme ayarlarının yedeklenmesi ve hata durumunda geri yüklenmesi
  - ChefServiceInterval seçeneğinin adı ChefDaemonInterval olarak değiştirildi. Ancak eskisi de çalışmaya devam ediyor.
  - PS VM nesnesinden yinelenen DataDiskNames ve NetworkInterfaceIDs özellikleri kaldırıldı.
  - Remove-AzureRmVMDataDisk ve Remove-AzureRmVMNetworkInterface cmdlet'lerindeki Make DataDiskNames ve NetworkInterfaceIDs parametreleri isteğe bağlı hale getirildi.
  - Get cmdlet'leri liste nesnesi döndürdüğünde karşılaşılan kanal sorunu düzeltildi.
  - RDFE cmdlet'leriyle çakışan cmdlet'ler yeniden adlandırıldı. Daha fazla bilgi için bkz. https://github.com/Azure/azure-powershell/issues/2917
    + `New-AzureVMSqlServerAutoBackupConfig`, `New-AzureRmVMSqlServerAutoBackupConfig` olarak yeniden adlandırıldı
    + `New-AzureVMSqlServerAutoPatchingConfig`, `New-AzureRmVMSqlServerAutoPatchingConfig` olarak yeniden adlandırıldı
    + `New-AzureVMSqlServerKeyVaultCredentialConfig`, `New-AzureRmVMSqlServerKeyVaultCredentialConfig` olarak yeniden adlandırıldı
* Tüketim
  - Yeni cmdlet: Get-AzureRmConsumptionUsageDetail
    + Abonelik kullanım ayrıntılarını alma cmdlet'i.
* ContainerRegistry
  - Azure Container Registry için PowerShell cmdlet'leri eklendi
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Katalog paketleri için alma ve listeleme desteği eklendi
  - Aşağıdaki katalog öğeleri için daha üst öğelerden listeleme desteği eklendi:
    + Tablo
    + TVF
    + Görünüm
    + İstatistikler
* DataLakeStore
  - Performansı artırmak için `Import-AzureRMDataLakeStoreItem` ve `Export-AzureRMDataLakeStoreItem` için izleme günlüğü varsayılan olarak devre dışı bırakıldı. İzleme günlüğünden faydalanmak isterseniz lütfen `-DiagnosticLogLevel` ve `-DiagnosticLogPath` parametrelerini kullanın
  - Bazen ADLS'ye çok sayıda küçük dosya yüklerken PowerShell'in çökmesine neden olan bir hata düzeltildi.
* EventHub
  - Hata düzeltmesi:
    + Set-AzureRmEventHubNamespace cmdlet'inin "Tier" null olamaz, "SkuName" olmalı hatası için düzeltme
    + Set-AzureRmEventHub - EventHub güncelleştirilirken karşılaşılan "Nesne başvurusu bir nesnenin örneğine ayarlanmadı" hatası düzeltildi
* Insights
  - Add-AzureRm*AlertRule
    + Tek bir nesne döndürür: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Çıktı artık tek bir nesne yerine numaralandırılmış alan şeklinde. Türü değişmedi, yine bir liste.
  - Remove-AzureRmAlertRule
    + statusCode, istek tarafından döndürülen durum kodunu takip ediyor, önceden sürekli Tamam şeklindeydi.
  - Add-AzureRmAutoscaleSetting
    + Artık statusCode, requestId ve yeni oluşturulan/güncelleştirilen kaynağı içeren tek bir nesne (eskisi gibi liste değil) döndürüyor.
    + Durum kodu istek tarafından döndürülen durumu takip ediyor, önceden sürekli Tamam şeklindeydi.
  - New-AzureRmAutoscaleRule
    + ScaleActionType parametresi genişletildi, artık şu değerleri alıyor: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + Çıktıdaki statusCode, istek tarafından döndürülen statusCode değerini takip ediyor. Önceden sürekli Tamam şeklindeydi.
  - Get-AzureRMLogProfile
    + Çıktı artık numaralandırılmış alan şeklinde. Önceden tek bir nesne olarak kabul ediliyordu. Çıktı türü, daha önce olduğu gibi liste olarak kalıyor.
  - Remove-AzureRmLogProfile
    + PassThru paremetresi uygulandı.
  - Ölçüm API'si
    + SDK artık ölçümleri MDM'den alıyor.
  - Get-AzureRmMetricDefinition
    + Çıktı hala bir liste, ancak liste yapısı değiştirildi.
  - Get-AzureRmMetric
    + Çağrı değiştirildi. Yeni sözdizimi şu şekildedir: Get-AzureRmMetric ResourceId [ÖlçümAdları [ZamanDilimi] [ToplamaTürü] [BaşlangıçZamanı] [BitişZamanı]] [AyrıntılıÇıktı]
    + Çıktı bir liste, ancak öğelerinin yapısı değiştirildi.
* KeyVault
  - KeyVault gizli dizileri için yedekleme/geri yükleme desteği eklendi
    + Gizli diziler yedeklenip geri yüklenebilir, Anahtarlar için desteklenen işlevlerle birlikte kullanılabilir

  - Anahtarlar ve Gizli Diziler için yedekleme cmdlet'leri artık giriş parametresi için karşılık gelen bir nesneyi kabul ediyor
    + Çağrıda bulunan alma ve yedekleme işlemlerini bir arada kullanabilir: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Yedekleme cmdlet'i artık var olan bir dosyanın üzerine yazmak için -Force anahtarı kullanılmasını destekliyor
    + Var olan dosyanın üzerine yazma girişiminin artık işlemi sonlandırmayacağını, kullanıcıya nasıl devam etmek istediğinin sorulacağını unutmayın.
* LogicApp
  - Değişim Denetim Numarası olağanüstü durum kurtarma cmdlet'leri için yeni parametreler:
    + İlgili kontrol numaralarını belirtmek için isteğe bağlı -AgreementType parametresi ("X12" veya "Edifact")
* MachineLearning
  - Yeni Azure Machine Learning .Net SDK'sı sürümü kullanılıyor ve yeni bir cmdlet eklendi
    + Add-AzureRmMlWebServiceRegionalProperty
  - Yardım metninde küçük metin düzeltmeleri yapıldı.
* Ağ
  - Test-AzureRmNetworkWatcherConnectivity cmdlet'i eklendi
    + Belirtilen kaynak VM ve hedef için bağlantı durumu bilgilerini döndürür
    + Kaynak ve hedef arasında bağlantı kurulamazsa cmdlet sorunla ilgili ayrıntıları döndürür
* Profil
  - "Send-Feedback" cmdlet'i eklendi: Kullanıcının Azure PowerShell ekibine geri bildirim gönderen komut dizisi başlatmasını sağlar.
  - Azure modülündeki var olan cmdlet adlarıyla çakıştığından aşağıdaki diğer adlar kaldırıldı:
    + `Enable-AzureDataCollection` (destekleyen: `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (destekleyen: `Disable-AzureRmDataCollection`)
* Geçiş
  - Kullanıcıların Azure Geçişi kaynakları oluşturmasını ve yönetmesini sağlayan Azure Geçişi cmdlet'leri eklendi.
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
* Kaynaklar
  - New-AzureRmResourceGroupDeployment için kaynak grupları arası dağıtım desteği eklendi
    + Kullanıcılar artık farklı kaynak gruplarında dağıtım yapmak için iç içe geçmiş dağıtımlar kullanabilir.
* ServiceBus

  - Hata Düzeltmesi: ServiceBus Kuyruğu nesnesi özellik değerleri null olarak belirlenmişti, nesne Kuyruğu güncelleştirmek için Set-AzureRmServiceBusQueue cmdlet'inde giriş parametresi olarak kullanılıyor.
   - Etkilenen özellikler: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount ve MessageCount
* ServiceFabric

  - Service Fabric için cmdlet'ler eklendi
    + Add-AzureRmServiceFabricApplicationCertificate       Uygulama sertifikası olarak kullanılacak bir sertifika ekler
    + Add-AzureRmServiceFabricClientCertificate       Küme ayarlarına istemci kimlik doğrulaması için ortak ad veya parmak izi ekler
    + Add-AzureRmServiceFabricClusterCertificate       Var olan sertifikaya geçmek için kümeye ikincil küme sertifikası ekler
    + Add-AzureRmServiceFabricNodes       Bir kümeye belirli bir düğüm türünde düğümler/VM'ler ekler
    + Add-AzureRmServiceFabricNodeType       Var olan bir kümeye düğüm türü/VM'ler ekler
    + Get-AzureRmServiceFabricCluster       Küme kaynağının ayrıntılarını döndürür
    + New-AzureRmServiceFabricCluster Yeni bir ServiceFabric kümesi oluşturur. Bu komut farklı senaryoları kapsayacak şekilde kullanılabilir
    + Remove-AzureRmServiceFabricClientCertificate       Bir kümeye erişmek için kullanılan bir istemci sertifikasını engeller
    + Remove-AzureRmServiceFabricClusterCertificate       Bir kümenin güvenliği için kullanılan bir küme sertifikasını kaldırır
    + Remove-AzureRmServiceFabricNodes       Bir kümede yer alan belirli türdeki düğümleri kaldırır
    + Remove-AzureRmServiceFabricNodeType       Bir kümedeki düğüm türünü kaldırır
    + Remove-AzureRmServiceFabricSettings       Bir kümeden bir veya daha fazla ServiceFabric ayarını kaldırır
    + Set-AzureRmServiceFabricSettings       Bir kümeye bir veya daha fazla ServiceFabric ayarı ekler veya var olan ayarları güncelleştirir
    + Set-AzureRmServiceFabricUpgradeType       Bir kümenin ServiceFabric yükseltme türünü değiştirir
    + Update-AzureRmServiceFabricDurability       Bir kümenin dayanıklılık katmanını değiştirir
    + Update-AzureRmServiceFabricReliability       Bir kümenin güvenilirlik katmanını değiştirir
* Sql
  - New-AzureRmSqlDatabase cmdlet'ine Added -SampleName parametresi eklendi
  - Yük Devretme Grubu cmdlet'leri güncelleştirildi
  - "Etiket" parametreleri kaldırıldı
  - Remove-AzureRmSqlDatabaseFailoverGroup cmdlet'inden "PartnerResourceGroupName" ve "PartnerServerName" parametreleri kaldırıldı
  - New- ve Set- cmdlet'lerine "GracePeriodWithDataLossHours" paremetresi eklendi, "GracePeriodWithDataLossHour" parametresinin yerini alması planlanıyor
  - Belgeler gözden geçirildi ve güncelleştirildi
  - Geri döndürülen nesnelerin biçimi değiştirildi ve alanların doldurulmadığı bazı hatalar düzeltildi
  - Yük Devretme Grubu nesnesine "DatabaseNames" ve "PartnerLocation" özellikleri eklendi
  - Switch- cmdlet'inin işlemin tamamlanmasını beklemek yerine hemen sonuç döndürmesine neden olan hata düzeltildi
  - Yüksek yetkisiz kullanım süresi değerleri kullanıldığında ortaya çıkan tamsayı taşma hatası düzeltildi
  - Daha düşük bir değer girildiğinde yetkisiz kullanım süresi en az 1 saat olacak şekilde ayarlandı
  - Set-AzureRmSqlDatabaseThreatDetectionPolicy ve Set-AzureRmSqlServerThreatDetectionPolicy cmdlet'lerinin "ExcludedDetectionType" parametresinin kabul edilen değerlerinden "Usage_Anomaly" kaldırıldı.
* Depolama
  - SRP SDK'sı 6.3.0 sürümüne yükseltildi
  - New/Set-AzureRmStorageAccount: EnableHttpsTrafficOnly desteği için yeni bir parametre eklendi
  - New/Set/Get-AzureRmStorageAccount: Döndürülen Depolama Hesabı artık yeni EnableHttpsTrafficOnly özniteliğini içeriyor
* Azure Depolama
  - Azure Depolama İstemci Kitaplığı 8.1.1 ve Azure Depolama Veri Taşıma Kitaplığı 0.5.1 sürümüne yükseltildi
  - Blob Artımlı Kopya özelliğini desteklemek için yeni bir cmdlet eklendi
