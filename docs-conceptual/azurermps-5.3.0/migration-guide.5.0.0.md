# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="997d2-101">Microsoft Azure PowerShell 5.0.0 için bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="997d2-102">Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="997d2-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="997d2-103">Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır.</span><span class="sxs-lookup"><span data-stu-id="997d2-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="997d2-104">Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="997d2-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="997d2-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="997d2-105">Table of Contents</span></span>

- [<span data-ttu-id="997d2-106">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="997d2-107">Batch cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="997d2-108">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="997d2-109">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="997d2-110">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="997d2-111">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="997d2-112">Kaynaklar cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="997d2-113">ServiceBus Cmdlet’lerinde Bozucu Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="997d2-114">ApiManagement cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="997d2-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="997d2-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="997d2-116">"UserName" ve "Password" parametreleri bir PSCredential ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="997d2-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="997d2-118">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="997d2-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="997d2-120">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="997d2-121">Batch cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="997d2-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="997d2-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="997d2-123">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="997d2-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="997d2-125">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="997d2-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="997d2-127">`Password` parametresi bir Secure dizesi ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="997d2-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="997d2-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="997d2-129">`RunElevated` anahtarı kaldırılıp `UserIdentity` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="997d2-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="997d2-130">Bundan `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` ve `PSJobReleaseTask` üzerindeki `RunElevated` özelliği de etkilenir.</span><span class="sxs-lookup"><span data-stu-id="997d2-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="997d2-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="997d2-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="997d2-132">`PSMultiInstanceSettings` oluşturucusu artık gerekli bir `numberOfInstances` parametresi almak yerine gerekli bir `coordinationCommandLine` parametresi alır.</span><span class="sxs-lookup"><span data-stu-id="997d2-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="997d2-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="997d2-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="997d2-134">`PSCloudTask` üzerinde `RunElevated` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="997d2-135">`RunElevated` yerine `UserIdentity` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="997d2-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="997d2-136">Bundan `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` ve `PSJobReleaseTask` üzerindeki `RunElevated` özelliği de etkilenir.</span><span class="sxs-lookup"><span data-stu-id="997d2-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="997d2-137">**Birden çok tür**</span><span class="sxs-lookup"><span data-stu-id="997d2-137">**Multiple types**</span></span>

- <span data-ttu-id="997d2-138">`PSExitConditions` üzerinde `SchedulingError` özelliği `PreProcessingError` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="997d2-139">**Birden çok tür**</span><span class="sxs-lookup"><span data-stu-id="997d2-139">**Multiple types**</span></span>

- <span data-ttu-id="997d2-140">`PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` ve `PSTaskExecutionInformation` üzerinde `SchedulingError` özelliği `FailureInformation` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="997d2-141">Her görev hatası için `FailureInformation` döndürülür.</span><span class="sxs-lookup"><span data-stu-id="997d2-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="997d2-142">Buna, önceki tüm zamanlama hata durumlarının yanı sıra yeni çıktı dosyaları özelliğinden sıfır olmayan görev çıkış kodları ve karşıya dosya yükleme hataları dahildir.</span><span class="sxs-lookup"><span data-stu-id="997d2-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="997d2-143">Bu türün yapısı aynı kaldığından, türü kullanırken kod değişikliği yapmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="997d2-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="997d2-144">Ek olarak şunlar da etkilenir: Get-AzureBatchPool, Get-AzureBatchSubtask ve Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="997d2-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="997d2-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="997d2-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="997d2-146">`TargetDedicated` kaldırılıp `TargetDedicatedComputeNodes` ve `TargetLowPriorityComputeNodes` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="997d2-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="997d2-147">`TargetDedicatedComputeNodes` öğesinin `TargetDedicated` şeklinde bir diğer adı vardır.</span><span class="sxs-lookup"><span data-stu-id="997d2-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="997d2-148">Şu da etkilenir: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="997d2-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="997d2-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="997d2-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="997d2-150">`PSCloudPool` üzerinde `TargetDedicated` ve `CurrentDedicated` özellikleri `TargetDedicatedComputeNodes` ve `CurrentDedicatedComputeNodes` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="997d2-151">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="997d2-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="997d2-152">`PSCloudPool` üzerinde `ResizeError` ve `ResizeErrors` yeniden adlandırıldı ve artık bir koleksiyon.</span><span class="sxs-lookup"><span data-stu-id="997d2-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="997d2-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="997d2-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="997d2-154">`PSPoolSpecification` üzerinde `TargetDedicated` özelliği `TargetDedicatedComputeNodes` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="997d2-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="997d2-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="997d2-156">`Name` kaldırılıp `Path` ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="997d2-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="997d2-157">`Path` öğesinin `Name` şeklinde bir diğer adı vardır.</span><span class="sxs-lookup"><span data-stu-id="997d2-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="997d2-158">Şunlar da etkilenir: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="997d2-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="997d2-159">**PSNodeFile** Türü</span><span class="sxs-lookup"><span data-stu-id="997d2-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="997d2-160">`PSNodeFile` üzerinde `Name` özelliği `Path` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="997d2-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="997d2-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="997d2-162">`PSSubtaskInformation` öğesinin `PreviousState` ve `State` özellikleri artık `TaskState` türünde değil, `SubtaskState` türündedir.</span><span class="sxs-lookup"><span data-stu-id="997d2-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="997d2-163">Alt görevlerin `Active` durumunda olması mümkün olmadığından, `SubtaskState` öğesinin `TaskState` öğesinden farklı olarak `Active` değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="997d2-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="997d2-164">İşlem cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="997d2-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="997d2-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="997d2-166">"UserName" ve "Password" parametreleri bir PSCredential ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="997d2-167">EventHub cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="997d2-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-169">'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-170">Lütfen 'New-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="997d2-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-172">'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-173">Lütfen 'Get-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="997d2-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-175">'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-176">Lütfen 'Set-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="997d2-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-178">'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-179">Lütfen 'Remove-AzureRmEventHubAuthorizationRule' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="997d2-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="997d2-181">'New-AzureRmEventHubNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-182">Lütfen 'New-AzureRmEventHubKey' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="997d2-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="997d2-184">'Get-AzureRmEventHubNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-185">Lütfen 'Get-AzureRmEventHubKey' cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="997d2-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="997d2-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="997d2-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="997d2-187">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="997d2-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="997d2-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="997d2-189">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="997d2-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="997d2-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="997d2-191">NamespceAttributes’tan 'Status' ve 'Enabled' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="997d2-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="997d2-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="997d2-193">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="997d2-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="997d2-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="997d2-195">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="997d2-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="997d2-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="997d2-197">ConsumerGroupAttributes’tan 'EventHubPath' özelliği kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="997d2-198">Insights cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="997d2-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="997d2-200">**Add-AzureRMLogAlertRule** cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="997d2-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="997d2-201">Bu işlevsellik Etkinlik Günlüğü Uyarılarına geçirildiğinden, 1 Ekim’den sonra bu cmdlet’in kullanılmasının herhangi bir etkisi olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="997d2-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="997d2-202">Daha fazla bilgi için bkz. https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="997d2-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="997d2-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="997d2-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="997d2-204">**Get-AzureRMUsage** cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="997d2-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="997d2-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="997d2-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="997d2-206">Çıktı değişikliği: EventData nesnesinden (bu cmdlet’ler tarafından döndürülür) EventChannels alanı artık sabit bir değer (Admin,Operation) döndürdüğünden kullanım dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="997d2-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="997d2-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="997d2-208">Çıktı değişikliği: Kullanıcı deneyiminin geliştirilmesi için bu cmdlet’in çıktısı, özellikler alanı kaldırılarak düzleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="997d2-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="997d2-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="997d2-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="997d2-210">Çıktı değişikliği: AutoscaleSettingResourceName alanı her zaman Name alanına eşit olduğundan kullanımdan kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="997d2-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="997d2-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="997d2-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="997d2-212">Çıktı değişikliği: Çıktının türü, istek kimliğini ve durum kodunu içeren tek bir nesne döndürecek şekilde değiştirilecek.</span><span class="sxs-lookup"><span data-stu-id="997d2-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="997d2-213">Ağ cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="997d2-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="997d2-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="997d2-215">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="997d2-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="997d2-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="997d2-217">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="997d2-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="997d2-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="997d2-219">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="997d2-220">Kaynaklar cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="997d2-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="997d2-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="997d2-222">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="997d2-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="997d2-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="997d2-224">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="997d2-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="997d2-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="997d2-226">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="997d2-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="997d2-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="997d2-228">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="997d2-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="997d2-230">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="997d2-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="997d2-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="997d2-232">"Password" parametresi bir SecureString ile değiştiriliyor</span><span class="sxs-lookup"><span data-stu-id="997d2-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="997d2-233">ServiceBus cmdlet’lerinde bozucu değişiklikler</span><span class="sxs-lookup"><span data-stu-id="997d2-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="997d2-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-235">'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-236">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="997d2-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="997d2-238">'Get-AzureRmServiceBusTopicKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-239">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="997d2-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-241">'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-242">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="997d2-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="997d2-244">'New-AzureRmServiceBusTopicKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-245">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="997d2-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-247">'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-248">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="997d2-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-250">'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-251">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="997d2-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="997d2-253">'New-AzureRmServiceBusNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-254">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="997d2-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-256">'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-257">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="997d2-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="997d2-259">'Get-AzureRmServiceBusQueueKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-260">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="997d2-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-262">'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-263">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="997d2-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="997d2-265">'New-AzureRmServiceBusQueueKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-266">Lütfen 'New-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="997d2-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-268">'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-269">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="997d2-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-271">'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-272">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="997d2-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-274">'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-275">Lütfen 'Get-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="997d2-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="997d2-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="997d2-277">'Get-AzureRmServiceBusNamespaceKey' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-278">Lütfen 'Get-AzureRmServiceBusKey' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="997d2-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-280">'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-281">Lütfen 'New-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="997d2-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-283">'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-284">Lütfen 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="997d2-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="997d2-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="997d2-286">'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet’i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="997d2-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="997d2-287">Lütfen 'Set-AzureRmServiceBusAuthorizationRule' cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="997d2-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="997d2-288">**NamespaceAttributes Türü**</span><span class="sxs-lookup"><span data-stu-id="997d2-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="997d2-289">Aşağıdaki özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="997d2-289">The following properties have been removed</span></span>
    - <span data-ttu-id="997d2-290">Etkin</span><span class="sxs-lookup"><span data-stu-id="997d2-290">Enabled</span></span>
    - <span data-ttu-id="997d2-291">Durum</span><span class="sxs-lookup"><span data-stu-id="997d2-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="997d2-292">**QueueAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="997d2-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="997d2-293">Aşağıdaki özellikler eski olarak işaretlendi:</span><span class="sxs-lookup"><span data-stu-id="997d2-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="997d2-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="997d2-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="997d2-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="997d2-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="997d2-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="997d2-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="997d2-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="997d2-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="997d2-298">**TopicAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="997d2-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="997d2-299">Aşağıdaki özellikler eski olarak işaretlendi:</span><span class="sxs-lookup"><span data-stu-id="997d2-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="997d2-300">Konum</span><span class="sxs-lookup"><span data-stu-id="997d2-300">Location</span></span>
    - <span data-ttu-id="997d2-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="997d2-301">IsExpress</span></span>
    - <span data-ttu-id="997d2-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="997d2-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="997d2-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="997d2-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="997d2-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="997d2-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="997d2-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="997d2-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="997d2-306">**SubscriptionAttribute Türü**</span><span class="sxs-lookup"><span data-stu-id="997d2-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="997d2-307">Aşağıdaki özellikler eski olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="997d2-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="997d2-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="997d2-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="997d2-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="997d2-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="997d2-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="997d2-310">IsReadOnly</span></span>
    - <span data-ttu-id="997d2-311">Konum</span><span class="sxs-lookup"><span data-stu-id="997d2-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```