Azure PowerShell 4.3.1 Yükleyicisi: [bağlantı](https://github.com/Azure/azure-powershell/releases/download/v4.3.1-August2017/azure-powershell.4.3.1.msi)

ARM Cmdlet’leri için Galeri Modülü: [bağlantı](https://www.powershellgallery.com/packages/AzureRM/4.3.1)

Hizmet Yönetimi’ne (RDFE) yönelik Eski Cmdlet’ler için Galeri Modülü: [bağlantı](https://www.powershellgallery.com/packages/Azure/4.3.1)

## <a name="changes-in-431"></a>4.3.1 sürümündeki değişiklikler

- Belirli bütünleştirilmiş kodların imzalanmayarak modüller içeri aktarılırken oluşan `could not load file or assembly` hatasına neden olması sorunu düzeltildi

## <a name="changes-in-430"></a>4.3.0 sürümündeki değişiklikler

* AnalysisServices
    * Set-AzureRmAnalysisServciesServer içinde bir hata düzeltildi
        - Yönetici sağlanmadığında, yönetici kaldırılır.
    * New-AzureRmAnalysisServicesServer ve Set-AzureRmAnalysisServicesServer içine BackupBlobContainerUri eklendi
        - Azure Analysis Services Server’ı yedeklemek/geri yüklemek için yedekleme blob kapsayıcısını ayarlama/devre dışı bırakma etkinleştirildi
    * New-AzureRmAnalysisServicesServer ve Set-AzureRmAnalysisServicesServer içinde güncelleştirilmiş SKU arama
        - Sabit kodlanmış SKU, dinamik arama olarak değiştirildi.
    * Hizmet Sorumlusu ile oturum açmayı desteklemek için Add-AzureAnalysisServicesAccount
* Otomasyon
    * 100’den fazla kayıt çekmek için AutomationDSC* cmdlet’lerinde değişiklikler yapıldı
    * Ayrıntılı akışların bazı Otomasyon cmdlet’leri (örneğin Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob) çağrıldıktan sonra çalışmayı durdurması sorunu çözüldü.
    * StartAzureAutomationDscCompilationJob ve ImportAzureAutomationDscNodeConfiguration içinde NodeConfiguration Derleme sürümü oluşturma desteği eklendi.
    * Mevcut sorunlar için hata düzeltmeleri - #3775 içindeki diğer ad ve HybridWorkers için runOn diğer adı ve desteği sorunu düzeltildi.
* İşlem
    * Set-AzureRmVMAEMExtension: Yeni Premium Disk boyutları için destek ekleme
    * Set-AzureRmVMAEMExtension: M serisi için destek ekleme
    * Add-AzureRmVmssExtension öğesine ForceUpdateTag parametresi ekleme
    * New-AzureRmVmssIpConfig öğesine Primary parametresi ekleme
    * Add-AzureRmVmssNetworkInterfaceConfig öğesine EnableAcceleratedNetworking parametresi ekleme
    * Set-AzureRmVmss öğesine InstanceId ekleme
    * Get-AzureRmVM -Status çıkışını almak için MaintenanceRedeployStatus öğesini kullanıma sunma
    * Get-AzureRmComputeResourceSku öğesinin tablo biçimine yönelik Restriction ve Capability öğelerini kullanıma sunma
* DataLakeStore
    * Sorun için düzeltme: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
    * NamespaceAttributes öğesine ResourceGroup özelliği eklendi
        - 'ResourceGroup', Ad Alanının bulunduğu kaynak grubunun adını alır
    * commandlet’ler yeni parametre ve parametre diğer adı ile güncelleştirildi
        - aşağıdaki cmdlet’ler AuthorizationRule işlemine yönelik Namespace ve EventHub için Parametersets ile güncelleştirildi
        - New-AzureRmEventHubAuthorizationRule
            + Mevcut NameSpace veya EventHub öğesine yeni bir AuthorizationRule ekler.
        - Get-AzureRmEventHubAuthorizationRule
            + Mevcut NameSpace veya EventHub öğesinin AuthorizationRule / AuthorizationRules Listesini alır.
        - Set-AzureRmEventHubAuthorizationRule
            + EventHub NameSpace için mevcut AuthorizationRule özelliklerini güncelleştirir.
        - Remove-AzureRmEventHubAuthorizationRule
            + Mevcut NameSpace veya EventHub için mevcut AuthorizationRule öğesini siler.
        - New-AzureRmEventHubKey
            + Mevcut NameSpace veya EventHub için AuthorizationRule öğesine yönelik yeni bir Birincil/İkincil Anahtar oluşturur.
        - Get-AzureRmEventHubKey
            + Mevcut NameSpace veya EventHub için AuthorizationRule öğesine yönelik Birincil/İkincil Anahtarı alır.
* Ağ
    * New-AzureRmExpressRouteCircuitPeeringConfig: IPv6 desteği eklendi. İsteğe bağlı yeni bir parametre eklendi
        - PeerAddressType
    * Set-AzureRmExpressRouteCircuitPeeringConfig: IPv6 desteği eklendi. İsteğe bağlı yeni bir parametre eklendi
        - PeerAddressType
    * Remove-AzureRmExpressRouteCircuitPeeringConfig: IPv6 desteği eklendi. İsteğe bağlı yeni bir parametre eklendi
        - PeerAddressType
    * -ProbeEnabled parametresi eski olarak işaretlendi
        - Add-AzureRmApplicationGatewayBackendHttpSettings
        - New-AzureRmApplicationGatewayBackendHttpSettings
        - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Veri toplama varsayılan olarak etkinleştirildi. Kullanım verileri, kullanıcı deneyimini geliştirmek için Microsoft tarafından toplanır. Veriler anonimdir ve komut satırı bağımsız değişkeni değerlerini içermez.
        - Özelliği kapatmak için Disable-AzureRmDataCollection cmdlet’ini kullanın
        - Özelliği açmak için Enable-AzureRmDataCollection cmdlet’ini kullanın
* Kaynaklar
    * İstek ARM’ye gönderilmeden önce aşağıdaki roledefinition ve roleassignment commandlet’leri için kapsam doğrulama desteği ekleme
        - Get-AzureRMRoleAssignment
        - New-AzureRMRoleAssignment
        - Remove-AzureRMRoleAssignment
        - Get-AzureRMRoleDefinition
        - New-AzureRMRoleDefinition
        - Remove-AzureRMRoleDefinition
        - Set-AzureRMRoleDefinition
* ServiceBus
    * NameSpace, Queue ve Topic için AuthorizationRules öğesine yönelik aşağıdaki yeni commandlet’ler eklendi. Yetkilendirme kuralı işlemleri, ayarlanan parametreye göre uygulanır.
     - New-AzureRmServiceBusAuthorizationRule
       - Mevcut ServiceBus NameSpace/Queue/Topic için yeni bir AuthorizationRule ekler.
     - Get-AzureRmServiceBusAuthorizationRule
       - Mevcut ServiceBus NameSpace/Queue/Topic öğesinin AuthorizationRule / AuthorizationRules Listesini alır.
     - Set-AzureRmServiceBusAuthorizationRule
       - ServiceBus NameSpace/Queue/Topic için mevcut AuthorizationRule özelliklerini güncelleştirir.
     - New-AzureRmServiceBusKey
       - Mevcut ServiceBus NameSpace/Queue/Topic için AuthorizationRule öğesine yönelik yeni bir Birincil/İkincil Anahtar oluşturur.
     - Get-AzureRmServiceBusKey
       - Mevcut ServiceBus NameSpace/Queue/Topic için AuthorizationRule öğesinin Birincil/İkincil Anahtarını alır.
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule
       - ServiceBus NameSpace/Queue/Topic için mevcut AuthorizationRule öğesini siler.
    * NamespceAttributes öğesine Kaynak Grubu özelliği eklendi
* Sql
    * Set-AzureRmSqlServerTransparentDataEncryptionProtector, Şifreleme Koruyucu Türü AzureKeyVault olarak ayarlandığında bir uyarı görüntülemek ve onay gerektirmek üzere güncelleştiriliyor
    * Denetim ayarları için yeni güncelleştirilmiş cmdlet’ler ekleniyor
        - Bir Azure SQL veritabanının denetim ayarlarını alan Get-AzureRmSqlDatabaseAuditing cmdlet’i ekleniyor.
        - Bir Azure SQL sunucusunun denetim ayarlarını alan Get-AzureRmSqlServerAuditing cmdlet’i ekleniyor.
        - Bir Azure SQL veritabanının denetim ayarlarını değiştiren Set-AzureRmSqlDatabaseAuditing cmdlet’i ekleniyor.
        - Bir Azure SQL sunucusunun denetim ayarlarını değiştiren Set-AzureRmSqlServerAuditing cmdlet’i ekleniyor.
    * Mevcut Denetim ilkesi cmdlet’leri kullanım dışı bırakılıyor
        - Get-AzureRmSqlDatabaseAuditingPolicy kullanım dışı bırakılıyor
        - Get-AzureRmSqlServerAuditingPolicy kullanım dışı bırakılıyor
        - Set-AzureRmSqlDatabaseAuditingPolicy kullanım dışı bırakılıyor
        - Set-AzureRmSqlServerAuditingPolicy kullanım dışı bırakılıyor
        - Use-AzureRmSqlServerAuditingPolicy kullanım dışı bırakılıyor
        - Remove-AzureRmSqlDatabaseAuditing kullanım dışı bırakılıyor
        - Remove-AzureRmSqlServerAuditing kullanım dışı bırakılıyor
    * Update-AzureRmSqlSyncGroup için şema dosyası ayrıştırma işlemi artık büyük/küçük harfe duyarlı değildir.
* Depolama
    * Kaynak modu depolama hesabı cmdlet’lerine NeworkRule desteği eklendi
        - New-AzureRmStorageAccount
        - Set-AzureRmStorageAccount
        - Get-AzureRmStorageAccountNetworkRuleSet
        - Update-AzureRmStorageAccountNetworkRuleSet
        - Add-AzureRmStorageAccountNetworkRule
        - Remove-AzureRmStorageAccountNetworkRule

[Son sürümden sonraki değişiklikleri](https://github.com/Azure/azure-powershell/compare/v4.2.1-July2017...v4.3.1-August2017) görüntüleyin
