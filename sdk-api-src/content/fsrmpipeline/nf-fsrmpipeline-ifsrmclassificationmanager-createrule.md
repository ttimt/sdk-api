---
UID: NF:fsrmpipeline.IFsrmClassificationManager.CreateRule
title: IFsrmClassificationManager::CreateRule (fsrmpipeline.h)
description: Creates a rule of the specified type.
old-location: fsrm\ifsrmclassificationmanager_createrule.htm
tech.root: fsrm
ms.assetid: ca9a97b7-eadd-4f57-8f3a-afa439222f21
ms.date: 12/05/2018
ms.keywords: CreateRule, CreateRule method [File Server Resource Manager], CreateRule method [File Server Resource Manager],FsrmClassificationManager class, CreateRule method [File Server Resource Manager],IFsrmClassificationManager interface, CreateRule method [File Server Resource Manager],IFsrmClassificationManager2 interface, FsrmClassificationManager class [File Server Resource Manager],CreateRule method, IFsrmClassificationManager interface [File Server Resource Manager],CreateRule method, IFsrmClassificationManager.CreateRule, IFsrmClassificationManager2 interface [File Server Resource Manager],CreateRule method, IFsrmClassificationManager2::CreateRule, IFsrmClassificationManager::CreateRule, fs.ifsrmclassificationmanager_createrule, fsrm.ifsrmclassificationmanager_createrule, fsrmpipeline/IFsrmClassificationManager2::CreateRule, fsrmpipeline/IFsrmClassificationManager::CreateRule
ms.topic: method
f1_keywords:
- fsrmpipeline/IFsrmClassificationManager.CreateRule
dev_langs:
- c++
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmClassificationManager.CreateRule
- IFsrmClassificationManager2.CreateRule
- FsrmClassificationManager.CreateRule
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmClassificationManager::CreateRule


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a> class.]

Creates a rule of the specified type.


## -parameters




### -param ruleType [in]

The type of rule to create, set this parameter to <b>FsrmRuleType_Classification</b>. 
      For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmruletype">FsrmRuleType</a>.


### -param Rule [out]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a> interface to the new rule. Query the 
       <b>IFsrmRule</b> interface to get the interface to get the 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationrule">IFsrmClassificationRule</a> interface.

To save the rule, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmRule::Commit</a> 
       method.


## -returns



The method returns the following return values.




## -remarks



There is no limit to the number of rules that you can create. Use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmrule-get_moduledefinitionname">IFsrmRule.ModuleDefinitionName</a> property 
    to associate the rule with a classification module.

FSRM cannot guarantee the order in which the rules 
    are run.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmclassificationmanager">FsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager">IFsrmClassificationManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassificationmanager2">IFsrmClassificationManager2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-getrule">IFsrmClassificationManager::GetRule</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmclassification">MSFT_FSRMClassification</a>
 

 

