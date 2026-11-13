## Developer Guide 

# Unit Test Framework 

# 2026 R2 


<!-- PAGE_BREAK -->
 Contents | 2 

## Contents 

 Copyright...............................................................................................................................................3 

 Preparing a Test Instance........................................................................................................................ 4 

 Test Instance for Unit Testing: General Information........................................................................................4 

 Test Instance for Unit Testing: To Deploy an Instance..................................................................................... 4 

 Creating a Test Project and a Test Class....................................................................................................6 

 Test Project and Test Class: General Information............................................................................................6 

 Test Project and Test Class: To Create a Test Project...................................................................................... 7 

 Test Project and Test Class: To Create a Test Class..........................................................................................9 

 Creating a Test Method......................................................................................................................... 11 

 Test Method: General Information..................................................................................................................11 

 Test Method: To Create a Test Method Without Parameters......................................................................... 14 

 Test Method: Test Management in Visual Studio........................................................................................... 16 

 Test Method: To Run a Test Method............................................................................................................... 16 

 Test Method: To Debug a Test Method........................................................................................................... 19 

 Test Method: To Create a Test Method with Parameters............................................................................... 20 

 Test Method: Registration of Services............................................................................................................ 23 

 Test Method: To Register a Service................................................................................................................. 23 

 Correctly Assigning Field Values in Tests.................................................................................................25 

 Correct Assignment of Field Values in Tests: General Information............................................................... 25 

 Correct Assignment of Field Values in Tests: To Test the Effect of Changing Field Values........................... 25 

 Testing the Display of Errors and Warnings.............................................................................................30 

 Testing of Errors and Warnings: General Information................................................................................... 30 

 Testing of Errors and Warnings: To Test the Display of Errors and Warnings............................................... 31 

 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests....................................................... 36 

 AI-Assisted Diagnostics and Testing with Automated Unit Tests: General Information............................... 36 

 AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Diagnose a Failing Unit Test.............. 38 

 AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Apply a Fix..........................................44 

 AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Run the Acuminator Console Runner on Customization Code.........................................................................................................................................48 


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
 Preparing a Test Instance | 4 

## Preparing a Test Instance 

 The topics of this chapter describe how to deploy an Acumatica ERP instance. You will use this instance for creating the unit tests that are described in the Unit Test Framework Guide and for becoming familiar with the Acumatica Unit Test Framework. 

### Test Instance for Unit Testing: General Information 

 In this chapter, you will learn how to deploy an Acumatica ERP test instance that contains custom and customized forms. You can use this instance to complete a training course or test a scenario described in this guide. Custom forms are forms that are created entirely from scratch by a customizer. Customized forms are forms that are based on predefined forms in Acumatica ERP, but are modified by a customizer to fit a specific business process. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Prepare the environment 

- Deploy an Acumatica ERP test instance 

#### Applicable Scenarios 

 You deploy an Acumatica ERP test instance by using the instructions in this chapter in the following cases: 

- You want to test the activities described in this guide. 

- You need to complete a training course. 

#### Deploying a Test Instance 

 You can use the Acumatica ERP Configuration wizard to deploy instances based on predefined datasets. It also makes it possible to deploy test instances that contain custom and customized forms. 

 In the Acumatica ERP Configuration wizard, you click Deploy a New Acumatica ERP Instance for T-Series Developer Courses and select the applicable training course in the list. The instance that you are preparing contains the data that is required to complete the activities of this guide. The instance can also include the published customization project. 

### Test Instance for Unit Testing: To Deploy an Instance 

 The following activity will walk you through the process of preparing and deploying an Acumatica ERP instance that you can use to perform the steps in the chapters of this guide that are related to the development of unit tests. 

#### Story 

 Suppose that you want to learn how to create any unit tests provided in the Unit Test Framework Guide. You need to deploy an Acumatica ERP instance by using the Acumatica ERP Configuration Wizard. 


<!-- PAGE_BREAK -->
 Preparing a Test Instance | 5 

#### Process Overview 

 You will prepare the environment—that is, install the soware that you need to use Acumatica ERP and to configure this soware. Then you will deploy an Acumatica ERP instance with the data for the T280 Testing Business Logic with the Acumatica Unit Test Framework course. 

#### Step 1: Preparing the Environment 

 Before you begin deploying the needed Acumatica ERP instance, do the following: 

1. Make sure that the environment you’re going to use conforms to the _System Requirements for the Acumatica_     _ERP Installation_. 

2. Make sure that the Web Server (IIS) features listed in _Configuration of IIS Web Server Features_ are turned on. 

3. Install the Acuminator extension for Visual Studio. 

4. Install Acumatica ERP. On the Main Soware Configuration page of the Acumatica ERP Setup wizard, select     the **Install Acumatica ERP** and **Install Debugger Tools** check boxes. 

 If you’ve already installed Acumatica ERP without the debugger tools, you should uninstall it and install it again with the Install Debugger Tools check box selected. The reinstallation of Acumatica ERP doesn’t affect existing Acumatica ERP instances. You can also install the Acumatica ERP Tools separately. For details, see Acumatica ERP Installation On-Premises: To Install the Acumatica ERP Tools (Optional). 

#### Step 2: Deploying an Acumatica ERP Instance with the Code of the Customization Project 

 To deploy an Acumatica ERP instance and configure it, do the following: 

1. Open the Acumatica ERP Configuration wizard, and do the following:     a. Click **Deploy a New Acumatica ERP Instance for T-Series Developer Courses**.     b. On the **Instance Configuration** page, do the following:        a. In the **Training Course** box, select _T280 Testing Business Logic with the Acumatica Unit Test_           _Framework_.        b. In the **Local Path to the Instance** box, select a folder that’s outside of the C:\Program Files           (x86), C:\Program Files, and C:\Users folders. (We recommend that you store the website           folder outside of these folders to avoid an issue with permission to work in these folders when you           customize the website.)     c. On the **Database Configuration** page, make sure the name of the database is _SmartFix_T280_.     The system creates a new Acumatica ERP instance, adds a new tenant, loads the data to it, and publishes     the customization project that is needed for this training course. 

2. Make sure that a Visual Studio solution is available in the App_Data\Projects\PhoneRepairShop     folder of the Acumatica ERP instance folder.     This is the solution of the extension library that you’ll modify in the activities of this guide. 


<!-- PAGE_BREAK -->
 Creating a Test Project and a Test Class | 6 

## Creating a Test Project and a Test Class 

 Before you begin creating unit tests in the Unit Test Framework, you need to create a Visual Studio project, which you will set up to be a test project. In the test project, you create a test class for each graph or graph extension you want to test. 

 The topics of this chapter describe how to create and configure a Visual Studio project that is intended to contain unit tests for an Acumatica Framework-based application and how to create test classes. 

### Test Project and Test Class: General Information 

 As the first step in creating a set of unit tests for an extension library in a customization project, you create a Visual Studio project and configure it to serve as the test project. For each graph or graph extension to be tested, you create a separate test class in the test project. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Configure a project in Visual Studio to be a test project that uses the xUnit.net library and the Acumatica     Unit Test Framework 

- Create the test class that will contain unit tests 

#### Applicable Scenarios 

 You create and configure a test project each time you need to create unit tests for graphs and graph extensions implemented in a customization project. You create a test class for each graph or graph extension for which you will create unit tests. 

#### Requirements for Using the Acumatica Unit Test Framework 

 By design, the Acumatica Unit Test Framework does not require you to sign in or access a database on a disk. To perform unit tests, you do not need to deploy an Acumatica ERP instance or a database instance. All actions are performed in RAM. 

 The Acumatica Unit Test Framework is designed to be used with the xUnit.net library. You may configure your project for using another unit test library (for example, NUnit), but Acumatica does not guarantee compatibility with a unit test library other than xUnit.net. 

 For details about xUnit.net library, see Getting Started with xUnit.net. 

#### Naming Conventions for Test Projects, Namespaces, and Test Classes 

 By performing the usual process, for each project whose functionality is going to be tested, you create a test project in the same Visual Studio solution and name it by adding .Tests to the end of the name of the project being tested. 

 Similarly, the namespace used in the test project should be named the same as the namespace of the project being tested with .Tests appended to the name. 

 The test class should also be named the same as the class being tested with Tests appended to the name. 

 For example, to test the InventoryItemMaint class, which is in the PhoneRepairShop_Code namespace and contained in the PhoneRepairShop_Code.csproj project, you create 


<!-- PAGE_BREAK -->
 Creating a Test Project and a Test Class | 7 

 the PhoneRepairShop_Code.Tests.csproj project; in this project, you create the InventoryItemMaintTests class and place it in the PhoneRepairShop_Code.Tests namespace. 

#### Test Class Definition 

 A test class is derived from the TestBase class, which is available in the PX.Tests.Unit namespace. 

### Test Project and Test Class: To Create a Test Project 

 The following activity will walk you through the process of creating and configuring a test project. 

#### Story 

 Suppose that you have an extension library implemented in the PhoneRepairShop_Code.csproj Visual Studio project. You need to create a test project in which you will develop unit tests for graphs and graph extensions in this extension library. You will use the xUnit.net library and the Acumatica Unit Test Framework in the unit tests. 

#### Process Overview 

 In Visual Studio, you will create a test project in the same solution with the extension library that implements the graphs and graph extensions being tested. You will add the required NuGet packages to the test project. You will also add the PX.Tests.Unit.dll library and other libraries from the Acumatica ERP instance to the test project. 

#### System Preparation 

 As a prerequisite, before you begin creating a test project, make sure that you have performed the Test Instance for Unit Testing: To Deploy an Instance activity. 

#### Step 1: Creating a Test Project 

 To create the PhoneRepairShop_Code.Tests.csproj project, proceed as follows: 

1. Open the PhoneRepairShop_Code.sln file, which is located in the \App_Data\Projects     \PhoneRepairShop subfolder of the SmartFix_T280 instance folder. 

2. In Visual Studio, in the **Solution Explorer** panel, right-click the PhoneRepairShop_Code solution. 

3. Select **Add > New Project**. 

4. Select the _Class Library_ project template. 

5. Click **Next**. 

6. Enter the PhoneRepairShop_Code.Tests project name, leave the value in the **Location** box     unchanged, and click **Next**. 

7. In the **Framework** box, leave the default setting. 

8. Click **Create**. 

9. In the Solution Explorer, click the created project and specify its properties as follows: 

- TargetFramework: _net48_ 

- LangVersion: _9.0_ 

- Nullable: _enable_ An example of the configuration is shown in the following code. 


<!-- PAGE_BREAK -->
 Creating a Test Project and a Test Class | 8 

 <PropertyGroup> <TargetFramework>net48</TargetFramework> <RootNamespace>PhoneRepairShop_Code.Tests</RootNamespace> <AssemblyName>PhoneRepairShop_Code.Tests</AssemblyName> <AppendTargetFrameworkToOutputPath>false</AppendTargetFrameworkToOutputPath> <OutputPath>bin\$(Configuration)</OutputPath> <GenerateAssemblyInfo>false</GenerateAssemblyInfo> <FileVersion>26.100.0217</FileVersion> <InformationalVersion>26.100.0217</InformationalVersion> <LangVersion>9.0</LangVersion> <Nullable>enable</Nullable> <Copyright>Copyright © 2005-2026 Acumatica, Inc. All rights reserved.</Copyright> </PropertyGroup> 

 10.Delete the Class1.cs item from the PhoneRepairShop_Code.Tests.csproj project. You will create the required C# classes later. 11.Save your changes. 

#### Step 2: Adding NuGet Packages 

 Do the following to add the necessary NuGet packages to the PhoneRepairShop_Code.Tests.csproj project: 

1. In the **Solution Explorer** panel of Visual Studio, right-click the PhoneRepairShop_Code.Tests     project, and select **Manage NuGet Packages**. 

2. Install the following packages: 

- xunit (Version 2.4.2) 

- xunit.runner.visualstudio (Version 2.4.5) 

- System.Runtime.CompilerServices.Unsafe (Version 6.1.2) 

- Microsoft.Bcl.AsyncInterfaces (Version 10.0.7) 

- Microsoft.Extensions.Configuration (Version 10.0.7) 

- Moq (Version 4.20.72) 

#### Step 3: Adding References to the Customization Code and Acumatica ERP Libraries 

 To add references to the customization project and Acumatica ERP libraries to the PhoneRepairShop_Code.Tests.csproj project, proceed as follows: 

1. Copy the PX.Tests.Unit.dll file from the UnitTesting subfolder of the Acumatica ERP installation     folder to any folder you choose. 

2. In the PhoneRepairShop_Code.Tests project, add references to all Acumatica ERP libraries that     are referred in the project of the extension library—that is, add reference to the following files in the     SmartFix_T280\Bin folder: 

- PX.Common.dll 

- PX.Common.Std.dll 

- PX.Data.BQL.Fluent.dll 

- PX.Data.dll 

- PX.Objects.dll 

- PX.CS.Contracts.dll 

- PX.Web.Customization.dll 


<!-- PAGE_BREAK -->
 Creating a Test Project and a Test Class | 9 

3. Add a reference to the Autofac.dll file in the SmartFix_T280\Bin folder. 

4. Add a reference to the PX.Tests.Unit.dll file in the folder where you have placed it. 

5. Add a reference to the PhoneRepairShop_Code project. 

### Test Project and Test Class: To Create a Test Class 

 The following activity will walk you through the process of creating a test class in the test project that you have created. 

#### Story 

 Suppose that you have created and configured the PhoneRepairShop_Code.Tests test project for the extension library implemented in the PhoneRepairShop_Code.csproj project. You need to create a class for testing the Repair Services (RS201000) custom form, whose business logic is implemented in the RSSVRepairServiceMaint class. 

#### Process Overview 

 In the test project, you create a test class derived from the PX.Tests.Unit.TestBase class. This class is intended for containing test methods. 

#### System Preparation 

 Before you begin creating the test class, make sure that you have performed the following prerequisite activities: 

1. _Test Instance for Unit Testing: To Deploy an Instance_ , to prepare the Acumatica ERP instance 

2. _Test Project and Test Class: To Create a Test Project_ , to create and configure the     PhoneRepairShop_Code.Tests.csproj test project 

#### Step: Creating a Test Class 

 To create a test class for the Repair Services (RS201000) form, do the following: 

1. In the **Solution Explorer** panel of Visual Studio, right-click the PhoneRepairShop_Code.Tests     project, and select **Add > New Item**. 

2. Select the _Visual C# item | Class_ template, and type RSSVRepairServiceMaintTests.cs as the file     name. 

3. Click **Add**. 

4. Specify the following using directives in the RSSVRepairServiceMaintTests.cs file. 

 using Xunit; using PX.Data; using PX.Tests.Unit; using PhoneRepairShop; 

5. Make the RSSVRepairServiceMaintTests class public and derived from TestBase as follows. 

 public class RSSVRepairServiceMaintTests : TestBase 


<!-- PAGE_BREAK -->
 Creating a Test Project and a Test Class | 10 

In this class, you will create a test method to test the logic of the RSSVRepairServiceMaint graph, as described in _Test Method: To Create a Test Method Without Parameters_. For more information about creating test methods, see _Creating a Test Method_. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 11 

## Creating a Test Method 

 While the purpose of a test project is to contain tests for a customization library, the purpose of a test class is to contain tests for a graph or graph extension, the purpose of a test method is to contain tests of some functionality implemented in the graph or graph extension being tested. 

 The topics of this chapter describe how to create a method that contains unit tests for a graph, how to register the necessary services, and how to manage a single test or a group of tests. 

### Test Method: General Information 

 In a test class, which is intended for testing a graph or graph extension, you will create test methods, each of which will test a particular functionality. Through the xUnit.net library, which you will use for creating unit tests in the activities of this guide, you can create test methods without parameters and test methods with parameters. In addition to the presence or absence of parameters, these kinds of methods differ in the attributes they have and the number of unit tests they produce. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Create test methods without parameters 

- Create an instance of the tested graph 

- Create and update objects in the graph cache 

- Verify that the desired conditions are met for the values present in the method 

- Run and debug test methods 

- Create test methods with parameters 

- Set values for the test parameters 

- Create unit tests for graph extensions 

#### Applicable Scenarios 

 You create a test method if you want to test some business logic of a graph or graph extension. 

#### Development of a Test 

 A unit test is an automated test written by a soware developer that tests some independent unit of code. A unit test usually launches some functionality of a soware component and then compares the resulting values with the expected values. As you develop unit tests, the best practice is to create them according to the standard AAA pattern: 

1. _Arrange_ : You prepare the test's context and assign some values. 

2. _Act_ : You launch the functionality of a graph or graph extension. 

3. _Assert_ : You check the result. 

 With the Acumatica Unit Test Framework, you can easily create unit tests according to this process. 

 In the arrange part, you initialize the context until actions can be correctly executed. To use the Acumatica Unit Test Framework for this part, you may need to first enable some application features (by using the Common.UnitTestAccessProvider.EnableFeature<FeatureType> generic method) or initialize 


<!-- PAGE_BREAK -->
 Creating a Test Method | 12 

 the required setup DACs (by using the Setup<PXGraph> generic method). Aer that, you create an instance of a graph (by using the PXGraph.CreateInstance<PXGraph> generic method) and fill its caches. 

 Some automated tests, typically referred to as integration tests , validate the interaction of multiple independent components. With Acumatica Unit Test Framework, you can implement these tests and check the interaction of multiple components within a graph. 

#### Creation of Test Methods Without Parameters 

 You create a test method without parameters as follows: 

- You declare a method as public void. 

- You assign the [Fact] attribute to the test method. This produces one test for the test method. 

#### Creation of Test Methods with Parameters 

 When you create a test method with parameters, you declare it as public void and assign it the needed parameters. You assign the [Theory] attribute to the test method and add as many [InlineData] attributes as the method has parameters. This produces one test for each set of parameters provided in the [InlineData] attribute. 

 In each [InlineData] attribute, you specify constants separated by commas as the values for the method parameters. The number of the constants and their types must match the number and the types of the test method parameters. 

 You can provide values for the method parameters in the [ClassData] or [MemberData] attributes instead of the [InlineData] attributes. 

#### Testing of the Business Logic of a Graph 

 In the test method, you create an instance of the tested graph by calling the PXGraph.CreateInstance<> generic method. In this generic method, you use the graph class as the type parameter. 

 You create data access class (DAC) records in the graph cache (PXCache objects). You can address a specific cache of a graph either by the DAC name (<graph>.Caches[typeof(<DAC_name>)]) or by the graph view that contains the DAC objects (<graph>.<DACView>.Cache). 

#### Creation of a Test Method for a Graph Extension 

 In a test method for a graph extension that contains logic for a DAC extension, you get the DAC extension object with the GetExtension<> generic method. You alter the DAC extension object as you wish, and then you update the whole DAC object along with its extension in the cache by using the PXCache.Update method. This executes the logic implemented in the graph extension so that you can verify its correctness. 

#### Assertions 

 You can use the methods of the Xunit.Assert class to make assertions in unit tests. For example, the Assert.True static method verifies that its argument is equal to True , and the Assert.False static method verifies that its argument is equal to False. The following table lists additional methods of the Xunit.Assert class that may be useful. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 13 

**_Table: Assert Class Methods_** 

 Method Description 

 False(bool condition) Verifies that condition is false. The method also throws a FalseException if condition is not false. 

 True(bool condition) Verifies that condition is true and throws a True- Exception if condition is not true. 

 Contains<T>(T expected, IEnumerable<T> collection) 

 Verifies that a collection contains a given object. The method also throws a ContainsException if the collection does not contain the object. 

 DoesNotContain<T>(T expected, IEnumerable<T> collection) 

 Verifies that a collection does not contain a given object. The method also throws a DoesNotContainException if the collection contains the object. 

 Empty(IEnumerable collection) Verifies that collection is empty and throws an EmptyException if collection is not empty. 

 NotEmpty(IEnumerable collection) Verifies that collection is not empty and throws a NotEmptyException if collection is empty. 

 Single(IEnumerable collection) Verifies that collection contains a single element. The method also throws a SingleException if collection does not contain exactly one element. 

 Null(object? obj) Verifies that the object reference is null and throws a NullException if the object reference is not null. 

 NotNull(object? obj) Verifies that an object reference is not null , and throws a NotNullException if the object reference is null. 

 Contains(string expectedSubstring, string? actualString) 

 Verifies that actualString contains expectedSubstring by using the current culture. The method also throws a ContainsException if actualString does not contain expectedSubstring. 

 DoesNotContain(string expectedSubstring, string? actualString) 

 Verifies that actualString does not contain expectedSubstring by using the current culture. The method also throws a DoesNotContainException if actualString contains expectedSubstring. 

 StartsWith(string? expectedStartString, string? actualString) 

 Verifies that actualString starts with expectedStartString by using the current culture. The method also throws a StartsWithException if actualString does not start with expectedStartString. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 14 

 Method Description 

 EndsWith(string? expectedEndString, string? actualString) 

 Verifies that actualString ends with expectedEndString by using the current culture, and throws an EndsWithException if actualString does not end with expectedEndString. 

 Equal(string? expected, string? actual) 

 Verifies that the actual and expected strings are equivalent. The method also throws an EqualException if the actual and expected strings are not equivalent. 

 Equal<T>(T expected, T actual) Verifies that two objects are equal by using a default comparer, and throws an EqualException if the objects are not equal. 

 Equal<T>(IEnumerable<T> expected, IEnumerable<T> actual) 

 Verifies that two sequences of the unmanaged type T are equal. The method also throws an EqualException if the sequences are not equal. 

 You can use another assertion library instead of the Xunit.Assert class. 

#### Running and Debugging of Test Methods 

 Visual Studio includes the Test Explorer tool, which you can use to run a test, a test method, a group of test methods, or all available test methods. You can also debug a single test or multiple tests. 

### Test Method: To Create a Test Method Without Parameters 

 The following activity will walk you through the process of creating a test method without parameters. 

#### Story 

 Suppose that you want to make sure that the following behavior of the Repair Services (RS201000) custom form has not changed: The selection of the Walk-In Service check box and the selection of the Requires Preliminary Check check box are mutually exclusive. You need to create a test method that changes the state of one check box and checks the state of the other check box. 

#### Process Overview 

 To create the test method, you will create a public void method and assign it the [Fact] attribute. In the method, you will create an instance of the tested graph. In the cache of the graph, you will create a record. In this record, you will change the values of the fields that indicate the states of the check boxes, update the cache of the graph, and check that the values of dependent fields have been changed according to the tested logic of the graph. 

#### System Preparation 

 Before you begin creating the test method, make sure that you have performed the following prerequisite activities: 

1. _Test Instance for Unit Testing: To Deploy an Instance_ , to prepare the Acumatica ERP instance that you will use 

2. _Test Project and Test Class: To Create a Test Project_ , to create and configure the     PhoneRepairShop_Code.Tests.csproj test project 


<!-- PAGE_BREAK -->
 Creating a Test Method | 15 

3. _Test Project and Test Class: To Create a Test Class_ , to create the RSSVRepairServiceMaintTests test     class 

#### Step: Creating a Test Method Without Parameters 

 To create a method for checking the states of the check boxes of the Repair Services (RS201000) form, do the following: 

1. In the RSSVRepairServiceMaintTests class, use the following code to create a public void method     and name it _PreliminaryCheckAndWalkInServiceFlags_AreOpposite_. 

 public void PreliminaryCheckAndWalkInServiceFlags_AreOpposite() { } 

2. By using the following code, assign the [Fact] attribute to the method to specify that this unit test is     called without parameters. 

 [Fact] public void PreliminaryCheckAndWalkInServiceFlags_AreOpposite() 

3. In the PreliminaryCheckAndWalkInServiceFlags_AreOpposite method, create an instance of     the RSSVRepairServiceMaint graph as follows. 

 var graph = PXGraph.CreateInstance<RSSVRepairServiceMaint>(); 

4. Now that the RSSVRepairServiceMaint graph is initialized, use the following code to create an     RSSVRepairService object that represents a record in the table of the Repair Services form. 

 var repairService = graph.Caches[typeof(RSSVRepairService)]. Insert(new RSSVRepairService { ServiceCD = "Service1", Description = "Service 1", WalkInService = true, PreliminaryCheck = false }) as RSSVRepairService; 

 Objects that represent table records are created in the graph cache (PXCache objects). You can address a specific cache of a graph either by the DAC name (graph.Caches[typeof(<DAC_name>)]) or by the graph view that contains the DAC objects (graph.<DACView>.Cache). 

5. Aer a record is created, determine whether a change of the **Walk-In Service** check box state leads to a     change of the **Requires Preliminary Check** check box state. Also, determine whether a change of the     **Requires Preliminary Check** check box state leads to a change of the **Walk-In Service** check box. Perform     this checking by adding the following code. 

 if (repairService != null) { repairService.WalkInService = false; graph.Caches[typeof(RSSVRepairService)].Update(repairService); Assert.True(repairService.PreliminaryCheck); 

 repairService.WalkInService = true; graph.Caches[typeof(RSSVRepairService)].Update(repairService); Assert.False(repairService.PreliminaryCheck); 


<!-- PAGE_BREAK -->
 Creating a Test Method | 16 

 repairService.PreliminaryCheck = false; graph.Caches[typeof(RSSVRepairService)].Update(repairService); Assert.True(repairService.WalkInService); 

 repairService.PreliminaryCheck = true; graph.Caches[typeof(RSSVRepairService)].Update(repairService); Assert.False(repairService.WalkInService); } 

 To walk through the process of running the test method, see Test Method: To Run a Test Method. For details about debugging the test method, see Test Method: To Debug a Test Method. 

### Test Method: Test Management in Visual Studio 

 The test methods that you have created appear in the Test Explorer window of Visual Studio, which is shown in the following screenshot. 

 For each test method without parameters (see Test Method: To Create a Test Method Without Parameters ), a test is added. For parameterized test methods (see Test Method: To Create a Test Method with Parameters ), a test is added for each set of parameter values that you have specified for the method. 

 In the Test Explorer window of Visual Studio, you can select the desired test, test method, or group of test methods, and you can run (see Test Method: To Run a Test Method ) or debug (see Test Method: To Debug a Test Method ) them. You can also get information about the tests' outcomes (whether they have succeeded or not) and execution time. 

 Figure: The Test Explorer window with added tests 

### Test Method: To Run a Test Method 

 The following activity will walk you through the process of running a single test method. 

#### Story 

 Suppose that you have a test method implemented in a test class. You need to run the test method. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 17 

#### Process Overview 

 In the Test Explorer window of Visual Studio, you will select a method and run it. 

#### System Preparation 

 Before you begin running the test method, make sure that you have performed the following prerequisite activities: 

1. _Test Instance for Unit Testing: To Deploy an Instance_ , to prepare the Acumatica ERP instance that you will use 

2. _Test Project and Test Class: To Create a Test Project_ , to create and configure the     PhoneRepairShop_Code.Tests.csproj test project 

3. _Test Project and Test Class: To Create a Test Class_ , to create the RSSVRepairServiceMaintTests test     class 

4. _Test Method: To Create a Test Method Without Parameters_ , to create the     PreliminaryCheckAndWalkInServiceFlags_AreOpposite test method 

#### Step: Running a Test Method 

 If your code contains test methods other than the one created in Test Method: To Create a Test Method Without Parameters , or if you have already run the existing test method before, the number of items mentioned in the following instruction may differ. 

 Do the following to run the method created in Test Method: To Create a Test Method Without Parameters : 

1. In Visual Studio, in the solution properties, make sure the website project is excluded from the solution     building (see below). 


<!-- PAGE_BREAK -->
 Creating a Test Method | 18 

 Figure: Solution properties 

2. Select the **Test > Test Explorer** menu item. The **Test Explorer** window opens, which currently displays no     tests. 

3. Click **Run All Tests In View**. The solution is built, and one test for the     PreliminaryCheckAndWalkInServiceFlags_AreOpposite test method appears in the **Test**     **Explorer** window (shown in the following screenshot) and is run. 

 Figure: The Test Explorer window with one test 


<!-- PAGE_BREAK -->
 Creating a Test Method | 19 

### Test Method: To Debug a Test Method 

 The following activity will walk you through the process of debugging a test method. 

#### Story 

 Suppose that you have a test method implemented in a test class. You need to debug the test method in order to detect possible errors. 

#### Process Overview 

 In Visual Studio, you will set breakpoints both in the code being tested and in the test method, launch the debugging for the test method from the Test Explorer window, and check that the values of the fields are as expected. 

#### System Preparation 

 Before you begin debugging the test method, make sure that you have performed the following prerequisite activities: 

1. _Test Instance for Unit Testing: To Deploy an Instance_ , to prepare the Acumatica ERP instance that you will use 

2. _Test Project and Test Class: To Create a Test Project_ , to create and configure the     PhoneRepairShop_Code.Tests.csproj test project 

3. _Test Project and Test Class: To Create a Test Class_ , to create the RSSVRepairServiceMaintTests test     class 

4. _Test Method: To Create a Test Method Without Parameters_ , to create the     PreliminaryCheckAndWalkInServiceFlags_AreOpposite test method 

#### Step: Debugging a Test Method 

 To debug the PreliminaryCheckAndWalkInServiceFlags_AreOpposite method, do the following: 

1. In the PhoneRepairShop_Code.Tests project, open the RSSVRepairServiceMaintTests.cs     file. 

2. Move the caret to the following line. 

 repairService.WalkInService = false; 

3. Press F9 to set a breakpoint on the line. 

4. In the PhoneRepairShop_Code project, open the RSSVRepairServiceMaint.cs file. 

5. In the _(Events.FieldUpdated<RSSVRepairService,     RSSVRepairService.walkInService> e) method, move the caret to the following line. 

 row.PreliminaryCheck = !(row.WalkInService == true); 

6. Press F9 to set a breakpoint on the line. 

7. Select the **Test > Test Explorer** menu command to open the **Test Explorer** window. 

8. Right-click the PreliminaryCheckAndWalkInServiceFlags_AreOpposite     method, and select **Debug**. Aer the debugging process starts, the execution initially     pauses at the breakpoint in the RSSVRepairServiceMaint.cs file. This is because the 


<!-- PAGE_BREAK -->
 Creating a Test Method | 20 

 _(Events.FieldUpdated<RSSVRepairService, RSSVRepairService.walkInService> e) method gets triggered when the repairService object is first created and added to the cache using the graph.Caches[typeof(RSSVRepairService)].Insert(...) method of the graph. Continue debugging (you can press F5 for this). 

9. The execution pauses in the RSSVRepairServiceMaintTests.cs file. You can verify that the value of     repairService.WalkInService is _true_. 10.Step over the statement in the current line (you can use F10 for this). The value of     repairService.WalkInService becomes _false_. 11.Step over the statement in the current line. This updates the repairService object in the cache.     During the update, the FieldUpdated event is generated for the **Walk-In Service** check box, and the     _(Events.FieldUpdated<RSSVRepairService, RSSVRepairService.walkInService>     e) method of the RSSVRepairServiceMaint class is launched. The execution pauses at the breakpoint     in the RSSVRepairServiceMaint.cs file, which signifies that the extension library and unit test match     each other. 12.Continue debugging (you can press F5 for this). The debugging process continues until it completes     successfully. 

### Test Method: To Create a Test Method with Parameters 

 The following activity will walk you through the process of creating a test method with parameters. 

#### Story 

 Suppose that you want to make sure that the following behavior of the customized Stock Items (IN202500) form has not changed: 

- The selection of the **Repair Item** check box causes the **Repair Item Type** drop-down list to be available. 

- The clearing of the **Repair Item** check box causes the **Repair Item Type** drop-down list to be unavailable. You need to create a test method that selects or clears the **Repair Item** check box and checks whether the **Repair Item Type** drop-down list is available or unavailable, respectively. 

#### Process Overview 

 To create the test method, you will create a public void method with one Boolean parameter. You will assign the method the [Theory] attribute and two [InlineData] attributes, each of which has the possible values of the method parameter ( true and false ). In the method, you will create an instance of the tested graph. In the cache of the graph, you will create a record. For this record, by using the GetExtension generic method, you will retrieve the extension, which contains custom fields. Depending on the method parameter, you will change the state of the check box, update the cache of the graph, and make sure that the availability of the drop-down list has been changed according to the tested logic of the graph. 

#### System Preparation 

 Before you begin creating the test method, do the following: 

1. Make sure that you have performed the _Test Instance for Unit Testing: To Deploy an Instance_ prerequisite     activity to prepare the Acumatica ERP instance that you will use. 

2. Make sure that you have performed the _Test Project and Test Class: To Create a Test Project_ prerequisite     activity to create and configure the PhoneRepairShop_Code.Tests.csproj test project. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 21 

3. Create the InventoryItemMaintTests test class. For an example that shows how to create a test class,     see _Test Project and Test Class: To Create a Test Class_. 

#### Step 1: Creating and Configuring a Test Method with Parameters 

 To create and configure a method for testing the business logic of the InventoryItemMaint class, do the following: 

1. In the InventoryItemMaintTests class, create a public void method, and name it     _RepairItemTypeEnabled_WhenRepairItemSelected_. 

2. To specify that this unit test is called with parameters, assign the [Theory] attribute to the method as     follows. 

 [Theory] public void RepairItemTypeEnabled_WhenRepairItemSelected 

3. Add the Boolean enabled parameter to the     RepairItemTypeEnabled_WhenRepairItemSelected method as follows. 

 public void RepairItemTypeEnabled_WhenRepairItemSelected (bool enabled) 

4. Add two [InlineData] attributes, which provide two values for the enabled parameter, as follows. 

 [Theory] [InlineData(true)] [InlineData(false)] public void RepairItemTypeEnabled_WhenRepairItemSelected (bool enabled) 

 The RepairItemTypeEnabled_WhenRepairItemSelected method will be called twice: The first call will pass true as its argument, and the second will pass false. 

#### Step 2: Implementing a Method for Testing the InventoryItemMaint Class 

 To test the business logic of the InventoryItemMaint class, do the following: 

1. In the RepairItemTypeEnabled_WhenRepairItemSelected method, create an instance of the     InventoryItemMaint graph by adding the following code. 

 var graph = PXGraph.CreateInstance<InventoryItemMaint>(); 

2. Aer the InventoryItemMaint graph is initialized, create an InventoryItem object as follows. 

 InventoryItem item = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert( new InventoryItem { InventoryCD = "Item1", Descr = "Item 1" }); 

3. Get the InventoryItemExt extension of the InventoryItem object as follows. 

 InventoryItemExt itemExt = item.GetExtension<InventoryItemExt>(); 


<!-- PAGE_BREAK -->
 Creating a Test Method | 22 

4. Select (or clear) the **Repair Item** check box by using the needed value of the enabled parameter, and     make sure that the **Repair Item Type** drop-down list is available (or, respectively, unavailable) by adding     the following code. 

 itemExt.UsrRepairItem = enabled; graph.Caches[typeof(InventoryItem)].Update(item); PXFieldState fieldState = ((PXFieldState)graph.Caches[typeof(InventoryItem)].GetStateExt< InventoryItemExt.usrRepairItemType>(item)); Assert.True(enabled == fieldState.Enabled); 

 A call of the PXCache.Update method for the InventoryItem object updates both the object and its extension. 

As a result of the actions you have performed in this activity, the InventoryItemMaintTests.cs file contains the following code. 

 using Xunit; using PX.Data; using PX.Tests.Unit; using PX.Objects.IN; using PhoneRepairShop; 

 namespace PhoneRepairShop_Code.Tests { public class InventoryItemMaintTests : TestBase { [Theory] [InlineData(true)] [InlineData(false)] public void RepairItemTypeEnabled_WhenRepairItemSelected (bool enabled) { var graph = PXGraph.CreateInstance<InventoryItemMaint>(); 

 InventoryItem item = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert( new InventoryItem { InventoryCD = "Item1", Descr = "Item 1" }); 

 InventoryItemExt itemExt = item.GetExtension<InventoryItemExt>(); 

 itemExt.UsrRepairItem = enabled; graph.Caches[typeof(InventoryItem)].Update(item); PXFieldState fieldState = ((PXFieldState)graph.Caches[typeof(InventoryItem)].GetStateExt< InventoryItemExt.usrRepairItemType>(item)); Assert.True(enabled == fieldState.Enabled); } } } 


<!-- PAGE_BREAK -->
 Creating a Test Method | 23 

 This test uses the arrange-act-assert pattern. 

 In some circumstances, running this test method may fail. To learn the actions that you must perform to make this test method successful, see Test Method: To Register a Service. 

### Test Method: Registration of Services 

 Acumatica uses the dependency injection technique to design soware. With this technique, an object (a client ) receives other objects ( services ) that it depends on; in this context, these services are called dependencies. Each of these services must be registered: For each needed interface, you must specify the service that implements this interface. 

 This soware design pattern is used to decouple code components and make them easier to extend and test. For more information about dependency injection, see https://docs.microsoft.com/en-us/dotnet/core/extensions/ dependency-injection. 

#### Implementation of the Dependency Injection in Acumatica ERP and Unit Tests 

 In Acumatica ERP, the Autofac library is used to implement the dependency injection. For more information, see Dependency Injection: General Information. 

 In unit tests, mock services are used instead of real complex objects. These mock services are simplified services that mimic real ones. 

 To register a service, you need to override the TestBase.RegisterServices method and make calls to the Autofac.ContainerBuilder.RegisterType generic method. 

 The following table includes the frequently used mock services that are available in Acumatica ERP. 

 Table: Frequently Used Mock Services 

 Mocked Interface Mock Service 

 IFinPeriodRepository (defined in the PX.Objects.GL.FinPeriods namespace) 

 FinPeriodServiceMock (defined in the PX.Objects.Unit namespace) 

 IPXCurrencyService (defined in the PX.Objects.CM.Extensions namespace) 

 CurrencyServiceMock (defined in the PX.Objects.Unit namespace) 

 You can also define your own service, register it, and use it in a PX.Tests.Unit.TestBase-derived class as described in Dependency Injection: General Information. 

### Test Method: To Register a Service 

 The following activity will walk you through the process of registering a mock service in a test class. 

#### Story 

 Suppose that running a test method leads to the generation of the Autofac.Core.Registration.ComponentNotRegisteredException exception. When this exception occurs, the error message specifies which component (interface) is not registered. You need to register the service that implements the specified interface. 


<!-- PAGE_BREAK -->
 Creating a Test Method | 24 

#### Process Overview 

 To get rid of the exception, you will add the use of the Autofac library and override the TestBase.RegisterServices method in the test class. In the overridden RegisterServices method, you will register the needed service that implements the interface specified in the exception message. 

#### System Preparation 

 Before you begin implementing the registration of a service, do the following: 

1. Make sure that you have performed the _Test Instance for Unit Testing: To Deploy an Instance_ prerequisite     activity to prepare the Acumatica ERP instance that you will use. 

2. Make sure that you have performed the _Test Project and Test Class: To Create a Test Project_ prerequisite     activity to create and configure the PhoneRepairShop_Code.Tests.csproj test project. 

3. Create the InventoryItemMaintTests test class. For an example that shows how to create a test class,     see _Test Project and Test Class: To Create a Test Class_. 

4. Make sure that you have performed the _Test Method: To Create a Test Method with Parameters_ prerequisite     activity to create the RepairItemTypeEnabled_WhenRepairItemSelected test method. 

5. Run the RepairItemTypeEnabled_WhenRepairItemSelected test method. 

#### Step: Registering a Service 

 When the test method created in Test Method: To Create a Test Method with Parameters is run, the following error message is generated if a proper service is not registered (only part of the error message is quoted). 

 Autofac.Core.Registration.ComponentNotRegisteredException : The requested service 'System.Func2[[PX.Data.PXGraph, PX.Data, Version=1.0.0.0, Culture=neutral, PublicKeyToken=3b136cac2f602b8e], [PX.Objects.CM.Extensions.IPXCurrencyService, PX.Objects, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]' has not been registered. To avoid this exception, either register a component to provide the service, check for service registration using IsRegistered(), or use the ResolveOptional() method to resolve an optional dependency. 

 To register this service, do the following: 

1. In the PhoneRepairShop_Code.Tests.csproj project, add a reference to Autofac.dll from the     Bin folder of the Acumatica ERP instance if it has not been added yet. For details, see _Test Project and Test_     _Class: To Create a Test Project_. 

2. In the InventoryItemMaintTests class, override the TestBase.RegisterServices method as     follows. 

 protected override void RegisterServices(ContainerBuilder builder) { base.RegisterServices(builder); builder.RegisterType<PX.Objects.Unit.CurrencyServiceMock>(). As<IPXCurrencyService>(); } 

3. Make sure the following using directives have been added to the InventoryItemMaintTests.cs file. 

 using Autofac; using PX.Objects.CM.Extensions; 

 Aer the service is registered, run the tests for the RepairItemTypeEnabled_WhenRepairItemSelected test method, which had failed previously. Make sure that the tests succeed. 


<!-- PAGE_BREAK -->
 Correctly Assigning Field Values in Tests | 25 

## Correctly Assigning Field Values in Tests 

 When you develop unit tests for Acumatica Framework-based applications, you need to make sure that you assign field values in the appropriate places in the code. The topics of this chapter describe how to assign values to key and non-key fields and use default field values in unit tests. 

### Correct Assignment of Field Values in Tests: General Information 

 When you create unit tests for graphs or graph extensions, you may encounter various difficulties related to assigning field values: If you assign field values in the wrong places, the results of the code execution may be unpredictable. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Specify the values of key and non-key fields when an object is created or updated 

- Use the default field values when an object is created 

#### Applicable Scenarios 

 In unit tests, you specify field values every time you create or update DAC objects in the cache. 

#### Assignment of Values to Fields 

 When you are assigning values to DAC fields in unit tests, you need to handle key fields and non-key fields differently. 

 When you create a DAC object in the cache, you use the PXCache.Insert method. As a result, some values (either default values or values you specify) are assigned to the key fields of the DAC object. Aer a DAC object is created, you alter its fields by using the PXCache.Update method. If you alter the key fields in this way, the old DAC object remains unchanged in the cache, but another DAC object with the specified values of the key fields is created or updated in the cache. 

 So to avoid mistakes, you should assign values to the key fields of a DAC object at the stage of creation and should not change them aerward. 

 If a DAC object you are going to create has a key field that is defined with the PXSelector or PXDBDefault attribute, the default value of this key field is taken from the Current property of the DAC specified in the attribute. 

### Correct Assignment of Field Values in Tests: To Test the Effect of Changing Field 

### Values 

 The following activity will walk you through the process of creating a method that tests complicated business logic involving the assignment of field values. 


<!-- PAGE_BREAK -->
 Correctly Assigning Field Values in Tests | 26 

#### Story 

 Suppose that you want to make sure that the following behavior of the Services and Prices (RS203000) form has not changed: 

- If changes are made to the state of the **Required** or **Default** check box (or both check boxes) of a row, these     changes affect the states of these check boxes in other rows. 

- The prices are calculated correctly. You need to create a test method. In this method, you need to create at least three repair items of different types and a labor item, configure them, and make sure that the fields that correspond to the **Required** and **Default** check boxes have the correct states and that the boxes with prices have the correct values. 

#### Process Overview 

 You will create a test method without parameters for the Services and Prices (RS203000) form. In this method, you will create an instance of the tested graph, RSSVRepairPriceMaint. In the cache of the graph, you will create the necessary objects by using the PXCache.Insert method, and configure them by using the PXCache.Update method. Then you will use the methods of the Assert class to verify that the necessary conditions for the values of the objects' fields are met. 

#### System Preparation 

 Before you begin creating the test method, do the following: 

1. Make sure that you have performed the _Test Instance for Unit Testing: To Deploy an Instance_ prerequisite     activity to prepare the Acumatica ERP instance that you will use. 

2. Make sure that you have performed the _Test Project and Test Class: To Create a Test Project_ prerequisite     activity to create and configure the PhoneRepairShop_Code.Tests.csproj test project. 

3. Create the RSSVRepairPriceMaintTests test class. For an example that shows how to create a test     class, see _Test Project and Test Class: To Create a Test Class_. 

#### Step 1: Creating a Test Method for the Services and Prices Form 

 In this step, you will create a test method for the Services and Prices (RS203000) form. (For basic information on the creation of a test method without parameters, see Test Method: General Information .) Do the following: 

1. In the RSSVRepairPriceMaintTests class, create a public void method, and name it     TestServicesAndPricesForm. 

2. Specify the [Fact] attribute for the method to indicate that this unit test is called without parameters. 

#### Step 2: Creating Necessary Objects 

 To create the objects that are necessary for testing the business logic, do the following: 

1. In the TestServicesAndPricesForm method, create an instance of the RSSVRepairPriceMaint     graph by adding the following code. 

 var graph = PXGraph.CreateInstance<RSSVRepairPriceMaint>(); 

2. Create a device to repair (an RSSVDevice object) and a service for repairing the device (an     RSSVRepairService object) by adding the following code. You will use the IDs of the device and the     service to create an RSSVRepairPrice object. 

 graph.Caches[typeof(RSSVDevice)].Insert(new RSSVDevice 


<!-- PAGE_BREAK -->
 Correctly Assigning Field Values in Tests | 27 

 { DeviceCD = "Device1" }); graph.Caches[typeof(RSSVRepairService)].Insert(new RSSVRepairService { ServiceCD = "Service1" }); 

 When you are creating an object, you need to specify values for its key fields. If you do not specify a value for an object's key field during the creation of the object, you cannot change the field value later. 

3. Create an RSSVRepairPrice object that will contain details about the repair service as follows. 

 RSSVRepairPrice repairPrice = (RSSVRepairPrice)graph.Caches[typeof(RSSVRepairPrice)]. Insert(new RSSVRepairPrice()); 

 You could have specified the values for the key fields, DeviceID and ServiceID, but you did not because the DeviceID and ServiceID fields are assigned their values from the Current properties of the RSSVDevice and RSSVRepairService types. 

4. Make sure that you have added the using PX.Objects.IN; directive to the     RSSVRepairPriceMaintTests class. 

5. Create three repair items—two of the Battery type, and one of the BackCover type—by using the     following code. 

 InventoryItem battery1 = (InventoryItem)graph. Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "Battery1" }); graph.Caches[typeof(InventoryItemCurySettings)].Insert(new InventoryItemCurySettings { InventoryID = battery1.InventoryID, CuryID = "USD" }); InventoryItemExt batteryExt1 = battery1.GetExtension<InventoryItemExt>(); batteryExt1.UsrRepairItem = true; batteryExt1.UsrRepairItemType = RepairItemTypeConstants.Battery; graph.Caches[typeof(InventoryItem)].Update(battery1); 

 InventoryItem battery2 = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "Battery2" }); graph.Caches[typeof(InventoryItemCurySettings)].Insert(new InventoryItemCurySettings { InventoryID = battery2.InventoryID, CuryID = "USD" 


<!-- PAGE_BREAK -->
 Correctly Assigning Field Values in Tests | 28 

 }); InventoryItemExt batteryExt2 = battery2.GetExtension<InventoryItemExt>(); batteryExt2.UsrRepairItem = true; batteryExt2.UsrRepairItemType = RepairItemTypeConstants.Battery; graph.Caches[typeof(InventoryItem)].Update(battery2); 

 InventoryItem backCover1 = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "BackCover1" }); graph.Caches[typeof(InventoryItemCurySettings)].Insert(new InventoryItemCurySettings { InventoryID = backCover1.InventoryID, CuryID = "USD" }); InventoryItemExt backCoverExt1 = backCover1.GetExtension<InventoryItemExt>(); backCoverExt1.UsrRepairItem = true; backCoverExt1.UsrRepairItemType = RepairItemTypeConstants.BackCover; graph.Caches[typeof(InventoryItem)].Update(backCover1); 

 This code adds an InventoryItemCurySettings object to the cache for each created repair item to give users the ability to specify the price of the repair items. This code also demonstrates the right order of instructions when you are implementing unit tests: You insert a new object into the cache by calling the PXCache.Insert method, and then you change non-key fields of the object and call the PXCache.Update method. 

6. Create a non-stock item that represents the work to be done by adding the following code. 

 InventoryItem work1 = (InventoryItem)graph. Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "Work1", StkItem = false }); 

7. Create repair items based on the stock items, and configure them by adding the following code. 

 // Configure the back cover repair item RSSVRepairItem repairItemBackCover1 = (RSSVRepairItem)graph.Caches[typeof(RSSVRepairItem)].Insert( new RSSVRepairItem { InventoryID = backCover1.InventoryID, Required = true, BasePrice = 10, IsDefault = true }); 

 // Configure the first battery repair item RSSVRepairItem repairItemBattery1 = (RSSVRepairItem)graph.Caches[typeof(RSSVRepairItem)].Insert( new RSSVRepairItem { 


<!-- PAGE_BREAK -->
 Correctly Assigning Field Values in Tests | 29 

 InventoryID = battery1.InventoryID }); repairItemBattery1.Required = true; repairItemBattery1.BasePrice = 20; repairItemBattery1.IsDefault = true; graph.Caches[typeof(RSSVRepairItem)].Update(repairItemBattery1); 

 // Configure the second battery repair item RSSVRepairItem repairItemBattery2 = (RSSVRepairItem)graph.Caches[typeof(RSSVRepairItem)].Insert( new RSSVRepairItem { InventoryID = battery2.InventoryID }); repairItemBattery2.Required = false; repairItemBattery2.BasePrice = 30; repairItemBattery2.IsDefault = true; graph.Caches[typeof(RSSVRepairItem)].Update(repairItemBattery2); 

 This code creates three repair items: one back cover, and two batteries. 

#### Step 3: Testing the Calculated Values 

 To test the calculated values, do the following: 

1. Add the following code to check the values of the Required and IsDefault fields. 

 // 2nd battery is not required -> 1st battery is also not required Assert.False(repairItemBattery1.Required); // 2nd battery is used by default -> 1st battery is not used by default Assert.False(repairItemBattery1.IsDefault); // The back cover's Required and Default fields are not affected Assert.True(repairItemBackCover1.Required); Assert.True(repairItemBackCover1.IsDefault); 

2. Add the following code to ensure that the prices are calculated correctly. 

 RSSVLabor labor = (RSSVLabor)graph.Caches[typeof(RSSVLabor)]. Insert(new RSSVLabor { InventoryID = work1.InventoryID, DefaultPrice = 2, Quantity = 3 }); Assert.Equal(6, labor.ExtPrice); Assert.Equal(66, repairPrice.Price); 

3. Run the created test, and make sure that it succeeds. 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 30 

## Testing the Display of Errors and Warnings 

 The topics of this chapter describe how to test whether error or warning messages are displayed properly on the UI when users perform particular actions. 

### Testing of Errors and Warnings: General Information 

 The logic of a graph can include the displaying of errors and warnings on the UI. In a test method, you can verify that certain actions cause an error or warning to be displayed. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Test the logic of a graph that has a setup DAC 

- Test whether a proper error is attached to a field 

- Test whether a proper warning is attached to a field 

- Clear the cache of errors 

- Find the proper DAC object in the cache 

#### Applicable Scenarios 

 In unit tests, you can check whether an appropriate warning or error is attached to a box when the entered value does not fit the logic of the form. 

#### Creation of an Instance of a Graph That Has a Setup DAC 

 If a tested graph has setup DACs, you must call the Setup<Graph>(params IBqlTable[] items) generic method to initialize and bind the setup DACs. In this case, you specify the tested graph as a type parameter and the objects of the setup DACs as the parameters. Aer that, you create an instance of the tested graph. If you do not initialize and bind the setup DACs for the test, they will not be used by the graph. 

 The Setup<Graph>(params IBqlTable[] items) method mocks the Acumatica ERP setup preferences. The Setup method should not be used to initialize non-setup DACs. 

#### Testing of the Displayed Errors and Warnings 

 The tested graph may contain the logic that attaches an error or warning to a DAC field in some circumstances. The use of the PXCache.GetStateExt<> generic method is the recommended way to get the state of a field to test whether an error or warning is attached to the field. You can also use the PXCache.GetError, PXCache.GetErrors, and PXCache.GetWarning method for it. 

 You pass the class that corresponds to the tested field as the type parameter of the PXCache.GetStateExt<> generic method, and you pass the tested DAC object as the parameter of this method. The method returns a PXFieldState object for which the following are true: 

- The object's Error property contains the error message. 

- The Warning property of the object contains the warning message. 

- The object's ErrorLevel property contains the level of the warning or error attached. (The value of this     property is PXErrorLevel.Error if there is an error attached, and PXErrorLevel.Warning if there     is a warning attached.) 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 31 

 In your code, aer you have tested the displaying of an error or warning, you clear the cache of errors and warnings with the PXCache.Clear method. 

 The attaching of an error or warning to a field may be the result of an action that generates an exception or cancels the assignment of a value. In this case, the cache may contain different DAC objects before and aer performing such an action. To pick the proper DAC object for testing, you call the PXCache.Locate method and pass an object of that DAC type having the correct values of the key fields. 

### Testing of Errors and Warnings: To Test the Display of Errors and Warnings 

 The following activity will walk you through the process of creating a method that tests the display of warning and error messages. 

#### Story 

 Suppose that you want to make sure that the following behavior of the Repair Work Orders (RS301000) form has not changed: 

- When a new work order is initialized, the system copies to it the repair items and labor items of the     RSSVRepairPrice object that has the same DeviceID and ServiceID values as the work order being     initialized. 

- Negative values of labor quantities are prohibited. 

- The values of labor quantities are not permitted to be less than the minimum values. 

- In work orders for which the priority is _Low_ , repair services that are marked as requiring preliminary checks     are prohibited. You need to create a test method. In this method, you need to initialize the settings of the graph. 

#### Process Overview 

 You will create a test method without parameters for the Repair Work Orders (RS301000) form. In this method, you will initialize the settings of the tested graph RSSVWorkOrderEntry by calling the Setup<> generic method. Then you will create an instance of the RSSVWorkOrderEntry graph. In the cache of the graph, you will create the necessary objects and configure them. You will assign to the fields values that are not allowed by the business logic of the graph and ensure that the appropriate warnings or errors appear in the UI; you will do this by calling the PXCache.GetStateExt method. 

#### System Preparation 

 Before you begin creating the test method, do the following: 

1. Make sure that you have performed the _Test Instance for Unit Testing: To Deploy an Instance_ prerequisite     activity to prepare the Acumatica ERP instance that you will use. 

2. Make sure that you have performed the _Test Project and Test Class: To Create a Test Project_ prerequisite     activity to create and configure the PhoneRepairShop_Code.Tests.csproj test project. 

3. Create the RSSVWorkOrderEntryTests test class. For an example that shows how to create a test class,     see _Test Project and Test Class: To Create a Test Class_. 

#### Step 1: Creating a Test Method for the Repair Work Orders Form 

 In this step, you will create a test method for the Repair Work Orders (RS301000) form. (For basic information on the creation of a test method without parameters, see Test Method: General Information .) Do the following: 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 32 

1. In the RSSVWorkOrderEntryTests class, create a public void method, and name it     TestRepairWorkOrdersForm. 

2. Specify the [Fact] attribute for the method to indicate that this unit test is called without parameters. 

3. Initialize the settings for the RSSVWorkOrderEntry graph by adding the following code. 

 Setup<RSSVWorkOrderEntry>(new RSSVSetup()); 

 The RSSVSetup DAC contains settings for the RSSVWorkOrderEntry graph. The call of the Setup<> generic method is mandatory because it initializes an RSSVSetup object. 

4. Create an instance of the RSSVWorkOrderEntry graph as follows. 

 var graph = PXGraph.CreateInstance<RSSVWorkOrderEntry>(); 

#### Step 2: Creating the Necessary Objects 

 In the TestRepairWorkOrdersForm method, create the objects that are needed to test the displaying of warnings and errors as follows: 

1. Create an RSSVDevice object and two RSSVRepairService objects (one of these is the main object,     and the other is auxiliary) by adding the following code. 

 RSSVDevice device = (RSSVDevice)graph.Caches[typeof(RSSVDevice)]. Insert(new RSSVDevice { DeviceCD = "Device1" }); 

 RSSVRepairService repairService = (RSSVRepairService)graph.Caches[typeof(RSSVRepairService)]. Insert(new RSSVRepairService { ServiceCD = "Service1" }); RSSVRepairService repairService2 = (RSSVRepairService)graph.Caches[typeof(RSSVRepairService)]. Insert(new RSSVRepairService { ServiceCD = "Service2" }); 

2. Create an RSSVRepairPrice object, and initialize it with the RSSVDevice object and the main     RSSVRepairService object. You do this by adding the following code. 

 graph.Caches[typeof(RSSVRepairPrice)].Insert(new RSSVRepairPrice { DeviceID = device.DeviceID, ServiceID = repairService.ServiceID }); 

3. Make sure that you have added the using PX.Objects.IN; directive to the     RSSVWorkOrderEntryTests class. 

4. Add the following code to create two stock items and one non-stock item, and to make the two stock items     repair items. 

 InventoryItem battery1 = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert(new InventoryItem { 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 33 

 InventoryCD = "Battery1" }); InventoryItemExt batteryExt1 = battery1.GetExtension<InventoryItemExt>(); batteryExt1.UsrRepairItem = true; batteryExt1.UsrRepairItemType = RepairItemTypeConstants.Battery; graph.Caches[typeof(InventoryItem)].Update(battery1); 

 InventoryItem backCover1 = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "BackCover1" }); InventoryItemExt backCoverExt1 = backCover1.GetExtension<InventoryItemExt>(); backCoverExt1.UsrRepairItem = true; backCoverExt1.UsrRepairItemType = RepairItemTypeConstants.BackCover; graph.Caches[typeof(InventoryItem)].Update(backCover1); 

 InventoryItem work1 = (InventoryItem)graph.Caches[typeof(InventoryItem)].Insert(new InventoryItem { InventoryCD = "Work1", StkItem = false }); 

5. Create two repair items based on the two stock items as follows. 

 RSSVRepairItem repairItemBackCover1 = (RSSVRepairItem)graph.Caches[typeof(RSSVRepairItem)].Insert( new RSSVRepairItem { DeviceID = device.DeviceID, ServiceID = repairService.ServiceID }); repairItemBackCover1.InventoryID = backCover1.InventoryID; repairItemBackCover1.Required = true; repairItemBackCover1.BasePrice = 10; repairItemBackCover1.IsDefault = true; repairItemBackCover1.RepairItemType = backCoverExt1.UsrRepairItemType; graph.Caches[typeof(RSSVRepairItem)].Update(repairItemBackCover1); 

 RSSVRepairItem repairItemBattery1 = (RSSVRepairItem)graph.Caches[typeof(RSSVRepairItem)].Insert( new RSSVRepairItem { DeviceID = device.DeviceID, ServiceID = repairService.ServiceID }); repairItemBattery1.InventoryID = battery1.InventoryID; repairItemBattery1.Required = true; repairItemBattery1.BasePrice = 20; repairItemBattery1.IsDefault = true; 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 34 

 repairItemBattery1.RepairItemType = batteryExt1.UsrRepairItemType; graph.Caches[typeof(RSSVRepairItem)].Update(repairItemBattery1); 

6. Create an RSSVLabor object based on the non-stock item by using the following code. 

 RSSVLabor labor = (RSSVLabor)graph.Caches[typeof(RSSVLabor)]. Insert(new RSSVLabor { InventoryID = work1.InventoryID, DeviceID = device.DeviceID, ServiceID = repairService.ServiceID }); labor.DefaultPrice = 2; labor.Quantity = 3; graph.Caches[typeof(RSSVLabor)].Update(labor); 

7. Create a work order with the same DeviceID and ServiceID values as those specified for the     RSSVRepairPrice object, which was created in Instruction 2. To do this, add the following code. 

 RSSVWorkOrder workOrder = (RSSVWorkOrder)graph. Caches[typeof(RSSVWorkOrder)].Insert(new RSSVWorkOrder()); workOrder.DeviceID = device.DeviceID; workOrder.ServiceID = repairService.ServiceID; graph.Caches[typeof(RSSVWorkOrder)].Update(workOrder); 

#### Step 3: Testing the Display of Errors and Warnings 

 Now that the necessary objects have been created, perform the following instructions to test the display of errors and warnings: 

1. As the first test, add the following code to make sure that there are two RSSVWorkOrderItem objects,     which have been created based on the two RSSVRepairItem objects, and an RSSVWorkOrderLabor     object, which has been created based on the RSSVLabor object. 

 Assert.Equal(2, graph.RepairItems.Select().Count); Assert.Single(graph.Labor.Select()); 

2. As the second test, add the following code to ensure that the changing of the ServiceID field of the work     order does not affect the RepairItems and Labor views. 

 workOrder.ServiceID = repairService2.ServiceID; graph.Caches[typeof(RSSVWorkOrder)].Update(workOrder); Assert.Equal(2, graph.RepairItems.Select().Count); Assert.Single(graph.Labor.Select()); 

3. Restore the ServiceID value as follows. 

 workOrder.ServiceID = repairService.ServiceID; graph.Caches[typeof(RSSVWorkOrder)].Update(workOrder); 

4. Obtain the RSSVWorkOrderLabor object (the value of its Quantity field must be _3_ ), and try to assign a     negative value to its Quantity field by using the following code. An error message must be attached to the     Quantity field instead. 

 RSSVWorkOrderLabor woLabor = graph.Labor.SelectSingle(); Assert.Equal(3, woLabor.Quantity); woLabor.Quantity = -1; 


<!-- PAGE_BREAK -->
 Testing the Display of Errors and Warnings | 35 

 graph.Caches[typeof(RSSVWorkOrderLabor)].Update(woLabor); PXFieldState fieldState = (PXFieldState)graph.Caches[typeof(RSSVWorkOrderLabor)]. GetStateExt<RSSVWorkOrderLabor.quantity>(woLabor); Assert.Equal(PhoneRepairShop.Messages.QuantityCannotBeNegative, fieldState.Error); Assert.Equal(PXErrorLevel.Error, fieldState.ErrorLevel); graph.Labor.Cache.Clear(); 

 In the code, the PXCache.Clear method is called to clear the cache of the generated error. 

5. By using the following code, assign to the Quantity field of the RSSVWorkOrderLabor object a value     that is less than the value of the corresponding RSSVLabor.Quantity field. Then make sure that the     following result is achieved: A warning message is attached to the RSSVWorkOrderLabor.Quantity     field, and the field is assigned the value of the corresponding RSSVLabor.Quantity field. 

 woLabor.Quantity = 1; graph.Caches[typeof(RSSVWorkOrderLabor)].Update(woLabor); woLabor = (RSSVWorkOrderLabor)graph. Caches[typeof(RSSVWorkOrderLabor)].Locate(woLabor); fieldState = (PXFieldState)graph. Caches[typeof(RSSVWorkOrderLabor)]. GetStateExt<RSSVWorkOrderLabor.quantity>(woLabor); Assert.Equal(PhoneRepairShop.Messages.QuantityTooSmall, fieldState.Error); Assert.Equal(PXErrorLevel.Warning, fieldState.ErrorLevel); Assert.Equal(3, woLabor.Quantity); 

 In the code, you use the PXCache.Locate method to obtain the proper RSSVWorkOrderLabor object from the cache to check the presence and text of the warning. 

6. By using the following code, configure the second repair service repairService2 to require a     preliminary check, and assign it to the work order. The code also sets the priority of the work order to _Low_     and makes sure that an error message is attached to the Priority field of the work order; this error     message informs the user that the priority of the work order is too low. 

 repairService2.PreliminaryCheck = true; graph.Caches[typeof(RSSVRepairService)].Update(repairService2); workOrder.ServiceID = repairService2.ServiceID; workOrder.Priority = WorkOrderPriorityConstants.Low; graph.Caches[typeof(RSSVWorkOrder)].Update(workOrder); workOrder = (RSSVWorkOrder)graph.Caches[typeof(RSSVWorkOrder)]. Locate(workOrder); fieldState = (PXFieldState)graph.Caches[typeof(RSSVWorkOrder)]. GetStateExt<RSSVWorkOrder.priority>(workOrder); Assert.Equal(PhoneRepairShop.Messages.PriorityTooLow, fieldState.Error); Assert.Equal(PXErrorLevel.Error, fieldState.ErrorLevel); 

7. Run the test method you have created, and make sure that it succeeds. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 36 

## Using AI-Assisted Diagnostics and Testing with Automated 

## Unit Tests 

 In this chapter, you'll learn how to use AI as a practical assistant while diagnosing and fixing defects in Acumatica ERP customization projects. You will: 

- Reproduce a failing unit test 

- Use AI to investigate the failure and propose a targeted fix 

- Review the suggested changes 

- Validate the result with automated tests and static analysis 

### AI-Assisted Diagnostics and Testing with Automated Unit Tests: General 

### Information 

 While creating or modifying a customization project for Acumatica ERP, you need a reliable way to detect when changes break the existing business logic. Automated unit tests give you a repeatable way to reproduce defects, verify expected behavior, and confirm that fixes work. AI tools such as GitHub Copilot can then help you interpret failures, diagnose the likely causes, and dra possible fixes or regression tests. 

 Throughout the process, you remain in control, reviewing and validating the suggestions before accepting them. 

#### Learning Objectives 

 In this chapter, you will learn how to do the following: 

- Use automated unit tests to reproduce a customization defect 

- Interpret failing assertions, exception messages, and stack traces 

- Prompt an AI assistant to explain a failure and suggest likely root causes 

- Review AI-suggested fixes before applying them 

- Use the AI assistant to help generate focused regression tests 

- Validate fixes by running automated tests 

#### Applicable Scenarios 

 The following are some of the scenarios in which you can use an AI assistant to help with diagnostics, fixes, and testing: 

- You make a change that causes an existing unit test to fail. 

- You notice that a graph or graph extension behaves differently than expected aer a code change. 

- You need to diagnose whether a failure is caused by implementation logic, test setup, missing     dependencies, or test data. 

- You want to add regression coverage aer fixing a defect. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 37 

#### AI-Assisted Unit Test Diagnostics 

 Effective AI-assisted diagnosis starts with a reproducible failure. Instead of first inspecting all the related source code manually, you run the test and collect the most important evidence: the failed assertion, expected value, actual value, exception message, stack trace, and relevant source files. 

 In Visual Studio, you may be able to start this workflow directly from Test Explorer. For example, if a Copilot menu command is available for a failed test, you can use it to explain the failure or start a debugging conversation with Copilot with the relevant test context. If no such Copilot menu command is available, provide the failed assertion, stack trace, and relevant source files to Copilot manually. 

 Aer you collect the evidence, you can ask the AI assistant to classify the failure and explain where to inspect first. AI can oen identify likely causes more quickly when it has enough context, such as the failing test method, related graph or graph extension, business rule, and failure output. You can then ask the AI assistant to suggest a fix. 

 However, you must review the AI assistant's output carefully. A suggested fix should be small , targeted , consistent with the existing architecture , and verifiable through the use of automated tests. You should reject suggestions that remove business validation, hard-code test-only values, rewrite unrelated code, or change the test expectation without justification. 

 Aer the fix is applied, you run the original test again. Then you can ask the AI assistant to help generate a focused regression test that directly protects the repaired behavior. 

 Automated tests validate behavior, but they are not the only automated validation tool available to you. Static analysis tools such as Acuminator can help you check customization code against Acumatica Framework rules and conventions. Acuminator diagnostics can also provide useful context for AI prompts because they identify framework-specific issues by diagnostic ID and rule description. 

#### Workflow of the Process 

 For AI-assisted diagnostics with automated unit tests and static validation, the typical process involves the following steps: 

1. Running the failing unit test 

2. Capturing the failure evidence 

3. Using a Test Explorer Copilot menu command or prompt AI to explain the likely cause and suggest a fix 

4. Reviewing the AI-suggested fix 

5. Applying a small, validated code change 

6. Rerunning the original test 

7. Using a reusable prompt file, inline chat, or chat prompt to dra a focused regression test 

8. Review and run the new test 

9. Run the Acuminator Console Runner on the customization code 10.Using AI to review and classify any Acuminator diagnostics 11.Building, testing, and rerunning static validation aer any accepted change 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 38 

### AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Diagnose a 

### Failing Unit Test 

 This activity will walk you through the process of using GitHub Copilot in Visual Studio to diagnose a failing unit test and suggest the smallest safe fix. 

#### Story 

 Suppose that the Smart Fix company has changed the customization project for the Repair Work Orders (RS301000) form. Aer the change, a unit test for the form's business logic fails. 

 The reported problem occurs when a user enters a labor quantity that is lower than the default labor quantity for the repair service. The system should show a warning and restore the quantity to the default value. You need to reproduce the failure, collect the evidence, and use Copilot to identify the likely root cause. You also need to ask Copilot to suggest the smallest safe fix. 

#### Process Overview 

 You'll diagnose the failing unit test and generate a fix by performing the following steps: 

1. Reviewing the expected labor quantity behavior 

2. Running the failing unit test in Visual Studio 

3. Capturing the failed assertion and stack trace, or using a Test Explorer Copilot menu command to start the     failure analysis 

4. Classifying the failure pattern 

5. Asking Copilot to inspect the relevant test and graph files 

6. Reviewing Copilot’s root-cause analysis and suggested fix 

#### System Preparation 

 Before you begin performing the steps of this activity, do the following: 

1. Verify that you’re signed in to Visual Studio with a GitHub account that has GitHub Copilot access. Use Visual     Studio 2026 if it’s available in your environment; if not, use Visual Studio 2022, Version 17.10 or later.     If Copilot is not installed or is inactive, open the Visual Studio Installer, select your Visual Studio installation,     click **Modify** , and make sure that **GitHub Copilot** is selected under optional components. Then restart     Visual Studio, sign in with a GitHub account that has Copilot access, and confirm that the status icon shows     that Copilot is active. 

 The exact Copilot commands, context-menu options, and mode names may differ between Visual Studio versions. If your integrated development environment (IDE) provides menu commands such as Explain failure with Copilot or Debug with Copilot in Test Explorer, use these commands as the primary path. Otherwise, use the prompts provided in this activity. 

2. Make sure that the environment you’re going to use conforms to the _System Requirements for the Acumatica_     _ERP Installation_. 

3. Make sure that the Web Server (IIS) features listed in _Configuration of IIS Web Server Features_ are turned on. 

4. Install the Acuminator extension for Visual Studio. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 39 

5. Install Acumatica ERP Version 2026 R1 or higher in your system. On the Main Soware Configuration page     of the Acumatica ERP Setup wizard, select the **Install Acumatica ERP** and **Install Debugger Tools** check     boxes. 

6. Deploy an Acumatica ERP instance as described in Step 2 of the _Test Instance for Unit Testing: To Deploy an_     _Instance_ activity. 

7. Download the _Help-and-Training-Examples_ repository in Acumatica GitHub to a folder on your     computer. You’ll find the Visual Studio solution with the failing unit test in the UnitTesting     \AIAssistedDiagnosticsAndTesting\DefectiveSolution\PhoneRepairShop folder. 

8. Replace the PhoneRepairShop folder in the App_Data\Projects folder of your instance     with the PhoneRepairShop folder, which you can find in the repository’s UnitTesting     \AIAssistedDiagnosticsAndTesting\DefectiveSolution\ folder. 

 The copied PhoneRepairShop folder includes course assets in the Assets folder. The Assets\CopilotPrompts folder contains the reusable prompt templates used in this activity and the next two activities. 

 The Assets\Acuminator folder contains prepared Acuminator report artifacts used in the AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Run the Acuminator Console Runner on Customization Code activity. 

9. Initialize a local Git repository in the PhoneRepairShop folder and copy the prompt templates to     .github\prompts folder. To do this, use Windows PowerShell to run each command shown below. 

 cd "C:\SmartFix_T280\App_Data\Projects\PhoneRepairShop" 

 git init 

 New-Item -ItemType Directory -Force -Path ".github\prompts" | Out-Null 

 Copy-Item ".\Assets\CopilotPrompts\*.prompt.md" ".\.github\prompts\" -Force Copy-Item ".\Assets\CopilotPrompts\copilot-instructions-template.md" ".\.github\copilot-instructions.md" -Force 

 Adjust the path if your Acumatica ERP instance is installed in a different folder. If your Visual Studio version doesn’t show the prompt files in Copilot Chat aer this setup, open the corresponding prompt template from Assets\CopilotPrompts and paste the prompt text into Copilot Chat manually. 10.In the App_Data\Projects\PhoneRepairShop folder, launch the PhoneRepairShop_code solution in Visual Studio. 11.Build the PhoneRepairShop_Code project. 12.Verify that the necessary NuGet packages and assembly references have already been added to the PhoneRepairShop_Code.Tests project. For details, see Steps 2 and 3 of the Test Project and Test Class: To Create a Test Project activity. 

#### Step 1: Reviewing the Expected Behavior 

 In this step, you'll review the expected behavior before reproducing the failure. Do the following: 

1. In Visual Studio, open RSSVWorkOrderEntryTests.cs. 

2. Locate the TestRepairWorkOrdersForm test method. 

3. Find the section where the test changes the Quantity field of an RSSVWorkOrderLabor record to 1. 

4. Review the expected result: 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 40 

- The QuantityTooSmall warning should be attached to the Quantity field. 

- The warning level should be PXErrorLevel.Warning. 

- The quantity should be restored to the default value, which is 3. 

5. Note the related graph, DAC, field, and message constant: 

- Graph: RSSVWorkOrderEntry 

- DAC: RSSVWorkOrderLabor 

- Field: Quantity 

- Message: Messages.QuantityTooSmall 

#### Step 2: Running the Failing Test 

 In this step, you'll reproduce the regression. Do the following: 

1. In Visual Studio, launch the Test Explorer by clicking **Test > Test Explorer**. 

2. In the Test Explorer window, expand the **PhoneRepairShop_Code.Tests** node and the     **RSSVWorkOrderEntryTests** node within it. Select the **TestRepairWorkOrdersForm** test and run it. 

3. Wait for the test to fail. 

4. If your Visual Studio version provides Copilot menu commands in Test Explorer, right-click the failed test     and select **Explain failure with Copilot**. Depending on your Visual Studio and Copilot settings, Copilot     may open a chat with the failed-test context and may offer to make edits. For this activity, use the menu     command only for diagnosis. If Copilot opens in a mode that can edit files, switch to Ask or Plan mode     before continuing. Do not allow Copilot to apply code changes in this step. 

5. If you aren’t using the **Explain failure with Copilot** menu command in Test Explorer or if the command is     unavailable, copy the following information into a file, which you can then paste into Copilot Chat: 

- Stack trace 

- Test method name 

- Failed assertion 

- Expected value 

- Actual value 

- Graph 

- DAC 

- Field 

- Warning expected 

- Warning level expected For example, here's how this information looks for the current scenario. 

 Item Value 

 Stack trace RSSVWorkOrderEntryTests.TestRepair- WorkOrdersForm() line 152 

 Test method TestRepairWorkOrdersForm 

 Failed assertion Assert.Equal(3, woLabor.Quantity); 

 Expected value 3 

 Actual value 1 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 41 

 Item Value 

 Graph RSSVWorkOrderEntry 

 DAC RSSVWorkOrderLabor 

 Field Quantity 

 Warning expected Messages.QuantityTooSmall 

 Warning level expected PXErrorLevel.Warning 

 The goal is to capture enough evidence for Copilot to analyze the failure without guessing. 

#### Step 3: Classifying the Failure Pattern with Copilot 

 In this step, you'll use Copilot to classify the failure before looking for a fix. 

 When a test fails, the first task is to determine what kind of failure you are dealing with—for example, a failed assertion, a runtime exception, a missing dependency, a test-data issue, or an implementation defect. Each type of failure can point to a different troubleshooting path. In this activity, the failure is expected to be a failed assertion, but you should still classify it before asking Copilot to suggest a fix. 

 Do the following: 

1. Review the failure output from Test Explorer. 

2. If you used the **Explain failure with Copilot** menu command in the previous step, review Copilot’s     explanation and classify the failure based on that response. 

3. If the **Explain failure with Copilot** menu command is not available, make sure these files are open in Visual     Studio: 

- RSSVWorkOrderEntryTests.cs 

- RSSVWorkOrderEntry.cs 

- Messages.cs 

4. Open GitHub Copilot Chat in Ask mode and use the reusable prompt file classify-acumatica-unit-     test-failure.prompt.md if it is available in Copilot Chat by typing _/_ and selecting the prompt. If     this file is not available, open Assets\CopilotPrompts\classify-acumatica-unit-test-     failure.prompt.md and paste the prompt text into Copilot Chat.     If you are not using the reusable prompt file, use the following prompt. 

 Classify this Acumatica unit test failure. 

 Failure output: 

- Failed assertion: Assert.Equal() 

- Expected value: 3 

- Actual value: 1 

- Stack Trace: RSSVWorkOrderEntryTests.TestRepairWorkOrdersForm() line 152 

 Use the open test and implementation files as context. 

 Please classify the failure as one of the following: 

1. Failed assertion 

2. Runtime exception 

3. Missing dependency/service registration 

4. Setup DAC or test data issue 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 42 

5. Implementation defect 

 Then explain: 

- What evidence supports the classification 

- Which file or method to inspect first 

- What not to change yet 

- Why the other categories are less likely 

- Whether this failure should be investigated as a test issue, setup issue,     or implementation issue 

 Do not propose a code change yet. Do not modify files. Do not change the test expectation. 

 Do not ask Copilot to edit files in this step. The goal is to classify the failure and identify where to inspect first. 

5. Confirm that Copilot classifies the current failure as a failed assertion that likely points to an     implementation defect. 

 By contrast, another common unit-test failure pattern involves a missing dependency registration. For example, a test can throw Autofac.Core.Registration.ComponentNotRegisteredException when a required service, such as a mock currency service, hasn’t been registered in the test class. In that kind of failure, the next action is not to inspect field validation logic but to register the required service. 

#### Step 4: Asking Copilot to Inspect the Failure and Suggest a Fix Plan 

 In this step, you'll ask Copilot to analyze the failing test without editing any files. Do the following: 

1. Use Copilot Chat in Plan mode. Do not edit files yet. If your Visual Studio version provides the **Debug with**     **Copilot** menu command, you can use it as a way to inspect the failing test and stack trace. However, for this     activity, continue with a review-only Copilot interaction until you understand the proposed diagnosis. Use     the reusable prompt file inspect-acumatica-unit-test-failure.prompt.md if it is available     in Copilot Chat. If it is not available, open Assets\CopilotPrompts\inspect-acumatica-unit-     test-failure.prompt.md and paste the prompt text into Copilot Chat.     If you're not using the reusable prompt file, use the following prompt. 

 Inspect the failing TestRepairWorkOrdersForm unit test. 

 Files to review: 

- PhoneRepairShop_Code.Tests/RSSVWorkOrderEntryTests.cs 

- PhoneRepairShop_Code/RSSVWorkOrderEntry.cs 

- PhoneRepairShop_Code/Helper/Messages.cs 

 The expected rule is: When RSSVWorkOrderLabor.Quantity is lower than the configured labor quantity, the system should attach the QuantityTooSmall warning and restore the quantity to the configured value. 

 Observed failure: The test sets woLabor.Quantity to 1. The QuantityTooSmall warning is expected, and woLabor. Quantity should be restored to 3. The test fails at the quantity assertion. 

 Failing assertion: Assert.Equal(3, woLabor.Quantity) 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 43 

 Actual value: 1 

 Do not edit files yet. 

 Please: 

1. Explain what the failing assertion means. 

2. Identify the most likely root cause. 

3. Point to the method or event handler to inspect first. 

4. Explain why the warning can still appear while the quantity is not restored. 

5. Propose the smallest safe fix as a plan only. 

6. List assumptions I should verify before editing code. 

7. Identify any Acumatica Framework convention or Acuminator rule that may be     relevant. 

8. Explain how the proposed fix should be validated. 

 Constraints: 

- Do not edit files. 

- Do not change the test expectation. 

- Do not remove Messages.QuantityTooSmall. 

- Do not change PXErrorLevel.Warning. 

- Do not hardcode a value only to make the test pass. 

- Do not rewrite unrelated graph logic. 

#### Step 5: Reviewing Copilot’s Diagnosis and Suggested Fix 

 In this step, you'll evaluate Copilot’s response before changing any code. 

 Confirm the following: 

1. Copilot points to the RSSVWorkOrderLabor.Quantity validation logic. 

2. The proposed root cause is related to the missing restoration of the quantity value. 

3. Copilot does not suggest changing the test expectation or removing the warning. 

4. Use the following checklist. 

 Review Item Question 

 Root cause Does Copilot explain why the quantity remains 1 instead of being restored to 3? 

 Architecture Does the proposed fix stay in RSSVWorkOrder- Entry.cs? 

 Scope Is the fix limited to labor quantity validation? 

 Warning behavior Does the proposed fix preserve Messages.QuantityTooSmall and PXError- Level.Warning? 

 Testability Can the fix be verified by rerunning the failing test? 

 Safety Did Copilot avoid invented APIs, unrelated rewrites, and test-only logic? 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 44 

 Review Item Question 

 Copilot mode Did you use Copilot for diagnosis only, without applying edits before review? 

 Acuminator convention If Copilot mentioned an Acuminator rule or Acumatica Framework convention, is the rule relevant to this failure? 

 In this activity, you've reproduced the labor quantity restoration regression and used Copilot to identify the likely source of the failure without making any code changes. You've also used Copilot to propose the smallest safe fix plan for the issue. 

 If Copilot proposes a fix, treat it as a plan until you review the exact code change in the AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Apply a Fix activity. 

### AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Apply a Fix 

 This activity will walk you through the process of using Copilot to apply a validated fix for the business logic and generate a focused regression test. 

#### Story 

 Suppose that Copilot has helped you identify the likely cause of the failing test: The validation logic still raises the warning, but it no longer restores the invalid labor quantity to the default quantity. 

 Copilot also suggested a fix as a response to your submitted prompt in Step 4 of the AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Diagnose a Failing Unit Test activity. 

 You now need to review and apply the suggested fix and add a focused regression test so that this defect is easier to diagnose if it recurs. 

#### Process Overview 

 You'll fix and regression-test the business logic by performing the following steps: 

1. Reviewing the proposed code changes of Copilot's suggested fix 

2. Applying the suggested fix through an inline chat aer reviewing the proposed diff 

3. Running the original TestRepairWorkOrdersForm test 

4. Asking Copilot to plan and generate a focused regression test by using a reusable prompt file, Copilot Chat,     or an inline chat 

5. Reviewing and running the new test 

#### System Preparation 

 Before you begin performing the steps of this activity, do the following: 

1. Complete the _AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Diagnose a Failing Unit Test_     activity. 

2. Keep the Copilot diagnosis available. 

3. Keep these files open in Visual Studio: 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 45 

- RSSVWorkOrderEntry.cs 

- RSSVWorkOrderEntryTests.cs 

- Messages.cs 

4. Confirm that the test still fails. 

#### Step 1: Reviewing and Applying the Suggested Fix 

 In this step, you'll verify that the suggested code change is correct and minimal and apply the suggested fix. You'll use a plan-before-edit workflow: 

1. Review Copilot’s proposed fix as an explanation. 

2. Apply the code change in the appropriate file 

 Do the following: 

1. Review the proposed diff in Copilot. 

2. Confirm that the change restores the invalid quantity to the default labor quantity. 

3. Confirm that no unrelated files were modified. 

4. Confirm that the warning behavior remains unchanged. 

5. Reject or revise the change if Copilot: 

- Changes the test instead of the implementation code 

- Removes Messages.QuantityTooSmall 

- Changes PXErrorLevel.Warning to PXErrorLevel.Error 

- Hardcodes 3 instead of using the default value 

- Rewrites unrelated event handlers or graph logic The correct fix should restore the value from the related default labor record. 

6. Make sure the RSSVWorkOrderEntry.cs file is open and currently in focus in Visual Studio. In the     Copilot Chat window, apply the proposed fix by selecting **Apply in Active Document** for the code snippet     that contains the proposed fix. 

7. Review the changes and click the **Keep** button that appears in the editor window of the     RSSVWorkOrderEntry.cs file to save these changes. 

#### Step 2: Running the Original Test 

 In this step, you'll verify that the fix restores the original behavior. Do the following: 

1. In Visual Studio's Test Explorer, rerun the TestRepairWorkOrdersForm test. 

2. Confirm that the test passes. 

3. If the test still fails and your Visual Studio version provides the **Explain failure with Copilot** menu     command for failed tests, right-click the failed test and select that command. If the menu command is not     available, use the prompt below. 

4. Ask Copilot to compare the new failure with the original one, but keep any follow-up changes small and     reviewable. Use the following prompt if the test still fails. 

 The fix did not make the original TestRepairWorkOrdersForm test pass. 

 Original failure: Expected woLabor.Quantity to be 3 after setting it to 1, but it remained 1. 

 New failure: 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 46 

 [Paste the new failure output.] 

 Do not edit files yet. 

 Please compare the new failure with the original failure and identify whether the fix was incomplete or whether a different assertion is now failing. 

#### Step 3: Asking Copilot to Plan and Generate a Focused Regression Test 

 In this step, you'll ask Copilot to add a smaller test that targets only the repaired behavior. 

 Use one of the following approaches: 

- **Preferred** : Use the reusable prompt file generate-acumatica-unit-regression-     test.prompt.md if it is available in Copilot Chat. If the file is not available, open Assets     \CopilotPrompts\generate-acumatica-unit-regression-test.prompt.md and paste the     prompt text into Copilot Chat or inline chat. 

- **Alternative** : Use Copilot inline chat in the RSSVWorkOrderEntryTests.cs file. 

- **Fallback** : Paste the prompt below into Copilot Chat. Ask Copilot to describe the test plan first. Aer you review the plan, ask Copilot to generate the test method. 

 Add one focused xUnit regression test to PhoneRepairShop_Code.Tests/RSSVWorkOrderEntryTests.cs. 

 Before generating code, briefly state the test goal and assumptions. Then generate the test method. 

 Test name: LaborQuantity_WhenBelowDefault_AttachesQuantityTooSmallWarningAndRestoresDefaultQuantity 

 Business rule: When RSSVWorkOrderLabor.Quantity is lower than the configured/default labor quantity, the system should attach the QuantityTooSmall warning and restore the quantity to the configured/default value. 

 The test should specifically verify: 

1. Setting the work order labor quantity to 1 triggers Messages.QuantityTooSmall. 

2. The field state has PXErrorLevel.Warning. 

3. The work order labor quantity is restored to the configured/default value of 3. 

 Use the existing setup pattern already present in RSSVWorkOrderEntryTests.cs: 

- Setup<RSSVWorkOrderEntry>(new RSSVSetup()) 

- PXGraph.CreateInstance<RSSVWorkOrderEntry>() 

- PXCache.GetStateExt to inspect PXFieldState 

- PXCache.Locate to retrieve the proper RSSVWorkOrderLabor object after validation 

- Existing message constants from PhoneRepairShop.Messages 

 Constraints: 

- Follow Acumatica Unit Test Framework patterns and Acuminator-friendly coding conventions. 

- Do not change production code. 

- Do not require a live database or browser session. 

- Reuse existing setup patterns from the file. 

- Use Arrange, Act, Assert comments. 

- Keep the test readable. 

- Do not hide the tested business rule behind too many helper methods. 

- Show me the diff before running the test. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 47 

 After generating the code, list what I should verify before running the test. 

 If Copilot provides a code block in chat, prefer the Preview or Apply in Active Document commands so you can review the diff. Do not copy code blindly into the file. 

#### Step 4: Reviewing and Accepting the Generated Test 

 In this step, you'll confirm that the generated test protects the repaired behavior. Do the following: 

1. Confirm that the test initializes the setup DAC by using Setup<RSSVWorkOrderEntry>(new     RSSVSetup()). 

2. Confirm that the test creates the graph with     PXGraph.CreateInstance<RSSVWorkOrderEntry>(). 

3. Confirm that the test creates or reuses the same repair service, device, repair price, labor, and work order     setup used in the originally failing test. 

4. Confirm that the test sets woLabor.Quantity to 1. 

5. Confirm that the test calls PXCache.Locate before inspecting the final cached object. 

6. Confirm that the test asserts: 

- Messages.QuantityTooSmall 

- PXErrorLevel.Warning 

- Restored quantity of 3 

7. Remove or revise any generated code that: 

- Hardcodes values unrelated to the original test setup 

- Changes production code 

- Avoids PXFieldState 

- Omits verification of the restored quantity 

8. Save the generated test to the RSSVWorkOrderEntryTests.cs file. 

9. Confirm that Copilot generated the test in the correct class and did not add unrelated helper methods. 10.Make sure that the generated test follows the Arrange, Act, Assert structure. 11.Confirm that the generated test is not larger or more complex than the original broad test. 

#### Step 5: Running the Regression Test 

 In this step, you'll verify that the focused test works. Do the following: 

1. Build the test project. 

2. Run the new focused regression test. 

3. Run the original TestRepairWorkOrdersForm test again. 

4. Confirm that both tests pass. 

 In this activity, you have used Copilot to restore the labor quantity validation behavior and to add a focused regression test that protects the quantity restoration rule. You have also used a review-first workflow so that AIgenerated changes are reviewed, applied intentionally, and validated by automated tests. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 48 

### AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Run the 

### Acuminator Console Runner on Customization Code 

 This activity will walk you through the process of running Acuminator static analysis on the customization project and using an AI assistant to review the diagnostics. You'll use the Acuminator Console Runner to run the static analysis. 

#### Story 

 Suppose that you’ve fixed the labor quantity restoration defect and verified the fix with automated unit tests. Before moving to browser-level validation, you want to run a static analysis check to confirm that the customization code follows Acumatica Framework rules and conventions. 

 Automated tests validate behavior. Acuminator static analysis validates a different concern: whether the customization code follows Acumatica Framework patterns and avoids common framework-specific mistakes. 

#### Process Overview 

 You'll run static validation and review the results by performing the following steps: 

1. Building the customization project 

2. Running the Acuminator Console Runner on the customization project 

3. Reviewing the generated report 

4. Asking Copilot to classify the diagnostics 

5. Reviewing any AI-suggested changes 

6. Validating any accepted change if you decide to apply the suggested fix 

#### System Preparation 

 Before you begin performing the steps of this activity, do the following: 

1. Complete the _AI-Assisted Diagnostics and Testing with Automated Unit Tests: To Apply a Fix_ activity. 

2. Make sure the PhoneRepairShop_Code project builds successfully. 

3. Make sure the original unit test and the focused regression test pass. 

4. Verify the availability of the Acuminator Console Runner on your machine. You can download the latest     version of the Acuminator.Runner.NetFramework.zip file from Acumatica GitHub _here_ and extract     it to a local folder on your machine. 

5. Create a folder, such as C:\acuminator\reports\, for the Acuminator report. 

6. Identify the path to the customization project that should be analyzed. This should be the customization     project (PhoneRepairShop_Code), not the test project (PhoneRepairShop_Code.Tests).     For example: C:\SmartFix_T280\App_Data\Projects\PhoneRepairShop     \PhoneRepairShop_Code\PhoneRepairShop_Code.csproj 

#### Step 1: Building the Customization Project 

 In this step, you'll confirm that you can successfully build the customization project before you run static analysis. Do the following: 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 49 

1. In Visual Studio, build the PhoneRepairShop_Code project. 

2. Confirm that the build succeeds. 

3. If the build fails, address the failure before running the Acuminator Console Runner. 

 Do not run Acuminator on the PhoneRepairShop_Code.Tests project. The goal is to analyze the customization code. 

#### Step 2: Running the Acuminator Console Runner 

 In this step, you'll run the Acuminator Console Runner on the customization code and save the report. Do the following: 

1. Open Windows PowerShell on your computer and run the following commands one by one. Adjust the paths     for your environment: 

- $ACUMINATOR_RUNNER =     "C:\Acuminator.Runner.NetFramework\Acuminator.Runner.NetFramework.exe" 

#####
• $CUSTOMIZATION_PROJECT = 

 "C:\SmartFix_T280\App_Data\Projects\PhoneRepairShop\ PhoneRepairShop_Code\PhoneRepairShop_Code.csproj" 

#####
• $REPORT_PATH = 

 "C:\AIAssistedDiagnostics\artifacts\acuminator\acuminator-report.json" 

- New-Item -ItemType Directory -Force -Path (Split-Path $REPORT_PATH)     | Out-Null 

 You use the commands above to specify variables for the locations of the following: 

- The Acuminator Console Runner executable file. 

- The customization project on which you want to run the Acuminator Console Runner. 

- The folder where the generated report should be saved. The last command in the list above tells     PowerShell to create the folder that will contain the report if it doesn't already exist. 

2. Use the variables created in the preceding instruction to run the following command in the same     PowerShell terminal. 

 & $ACUMINATOR_RUNNER $CUSTOMIZATION_PROJECT --format json -f $REPORT_PATH -g FD --non-interactive 

 The command uses the following parts. 

 Command Part Purpose 

 $ACUMINATOR_RUNNER Stores the path to the Acuminator Console Runner. 

 $CUSTOMIZATION_PROJECT Stores the path to the customization project to analyze. 

 --format json Saves the report in JSON format. 

 -f $REPORT_PATH Writes the report to the specified file. 

 -g FD Groups diagnostics by file and diagnostic ID. 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 50 

 Command Part Purpose 

 --non-interactive Runs in non-interactive mode, which is suitable for automated environments. 

#### Step 3: Reviewing the Report 

 In this step, you'll inspect the generated report before asking Copilot for help. Do the following: 

1. Open the generated report file from the location you’d specified in the previous step. 

2. Determine whether the report contains diagnostics, and identify the following information for one or two     important diagnostics: 

- The Diagnostic ID, such as PX1077 

- The file in which the issue was found 

- The message related to the raised diagnostic 

- The severity of the diagnostic 

#### Step 4: Asking Copilot to Classify the Diagnostics 

 In this step, you'll use Copilot to interpret the report generated by the Acuminator Console Runner. 

 The Acuminator diagnostics summary lists diagnostic IDs, rule descriptions, severity information, and code-fix availability, which makes it useful context for AI prompts. 

 For the purposes of this activity, you'll only use the following two diagnostics from a modified version of the generated report. Adjust the path to the customization project based on your environment. 

 { "codeSourceName": "C:\\AcuTestInstances\\SmartFix_T280\\App_Data\\Projects \\PhoneRepairShop\\PhoneRepairShop_Code\\ PhoneRepairShop_Code.csproj", "totalDiagnosticsCount": 4, "projectReports": [ { "projectName": "PhoneRepairShop_Code", "totalDiagnosticsCount": 4, "distinctDiagnosticsCount": 2, "reportDetails": { "totalDiagnosticsCount": 4, "distinctDiagnosticsCount": 2, "childrenTitle": "Found Errors", "childrenGroups": [ { "groupTitle": "C:\\AcuTestInstances\\SmartFix_T280\\App_Data\\Projects \\PhoneRepairShop\\PhoneRepairShop_Code\\ RSSVWorkOrderEntry.cs", "totalDiagnosticsCount": 4, "distinctDiagnosticsCount": 2, "childrenGroups": [ { "groupTitle": "PX1077", "totalDiagnosticsCount": 2, "lines": 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 51 

 [ "PX1077: Event handlers should be protected virtual: \u0022.\\RSSVWorkOrderEntry.cs: (107,23)-(107,24)\u0022", "PX1077: Event handlers should be protected virtual: \u0022.\\RSSVWorkOrderEntry.cs: (123,23)-(123,24)\u0022" ] }, { "groupTitle": "PX1094", "totalDiagnosticsCount": 2, "lines": [ "PX1094: A DAC must be decorated with the PXHidden or PXCacheName attribute: \u0022.\\RSSVWorkOrderEntry.cs: (44,15)-(44,26)\u0022", "PX1094: A DAC must be decorated with the PXHidden or PXCacheName attribute: \u0022.\\RSSVWorkOrderEntry.cs: (50,15)-(50,27)\u0022" ] } ] } ] } } ] } 

Open Copilot Chat in Ask mode and use the reusable prompt file review-acuminator-report.prompt.md if it is available in Copilot Chat. If it isn’t available, open Assets\CopilotPrompts\review-acuminatorreport.prompt.md and paste the prompt text into Copilot Chat. 

If prompt files are not available, use the following prompt. 

 Review this Acuminator Console Runner report for the PhoneRepairShop customization project. 

 Do not modify files yet. 

 Please: 

1. Group the diagnostics by severity and diagnostic ID. 

2. Explain the Acumatica Framework rule behind each important diagnostic. 

3. Identify the first file or method to inspect. 

4. Classify each diagnostic as one of the following: 

- Fix now 

- Review with SME 

- Probably not relevant to this scenario 

- Suppression may be justified 

5. If a fix is appropriate, suggest the smallest safe change. 

6. Explain how to verify the fix after applying it. 

7. Identify any diagnostics that may be unrelated to the current labor quantity scenario. 

 Use Acuminator diagnostic IDs when possible. Do not suppress diagnostics unless there is a clear justification. Do not rewrite unrelated code. 

 Report: [Paste the report excerpt.] 


<!-- PAGE_BREAK -->
 Using AI-Assisted Diagnostics and Testing with Automated Unit Tests | 52 

#### Step 5: Reviewing AI Output 

 In this step, you'll review Copilot’s explanation before deciding whether to change the code. To do this, use the following checklist. 

 Review Item Question 

 Diagnostic ID Did Copilot identify the correct Acuminator rule? 

 Rule explanation Did Copilot explain Acumatica Framework's reason for the rule? 

 Scope Is the suggested fix limited to the reported code? 

 Safety Does the suggestion avoid broad rewrites? 

 Verification Can the change be verified by building, running tests, and rerunning Acuminator? 

 Suppression Did Copilot avoid suppressing the diagnostic without justification? 

 SME review Should this diagnostic be reviewed by an SME before a fix is applied? 

 Do not apply a code change just because Copilot suggests one. Treat the AI output as a diagnostic aid. 

#### Step 6: Validating the Applied Changes (Optional) 

 If you decide to apply a fix based on Copilot's suggestions in the preceding step, do the following: 

1. Apply the smallest safe code change. 

2. Build the PhoneRepairShop_Code project. 

3. Run the original unit test. 

4. Run the focused regression test. 

5. Rerun the Acuminator Console Runner. 

6. Confirm that the diagnostic is resolved, or record why it should remain for SME review. 

 In this activity, you have run an automated static validation check on the customization code and used Copilot to interpret the results. The unit tests confirm behavior, while the Acuminator static analysis helps confirm that the customization code follows Acumatica Framework rules and conventions. 


