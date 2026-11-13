## Developer Guide 

# Customization Update 

# 2026 R2 


<!-- PAGE_BREAK -->
 Contents | 2 

## Contents 

 Copyright...............................................................................................................................................3 

 Validating Customization Projects........................................................................................................... 4 

 Validation of Customization Projects: General Information............................................................................4 

 Validation of Customization Projects: Compatibility Validation..................................................................... 4 

 Validation of Customization Projects: Compatibility Validation Errors.......................................................... 6 

 Validation of Customization Projects: Using AI Tools...................................................................................... 7 

 Validation of Customization Projects: Ignore List for the Compatibility Validation Errors............................ 8 

 Validation of Customization Projects: ISV Solutions....................................................................................... 9 

 Validation of Customization Projects: Certification Status of Projects.........................................................10 

 Updating Customization Projects to Acumatica ERP 2026 R2.................................................................... 12 

 Customization Update to 2026 R2: Retirement of the Classic UI ................................................................. 12 

 Customization Update to 2026 R2: Async Credit Card Processing Interfaces and Methods........................ 14 

 Customization Update to 2026 R2: Refactored CBAPIService Extension Methods.......................................15 

 Customization Update to 2026 R2: Removal of Obsolete Commerce APIs...................................................18 

 Updating Customization Projects for the Modern UI................................................................................ 21 

 Updating a Customization Project for the Modern UI: General Information................................................21 

 Updating a Customization Project for the Modern UI: Customization Project Converter............................23 

 Updating a Customization Project to the Modern UI: To Convert a Customization Project.........................26 

 Updating a Customization Project for the Modern UI: To Convert a Customized Form...............................29 

 Updating a Customization Project for the Modern UI: Form Converter....................................................... 33 

 Updating a Customization Project for the Modern UI: To Convert a Custom Form..................................... 34 

 Migrating JavaScript and ASPX.CS Code to the Modern UI........................................................................39 

 Migrating Custom Frontend Code: General Information............................................................................... 39 

 Migrating Custom Frontend Code: To Implement an Event Handler............................................................45 

 Migrating Custom Frontend Code: Helping Tools.......................................................................................... 47 


<!-- PAGE_BREAK -->
 Copyright | 3 

## Copyright 

 © 2026 Acumatica, Inc. 

 ALL RIGHTS RESERVED. 

 No part of this document may be reproduced, copied, or transmitted without the express prior consent of Acumatica, Inc. 

 3075 112th Avenue NE, Suite 200, Bellevue, WA 98004, USA 

#### Restricted Rights 

 The product is provided with restricted rights. Use, duplication, or disclosure by the United States Government is subject to restrictions as set forth in the applicable License and Services Agreement and in subparagraph (c)(1)(ii) of the Rights in Technical Data and Computer Soware clause at DFARS 252.227-7013 or subparagraphs (c)(1) and (c)(2) of the Commercial Computer Soware-Restricted Rights at 48 CFR 52.227-19, as applicable. 

#### Disclaimer 

 Acumatica, Inc. makes no representations or warranties with respect to the contents or use of this document, and specifically disclaims any express or implied warranties of merchantability or fitness for any particular purpose. Further, Acumatica, Inc. reserves the right to revise this document and make changes in its content at any time, without obligation to notify any person or entity of such revisions or changes. 

#### Trademarks 

 Acumatica is a registered trademark of Acumatica, Inc. HubSpot is a registered trademark of HubSpot, Inc. Microso Exchange and Microso Exchange Server are registered trademarks of Microso Corporation. All other product names and services herein are trademarks or service marks of their respective companies. 

 Soware Version: 2026 R2 

 Last Updated: 09/15/2026 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 4 

## Validating Customization Projects 

 A customization project must meet various technical requirements to integrate with and operate within the Acumatica ERP application. Also, the Acumatica ERP code is continuously updated to add or enhance functionality —so a customization project’s code can become inconsistent with the code of an upgraded instance of Acumatica ERP. To make sure your customization project stays compatible, you can validate customization projects. 

### Validation of Customization Projects: General Information 

 By validating customization projects, you can ensure that they can be published in the current Acumatica ERP instance, meet specific requirements, and have passed technical validation in Acumatica. 

#### Learning Objectives 

 In this chapter, you’ll learn how to do the following: 

- Validate customization projects for compatibility with the new version before an upgrade 

- Validate customization projects of independent soware vendor (ISV) solutions before submitting them for     technical validation 

- Check whether customization projects have passed technical validation by Acumatica 

#### Applicable Scenarios 

 You validate a customization project in the following cases: 

- You have a customization project that works properly for a version of Acumatica ERP, and you need     to upgrade an application instance to a newer version. Before the upgrade, you need to validate the     customization project with the newer version. For details on this scenario, see _Validation of Customization_     _Projects: Compatibility Validation_. 

- As a developer for an ISV partner of Acumatica ERP, you have developed a customization project, which you     need to submit to Acumatica for technical validation. To successfully pass this validation, you first need to     validate the customization project by using Acumatica ERP validation tools. To learn about the available     validation techniques, see _Validation of Customization Projects: ISV Solutions_. 

- You’re a system administrator who needs to check whether the customization projects you’re going to     publish on an Acumatica ERP instance have passed Acumatica’s technical validation. For more information,     see _Validation of Customization Projects: Certification Status of Projects_. 

### Validation of Customization Projects: Compatibility Validation 

 To prevent issues between a customization project and a new version of Acumatica ERP, you need to validate the customization project before upgrading a customized instance of Acumatica ERP. During publication, the Acumatica Customization Platform validates the compatibility of the project’s code with the application code of the instance. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 5 

 By default, the validation that detects breaking changes is turned on in an instance of Acumatica ERP. If you need to temporarily omit this validation, you can turn off the CheckCustomizationCompatibility key by including the following string in the <appSettings> section of the web.config file located in the website folder. 

 <add key="CheckCustomizationCompatibility" value="False" /> 

 We don’t recommend turning off the validation permanently. 

#### Before the Upgrade 

 In a development environment, test your customizations before a production upgrade to Acumatica ERP 2026 R2: 

1. Deploy a new instance of Acumatica ERP 2026 R2. (See _Deploying Acumatica ERP Instances_ for details.) 

2. On the _Customization Projects_ (SM204505) form, import all customization projects that you need to upgrade     for Acumatica ERP 2026 R2. 

3. Start the publication of these customization projects. The system first validates the projects for     compatibility with the current version. 

 If validation errors occur: 

- Learn what each error message means. (See _Validation of Customization Projects: Compatibility Validation_     _Errors_ .) 

- Check the developer release notes for descriptions of specific issues. You can find the release notes, along     with the needed Acumatica ERP build, on the _Acumatica Community_ website. 

- Replace updated or deprecated objects with the recommended alternatives. You can use AI tools to simplify     update. (See _Validation of Customization Projects: Using AI Tools_ .) 

- Redesign solutions if no alternatives are available for removed objects. 

#### During Validation 

 This validation process executes the following checks in the code of a customization project to detect the breaking changes in the code of Acumatica ERP: 

- In graph extensions: 

- Checking the signature for each method that is overridden by using the PXOverride attribute 

- Checking that each base graph exists 

- In data access class extensions when a field attribute is overridden: 

- Checking that the field exists 

- Checking that the field type hasn’t changed 

- In binary DLL files: Checking all the referenced methods, properties, fields, return types, and signatures If the validation has completed successfully, you can upgrade an instance of Acumatica ERP. For details, see _Upgrading of Acumatica ERP: General Information_. 

#### During the Upgrade 

 In the production environment, do the following during the upgrade to Acumatica ERP 2026 R2: 

1. Unpublish all customization projects. (See _Unpublishing Customization Projects_ for details.) 

2. Upgrade the Acumatica ERP instance. (Learn more in _Upgrading of Acumatica ERP: General Information_ .) 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 6 

3. Replace the old customization projects with those validated for Acumatica ERP 2026 R2. (See _To Replace the_     _Content of a Project from a Package_ for more information.) 

4. Publish the validated customization projects. (See _Publishing Customization Projects_ for details.) 

### Validation of Customization Projects: Compatibility Validation Errors 

 This topic explains the error messages that may occur during the validation of the customization code’s compatibility with the code of Acumatica ERP. 

#### Failed to resolve method reference 

 This error occurs if a custom DLL has a reference to a method that either no longer exists in Acumatica ERP or has a different signature. 

 Example: The following error message indicates that the AM.Objects.dll file contains a reference to the System.Void PX.Data.PXLineNbrAttribute::.ctor(System.Type) method, which hasn’t been declared or has another signature in the PX.Data assembly. 

 AM.Objects.dll Failed to resolve method reference: System.Void PX.Data.PXLineNbrAttribute::.ctor(System.Type) declared in PX.Data, Version=1.0.0.0, Culture=neutral, PublicKeyToken=3b136cac2f602b8e 

 Because the customization code was written for a previous version of Acumatica ERP, this error occurs because the method overridden in the customization code has since been removed or its signature has been changed. To confirm that this change is implemented in the new version of Acumatica ERP, check the developer release notes for this version. You can find the release notes, along with the needed Acumatica ERP build, on the Acumatica Community website. 

 To fix the error: In the code of the specified extension library, refer to an appropriate method declared in the current assembly. 

#### Failed to resolve type reference 

 This error occurs if a custom DLL refers to a type whose declaration no longer exists in Acumatica ERP. 

 Example: The following error message means that the FETempFix.dll file contains a reference to the PX.Data.PXGraphWithActionsBase2 type, which is not declared in the PX.Data assembly. 

 FETempFix.dll Failed to resolve type reference: PX.Data.PXGraphWithActionsBase2 declared in PX.Data, Version=1.0.0.0, Culture=neutral, PublicKeyToken=3b136cac2f602b8e 

 To fix the error: In the extension library, refer to an appropriate type declared in the current assembly. 

#### Could not resolve 

 This error occurs if the validation process finds a reference to a custom DLL that it can’t locate. 

 Example: The following error message tells you that the FullRegen.dll file contains the ADODB reference, which cannot be resolved. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 7 

 FullRegen.dll Could not resolve: ADODB, Version=7.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a 

 To fix the error: In the extension library, refer to a DLL file located in the Bin folder of the website. 

#### Declaring Type missing 

 This error occurs if the customization code in the App_RuntimeCode folder contains a reference to a type whose declaration doesn’t exist in Acumatica ERP. 

 Example: The following error message indicates that the PX.Objects.EP.CRBaseActivityMaint1<PX.Objects.CR.CRTaskMaint> class refers to the undeclared BaseBAccount type. 

 Declaring Type missing: BaseBAccount from PX.Objects.EP.CRBaseActivityMaint1<PX.Objects.CR.CRTaskMaint> 

 To fix the error: In the corresponding Code or DAC item of the customization project, refer to an appropriate type. 

#### Referenced Field missing 

 This error occurs if the customization code in the App_RuntimeCode folder contains a field that’s undeclared in the data access class (DAC). 

 Example: The following error message tells you that the PX.Objects.CS.CSAnswers DAC doesn’t contain the _EntityID field. 

 Referenced Field missing: _EntityID from PX.Objects.CS.CSAnswers 

 To fix the error: In the corresponding Code or DAC item of the customization project, refer to an existing field. 

### Validation of Customization Projects: Using AI Tools 

 Suppose that you have a customization project that works properly for Acumatica ERP 2026 R1, and you need to upgrade an application instance to 2026 R2. Before the upgrade, you validate the customization project with the newer version, as described in Validation of Customization Projects: Compatibility Validation. If validation errors occur, you need to fix these errors. 

 You can use an AI tool, such as Claude Code or GitHub Copilot, to speed up and simplify fixing of errors. 

#### Using the AI Tool Skill for Customization Project Update 

 In the Acumatica-AI-Resources repository on GitHub, you can find plug-ins and skills that you can use for development of your Acumatica ERP applications. The acumatica-customization-update skill helps your AI tool to edit, update, validate, and publish customization projects. Follow the documentation of your AI tool to use the repository and the skill in it. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 8 

#### Using the Release Notes in an AI Tool in Visual Studio 

 You can use the following general steps to update your customization project by using an AI tool: 

1. Review the developer release notes to understand the changes in the new version. 

2. Open your customization project’s extension library in Visual Studio. 

3. Add the **Markdown** version of the developer release notes from _https://beacon.acumatica.com/p/download_ to     the project of the extension library. 

4. Open a file with the Acumatica ERP-specific code, such as a graph or DAC extension. 

5. Launch a chat with your AI tool. 

6. Write a prompt, such as _Update this class to Acumatica ERP 2026 R2, use #<project name>/_     _AcumaticaERP_2026R1_ReleaseNotes_for_Developers.md_. 

 Instead of referencing the file in the prompt, you can copy and paste the contents of the file to the chat. 

7. Wait for the AI agent to process the context. 

8. Carefully review the provided recommendations and apply valid ones. Double-check them with the     developer release notes if you aren’t sure about the changes. 

9. Use the same context for other files in the project of your extension library. 

### Validation of Customization Projects: Ignore List for the Compatibility Validation 

### Errors 

 If the validation of the compatibility of the published customization with the new version fails, the platform cancels the upgrade process and shows an error message. However, if you’re sure that a generated error isn’t really an error, you can force the validation process to ignore it so that you can continue upgrading of the customized instance of Acumatica ERP. For example, you may need to ignore an error in a third-party DLL file. 

 To force the validation process to ignore an error, you perform the following actions: 

1. In the App_Data folder of the website, create a .txt file whose name has the _CstValidationIgnore_ prefix,     such as CstValidationIgnore.txt or CstValidationIgnore_ProjectName.txt. 

 You can create multiple CstValidationIgnore*.txt files with ignore lists for an instance of Acumatica ERP. 

2. In the file, paste the error message that you want to ignore. 

 You can add multiple error messages to each file with ignore lists. 

3. Save the file. 

4. Determine which customization project has the code that provokes the error message. 

5. Add the file with the ignore list to the project (see _To Add a Custom File to a Project_ for details). 

 If a file with a CstValidationIgnore prefix is placed in the App_Data folder, the Acumatica Customization Platform will ignore the specified errors during validation. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 9 

 As a result, if you publish the customization project or upgrade an Acumatica ERP instance where the project is published, the validation process ignores the error that is specified in the file. 

### Validation of Customization Projects: ISV Solutions 

 The validation of a customization project is especially important when the project is a part of an independent soware vendor (ISV) solution. 

 To learn the technical requirements for an ISV customization project, open the Acumatica Partner Portal and click ISV Program > ISV Solution Assessment. 

 To prepare your solution for technical validation, you can use the tools and validation techniques described below. 

#### Validation of Customization Projects 

 You can validate any number of customization projects to be sure each project meets the following criteria: 

- The database schema changes included in the customization project are valid. 

- The customization project does not replace or modify any files distributed as part of Acumatica ERP. 

- The data types of custom database columns correspond to the data access class (DAC) fields bound to them. You can perform this type of validation on the _Customization Projects_ (SM204505) form. On the More menu (under **Validations** ), click **Validate Highlighted Project** or **Validate Multiple Projects**. 

#### Validation of Data Consistency in Published Customization Projects 

 The validation of data consistency in published customization projects checks whether the data types of DAC fields match the field states generated by field attributes at runtime. To perform this validation, you use the commands on the More menu (under Validations ) of the Customization Projects (SM204505) form as follows: 

- To verify that the data types of DAC fields match the field states generated at runtime, click **DAC Field Types**     **(Runtime Validation)**. 

- To check for PXAttributeFamilyAttribute violations on DAC fields, click **DAC Attributes (Runtime**     **Validation)**. 

- To verify that PXDimensionAttribute attributes properly handle foreign key segments, click **Lookup**     **Definitions (Runtime Validation)**. 

#### Validation of a Project Prefix 

 In the Customization Project Editor, you can specify a prefix that should be added to all objects of the customization project. If a prefix is used, all project item names must start with it. 

 When validation of the customization project is performed, the platform checks all objects to be sure they have the prefix. 

 To add a prefix for a customization project and validate the project's items for the added prefix, do the following: 

1. On the main menu of the Customization Project Editor, select **File > Validate Project Prefix**.     The **Customization Project Prefix** dialog box opens. 

2. In the **Project Prefix** box of the dialog box, type the prefix for the customization project. The prefix can be     two to four case-insensitive Latin letters ( _A_ through _Z_ ). 

3. Click **Save**. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 10 

4. Click **Validate Project Items**. In the **Validation Result** area, the result of the validation appears. 

#### Format of the Validation Results 

 If any errors or warnings have been detected during project validation, the validation results have the following format: 

- <CustomizationProjectName> 

- <CustomizationRuleName> 

- <PathToTheDLL> | <ProjectItemType> | <NameOfTheProjectItem>     List of rules broken down by the specified item 

 The <PathToTheDLL> field is optional and appears only if a dll file included in the project is analyzed. 

#### Analysis of Assemblies Included in the Customization Project 

 You can analyze assemblies included in a customization project to verify that the project doesn’t replace or modify files distributed as part of Acumatica ERP. 

 To run the analysis, on the main menu of the Customization Project Editor, click Extension Library > Analyze Referenced Assemblies. A CSV file is downloaded with all references made in the project's custom files. 

#### Generation of a Workbook with Project Items 

 When you submit your solution for technical validation in Acumatica, you need to provide an Excel workbook with project items. You can generate this workbook in the Customization Project Editor by clicking File > Export Project Items Workbook. 

 The generated workbook contains a list of solution objects and integration scenarios grouped into the following types: 

- Site map nodes 

- Mobile site map nodes 

- BLСs and BLC extensions 

- DACs and DAC extensions 

- Push notifications 

- Import or export scenarios 

### Validation of Customization Projects: Certification Status of Projects 

 If a customization project doesn’t pass technical validation, it may negatively affect the performance of Acumatica ERP. To prevent this performance degradation, the system verifies the certification status of the customization projects that you create or upload. 

 This functionality is available for only licensed Acumatica ERP instances and is turned off by default. To use it, contact your Acumatica support provider. 


<!-- PAGE_BREAK -->
 Validating Customization Projects | 11 

#### Validating the Certification Status of Customization Projects 

 To validate the certification status of customization projects, you perform the following steps: 

1. Open the _Customization Projects_ (SM204505) form. 

2. On the More menu (under **Validations** ), click **Validate Certification Status**.     The system performs the check and displays the result in the **Certification Status** column for each project. 

 Each customization project has one of these certification statuses in the Acumatica ERP instance: 

- _Certified_ : The project has been imported and is available in the database with the certified customization     projects. 

- _Not Certified_ : The project has been imported but isn’t available in the database with the certified     customization projects. 

- _Not Verified_ : The project has been: 

- Uploaded before the upgrade to 2026 R2 

- Created manually 

- Certified—but then a customizer modified it 

- _Not Certified for Current Version_ : The project has been imported and is available in the database with the     certified customization projects. However, it was certified for a different major version than the major     version of the current Acumatica ERP instance. If a project isn’t certified or its certification status can’t be verified, the system displays a warning icon to the right of its name. 

 If you modify a certified customization project, its certification status will change to Not Verified. 

 We recommend that you avoid publishing a customization project with the Not Certified , Not Verified , or Not Certified For Current Version certification status. If you decide to publish one, the system will display a warning during publication. 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 12 

## Updating Customization Projects to Acumatica ERP 2026 

## R2 

 In this chapter, you can find details on the major changes in Acumatica ERP 2026 R2 that affect customization projects. The full list of changes is available in the developer release notes. You can find the release notes, along with the needed Acumatica ERP build, on the Acumatica Community website. 

### Customization Update to 2026 R2: Retirement of the Classic UI 

 As part of the ongoing transition to the Modern UI, Acumatica ERP 2026 R2 takes the next step toward retiring the Classic UI. The Modern UI is now the default user interface, and users can no longer switch between it and the Classic UI. 

 Starting in Acumatica ERP 2027 R1, forms that support only Classic UI will no longer be available. 

 Most importantly, this release gives organizations time to prepare for the next stage of the transition. Screens that are available only in the Classic UI can still be opened in 2026 R2, but they display a warning that they will be deprecated in the next release. 

 Organizations should use the 2026 R2 release to identify any remaining forms, dashboards, pivot tables, and customizations that use Classic UI and prepare them for the Modern UI. 

#### Modern UI as the Default User Experience 

 By default, the Classic UI is disabled in Acumatica ERP 2026 R2. When a form has a Modern UI version, it always opens in the Modern UI. 

 With the Classic UI disabled, options to select or switch the UI no longer appear in the installer, system menu, Site Map (SM200520), or Site Preferences (SM200505) forms. 

 Administrators can temporarily enable the Classic UI by setting the EnableLegacyUI=True flag in the web.config file. When set, users can still switch between the Modern UI and the Classic UI. 

#### Preparing Classic UI-Only Forms for Retirement 

 Forms and functionality not yet converted to the Modern UI remain accessible in 2026 R2, but users will be warned they will be deprecated in the next release. 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 13 

 Figure: A warning on the Classic UI-only form 

 The warning applies to Classic UI-only functionality such as: 

- Dashboards that haven't been migrated to the Modern UI and the _Classic Dashboards_ (SM208600) form 

- Pivot tables that haven't been migrated to the Modern UI and the _Pivot Tables_ (SM208010) form 

- Wizard forms (WZxxxxxx) 

- The Layout Editor in the Customization Editor 

- Custom forms that haven't been converted to the Modern UI 

- Other forms that are available only in the Classic UI 

#### No New Classic Dashboards or Pivot Tables 

 When the Classic UI is disabled, creating Classic dashboards or pivot tables is no longer possible. 

 Existing Classic dashboards and pivot tables can still be accessed in 2026 R2, giving organizations an opportunity to migrate the ones they need before the Classic UI functionality is removed in 2027 R1. 

 Figure: A warning on the Classic dashboard 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 14 

### Customization Update to 2026 R2: Async Credit Card Processing Interfaces and 

### Methods 

 Acumatica ERP credit card processing APIs now support asynchronous execution, making it easier to handle longrunning processing and cancellation in customization projects and integrations. 

 If your code calls, implements, or overrides credit card processing APIs, you’ll need to migrate to the new async interfaces. You should review the affected synchronous methods and replace them with their asynchronous equivalents. 

#### How to Migrate 

 To update your customization project or integration, do the following: 

- Use the new interfaces in the PX.CCProcessingBase.Interfaces.V2.Async namespace. 

- Replace synchronous credit card processing methods with the corresponding Async methods. 

- Pass a CancellationToken where required. 

- Rebuild and test any plug-ins, wrappers, or overrides that use the obsolete synchronous APIs. 

#### Asynchronous Plug-In Processors 

 All processor interfaces in PX.CCProcessingBase.Interfaces.V2 now have asynchronous equivalents in the PX.CCProcessingBase.Interfaces.V2.Async namespace. This change removes hidden blocking operations and allows you to use the async/await pattern throughout the call stack. 

 In the new interfaces, methods that communicate with a processing center have the Async suffix in their names and return Task or Task<T> (shown below). 

 namespace PX.CCProcessingBase.Interfaces.V2.Async { public interface ICCPayLinkProcessor { Task<PayLinkData> GetLinkAsync(PayLinkSearchParams searchParams, CancellationToken ct = default); Task<PayLinkData> CreateLinkAsync(PayLinkProcessingParams inputData, CancellationToken ct = default); Task<PayLinkData> UpdateLinkAsync(PayLinkProcessingParams inputData, CancellationToken ct = default); Task<PayLinkData> CloseLinkAsync(PayLinkProcessingParams payLinkData, CancellationToken ct = default); Task<PayLinkData> GetLinkWithTransactionsAsync( PayLinkSearchParams searchParams, CancellationToken ct = default); } } 

 The built-in plug-ins, such as Acumatica Payments, have also been modified so they implement the new async interfaces. 

#### Backward Compatibility 

 To support incremental migration, new adapters are available in the PX.CCProcessingBase.Interfaces.V2.Async.Adapter.SyncToAsync namespace. If your plug-in 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 15 

 hasn’t been updated yet, it automatically runs through the appropriate adapter and doesn’t require code changes. You can update existing plug-in assemblies gradually while continuing to support synchronous implementations. 

 Legacy methods and interfaces are marked as obsolete but remain available in 2026 R2. They are scheduled for removal in 2027 R2. 

#### New HttpContextData Class 

 If you need to use HTTP context data during asynchronous processing, your plug-in can work with the new PX.CCProcessingBase.Interfaces.V2.HttpContextData class. You cannot use the System.Web.HttpContext.Current property because it is available only on the main thread, not on the thread where an asynchronous operation is executed. 

 When an asynchronous operation is started by using the StartAsyncPaymentProcessingOperation or AwaitPaymentProcessingOperation extension method, the system creates an instance of HttpContextData and stores it in PXContext. Plug-in methods can access this instance by calling the CCPaymentProcessingHelper.GetHttpContextData method. 

#### Learn More 

 For more information, see Implementing Plug-Ins for Processing Credit Card Payments. 

### Customization Update to 2026 R2: Refactored CBAPIService Extension Methods 

 In Acumatica ERP 2026 R2, the extension methods previously defined in the PX.Commerce.Core.CBAPIService class have been moved to type-specific extension classes in the PX.Commerce.Core.Utilities.Extensions namespace. The original methods are now obsolete and are scheduled for removal in Acumatica ERP 2027 R2. 

 These changes do not affect functionality. They organize the methods according to the types they extend, reduce coupling, and give each extension class a clearer responsibility. 

#### Upgrade Notes 

 To determine whether your customization or integration is affected, review its code for the obsolete extension methods listed in this section—those with a replacement method and those without one. 

 Methods with a Replacement 

 The following table lists the obsolete methods and their direct replacements. The replacement extension classes are in the PX.Commerce.Core.Utilities.Extensions namespace. 

 For these methods, update the code before upgrading to Acumatica ERP 2027 R2. 

 Obsolete Method Replacement Method 

 TryCombineEntity(CBAPIEntity, CBAPIEntity, out CBAPIEntity) 

 CBAPIEntityExtensions.TryCombineEntity 

 PopulateResultEntity<ResultEntity> 

 (GenericResult, …) 

 GenericResultExtensions 

 .PopulateResultEntity 

 AddField(ActionImpl, EntityField) ActionImplExtensions.AddField 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 16 

**Obsolete Method Replacement Method** 

AddSearchField(EntityImpl, string, string, GeneralCondition) 

 EntityImplExtensions.AddSearchField 

AddSearchField(EntityImpl, string, string, string, GeneralCondition) 

 EntityImplExtensions.AddSearchField 

AddReturnField(EntityImpl, string) EntityImplExtensions.AddReturnField 

TryGetValueField(object, Type, out string) 

 ObjectExtensions.TryGetValueField 

GetValueFromEntityField(object, Type) ObjectExtensions 

 .GetValueFromEntityField 

CreateCustomFieldCopy(CustomField) CustomFieldExtension 

 .CreateCustomFieldCopy 

ValueField(string, bool) StringExtensions.ValueField 

ValueField(int) IntExtensions.ValueField 

ValueField(int?, bool) IntExtensions.ValueField 

ValueField(decimal) DecimalExtensions.ValueField 

ValueField(decimal?, bool) DecimalExtensions.ValueField 

ValueField(short) ShortExtensions.ValueField 

ValueField(short?, bool) ShortExtensions.ValueField 

ValueField(bool) BooleanExtensions.ValueField 

ValueField(bool?, bool) BooleanExtensions.ValueField 

ValueField(byte?, bool) ByteExtensions.ValueField 

ValueField(double?, bool) DoubleExtensions.ValueField 

ValueField(DateTime) DateTimeExtensions.ValueField 

ValueField(DateTime?, bool) DateTimeExtensions.ValueField 

ValueField(long?, bool) LongExtensions.ValueField 

ValueField(Guid) GuidExtensions.ValueField 

ValueField(Guid?, bool) GuidExtensions.ValueField 

SearchField(string, StringCondition) StringExtensions.SearchField 

SearchField(int, IntCondition) IntExtensions.SearchField 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 17 

 Obsolete Method Replacement Method 

 SearchField(int?, IntCondition) IntExtensions.SearchField 

 SearchField(Guid?, GuidCondition) GuidExtensions.SearchField 

 ToDate(string, PXTimeZoneInfo) StringExtensions.ToDate 

 ToDate(object, bool, PXTimeZoneInfo) ObjectExtensions.ToDate 

 TDToString(DateTime?, PXTimeZoneInfo, string) 

 DateTimeExtensions.TDToString 

 ToDecimal(string, NumberStyles) StringExtensions.ToDecimal 

 ToInt(string) StringExtensions.ToInt 

 ToInt(object) ObjectExtensions.ToInt 

 ToLong(string) StringExtensions.ToLong 

 ToGuid(object) ObjectExtensions.ToGuid 

 KeyCombine(object[]) ObjectExtensions.KeyCombine 

 KeySplit(string, int, string) StringExtensions.KeySplit 

 IsComplexKey(string, int) StringExtensions.IsComplexKey 

 FieldsSplit(string, int, string, params string[]) 

 StringExtensions.FieldsSplit 

 FirstNotEmpty(string[]) StringExtensions.FirstNotEmpty 

 HasParent(string) StringExtensions.HasParent 

**Obsolete Methods with No Replacement** 

The following obsolete methods have no replacement method provided: 

- AddField(EntityImpl, EntityField) 

- AddValueField(EntityImpl, string, object) 

- AddObjectField(EntityImpl, string, string, EntityImpl) 

- AddListField(EntityImpl, string, EntityImpl) 

- GetValueField(EntityImpl, string) 

- GetObjectField(EntityImpl, string) 

- GetListField(EntityImpl, string) 

- ValueField(byte) 

- ValueField(double) 

- ValueField(long) 

- SearchField(decimal, DecimalCondition) 

- SearchField(decimal?, DecimalCondition) 

- SearchField(short, ShortCondition) 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 18 

- SearchField(short?, ShortCondition) 

- SearchField(bool, BooleanCondition) 

- SearchField(bool?, BooleanCondition) 

- SearchField(byte, ByteCondition) 

- SearchField(byte?, ByteCondition) 

- SearchField(double, DoubleCondition) 

- SearchField(double?, DoubleCondition) 

- SearchField(DateTime, DateTimeCondition) 

- SearchField(DateTime?, DateTimeCondition) 

- SearchField(long, LongCondition) 

- SearchField(long?, LongCondition) 

- SearchField(Guid, GuidCondition) 

- ToLong(object) 

- ToBolean(string) 

- TrimExternID(string) 

- FieldCombine(string[]) Acumatica ERP does not use these methods, and marking them as obsolete does not introduce a breaking change in Acumatica ERP 2026 R2. The methods are scheduled for removal in Acumatica ERP 2027 R2. If your customization uses one of them, you may need to implement and maintain equivalent logic in your own code. 

### Customization Update to 2026 R2: Removal of Obsolete Commerce APIs 

 In Acumatica ERP 2026 R2, a number of obsolete methods, properties, and classes have been removed from the Commerce functional area. These items had already been marked with the [Obsolete] attribute in earlier releases. 

 This cleanup does not change any functionality. However, if you’ve developed customization projects or integrations that reference or override the removed APIs, you may need to update that code. 

#### Upgrade Notes 

 Before the upgrade, you need to review customization or integration code that uses APIs for Amazon, BigCommerce, or Shopify connectors. If your code overrides a removed virtual method, remove the override or migrate the customization to the replacement listed for the removed item. 

 The following sections list the removed obsolete items. 

#### Removed Amazon Connector APIs 

 The following items have been removed from the PX.Commerce.Amazon namespace. 

 Removed Item Replacement or Action 

 The AmazonInvoiceProcessor and AmazonInvoiceBucket classes 

 Use the AmazonFBASalesOrderProcessor class. 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 19 

 Removed Item Replacement or Action 

 The AmazonHelper.GetInventoryCDByExternID( 

 string sku, string asin, 

 string message, out string uom) 

 overload 

 Use the AmazonHelper.GetInventoryCDByExternID( 

 SearchInventoryItemOption) overload. 

 The SearchInventoryItemOption type is located in the PX.Commerce.Objects namespace. 

#### Removed BigCommerce Connector APIs 

 The following items have been removed from the PX.Commerce.BigCommerce namespace. 

 Removed Item Replacement or Action 

 The BCHelper.GetInventoryCDByExternID(..., out string uom, out string alternateID) overload 

 Use the BCHelper.GetInventoryCDByExternID( 

 SearchInventoryItemOption) overload. 

 The BCHelper.GetInventoryCDByExternID(..., out string uom, out string alternateID, out string itemStatus) overload 

 Use the BCHelper.GetInventoryCDByExternID( 

 SearchInventoryItemOption) overload. 

#### Removed Shopify Connector APIs 

 The following items have been removed from the PX.Commerce.Shopify namespace. 

 Removed Item Replacement or Action 

 TheSPHelper.AddCreditCardProcessingInfo( 

 BCPaymentMethods methodMapping, 

 Payment payment, string transaction- Type) method 

 Use the SPHelper.AddCreditCardInfo( 

 string processingCenterID, Payment payment, string paymentID, string transactionType) method. 

 The SPHelper.GetInventoryCDByExternID(..., out string uom, out string alternateID, out string itemStatus) overload 

 Use the SPHelper.GetInventoryCDByExternID( 

 SearchInventoryItemOption) overload. 

 The SPHelper.GetInventoryCDByExternID(..., out string uom, out string alternateID, out string itemStatus, out bool? stkItem, out bool? nonStock- Ship) overload 

 Use the SPHelper.GetInventoryCDByExternID( 

 SearchInventoryItemOption) overload. 


<!-- PAGE_BREAK -->
 Updating Customization Projects to Acumatica ERP 2026 R2 | 20 

 Removed Item Replacement or Action 

 The SPHelper.GetSubstituteTaxName( 

 BCBindingExt bindingExt, string taxID, decimal taxRate, string countryCode, string provinceCode) method 

 Use the SPHelper.TryGetSubstituteTax- Name( 

 TaxNameSubstitutionFilter taxNameSubstitutionFilter, out string substitutedTaxName) method. 

 The SPSalesOrderProcessor.GetPayment- Terms( 

 string externalPaymentTerms, Customer customer) 

 method 

 Use the SPHelper.GetLocalPayment- Terms(...) method. 

The following items have been removed from the PX.Commerce.Shopify.API.GraphQL namespace. 

 Removed Item Replacement or Action 

 The OrderExchangeGQL class Use the OrderDataGQL class. 

 The OrderExchangeAdditionGQL class Use the OrderDataGQL class. 

 The OrderExchangeLineItemGQL class Use the OrderLineItemGQL class. 

 The OrderExchangeReturnGQL class Use the OrderDataGQL class. 

 The IOrderGQLDataProvider 

 .GetOrderExchangesAsync( 

 string orderId, CancellationToken cancellationToken) method 

 Use the IOrderGQLDataProvider.GetOrdersAsync( 

 ...) method. 

The following items have been removed from the PX.Commerce.Shopify.API.REST namespace. 

 Removed Item Replacement or Action 

 The OrderData.ExchangeOrders property Use the PX.Commerce.Shopify.API 

 .GraphQL.OrderDataGQL class. 

 The OrderLineItem.OriginLocation property Use the PX.Commerce.Shopify.API.REST 

 .FulfillmentOrder.AssignedLocationId property. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 21 

## Updating Customization Projects for the Modern UI 

 If your customization project introduces new Acumatica ERP forms or customized versions of existing Acumatica ERP forms built for the Classic UI, you need to convert them to the Modern UI to deliver these forms in Acumatica ERP 2026 R2. You can convert these forms individually or convert all of a customization project’s forms with a single action. 

### Updating a Customization Project for the Modern UI: General Information 

 This chapter describes how to convert custom and customized forms in a customization project to the Modern UI by using Acumatica ERP’s conversion tools. 

#### Learning Objectives 

 In this chapter, you’ll learn how to: 

- Convert a custom form in the Classic UI by using the form converter and include the generated Modern UI     source files in the customization project 

- Convert a single custom or customized form—or all the forms in the customization project at once—by using     the customization project converter 

#### Applicable Scenarios 

 You update a customization project for the Modern UI if you have custom or customized forms built for the Classic UI and want to convert them to the Modern UI. 

#### Overview of Customization Files 

 Any form in the Modern UI—or the customization of such a form—is defined by a pair of files (TypeScript and HTML) with identical names. The file names follow this structure: <screenID>_<customizationProjectName> (for example, IN202500_PhoneRepairShop). 

 The TypeScript file should always contain a mixin (an extension) of the original screen class. You can generate the extension code in the Modern UI Editor or write it manually. 

 The HTML file must contain a top-level <template> tag. This tag can be empty or can contain the code to customize the layout. All customization tags should be located on the same level within the top-level template tag. You can generate an HTML extension in the Modern UI Editor or create it manually. 

 For details about creating HTML and TypeScript extensions manually, see UI Customization Development: General Information. 

#### Available Built-In Converters 

 Acumatica ERP provides three built-in converters for converting custom and customized forms to the Modern UI: 

- **Custom Form Converter** : Converts only custom forms that are published to an instance in the Classic UI     to the Modern UI. This converter is ideal for converting custom forms that don’t customize any existing     Acumatica ERP form.     You start the conversion by clicking **Convert to Modern UI** on the **Customization** menu of a form. The     generated Modern UI files are not automatically included in your customization project; you need to     manually include them. For details, see _Updating a Customization Project for the Modern UI: Form Converter_. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 22 

 Even though all out-of-the-box Acumatica ERP forms have already been converted to the Modern UI and use it by default, the form converter is still be available for these forms if you manually switch them to the Classic UI. 

- **Customization Project Converter** : Converts all custom or customized forms in a customization project     to the Modern UI with a single click and automatically includes all the generated Modern UI files in the     customization project.     This converter is ideal for quickly converting all the forms in a customization project to the Modern UI.     You can also use the converter to convert individual forms within the customization project instead of     converting all the forms in the customization project at once. For details, see _Updating a Customization_     _Project for the Modern UI: Customization Project Converter_. 

 The use of these converters doesn't guarantee a perfect conversion of the forms in your customization project to the Modern UI. The converters provide a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use these converters **only in your development environment**. 

- **Always review the files** generated by the converters and **make any required corrections**. 

- Publish the converted forms to your production environment **only aer fully testing** their     functionality in your development environment. 

#### Converting a Custom Form 

 To convert a custom form, you can use Acumatica ERP’s form converter. It generates the required TypeScript and HTML files with most fields and view classes configured as they were in the Classic UI. Then you need to modify the template configuration in the HTML file (if necessary) and include the files in the customization project. 

 To convert a custom form: 

1. Configure the converter. For more details, see _UI Definition in HTML and TypeScript: Form Converter_. 

2. Open the custom form in Acumatica ERP. 

3. On the **Customization** menu, click **Convert to Modern UI**. The system:     a. Generates the files.     b. Saves them in the appropriate folder in the FrontendSources\screen\src\development        \screens\ folder of the instance. The folder's name is the first two letters of the screen ID and        represents the functional area.     c. Displays a notification when the conversion has completed.     For example, for a custom form with the _IN202510_ screen ID, the files are located in the     FrontendSources\screen\src\development\screens\IN\IN202510 folder. 

4. Review the TypeScript file and adjust it, if necessary. For example, you might:     a. Remove unnecessary import directives.     b. Fix any formatting issues.     c. Adjust the name in the viewInfo decorator, which specifies the container name. (This name is used as        an object name during the configuration of particular functionality, such as workflows and import and        export scenarios.) 

5. Review the HTML file and adjust it, if necessary. For example, you might:     a. Modify the name attribute of the qp-template tag. The layout should follow the recommendations in        _Form Layout: Predefined Templates_.     b. Change the IDs so that they match the guidelines for UI component IDs. See _UI Component Guide_. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 23 

 c. Remove the wg-container attribute if you don’t have tests for the Classic UI of this form. (For details, see Testing the Modern UI .) 

6. Include the files in the customization project: In the Customization Project Editor, click **Modern UI Files** in     the navigation pane. On the _Modern UI Files_ page, add the TypeScript and HTML files for the form. 

7. Publish the customization project.     During publishing, the system builds the Modern UI code and shows log messages in the Compilation     window. When the customization project is published successfully, you can open the form in the Modern UI. 

#### Converting a Customized Form 

 To convert a customized form, you use the customization project converter. The converter generates the Modern UI version of the original form and the Modern UI version of the customized form—and then compares them to find the difference. The converter then creates an extension of the original form in the Modern UI that includes the differences, such as added fields or modified properties of a table. 

 You can use the customization project converter to convert a single customized form or all the forms in a customization project with a single click. This converter also processes any custom forms in the project. For detailed steps to perform both scenarios, see Updating a Customization Project for the Modern UI: Customization Project Converter. 

 To convert a customized form, you perform the following general steps: 

1. On the _Customization Projects_ (SM204505) form, open the customization project with the customized form in     the Customization Project Editor. 

2. On the _Screens_ page, click the row for the form that you want to convert to the Modern UI and click **Convert**     **to Modern UI** on the page toolbar.     When the conversion has completed, the system navigates to the _Modern UI Files_ page, which displays the     extension files generated for the converted customized form. 

3. Review the generated TypeScript and HTML extension files and make any needed corrections.     You can edit the generated files on the _Modern UI Files_ page or export the files to the development folder     and then edit them. 

4. Optional: If you’ve edited the generated files in the development folder, include these changes in your     customization project. 

5. Publish the customization project. During publishing, the system builds the Modern UI code and shows log     messages in the Compilation window. When the customization project has been published successfully, you     can open the form in the Modern UI. 

### Updating a Customization Project for the Modern UI: Customization Project 

### Converter 

 You can use Acumatica's customization project converter to convert—with a single click—a customization project that contains custom forms or customized versions of original Acumatica forms to the Modern UI. Alternatively, you can use the converter to individually convert specific forms within the project instead of converting all the forms in the customization project at once. 

 Regardless of the approach you choose, the converter does the following for each customized form: 

- Generates the Modern UI version of the original form and the Modern UI version of the customized form—     and then compares them to find the differences 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 24 

- Creates extension files for the original form in the Modern UI that include the difference, such as added     fields or modified table properties 

- Adds the extension files to the _Modern UI Files_ files page of the Customization Project Editor For each custom form, the converter does the following: 

- Generates the Modern UI version of the custom form by converting its ASPX code to TypeScript and HTML 

- Adds the generated TypeScript and HTML source files to the _Modern UI Files_ files page of the Customization     Project Editor 

 The use of the customization project converter doesn't guarantee a perfect conversion of the forms in your customization project to the Modern UI. The converter provides a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use the converter **only in your development environment**. 

- **Always review the files** generated by the converter and **make any required corrections**. 

- Publish the converted forms to your production environment **only aer fully testing** their     functionality in your development environment. 

#### Prerequisites for Using the Customization Project Converter 

 Before you use the converter, make sure the following requirements are met: 

- The Modern UI has been enabled and set as the default UI in your instance. For details, see _Modern UI_     _Development: General Information_. 

- The customization project you want to convert has already been published. 

- The _Customizer_ role has been assigned to your user account. 

 You must have the Customizer role to run the converter on a customization project or on a specific form within the project. 

- All Acumatica ERP features related to the form have been enabled before the conversion. This gives you the     converted version that’s the most similar to the original version. 

 The converter ignores any JavaScript code in ASPX files or the code in the ASPX.CS files. 

#### Running the Customization Project Converter on a Customization Project 

 To run the converter on an entire customization project: 

1. Open the _Customization Projects_ (SM204505) form and select the row in the table for the customization     project you want to convert to the Modern UI. 

2. On the form toolbar, click **Convert to Modern UI**.     The system displays a notification indicating that the conversion has started and updates it when the     conversion has completed.     As part of the conversion, the converter generates the following extension files for each customized form     that it converted to the Modern UI: 

- [SCREENID]_[CUSTOMIZATION_PROJECT_NAME]_converted.ts, which contains the     differences in TypeScript code between the original and customized versions of the form 

- [SCREENID]_[CUSTOMIZATION_PROJECT_NAME]_converted.html, which contains the     differences in HTML code between the original and customized versions of the form 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 25 

 When you publish the customization project, these files are saved in the FrontendSources \screen\src\customizationScreens\[TENANT_NAME]\screens \[FIRST_TWO_LETTERS_OF_SCREENID\[SCREENID]\extensions folder of your instance. The converter generates the following source files for each custom form that it converted to the Modern UI: 

- [SCREENID].ts, which contains the initialization of views for the form 

- [SCREENID].html, which contains the HTML layout of the form When you publish the customization project, these files are saved in the FrontendSources \screen\src\customizationScreens\[TENANT_NAME]\screens \[FIRST_TWO_LETTERS_OF_SCREENID\[SCREENID] folder of your instance. 

3. Open the converted customization project in the Customization Project Editor and click **Modern UI Files** in     the navigation pane. The _Modern UI Files_ page opens. Here you’ll find a list of the TypeScript and HTML files     for all the forms that were converted to the Modern UI. 

4. Review the generated TypeScript and HTML files and make any needed corrections. For example, for a     custom form that was converted, you may need to correct the IDs of some tags in the HTML code so that     they follow established naming conventions. For details, see _UI Component Guide_.     You can make changes to the generated files on the _Modern UI Files_ page or export the files to the     development folder (by clicking **Export to Development Folder** on the page toolbar) and edit them in     an external editor. For details about using the development folder, see _Modern UI Development: Creating_     _Modern UI Source Files for Custom and Customized Forms_. 

5. If you use the development folder to modify the generated files, you need to update these files in the     customization project. You do this by clicking **Detect Modified Files** on the _Modern UI Files_ page. 

6. Publish the customization project and open the forms in your instance to verify that they were converted     correctly. 

#### Running the Customization Project Converter on a Specific Customized Form 

 To run the customization converter on a specific customized form within a customization project: 

1. On the _Customization Projects_ (SM204505) form, open the customization project in the Customization Project     Editor. 

2. On the _Screens_ page, click the row for the form that you want to convert to the Modern UI and click **Convert**     **to Modern UI** on the page toolbar.     The system displays a notification indicating that the conversion has started.     When the conversion has completed, the system navigates to the _Modern UI Files_ page, which displays the     extension files that were generated for the converted form: 

- [SCREENID]_[CUSTOMIZATION_PROJECT_NAME]_converted.ts, which contains the     difference in the TypeScript code of the original and customized versions of the form 

- [SCREENID]_[CUSTOMIZATION_PROJECT_NAME]_converted.html, which contains the     difference in the HTML code of the original and customized versions of the form For example, if the customized form that you converted was the _Stock Items_ (IN202500) form and the name of your customization project was _PhoneRepairShop_ , the extension files generated from the conversion operation would be named as follows: 

- IN202500_PhoneRepairShop_converted.ts 

- IN202500_PhoneRepairShop_converted.html Aer you published the customization project, the converter would save these files in the FrontendSources\screen\src\customizationScreens\[TENANT_NAME]\screens\\IN \IN202500\extensions folder of your instance. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 26 

 If the screen is already customized in this project in the Modern UI, this customization will be overridden by the one generated by the converter. 

3. Review the generated TypeScript and HTML extension files and make any needed corrections,. For example,     in the HTML code, you may need to correct the ID of a qp-fieldset tag (so that it matches the ID     specified for this tag in the original HTML code of the form) if your customization of the form adds a UI     element to an existing section of a form.     You can make changes to the generated files on the _Modern UI Files_ page or export the files to the     development folder—by clicking **Export to Development Folder** on the page toolbar—and edit the     files in an external editor. For details about using the development folder, see _Modern UI Development:_     _Creating Modern UI Source Files for Custom and Customized Forms_. 

4. Optional: If you’ve edited the generated files in the development folder, update these files in the     customization project. To do this, click **Detect Modified Files** on the _Modern UI Files_ page. 

5. Publish the customization project and open the form in your instance to verify that it was converted     correctly. 

### Updating a Customization Project to the Modern UI: To Convert a Customization 

### Project 

 This activity will walk you through the process of migrating the entire customization project to the Modern UI. You'll convert the entire project by using the customization project converter. 

 The use of the customization project converter doesn't guarantee a perfect conversion of a form to the Modern UI. The converter provides a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use the converter **only in your development environment**. 

- **Always review the files** generated by the converter and **make any required corrections**. 

- Publish the converted form to your production environment **only aer fully testing** its     functionality in your development environment. 

#### Story 

 Suppose that you have a customization project that contains multiple changes in the Classic UI such as a customized Stock Items (IN202500) form and custom forms Repair Services (RS201000), Serviced Devices (RS202000), and Services and Prices (RS203000). You need to migrate all of those files to the Modern UI. 

#### Process Overview 

 You will use the customization project converter to convert the entire project. The converter will generate TypeScript and HTML files for custom forms and TypeScript and HTML extension files for the customized form. You will review the generated files and make necessary changes to them. You will then publish the corresponding customization project and view the Modern UI of the customized form. 

#### System Preparation 

 Before you begin converting the customization project, do the following: 

1. Deploy an instance of Acumatica ERP with the T100 dataset. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 27 

2. Optional: If you plan to build code manually, perform the prerequisite actions and build the source code for     the first time, as described in _Modern UI Development: To Build the Source Code of All Acumatica ERP Forms_     _for Modern UI Development_. 

3. Download the T210.zip archive that contains the customization project file from GitHub. The project     contains the Classic UI files for the forms that are implemented and customized throughout the _T200_     _Maintenance Forms_ and _T210 Customized Forms and Master-Details Relationships_ courses. 

#### Step 1: Loading and Converting the Customization Project 

 To convert the customization project, do the following: 

1. On the Customization Projects (SM204505) form, import the customization project:     a. On the form toolbar, click **Import**.     b. In the **Open Package** dialog box, choose the T210.zip file.     c. Click **Upload**.        The project is displayed on the Customization Projects form. 

2. Publish the customization project. 

3. On the form toolbar, click **Convert to Modern UI**.     The system generates the TypeScript and HTML files for each form in the project. 

#### Step 2: Reviewing the Generated Files and Correcting If Necessary 

 To review the code that the system has generated in the previous step, do the following: 

1. On the Customization Projects (SM204505) form, open the T210 project.     The Customization Project Editor opens. 

2. On the _Modern UI Files_ page, notice the following files: 

- IN202500_PhoneRepairShop_converted.ts 

- IN202500_PhoneRepairShop_converted.html 

- RS201000_PhoneRepairShop_converted.ts 

- RS201000_PhoneRepairShop_converted.html 

- RS202000_PhoneRepairShop_converted.ts 

- RS202000_PhoneRepairShop_converted.html 

- RS203000_PhoneRepairShop_converted.ts 

- RS203000_PhoneRepairShop_converted.html 

3. Review the code and make changes if necessary: 

- Correct the generates IDs according to coding conventions for each control. 

- Modify template names according to the layout recommendations for different types of forms. 

4. Save your changes. 

#### Step 3: Publishing the Project and Viewing the Form 

 Now you will publish the customization project and view the customized form in the Modern UI. Do the following: 

1. Publish the customization project. 

2. Open the following forms and make sure they are correctly displayed in the Modern UI: 

- Repair Services (RS201000) 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 28 

- Serviced Devices (RS202000) 

- Services and Prices (RS203000) 

 If a form doesn't already open in the Modern UI, click Tools > Switch to Modern UI on the form title bar. The Modern UI for the form will be displayed. 

3. Open the _Stock Items_ (IN202500) form. 

4. Select the _BAT3310EX_ item in the table. 

5. On the **General** tab ( **Item Defaults** section), make sure the **Repair Item** check box and the **Repair Item**     **Type** box are visible. 

6. Select the **Repair Item** check box. Make sure that the **Repair Item Type** box is available because the **Repair**     **Item** check box is selected, as shown below. 

 Figure: Custom boxes on the Stock Items form 

7. Make sure that the **Compatible Devices** tab is displayed, as shown below. (The tab is displayed because the     **Repair Item** check box is selected on the **General** tab.) 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 29 

 Figure: A custom tab on the Stock Items form 

8. On the **Compatible Devices** tab, add the _Nokia3310_ device to the list. 

9. Save your changes. 10.Select the _HEADSET_ item and make sure that the **Compatible Devices** tab is not displayed for this item.     (This is because the **Repair Item** check box is cleared.) 

### Updating a Customization Project for the Modern UI: To Convert a Customized Form 

 The following activity will walk you through the conversion of a customized Acumatica ERP form from the Classic UI to the Modern UI. You’ll convert the form by using the customized form converter. 

 The use of the customized form converter doesn't guarantee a perfect conversion of a form to the Modern UI. The converter provides a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use the converter **only in your development environment**. 

- **Always review the files** generated by the converter and **make any required corrections**. 

- Publish the converted form to your production environment **only aer fully testing** its     functionality in your development environment. 

#### Story 

 Suppose that you’ve customized the Stock Items (IN202500) form for the Smart Fix company. The customization project, developed for a previous version of Acumatica ERP, contains files created for the Classic UI. You need to convert the customized form to the Modern UI and want to use the customization project converter. 

#### Process Overview 

 You will use the customized form converter to convert the customized form and generate the TypeScript and HTML extension files. You will review the generated files and make necessary changes to them. You will then publish the corresponding customization project and view the Modern UI of the customized form. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 30 

#### System Preparation 

 Before you begin converting the customized Stock Items (IN202500) form, do the following: 

1. Complete the following prerequisite activity: _Modern UI Development: To Deploy an Instance with Custom_     _Forms and the Modern UI_. The prepared instance contains the customized _Stock Items_ (IN202500) form in the     Classic UI. 

2. Optional: If you plan to build code manually, perform the prerequisite actions and build the source code for     the first time, as described in _Modern UI Development: To Build the Source Code of All Acumatica ERP Forms_     _for Modern UI Development_. 

#### Step 1: Converting the Customized Form 

 To convert the customized Stock Items (IN202500) form and generate the TypeScript and HTML extensions, do the following: 

1. Publish the _PhoneRepairShop_ customization project (if it's not already published). 

2. On the _Customization Projects_ (SM204505) form, open the _PhoneRepairShop_ customization project in the     Customization Project Editor. 

3. On the _Screens_ page, click the row for the _Stock Items_ form and click **Convert to Modern UI** on the page     toolbar.     The system displays a notification indicating that the conversion operation has started.     When the operation has completed, the system navigates to the _Modern UI Files_ page, which displays the     extension files that were generated for the converted form: 

- IN202500_PhoneRepairShop_converted.ts, which contains the difference in the TypeScript     code of the original and customized versions of the form 

- IN202500_PhoneRepairShop_converted.html, which contains the difference in the HTML code     of the original and customized versions of the form 

 Now you can review the generated extension files and make some necessary changes. 

#### Step 2: Reviewing the Code of the TypeScript Extension 

 To review the code of the TypeScript extension that was generated in the previous step, open the IN202500_PhoneRepairShop_converted.ts file on the Modern UI Files page. 

 Notice the following additions in the extension file, which represents the differences between the original code of the form and its customized version: 

- The CompatibleDevices view, which is initialized in the     IN202500_PhoneRepairShop_converted class that extends the IN202500 screen class 

- The UsrRepairItem and UsrRepairItemType fields added in the     IN202500_ItemSettings_PhoneRepairShop_converted view class, which extends the     ItemSettings view class 

- The RSSVStockItemDevice grid view class 

#### Step 3: Reviewing the Code of the HTML Extension 

 To review the code of the HTML extension that was generated in the previous step, open the IN202500_PhoneRepairShop_converted.html file on the Modern UI Files page. 

 Notice the following additions in the extension file, which represents the differences between the original code of the form and its customized version: 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 31 

- The field tag that adds the custom UsrRepairItem field aer the existing ItemType field. 

- The field tag that adds the custom UsrRepairItemType field aer the custom UsrRepairItem     field. 

- The qp-tab tag with the _Compatible Devices_ caption; this tag adds a tab with the same name     aer the **Price/Cost** tab on the form. This qp-tab tag contains the qp-grid tag bound to the     CompatibleDevices view. Due to the conversion from ASPX to HTML, the converter may sometimes add incorrect IDs for some tags or use IDs that don’t follow the established naming conventions. 

 Update the IN202500_PhoneRepairShop_converted.html file on the Modern UI Files page as follows: 

1. Make sure the values of the after attribute for the two field tags are the same as the ones shown in the     following list. The ID of the fieldset to which they should be added is fsItemDefaults-General: 

- <field after="#fsItemDefaults-General FIELD[name='ItemType']"     name="UsrRepairItem"></field> 

- <field after="#fsItemDefaults-General FIELD[name='UsrRepairItem']"     name="UsrRepairItemType"></field> 

2. Make sure the qp-tab tag is defined as follows: <qp-tab id="tab-CompatibleDevices"     after="#tab-PriceCost" caption="Compatible Devices">. 

3. Correct the ID for the <qp-grid> tag as follows so that the ID follows established naming conventions:     <qp-grid id="grid-CompatibleDevices" view.bind="CompatibleDevices"></qp-     grid>.     The final code of the IN202500_PhoneRepairShop_converted.html file is shown below. 

 <template> <field after="#fsItemDefaults-General FIELD[name='ItemType']" name="UsrRepairItem"> </field> <field after="#fsItemDefaults-General FIELD[name='UsrRepairItem']" name="UsrRepairItemType"> </field> <qp-tab id="tab-CompatibleDevices" after="#tab-PriceCost" caption="Compatible Devices"> <qp-grid id="grid-CompatibleDevices" view.bind="CompatibleDevices"></qp-grid> </qp-tab> </template> 

4. Save your changes to the file. 

#### Step 4: Publishing the Project and Viewing the Form 

 Now you will publish the customization project and view the customized form in the Modern UI. Do the following: 

1. Publish the customization project. 

2. Open the _Stock Items_ (IN202500) form. 

3. Select the _BAT3310EX_ item in the table. 

4. If the form doesn't already open in the Modern UI, click **Tools > Switch to Modern UI** on the form title bar.     The Modern UI for the form is displayed. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 32 

5. On the **General** tab ( **Item Defaults** section), make sure the **Repair Item** check box and the **Repair Item**     **Type** box are visible. 

6. Select the **Repair Item** check box. Make sure that the **Repair Item Type** box is available because the **Repair**     **Item** check box is selected, as shown below. 

 Figure: Custom boxes on the Stock Items form 

7. Make sure that the **Compatible Devices** tab is displayed, as shown below. (The tab is displayed because the     **Repair Item** check box is selected on the **General** tab.) 

 Figure: A custom tab on the Stock Items form 

8. On the **Compatible Devices** tab, add the _Nokia3310_ device to the list. 

9. Save your changes. 

10.Select the _HEADSET_ item and make sure that the **Compatible Devices** tab is not displayed for this item. (This is because the **Repair Item** check box is cleared.) 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 33 

### Updating a Customization Project for the Modern UI: Form Converter 

 You can use Acumatica's form converter, which transforms an Acumatica ERP form from the Classic UI to the Modern UI. The converter parses an ASPX page of the form and generates the source files of the form in the Modern UI. These source files include a TypeScript definition and initialization of views and an HTML layout of the form. 

 The use of the form converter doesn't guarantee a perfect conversion of a form to the Modern UI. The converter provides a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use the converter **only in your development environment**. 

- **Always review the files** generated by the converter and **make any required corrections**. 

- Publish the converted form to your production environment **only aer fully testing** its     functionality in your development environment. 

#### Running the Converter 

 To use the converter, you need to first make sure that the Modern UI is enabled for your instance. For details on this, see Modern UI Development: General Information. You also need to check whether the following key exists in the appSettings section of the Web.config file of your Acumatica ERP instance: <add key="EnableSiteMapSwitchUI" value="False" />. If this key exists, remove it and save your changes to the file. 

 To run the converter, you open the needed Acumatica ERP form in the Classic UI and click Customization > Convert to Modern UI on the form title bar. 

 The Convert to Modern UI command appears on the form only if the Customizer role is assigned to your user account. 

 Aer you execute this command, the following files are generated: 

- views.ts, which contains declarations of all views that are used in the form 

- [SCREENID].ts, which contains the initialization of views for the form 

- [SCREENID].html, which contains the HTML layout of the form By default, the files are saved in a ZIP archive, which you can download. 

- Before conversion, you need to turn on all Acumatica ERP features related to the form. This     will give you the converted version that’s the most similar to the original. 

- The converter ignores any JavaScript code in ASPX files or the code in the ASPX.CS files. 

#### Configuring the Converter 

 You can modify the behavior of the converter by adjusting the px.core\ui\screenConverter tag of the web.config file of the instance, as shown in the following example. 

 <ui> <screenConverter declareViewsInViewModelFile="false" /> </ui> 

 You can use any of the following properties of the screenConverter tag: 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 34 

- declareViewsInViewModelFile: If you set this property to _True_ , the converter will declare the views     in the <ScreenID>.ts file instead of creating a separate views.ts file. 

- shouldFilesBeDownloaded: If you set this property to _False_ , the files are saved in the     folder that’s defined by the screenConverterOutputFolder property. By default, the     shouldFilesBeDownloaded property is _True_ and the files are saved in a ZIP archive. 

- screenConverterOutputFolder: You can use this property to specify the output folder for     the generated files. Use this property only if the shouldFilesBeDownloaded property is _False_.     By default, the output folder is FrontendSources\screen\src\development\screens     \[FirstTwoLettersOfSCREENID]\[SCREENID]. 

- usingOfPXJoinSyntaxEnabled: If you set this property to _True_ , the system uses the approach for     joined fields, which involves the use of periods. For details on the approaches to define joined fields, see _UI_     _Definition in HTML and TypeScript: Joined Fields_. By default, this property is _True_. 

- isAutoFormatEnabled: If you set this property to _True_ , the system uses the Prettier tool to     automatically format the HTML and TypeScript code generated by the converter. 

### Updating a Customization Project for the Modern UI: To Convert a Custom Form 

 The following activity will walk you through the conversion of a custom Acumatica ERP form from the Classic UI to the Modern UI. You’ll convert the form by using the form converter. 

 The use of the form converter doesn't guarantee a perfect conversion of a form to the Modern UI. The converter provides a baseline conversion that you should further fine-tune based on your specific requirements. We strongly recommend that you: 

- **Make necessary backups** and use the converter **only in your development environment**. 

- **Always review the files** generated by the converter and **make any required corrections**. 

- Publish the converted form to your production environment **only aer fully testing** its     functionality in your development environment. 

 You can also use the customization project converter to complete this activity. For details on how to use this converter, see Updating a Customization Project for the Modern UI: Customization Project Converter. 

#### Story 

 Suppose that you’ve developed the Serviced Devices (RS202000) form for the Smart Fix company. The form has been developed for a previous version of Acumatica ERP and is displayed in the Classic UI. You need to convert the form to the Modern UI and want to use the form converter. 

#### Process Overview 

 You will modify the converter settings to fit your needs and convert the form to the Modern UI. You’ll then review the contents of the TypeScript and HTML files and adjust them. You will include the Modern UI files in the customization project, publish it, and review the resulting form. 

#### System Preparation 

 Before you begin converting the Serviced Devices (RS202000) form, do the following: 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 35 

1. Complete the following prerequisite activity: _Modern UI Development: To Deploy an Instance with Custom_     _Forms and the Modern UI_. The prepared instance contains the Serviced Devices (RS202000) form in the     Classic UI. 

2. Optional: If you plan to build code manually, perform the prerequisite actions and build the source code for     the first time, as described in _Modern UI Development: To Build the Source Code of All Acumatica ERP Forms_     _for Modern UI Development_. 

#### Step 1: Adjusting the Converter Settings 

 The form converter comes with default settings. You need to adjust them to have the following results aer conversion: 

- The views are declared in the RS202000.ts file instead of in a separate views.ts file. 

- The files of the Serviced Devices (RS202000) form are saved in the FrontendSources\screen\src     \development\screens\RS\RS202000 folder of the instance instead of a ZIP file. To configure the converter, add the shouldFilesBeDownloaded and declareViewsInViewModelFile attributes in the px.core\ui\screenConverter tag of the web.config file of the instance, as shown in the following code. 

 <ui> <screenConverter usingOfPXJoinSyntaxEnabled="true" shouldFilesBeDownloaded="false" declareViewsInViewModelFile="true"/> </ui> 

 The usingOfPXJoinSyntaxEnabled attribute is specified in the web.config file by default. 

#### Step 2: Generating the Source Files with the Converter 

 Now you can generate the source files of the form by using the converter. To generate the files, do the following: 

1. Open the Serviced Devices (RS202000) form. 

2. On the **Customization** menu, click **Convert to Modern UI**.     The system generates the files, saves them in the FrontendSources\screen\src\development     \screens\RS\RS202000 folder of the instance, and displays a notification that the conversion has     completed. 

3. Close the notification by clicking **OK**. 

#### Step 3: Adjusting the Generated TypeScript File 

 The generated TypeScript file may contain unnecessary import directives. To clean up the code, do the following: 

1. Review the RS202000.ts file.     The TypeScript code contains the RS202000 screen class, which extends the PXScreen class and includes     a property for the data view of the form. The code also contains the RSSVDevice view class, which extends     the PXView class. 

2. Adjust the file as follows:     a. Remove unnecessary import directives.     b. Fix any formatting issues. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 36 

 c. Adjust the name in the viewInfo decorator, which specifies the container name. (This name is used as an object name during the configuration of the particular functionality, such as workflows and import and export scenarios.) The resulting file looks as follows. 

 import { createSingle, PXScreen, graphInfo, viewInfo, PXView, PXFieldState } from "client-controls"; 

 @graphInfo({ graphType: "PhoneRepairShop.RSSVDeviceMaint", primaryView: "ServDevices", }) export class RS202000 extends PXScreen { @viewInfo({containerName: "Service Devices"}) ServDevices = createSingle(RSSVDevice); } 

 // View export class RSSVDevice extends PXView { DeviceCD : PXFieldState; Description : PXFieldState; Active : PXFieldState; AvgComplexityOfRepair : PXFieldState; } 

#### Step 4: Adjusting the Generated HTML File 

 The generated HTML file may contain unnecessary code elements and inaccurate IDs. To adjust the file, do the following: 

1. Review the RS202000.html file.     The HTML code includes one qp-template element with the 1-1 name, which organizes the elements on     the form into two columns of equal width. Each column is defined with the qp-fieldset element, which     is marked with the slot attribute to identify the column of the template to which the fieldset belongs. Each     fieldset includes the field elements for the form’s UI elements. 

2. Adjust the file as follows:     a. Move fields from the fieldset with slot="B" to the end of the fieldset with slot="A", and remove the        fieldset with slot="B". Since the form has only four fields, it’s better to organize them in one column.     b. Change the IDs so that they match the guidelines for IDs. You can use the following IDs: 

- For the qp-template tag: form-ServDevices 

- For the qp-fieldset tag: fsColumnA 

 You can find the guidelines for IDs of particular UI components in UI Component Guide. 

 c. Remove the wg-container attribute because you don’t have tests for the Classic UI of the Serviced Devices (RS202000) form, which can be reused for the Modern UI. (For details about the tests, see Testing the Modern UI .) d. Fix any formatting issues. The resulting HTML code looks as follows. 

 <template> 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 37 

 <qp-template id="form-ServDevices" name="1-1"> <qp-fieldset id="fsColumnA" slot="A" view.bind="ServDevices"> <field name="DeviceCD"></field> <field name="Description"></field> <field name="Active"></field> <field name="AvgComplexityOfRepair"></field> </qp-fieldset> </qp-template> </template> 

#### Step 5: Publishing the Project and Viewing the Form 

 At this point, all Modern UI files for the form are prepared. You can build the code of the form manually from the console to make sure the files are correct, or you can include the files in the customization project and publish it. When the customization project is being published, the system builds the Modern UI code and displays any errors. For details on building the code manually, see Modern UI Development: Building the Source Code. 

 To include the Modern UI source files in the customization project, publish it, and view how the converted form looks in the Modern UI, do the following: 

1. Include the Modern UI files in the customization project:     a. Open the Customization Project Editor.     b. In the navigation pane, click **Modern UI Files**.     c. On the _Modern UI Files_ page toolbar, click **Add New Record**.     d. In the **Add Files** dialog box, select the RS202000.html and RS202000.ts files, which are located in        the FrontendSources\screen\src\development\screens\RS\RS202000 folder.     e. Click **Save**. 

2. Publish the customization project. 

3. Open the Serviced Devices (RS202000) form. 

4. While you’re on the Classic UI of the Serviced Devices (RS202000) form, click **Tools > Switch to Modern UI**     on the form title bar. The form is shown in the Modern UI. 

5. In the **Device Code** box, click the magnifier button.     The lookup table opens, as shown below. 


<!-- PAGE_BREAK -->
 Updating Customization Projects for the Modern UI | 38 

 Figure: The lookup table 

6. In the lookup table, select _MotorRAZR_. 

 The remaining elements on the form are filled in with the MotorRAZR device’s settings, as shown below. 

 Figure: The device settings 

7. Clear the **Active** check box. 

8. On the form toolbar, click **Save**. 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 39 

## Migrating JavaScript and ASPX.CS Code to the Modern UI 

 When you convert a customized Acumatica ERP form from the Classic UI to the Modern UI, the conversion tools migrate the standard ASPX markup but do not migrate custom JavaScript or code in ASPX.CS files. You need to review this custom frontend logic and determine whether it is already supported in the Modern UI or must be reimplemented. 

 This chapter explains how to select an approach for migrating custom frontend code, use tools that can assist with the migration, and implement and test a TypeScript event handler that replaces code from an ASPX.CS file. 

### Migrating Custom Frontend Code: General Information 

 In most cases, you can migrate Acumatica ERP forms from the Classic UI to the Modern UI by using the available conversion tools. However, forms that contain custom frontend logic, such as JavaScript code or code-behind implementations in ASPX.CS files, may require additional migration work. This section explains how to identify whether such customization needs a special approach and migrate them to the Modern UI. 

#### Learning Objectives 

- Identify the way that the frontend logic should be migrated 

- Migrate logic by writing code on TypeScript 

- Migrate logic by modifying backend code 

#### Applicable Scenarios 

 You need to migrate the custom frontend code when a form in the Classic UI 

- Includes inline JavaScript code 

- Has logic implemented in the ASPX.CS file 

#### Approaches for Migrating Custom Frontend Code 

 If a form in the Classic UI has custom frontend code, there are three cases it can be migrated to the Modern UI: 

- **No action needed**. Some of the logic implemented using JavaScript or ASPX.CS has already been     implemented out-of-the-box in the Modern UI. 

- **Use Modern UI capabilities** : Implement event handlers, write code in TypeScript classes, use configuration     properties in HTML. 

- **Use predefined UI definitions** : Some of the logic that was implemented multiple times in the Classic UI     forms has been united into predefined UI definitions 

- **Modify backend** code of a form. 

#### When No Migration Needed 

 You do not need to perform migration of the JavaScript or ASPX.CS code in the following cases: 

- The Modern UI includes a control that already includes a functionality that was implemented by custom     code. Before migration, you need to research existing Modern UI controls and replace the standard control     from the Classic UI with the new one implemented only in the Modern UI. Examples of controls that exist     only in the Modern UI or have functionality that has been greatly enhanced compared to the Classic UI are     shown in the following table. 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 40 

 Classic UI control with custom code 

 Modern UI control Comment 

 PXTextEdit for barcode input Barcode editor (qp-barcode-input) 

 The barcode editor includes all logic needed for barcode scanning out of the box. 

 PXGrid Data feed (qp-data-feed) Data feed is a new more powerful representation of a grid that can display multiple entities and a menu for each row. 

 PXFileUploader Upload Files Button (qp-multi-upload) 

 A button that can be placed anywhere on the form to upload multiple files and an area where the files can be dropped. 

- The Modern UI logic and layout covers the functionality implemented in JavaScript or ASPX.CS. All     calculations of control sizes are not applicable in the Modern UI because it recalculates the sizes of controls     depending on the Acumatica design guidelines and relative to the screen size. We do not recommend     changing that logic. 

- The frontend code in the Classic UI was serving as a fix when data from backend was not updated correctly.     In the Modern UI, update of data from backend has been improved so that you don't need to sync values in     frontend. 

#### Use of Modern UI Capabilities 

 If the code in the ASPX.CS file contains such logic as label assignments, declaration of variables, or configuration of values, you can use implement this logic in the TypeScript code of the form in the Modern UI. The following table lists scenarios that may be implemented in ASPX.CS and how to migrate them to the Modern UI. 

 ASPX.CS TypeScript or HTML 

 Register variables Declare properties in screen and view classes 

 Configure box values Define values using decorators or event handlers 

 Set label values Use the caption property of the fieldConfig decorator. 

 Complex controls such as table ( qp-grid ) and tab ( qp-tabbar and qp-tab ) have predefined hooks. You can define a method and specify it for the hook. For the list of predefined hooks, see the Frontend API Reference. 

 The following table shows examples of how the code in the ASPX.CS file in the Classic UI has been migrated to the Modern UI with the use of predefined hooks. The examples implement the matrix mode for the table. 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 41 

 Classic UI Modern UI ASPX: 

 <px:PXGrid ID="MatrixMatrix" OnColumnsGenerated="MatrixMatrix_ColumnsGenerated" OnRowDataBound="MatrixMatrix_RowData- Bound" OnAfterSyncState="MatrixMatrix_AfterSyncState"> <Levels> <px:PXGridLevel DataMember="Matrix" /> </Levels> ... </px:PXGrid> 

##### ASPX.CS: 

 protected void MatrixMatrix_AfterSyncState( object sender, EventArgs e) { InventoryMatrixEntry. EnableCommitChangesAndMoveExtraColumnAtTheEnd( MatrixMatrix.Columns); } protected void MatrixMatrix_RowDataBound( object sender, PXGridRowEventArgs e) { InventoryMatrixEntry.SetUOMFormat( e.Row, MatrixMatrix.Columns); } 

##### HTML: 

 <qp-grid id="gridMatrix-AddMatrixItems" view.bind="Matrix" class="framed-section" on-filter-columns.call="MatrixOnFilter- Columns(col)" on-initialize-columns.call="MatrixOn- ColumnsGenerated(columns)" on-get-cell-text.call="onGetMatrixCell- Text(args)" on-active-cell-changed.call="onMatrix- CellChanged(args)"> </qp-grid> 

 TypeScript: 

 public MatrixOnFilterColumns(column: IGridColumn) { return MatrixGridManager.MatrixFilter- Columns(column); } 

 public MatrixOnColumnsGenerated(columns: IGridColumn[]) { return MatrixGridManager.MatrixColumns- Generated(columns); } 

 public onGetMatrixCellText(args: QpGridEventArgs) { return MatrixGridManager.GetMatrixCell- Text( args.activeColumn?.field, args.activeRow?.cells, args.activeCell?.cellText); } 

 public onMatrixCellChanged(args: any) { if (this.Header.ShowAvailable.value === true) { MatrixGridManager.SetColumnName( this.screenService, args.activeColumn?.field); } } 

#### Use of Predefined UI Definitions 

 In Classic UI, some UI controls or groups of controls were repeated multiple times on different forms including tags in ASPX and logic implemented in JavaScript or ASPC.CS file or using the include (INC) files located in the Pages/ Includes folder. In Modern UI, such controls were implemented as a separate reusable UI definition. A reusable UI definition includes the layout defined in HTML and view classes and logic defined in TypeScript. You can insert 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 42 

 such reusable definition by using the qp-include tag and modify it if needed. For more details, see Reusing a UI Definition. 

#### Implementation of Event Handlers 

 In most cases, the logic that was implemented in JavaScript, can be implemented using event handlers in the TypeScript code of the Modern UI form. For details on implementing event handlers, see Handling UI Events. 

 The following table lists the possible scenarios and how to migrate them to the Modern UI. 

 ASPX.CS TypeScript or HTML 

 Change CSS of a row or a cell in a grid 

 Example: Change CSS style of a cell depending on a value 

 protected void gridRates_RowDataBound( object sender, PXGridRowEventArgs e) { var row = PX.Data.PXResult.Unwrap- Main(e.Row.DataItem); if (row == null) return; 

 PX.Data.PXCache cache = ds.Data- Graph.Caches[row.GetType()]; DateTime? deliveryDate = cache.GetValue(row, "DeliveryDate") as DateTime?; DateTime? requestDate = cache.GetValue(row, "RequestDate") as DateTime?; 

 if (deliveryDate == null || requestDate == null) return; 

 PXGridCell deliveryCell = e.Row.Cells.Cast<PXGridCell>() .FirstOrDefault(c => string.Equals(c.DataField, "DeliveryDate", StringComparison.OrdinalIgnoreCase)); 

 if (deliveryCell == null) return; 

 deliveryCell.Style.CssClass = (delivery- Date <= requestDate) ? DeliveryDateCss.OnOrBeforeRequest- Date : DeliveryDateCss.AfterRequestDate; } 

 Use the GetRowCss or GetCellCss evenr handler 

 @handleEvent(CustomEventType.GetCellCss, { view: "CarrierRates", column: "DeliveryDate" }) public setAmountColor(args: CellCssHandlerArgs): string { const row = args?.selector?.row; const requestDate = new Date(row?.RequestDate?.value); const deliveryDate = new Date(row?.DeliveryDate?.value); 

 if (deliveryDate <= requestDate) { return "green0"; } else { return "error"; } } 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 43 

**ASPX.CS TypeScript or HTML** 

Change one field value depending on another (if backend logic cannot be applied) 

Example: The value of two fields in a grid row are synchronized with each other. 

 <script type="text/javascript"> function UpdateItemSiteCell(n, c) { var activeRow = c.cell.row; var sCell = activeRow.getCell("Selected"); var qCell = activeRow.getCell("QtySelected"); if (sCell == c.cell) { if (sCell.getValue() == true) qCell.setValue("1"); else qCell.setValue("0"); } if (qCell == c.cell) { if (qCell.getValue() == "0") sCell.setValue(false); else sCell.setValue(true); } } </script> 

 Use the ValueChanged event handler 

 getQtySelected( activeRow: SiteStatusLookupResults): number { return 1; } 

 @handleEvent(CustomEventType.ValueChanged, { view: "ItemInfo", field: "Selected", order: 1 }) onSelectedChange(args: ValueChangedHandlerArgs <PXViewCollection<SiteStatusLookupResults>>) { const modelRow = args.viewModel.activeRow; 

 if (modelRow?.Selected?.value === undefined) { return; } 

 const selected = !!(modelRow?.Selected?.value); 

 if (selected) { if (modelRow?.QtySelected?.value === 0) { modelRow.QtySelected.value = this.getQtySelected(modelRow); } } else { modelRow.QtySelected.value = 0; } 

 this.ItemInfo.activeRowChanged = true; } 

 @handleEvent(CustomEventType.ValueChanged, { view: "ItemInfo", field: "QtySelected", order: 1 }) onQtySelectedChange(args: ValueChangedHandlerArgs <PXViewCollection<SiteStatusLookupResults>>) { const modelRow = args.viewModel.activeRow; 

 if (modelRow?.QtySelected?.value === undefined) { return; } 

 if (modelRow?.QtySelected?.value === 0) 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 44 

#### Modification of Backend Code 

 In some cases, you might need to move logic that was implemented in JavaScript to backend, particularly, to the graph. 

 The following table lists the possible scenarios and how to migrate them to the backend. 

 ASPX.CS or JavaScript Backend 

 Update one field value depending on another. 

 Example: The value of two fields in a grid row are synchronized with each other. 

 <script type="text/javascript"> function UpdateItemSiteCell(n, c) { var activeRow = c.cell.row; var sCell = activeRow.getCell("Selected"); var qCell = activeRow.getCell("QtySelected"); if (sCell == c.cell) { if (sCell.getValue() == true) qCell.setValue("1"); else qCell.setValue("0"); } if (qCell == c.cell) { if (qCell.getValue() == "0") sCell.setValue(false); else sCell.setValue(true); } } </script> 

 Implement an event handler and 

 protected virtual void OnSelectedUpdated(PXCache sender, PXFieldUpdatedEventArgs e) { bool? selected = (bool?)sender.GetValue(e.Row, Selected); decimal? qty = (decimal?)sender.GetValue(e.Row, QtySelected); if (selected == true) { if (qty == null || qty == 0m) sender.SetValue(e.Row, QtySelected, 1m); } else sender.SetValue(e.Row, QtySelected, 0m); } 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 45 

 ASPX.CS or JavaScript Backend 

 Change site map data of a form (workspace, category, visibility) 

 Example: A number of methods in the code of Generic Inquiries (SM208000) form 

 protected void edValue_RootFieldsNeeded( object sender, PXCallBackEventArgs e) { if (ds.DataGraph is GenericInquiryDesigner graph) { var fields = graph.GetAllFields(); var parameters = graph.GetAllParameters(); 

 e.Result = string.Join(";", parameters.Concat(fields)); } } 

 Implement logic in an interface and a service. The form graph should inherit from this interface and register the service. 

### Migrating Custom Frontend Code: To Implement an Event Handler 

 This activity will walk you through the process of implementing an event handler to migrate custom JavaScript code to the Modern UI. 

#### Story 

 Suppose that on the Services and Prices (RS203000) form, you need to change a CSS style of a cell in a table on the Repair Items tab. The Base Price cell should have different color depending on the value in the cell. 

#### Process Overview 

 You will review the code in the RS301000.aspx.cs file, implement the GetCellCss event handler in the RS203000.ts file, define the CSS styles, and publish the project. 

#### System Preparation 

 Before you begin migrating the ASPX.CS code, perform the Updating a Customization Project to the Modern UI: To Convert a Customization Project activity. In this activity, you import a customization project and convert it using the conversion tool. 

#### Step 1: Review the Code in the RS203000.aspx.cs file 

 To review the code in the RS203000.aspx.cs file, do the following: 

1. Open the T210 customization project. 

2. On the Files page, open the RS203000.aspx.cs file. 

3. Review code of the gridRepairItems_RowDataBound method. 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 46 

 The code of the method gets the value of the BasePrice cell, gets the PXGridCell object for the same cell, and assigns the CSS class for the cell depending on its value. 

 protected void gridRepairItems_RowDataBound(object sender, PXGridRowEventArgs e) { var row = PX.Data.PXResult.UnwrapMain(e.Row.DataItem); if (row == null) return; 

 PX.Data.PXCache cache = ds.DataGraph.Caches[row.GetType()]; decimal? basePrice = cache.GetValue(row, "BasePrice") as decimal?; 

 if (basePrice == null) return; 

 PXGridCell basePriceCell = e.Row.Cells.Cast<PXGridCell>() .FirstOrDefault(c => string.Equals(c.DataField, "BasePrice", StringComparison.OrdinalIgnoreCase)); 

 if (basePriceCell == null) return; 

 basePriceCell.Style.CssClass = (basePrice >= 15) ? BasePriceCss.FirstStyle : BasePriceCss.SecondStyle; } 

#### Step 2: Implement the Event Handler 

 To implement the event handlers, do the following: 

1. Open the T210 customization project. 

2. On the Modern UI Files page, open the RS203000.ts file. 

3. In the RS203000.ts file, in the RS203000 screen class, implement the GetCellCss event handler for     the BasePrice field of the RepairItems view. 

 @handleEvent(CustomEventType.GetCellCss, { view: "RepairItems", column: "BasePrice" }) getRepairItemsCellCss( args: CellCssHandlerArgs<PXViewCollection<RSSVRepairItem>>): string | undefined { if (args?.selector?.cellValue > 15) { // see static/custom.css return "red-text-cell"; } return "green-text-cell" } 

4. Implement the CSS styles: The default CSS styles are implemented in the FrontendSources\screen     \static\custom.scss file. The file already contains the definition of the red-text-cell style. To     add the missing CSS style:     a. Create the styles.css file in the following folder. 

 FrontendSources\screen\src\development\screens\RS\common 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 47 

 You need to create a separate file because the custom.scss file cannot be saved to the customization project. 

 b. In the styles.scss file, add the definition of the green-text-cell style as shown below. 

 .green-text-cell { color: green; } 

 c. In the RS203000.html file, link the styles.css file from the common folder: Add the require tag aer the first template tag. 

 <require from="../common/styles.scss"></require> 

5. Save your changes. 

6. Export the files from the development folder to the customization project. 

#### Step 3: Test the Changes 

 To test event handler, do the following: 

1. Publish the customization project. 

2. Open the Services and Prices (RS203000) form. 

3. Notice the cell styles on the **Repair Items** tab. 

### Migrating Custom Frontend Code: Helping Tools 

 You can use multiple tools both external and developed by Acumatica to simplify the migration of Classic UI code. 

#### AI Tools 

 You can using coding agents to help you with the different scenarios such as: 

- Compare code of forms that have already been migrated 

- Generate code in TypeScript and HTML 

- Check whether the code is correct according to the provided rules 

- Generate documentation in the code You can also use AI Assistant to ask questions about Modern UI and code migration. It will show you answers based on information from the Help Portal. For details, see _Working with AI Assistant_. 

#### Acumatica Conversion Tools 

 Conversion tools can be used only to migrate standard ASPX code. They do not migrate code on JavaScript or in ASPX.CS. 

 Acumatica provides the following tools that can help you to migrate Classic UI code: 

- Form Converter 

- Customization Project Converter 


<!-- PAGE_BREAK -->
 Migrating JavaScript and ASPX.CS Code to the Modern UI | 48 

 For details, see Updating a Customization Project for the Modern UI: General Information. 

#### Acuminator and Acumate 

 You can use tools developed by Acumatica to generate and check code: 

- Acuminator: A Visual Studio extension which you can use for backend code 

- Acumate: A VS Code plug-in which you can use for frontend code 


