Getting Started with xUnit.net
==============================

Using .NET Framework with Visual Studio
---------------------------------------

In this article, we will demonstrate getting started with xUnit.net, showing you how to write and run your first set of unit tests.

*   [Create a unit test project](#create-project)
*   [Learning to use Test Explorer](#test-explorer)
*   [Write your first tests](#write-first-tests)
*   [Write your first theory](#write-first-theory)
*   [Running tests against multiple target frameworks](#multi-targeting)

_Note: The examples were done with xUnit.net v2.4.1 and Visual Studio 2019. The version numbers, paths, and Visual Studio UI may differ for you, depending on which version you're using._

Create a unit test project
--------------------------

Start Visual Studio, which will bring you to the start splash screen. Under "Get Started", click "Create a new project". This will bring you to the first step of the new project wizard, where you pick your project type:

![](/images/getting-started/netcore/new-project-step1-vs2019.png)

In the drop down boxes, chooses your language (C#), your platform (All platforms), and your project type (Test). Scroll through the list if necessary until you find the item titled "xUnit Test Project (.NET Core)". Select it, then click "Next".

We're picking .NET Core even though we're planning to make a .NET Framework test project, because Visual Studio doesn't contain a test project template for xUnit.net for .NET Framework. We'll fix that in just a moment.

This leads you to the second part of the new project wizard:

![](/images/getting-started/netcore/new-project-step2-vs2019.png)

Type a name into the "Project name" box (like "MyFirstUnitTests"). Click "Create".

After a moment, Visual Studio will launch with your newly created project.

Find the project in the Solution Explorer (it will be titled "MyFirstUnitTests"), right click it, then click "Edit Project File". This will launch the text editor for your project file. It should look something like this:

    <Project Sdk="Microsoft.NET.Sdk">
    
      <PropertyGroup>
        <TargetFramework>net5.0</TargetFramework>
    
        <IsPackable>false</IsPackable>
      </PropertyGroup>
    
      <ItemGroup>
        <PackageReference Include="Microsoft.NET.Test.Sdk" Version="16.7.1" />
        <PackageReference Include="xunit" Version="2.4.1" />
        <PackageReference Include="xunit.runner.visualstudio" Version="2.4.3">
          <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
          <PrivateAssets>all</PrivateAssets>
        </PackageReference>
        <PackageReference Include="coverlet.collector" Version="1.3.0">
          <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
          <PrivateAssets>all</PrivateAssets>
        </PackageReference>
      </ItemGroup>
    
    </Project>

We need to make one quick change: use a target framework that indicates .NET Framework support. For example, if you want to support .NET Framework 4.8, change the `TargetFramework` element like so:

    <TargetFramework>net48</TargetFramework>

Let's quickly review what's in this project file:

*   `TargetFramework` specifies the target framework for your test project. We've already changed this to `net48` for .NET Framework 4.8. Later in this article, we will discuss [running tests against multiple target frameworks](#multi-targeting).
*   `IsPackable` is here, though it is redundant (unit test projects cannot be packed by default). You can safely remove this line if you wish.
*   The `xunit` package brings in three child packages which include functionality that most developers want: `xunit.core` (the testing framework itself), `xunit.assert` (the library which contains the `Assert` class), and `xunit.analyzers` (which enables Roslyn analyzers to detect common issues with unit tests and xUnit.net extensibility).
*   The packages `xunit.runner.visualstudio` and `Microsoft.NET.Test.Sdk` are required for being able to run your test project inside Visual Studio as well as with `dotnet test`.
*   The `coverlet.collector` package allows collecting code coverage. If you don't intend to collect code coverage, you should remove this package reference.

A single empty unit test was also generated into `UnitTest1.cs`:

    using System;
    using Xunit;
    
    namespace MyFirstUnitTests
    {
        public class UnitTest1
        {
            [Fact]
            public void Test1()
            {
    
            }
        }
    }

Let's make sure everything builds. Choose `Build > Build Solution` from the main menu. Your project should build without issue, as shown in the output window:

Build started...
1>------ Build started: Project: MyFirstUnitTests, Configuration: Debug Any CPU ------
1>MyFirstUnitTests -> C:\\Dev\\MyFirstUnitTests\\bin\\Debug\\net48\\MyFirstUnitTests.dll
========== Build: 1 succeeded, 0 failed, 0 up-to-date, 0 skipped ==========

Learning to use Test Explorer
-----------------------------

Test Explorer is the name of the window that lets you browse and run your tests from within Visual Studio. Open it by choosing `Test > Test Explorer` from the main menu. You should be greeted with a window that contains a hierarchy of the tests in your project, which should look something like this:

![](/images/getting-started/common/test-explorer-newproject-vs2019.png)

The toolbar of Test Explorer has buttons in several groups:

*   The first group contains buttons that are used for running tests, including the ability to run all tests, run selected tests, re-run the last tests, and re-run only the failed tests.
*   The second group contains buttons which allow filtering the list of tests based on current state (which includes "passed", "failed", and "not run").
*   The third group contains buttons which configure Test Explorer, including advanced options like changing processor architecture (x86, x64, or Auto) and automatically running tests after every successful build.

The main window of Test Explorer is split into two panes:

*   The left pane contains a tree view of the tests in your project (grouping criteria can be changed as you see fit). Columns can be configured to show details about the test, including things like the current state, how long the test took to run, metadata (traits) related to the test, and more.
*   As you select items in the tree view on the left pane, the right pane will provide information about your current selection, including test counts, outcomes, links to the source of the test, test output, and exception messages and stack traces for failed tests.

Click the left-most button on the Test Explorer toolbar (it looks like a double green arrow, titled "Run All Tests In View". This will run the single empty test, and the result should be success:

![](/images/getting-started/common/test-explorer-success-vs2019.png)

Now that we've ensured everything is working, it's time to write our first real tests.

Write your first tests
----------------------

Edit `UnitTest1.cs` and replace the default file contents with this:

    using Xunit;
    
    namespace MyFirstUnitTests
    {
        public class UnitTest1
        {
            [Fact]
            public void PassingTest()
            {
                Assert.Equal(4, Add(2, 2));
            }
    
            [Fact]
            public void FailingTest()
            {
                Assert.Equal(5, Add(2, 2));
            }
    
            int Add(int x, int y)
            {
                return x + y;
            }
        }
    }

Now let's go run the tests again and see what happens:

![](/images/getting-started/common/test-explorer-failure1-vs2019.png)

We purposefully wrote both a passing and failing test, and we can see that the results reflect that. By clicking on the failed test, we can see a link both to the top of the unit test (at line 14), but also the failure message (we expected 5 but got 4) as well as a link to the exact line where the failure occurred (line 16).

When you edit the source file, also take note of the fact that CodeLens decorations show up which indicate not only test status (passed/failed) on the test themselves, but also on functions that are called by the code, indicating how often the code is called in tests, and a count of which of those tests have passed or failed:

![](/images/getting-started/common/codelens-status-vs2019.png)

Now that we've gotten your first unit tests to run, let's introduce one more way to write tests: using theories.

Write your first theory
-----------------------

You may have wondered why your first unit tests use an attribute named `[Fact]` rather than one with a more traditional name like Test. xUnit.net includes support for two different major types of unit tests: facts and theories. When describing the difference between facts and theories, we like to say:

> _**Facts** are tests which are always true. They test invariant conditions._
> 
> _**Theories** are tests which are only true for a particular set of data._

A good example of this is testing numeric algorithms. Let's say you want to test an algorithm which determines whether a number is odd or not. If you're writing the positive-side tests (odd numbers), then feeding even numbers into the test would cause it fail, and not because the test or algorithm is wrong.

Let's add a theory to our existing facts (including a bit of bad data, so we can see it fail):

    [Theory]
    [InlineData(3)]
    [InlineData(5)]
    [InlineData(6)]
    public void MyFirstTheory(int value)
    {
        Assert.True(IsOdd(value));
    }
    
    bool IsOdd(int value)
    {
        return value % 2 == 1;
    }

This time when we run our tests, we see a second failure, for our theory that was given 6:

![](/images/getting-started/common/test-explorer-failure2-vs2019.png)

Although we've only written 3 test methods, the test runner actually ran 5 tests; that's because each theory with its data set is a separate test. Note also that the runner tells you exactly which set of data failed, because it includes the parameter values in the name of the test. The Test Explorer UI even shows a new level in the tree, as each row of data becomes a test result underneath its test method.

Running tests against multiple target frameworks
------------------------------------------------

Sometimes, you want to write tests and ensure they run against several target application platforms. The xUnit.net test runner that we've been using supports .NET Core 1.0 or later, .NET 5.0 or later, and .NET Framework 4.5.2 or later. With a single test project, we can have our tests run against multiple target frameworks. Open the `.csproj` file and make the following change.

Change `TargetFramework`:

    <PropertyGroup>
      <TargetFramework>net48</TargetFramework>
    </PropertyGroup>

To `TargetFrameworks`:

    <PropertyGroup>
      <TargetFrameworks>net48;net5.0</TargetFrameworks>
    </PropertyGroup>

When you change a project file from `TargetFramework` to `TargetFrameworks` (or back), Visual Studio might show you a yellow "alert bar" which indicates that you have to reload the project for your changes to take effect. It's best to make this kind of change from a clean environment with no dirty text editors, to prevent the possibility of losing any changes.

Test Explorer supports any combination of .NET Core (including .NET 5+) and .NET Framework targets. You can even include multiple versions of the same target framework (for example, it's legal to have something like `<TargetFrameworks>net452;net461;net48;netcoreapp2.1;netcoreapp3.1;net5.0</TargetFrameworks>`). Application authors will typically only use a single target framework, related to the target framework the application is intended to run on. Library authors are more likely to use several target frameworks, to ensure their tests run successfully on all supported target frameworks.

The Test Explorer tree view will now show your test project multiple times, once for each target framework. You can run individual tests from individual frameworks, or you can simply run all tests for all frameworks.

![](/images/getting-started/common/test-explorer-multitarget-vs2019.png)

###### Copyright © 2022 .NET Foundation. Contributions welcomed at [https://github.com/xunit/xunit/tree/gh-pages](https://github.com/xunit/xunit/tree/gh-pages).

 

[Cake ⭐ 3,172](https://awesomeopensource.com/project/cake-build/cake)

[🍰 Cake (C# Make) is a cross platform build automation system.](https://awesomeopensource.com/project/cake-build/cake)

 
[Xunit ⭐ 3,140](https://awesomeopensource.com/project/xunit/xunit)

[xUnit.net is a free, open source, community-focused unit testing tool for the .NET Framework.](https://awesomeopensource.com/project/xunit/xunit)

[Bats Core ⭐ 2,854](https://awesomeopensource.com/project/bats-core/bats-core)

[Bash Automated Testing System](https://awesomeopensource.com/project/bats-core/bats-core)

[Fluentassertions ⭐ 2,508](https://awesomeopensource.com/project/fluentassertions/fluentassertions)

[A very extensive set of extension methods that allow you to more naturally specify the expected outcome of a TDD or BDD-style unit tests. Targets .NET Framework 4.7, .NET Core 2.1 and 3.0, as well as .NET Standard 2.0 and 2.1. Supports the unit test frameworks MSTest2, NUnit3, XUnit2, MSpec, and NSpec3.](https://awesomeopensource.com/project/fluentassertions/fluentassertions)

[Specflow ⭐ 1,836](https://awesomeopensource.com/project/SpecFlowOSS/SpecFlow)

[#1 .NET BDD Framework. SpecFlow automates your testing & works with your existing code. Find Bugs before they happen. Behavior Driven Development helps developers, testers, and business representatives to get a better understanding of their collaboration](https://awesomeopensource.com/project/SpecFlowOSS/SpecFlow)

[Bunit ⭐ 626](https://awesomeopensource.com/project/bUnit-dev/bUnit)

[bUnit is a testing library for Blazor components that make tests look, feel, and runs like regular unit tests. bUnit makes it easy to render and control a component under test’s life-cycle, pass parameter and inject services into it, trigger event handlers, and verify the rendered markup from the component using a built-in semantic HTML comparer.](https://awesomeopensource.com/project/bUnit-dev/bUnit)
 

[Bash\_unit ⭐ 489](https://awesomeopensource.com/project/pgrange/bash_unit)

[bash unit testing enterprise edition framework for professionals](https://awesomeopensource.com/project/pgrange/bash_unit)

[Fsunit ⭐ 322](https://awesomeopensource.com/project/fsprojects/FsUnit)

[FsUnit makes unit-testing with F# more enjoyable. It adds a special syntax to your favorite .NET testing framework.](https://awesomeopensource.com/project/fsprojects/FsUnit)

[Camelotia ⭐ 290](https://awesomeopensource.com/project/worldbeater/Camelotia)

[Cross-platform .NET sample GUI app for cloud file management. Built with ReactiveUI, AvaloniaUI, Universal Windows Platform, Xamarin Forms, and WPF, runs on Windows, Linux, Mac and Android.](https://awesomeopensource.com/project/worldbeater/Camelotia)

[Unittest Xml Reporting ⭐ 259](https://awesomeopensource.com/project/xmlrunner/unittest-xml-reporting)

[unittest-based test runner with Ant/JUnit like XML reporting.](https://awesomeopensource.com/project/xmlrunner/unittest-xml-reporting)

[Ocaramba ⭐ 247](https://awesomeopensource.com/project/ObjectivityLtd/Ocaramba)

[C# Framework to automate tests using Selenium WebDriver](https://awesomeopensource.com/project/ObjectivityLtd/Ocaramba)

[Lightbdd ⭐ 238](https://awesomeopensource.com/project/LightBDD/LightBDD)

[BDD framework allowing to create easy to read and maintain tests.](https://awesomeopensource.com/project/LightBDD/LightBDD)

[Designpatterns ⭐ 217](https://awesomeopensource.com/project/Finickyflame/DesignPatterns)

[Simple repository containing one simple example for all existing patterns in C#](https://awesomeopensource.com/project/Finickyflame/DesignPatterns)

[Xunit.dependencyinjection ⭐ 175](https://awesomeopensource.com/project/pengweiqhca/Xunit.DependencyInjection)

[Use Microsoft.Extensions.DependencyInjection to resolve xUnit test cases.](https://awesomeopensource.com/project/pengweiqhca/Xunit.DependencyInjection)

[Snapshooter ⭐ 171](https://awesomeopensource.com/project/SwissLife-OSS/snapshooter)

[Snapshooter is a snapshot testing tool for .NET Core and .NET Framework](https://awesomeopensource.com/project/SwissLife-OSS/snapshooter)

[Aspnetcore Ddd ⭐ 166](https://awesomeopensource.com/project/ntxinh/AspNetCore-DDD)

[Full ASP.NET Core 5.0 LTS application with DDD, CQRS and Event Sourcing](https://awesomeopensource.com/project/ntxinh/AspNetCore-DDD)

[Xunit.gherkin.quick ⭐ 151](https://awesomeopensource.com/project/ttutisani/Xunit.Gherkin.Quick)

[BDD in .NET Core - using Xunit and Gherkin (compatible with both .NET Core and .NET)](https://awesomeopensource.com/project/ttutisani/Xunit.Gherkin.Quick)

[Xunit.analyzers ⭐ 112](https://awesomeopensource.com/project/xunit/xunit.analyzers)

[Roslyn analyzers for xUnit.net (please open issues in https://github.com/xunit/xunit)](https://awesomeopensource.com/project/xunit/xunit.analyzers)

[Xunit Logging ⭐ 97](https://awesomeopensource.com/project/martincostello/xunit-logging)

[Logging extensions for xunit](https://awesomeopensource.com/project/martincostello/xunit-logging)

[Xunitcontext ⭐ 89](https://awesomeopensource.com/project/SimonCropp/XunitContext)

[Extends xUnit to expose extra context and simplify logging](https://awesomeopensource.com/project/SimonCropp/XunitContext)

[Xunit.categories ⭐ 78](https://awesomeopensource.com/project/brendanconnolly/Xunit.Categories)

[Friendlier attributes to help categorize your tests](https://awesomeopensource.com/project/brendanconnolly/Xunit.Categories)

[Xharness ⭐ 74](https://awesomeopensource.com/project/dotnet/xharness)

[C# command line tool for running tests on Android / iOS / tvOS devices and simulators](https://awesomeopensource.com/project/dotnet/xharness)

 

[Ddd Tdd Rich Domain Model Dojo Kata ⭐ 70](https://awesomeopensource.com/project/ivanpaulovich/ddd-tdd-rich-domain-model-dojo-kata)

[DDD patterns implemented following TDD](https://awesomeopensource.com/project/ivanpaulovich/ddd-tdd-rich-domain-model-dojo-kata)

[Devices.xunit ⭐ 69](https://awesomeopensource.com/project/xunit/devices.xunit)

[xUnit.net Runners for Devices](https://awesomeopensource.com/project/xunit/devices.xunit)

[Aspnetcoreactivedirectorystarterkit ⭐ 58](https://awesomeopensource.com/project/WinLwinOoNet/AspNetCoreActiveDirectoryStarterKit)

[Starter kit to quickly create ASP.NET Core with On-Premises Active Directory Authentication.](https://awesomeopensource.com/project/WinLwinOoNet/AspNetCoreActiveDirectoryStarterKit)

[Pact Workshop Dotnet Core V1 ⭐ 58](https://awesomeopensource.com/project/pact-foundation/pact-workshop-dotnet-core-v1)

[A workshop for Pact using .NET Core](https://awesomeopensource.com/project/pact-foundation/pact-workshop-dotnet-core-v1)

[Xunit.testlogger ⭐ 58](https://awesomeopensource.com/project/spekt/xunit.testlogger)

[XUnit logger for vstest platform](https://awesomeopensource.com/project/spekt/xunit.testlogger)

[Chainingassertion ⭐ 49](https://awesomeopensource.com/project/neuecc/ChainingAssertion)

[Method Chaining base UnitTesting Extension Methods and Dynamic Private Accessor for MSTest, NUnit, xUnit.net.](https://awesomeopensource.com/project/neuecc/ChainingAssertion)

[Aspnetcoretests ⭐ 48](https://awesomeopensource.com/project/gpeipman/AspNetCoreTests)

[Simple, clean and minimalistic ASP.NET Core solution demonstrating unit and integration tests](https://awesomeopensource.com/project/gpeipman/AspNetCoreTests)

[Mscoreone ⭐ 48](https://awesomeopensource.com/project/trungcaot/MsCoreOne)

[MsCoreOne is a simple Ecommerce with using many technologies such as .NET 5, Entity Framework Core 5, React 16.13 with modern Clean Architecture, Domain-Driven Design, CQRS, SOLID, Identity Server 4, Blazor. It will focus on resolving the problems always see in the process to develop projects.](https://awesomeopensource.com/project/trungcaot/MsCoreOne)

[Kodkod ⭐ 47](https://awesomeopensource.com/project/alirizaadiyahsi/Kodkod)

[https://github.com/alirizaadiyahsi/Nucleus Web API layered architecture startup template with ASP.NET Core 2.1, EF Core 2.1 and Vue Client](https://awesomeopensource.com/project/alirizaadiyahsi/Kodkod)

[Generic For Core ⭐ 46](https://awesomeopensource.com/project/senvardarsemih/generic-for-core)

[🏗 Generic Repository & UOW Pattern For ASP.NET Core](https://awesomeopensource.com/project/senvardarsemih/generic-for-core)

[Toolbox ⭐ 38](https://awesomeopensource.com/project/deinsoftware/toolbox)

[dein ToolBox - C# .Net Library with utilities like: command line, files, log, platform, shell, system, transform and validation \[ Win+Mac+Linux \]](https://awesomeopensource.com/project/deinsoftware/toolbox)

[Aspnetcoremvcprotobufformatters ⭐ 37](https://awesomeopensource.com/project/damienbod/AspNetCoreMvcProtobufFormatters)

[ASP.NET Core MVC Protobuf Formatters (InputFormatter and OutputFormatter)](https://awesomeopensource.com/project/damienbod/AspNetCoreMvcProtobufFormatters)

[Tap Xunit ⭐ 35](https://awesomeopensource.com/project/aghassemi/tap-xunit)

[TAP to xUnit XML converter](https://awesomeopensource.com/project/aghassemi/tap-xunit)

[Architectnow.apistarter ⭐ 34](https://awesomeopensource.com/project/ArchitectNow/ArchitectNow.ApiStarter)

[Sample ASP.NET Core 2 API Setup used by ArchitectNow for corresponding workshop presentations](https://awesomeopensource.com/project/ArchitectNow/ArchitectNow.ApiStarter)

[Jsonnetunit ⭐ 34](https://awesomeopensource.com/project/yugui/jsonnetunit)

[Unit testing framework for Jsonnet](https://awesomeopensource.com/project/yugui/jsonnetunit)

[Xamarinstudio.xunit ⭐ 33](https://awesomeopensource.com/project/xunit/xamarinstudio.xunit)

[xUnit.net support for Xamarin Studio](https://awesomeopensource.com/project/xunit/xamarinstudio.xunit)

[Unittestingtools ⭐ 29](https://awesomeopensource.com/project/EduardoPires/UnitTestingTools)

[Great tools to increase the quality of your unit tests in .NET C#](https://awesomeopensource.com/project/EduardoPires/UnitTestingTools)

[Contoso University ⭐ 28](https://awesomeopensource.com/project/alimon808/contoso-university)

[Contoso University demo using asp net core and related technologies](https://awesomeopensource.com/project/alimon808/contoso-university)

[Scenariotests ⭐ 26](https://awesomeopensource.com/project/koenbeuk/ScenarioTests)

[ScenarioTests are a different way of writing tests with XUnit. The goal is to be able to write tests like you would write notebooks. ScenarioTests are great for documentation and integration/e2e tests.](https://awesomeopensource.com/project/koenbeuk/ScenarioTests)

[Tic Tac Toe Csharp Playground ⭐ 25](https://awesomeopensource.com/project/willianantunes/tic-tac-toe-csharp-playground)

[Another fun project just to update what I know about C# 🎮](https://awesomeopensource.com/project/willianantunes/tic-tac-toe-csharp-playground)

[Tap4j ⭐ 24](https://awesomeopensource.com/project/tupilabs/tap4j)

[tap4j - A TAP implementation for Java](https://awesomeopensource.com/project/tupilabs/tap4j)

[Specflow.xunitadapter ⭐ 23](https://awesomeopensource.com/project/gasparnagy/SpecFlow.xUnitAdapter)

[xUnit adapter for SpecFlow that allows running scenarios without code generation](https://awesomeopensource.com/project/gasparnagy/SpecFlow.xUnitAdapter)

[Tpunitpp ⭐ 23](https://awesomeopensource.com/project/tpounds/tpunitpp)

[A simple, portable C++ xUnit library contained in a single header.](https://awesomeopensource.com/project/tpounds/tpunitpp)

[Xunit Extensions ⭐ 20](https://awesomeopensource.com/project/natemcmaster/xunit-extensions)

[Making XUnit.NET test projects even better](https://awesomeopensource.com/project/natemcmaster/xunit-extensions)

 

[Bitrix Module Bunit ⭐ 19](https://awesomeopensource.com/project/worksolutions/bitrix-module-bunit)

[BUnit - фреймворк модульного тестрования для CMS Bitrix](https://awesomeopensource.com/project/worksolutions/bitrix-module-bunit)

[Test Class ⭐ 19](https://awesomeopensource.com/project/szabgab/test-class)

[Test::Class - an xUnit testing framework for Perl 5.x](https://awesomeopensource.com/project/szabgab/test-class)

[Testcube ⭐ 19](https://awesomeopensource.com/project/tobyqin/testcube)

[Testcube is a platform to manage and monitor automation test results.](https://awesomeopensource.com/project/tobyqin/testcube)

[Kekiri ⭐ 18](https://awesomeopensource.com/project/chris-peterson/kekiri)

[A .NET framework that supports writing low-ceremony BDD tests using Gherkin language](https://awesomeopensource.com/project/chris-peterson/kekiri)

[Scaling Robot ⭐ 18](https://awesomeopensource.com/project/buraksenyurt/scaling-robot)

[Clean Architecture için .Net tarafından bir deneme çalışması. Her zaman ki gibi Amazon'dan getirttiğimi kitap önümde ben ekran başında kodlara bakıp kopylamadan yazıp ne anladığımı comment olarak bırakmaya çalıştım.](https://awesomeopensource.com/project/buraksenyurt/scaling-robot)

[Resharper Xunit Templates ⭐ 16](https://awesomeopensource.com/project/JetBrains/resharper-xunit-templates)

[ReSharper Live Templates for xUnit.net](https://awesomeopensource.com/project/JetBrains/resharper-xunit-templates)

[Testcontainers Dotnet ⭐ 16](https://awesomeopensource.com/project/isen-ng/testcontainers-dotnet)

[dotnet port of testcontainers-java](https://awesomeopensource.com/project/isen-ng/testcontainers-dotnet)

[Xunit To Junit ⭐ 15](https://awesomeopensource.com/project/gabrielweyer/xunit-to-junit)

[This Extensible Stylesheet Language Transformations can transform a xUnit.net v2 XML test results file into a JUnit test results file.](https://awesomeopensource.com/project/gabrielweyer/xunit-to-junit)

[Xretry ⭐ 15](https://awesomeopensource.com/project/JoshKeegan/xRetry)

[Retry running tests via Xunit and Specflow](https://awesomeopensource.com/project/JoshKeegan/xRetry)

[Xunit Orderer ⭐ 15](https://awesomeopensource.com/project/fulls1z3/xunit-orderer)

[Implementation of ITestCaseOrderer enforcing xUnit to run the facts in strict order](https://awesomeopensource.com/project/fulls1z3/xunit-orderer)

[Mpunit ⭐ 13](https://awesomeopensource.com/project/hgsgtk/mpunit)

[Mini PHP xUnit Testing Framework](https://awesomeopensource.com/project/hgsgtk/mpunit)

[Fakeiteasy.autofakeit ⭐ 13](https://awesomeopensource.com/project/akamud/FakeItEasy.AutoFakeIt)

[A very simple, yet flexible, "AutoFaker" for FakeItEasy to easily auto generate classes with faked dependencies.](https://awesomeopensource.com/project/akamud/FakeItEasy.AutoFakeIt)

[Iisexpress Testkit ⭐ 13](https://awesomeopensource.com/project/shibayan/iisexpress-testkit)

[IIS Express TestKit](https://awesomeopensource.com/project/shibayan/iisexpress-testkit)

[Signalr\_unittestingsupport ⭐ 13](https://awesomeopensource.com/project/NightAngell/SignalR_UnitTestingSupport)

[Easy to use, small, SignalR Core unit testing support with NUnit, xUnit, MSTest and Moq. It\`s also possibility to use it with custom testing engine. (Docs ready to use)](https://awesomeopensource.com/project/NightAngell/SignalR_UnitTestingSupport)

[Xunit Unity Runner ⭐ 12](https://awesomeopensource.com/project/planetarium/xunit-unity-runner)

[Run Xunit tests on Unity player](https://awesomeopensource.com/project/planetarium/xunit-unity-runner)

[Autofixture.xunit2.automock ⭐ 12](https://awesomeopensource.com/project/ObjectivityLtd/AutoFixture.XUnit2.AutoMock)

[Autofixture auto-mocking for XUnit2 using Moq.](https://awesomeopensource.com/project/ObjectivityLtd/AutoFixture.XUnit2.AutoMock)

[Hk Financial Functions ⭐ 11](https://awesomeopensource.com/project/Hesapkurdu/hk-financial-functions)

[](https://awesomeopensource.com/project/Hesapkurdu/hk-financial-functions)

[Csharp Design Patterns ⭐ 10](https://awesomeopensource.com/project/deanagan/csharp-design-patterns)

[A demo for design patterns written in C# with Moq, Xunit and FluentAssertions](https://awesomeopensource.com/project/deanagan/csharp-design-patterns)

[Andculturecode.csharp.testing ⭐ 10](https://awesomeopensource.com/project/AndcultureCode/AndcultureCode.CSharp.Testing)

[Commonly used CSharp Automated Testing patterns and utilities](https://awesomeopensource.com/project/AndcultureCode/AndcultureCode.CSharp.Testing)

[Dotnet Core Xunit Example ⭐ 10](https://awesomeopensource.com/project/barisates/dotnet-core-xunit-example)

[Unit Test in .NET Core Web Api with xUnit](https://awesomeopensource.com/project/barisates/dotnet-core-xunit-example)

[Aspnet Core Vue Fullstack Testing ⭐ 10](https://awesomeopensource.com/project/based-ghost/aspnet-core-vue-fullstack-testing)

[Prototype with Vue.js client (testing with Jest/Nightwatch) and ASP.NET Core 5.0 Web API (testing with xUnit.net)](https://awesomeopensource.com/project/based-ghost/aspnet-core-vue-fullstack-testing)

[Testng Parser ⭐ 10](https://awesomeopensource.com/project/tupilabs/testng-parser)

[TestNG Parser](https://awesomeopensource.com/project/tupilabs/testng-parser)

[Evlog ⭐ 10](https://awesomeopensource.com/project/gldraphael/evlog)

[⚡️A cross-platform self-hosted software to publish the events you host.](https://awesomeopensource.com/project/gldraphael/evlog)

[Xunit Slack Reporter ⭐ 10](https://awesomeopensource.com/project/ivanklee86/xunit-slack-reporter)

[Github Action to send XUnit results to Slack 🎙️🎙️🎙️](https://awesomeopensource.com/project/ivanklee86/xunit-slack-reporter)

[Vjunit ⭐ 10](https://awesomeopensource.com/project/ahsayde/vjunit)

[Python tool to convert junit / xunit xml reports to html file](https://awesomeopensource.com/project/ahsayde/vjunit)

[Corebdd ⭐ 9](https://awesomeopensource.com/project/stevenknox/CoreBDD)

[BDD framework for xUnit.net](https://awesomeopensource.com/project/stevenknox/CoreBDD)

[Xunit Cli ⭐ 9](https://awesomeopensource.com/project/natemcmaster/xunit-cli)

[A global .NET Core command line tool for running XUnit tests](https://awesomeopensource.com/project/natemcmaster/xunit-cli)

[Starter\_netcore ⭐ 8](https://awesomeopensource.com/project/damirkusar/starter_netCore)

[.net core starter with, opendIdDict, token authentication, asp.net identity, possible micro service architecture](https://awesomeopensource.com/project/damirkusar/starter_netCore)

[Xunit To Html ⭐ 8](https://awesomeopensource.com/project/Zir0-93/xunit-to-html)

[Beautify your xUnit test reports.](https://awesomeopensource.com/project/Zir0-93/xunit-to-html)

[Pyedaa.reports ⭐ 8](https://awesomeopensource.com/project/edaa-org/pyEDAA.Reports)

[Proposal to define an XML-based logging format for outputs from EDA tools and logging libraries.](https://awesomeopensource.com/project/edaa-org/pyEDAA.Reports)

[Csharp Basic Skeleton ⭐ 8](https://awesomeopensource.com/project/CodelyTV/csharp-basic-skeleton)

[🐘🚀 C# Basic Skeleton: Bootstrap your new projects.](https://awesomeopensource.com/project/CodelyTV/csharp-basic-skeleton)

[Net Core Xunit Example ⭐ 8](https://awesomeopensource.com/project/fravezzimattia/net-core-xunit-example)

[](https://awesomeopensource.com/project/fravezzimattia/net-core-xunit-example)

[Samples ⭐ 8](https://awesomeopensource.com/project/pvlakshm/Samples)

[Sample code for various features](https://awesomeopensource.com/project/pvlakshm/Samples)

[Dotnettests ⭐ 8](https://awesomeopensource.com/project/rafaelfgx/DotNetTests)

[Examples using MSTest and XUnit projects with test libraries (Moq, NSubstitute, FakeItEasy, NBuilder).](https://awesomeopensource.com/project/rafaelfgx/DotNetTests)

[Awesomebank ⭐ 8](https://awesomeopensource.com/project/marcinstelmach/AwesomeBank)

[Bank system in .NET 5.0 using DDD, CQRS, modular monolith architecture](https://awesomeopensource.com/project/marcinstelmach/AwesomeBank)

[Code Challenges ⭐ 8](https://awesomeopensource.com/project/hantsy/code-challenges)

[Code challenges in learning new languages, frameworks, engineering tools, architectures, software design patterns, etc.](https://awesomeopensource.com/project/hantsy/code-challenges)

[Moqassist ⭐ 7](https://awesomeopensource.com/project/omeerkorkmazz/MoqAssist)

[A Lightweight Mocking Assistant for Moq Library in .NET Platforms.](https://awesomeopensource.com/project/omeerkorkmazz/MoqAssist)

[Uwp ⭐ 7](https://awesomeopensource.com/project/RedGreenCode/UWP)

[Universal Windows Platform (UWP) code examples. See https://www.redgreencode.com/uwp-c-xaml-mvvm-ef-sqlite/.](https://awesomeopensource.com/project/RedGreenCode/UWP)

[Api Core ⭐ 7](https://awesomeopensource.com/project/arditmezini/api-core)

[A simple ASP.NET Core API](https://awesomeopensource.com/project/arditmezini/api-core)

[Orion ⭐ 7](https://awesomeopensource.com/project/j-didi/orion)

[A sandbox where I experiment with new techniques, concepts, and technologies. Here you will find some DDD, CQRS, Clean Architecture, Event-Driven Architecture, Serverless, Microservices, RabbitMQ, gRPC, SOLID, Design Patterns, and more.](https://awesomeopensource.com/project/j-didi/orion)

[Code Samples ⭐ 6](https://awesomeopensource.com/project/PracticalTestDrivenDevelopment/Code-Samples)

[Code samples for the book Practical Test-Driven Development with C# 7](https://awesomeopensource.com/project/PracticalTestDrivenDevelopment/Code-Samples)

[Wwwlicious.bamboo.xunit ⭐ 6](https://awesomeopensource.com/project/wwwlicious/wwwlicious.bamboo.xunit)

[A bamboo plugin to parse xunit results](https://awesomeopensource.com/project/wwwlicious/wwwlicious.bamboo.xunit)

[Jiphylib ⭐ 6](https://awesomeopensource.com/project/jezztify/JiphyLib)

[making it easier to publish robotframework results to JIRA](https://awesomeopensource.com/project/jezztify/JiphyLib)

[Msaas ⭐ 6](https://awesomeopensource.com/project/ZJU-SE-2021/MSaaS)

[Medical System as a Service - ZJU Software Engineering Course Project 2021](https://awesomeopensource.com/project/ZJU-SE-2021/MSaaS)

[Timetortoise ⭐ 6](https://awesomeopensource.com/project/RedGreenCode/TimeTortoise)

[Slow and steady time tracking](https://awesomeopensource.com/project/RedGreenCode/TimeTortoise)

[Zcommerce ⭐ 6](https://awesomeopensource.com/project/nixgram/ZCommerce)

[An Open-Source E2E-Ecommerce API Provider](https://awesomeopensource.com/project/nixgram/ZCommerce)

[Dot Net On Azure Function App ⭐ 6](https://awesomeopensource.com/project/mathieu-benoit/dot-net-on-azure-function-app)

[ALM and DevOps practices with a sample compiled .NET method hosted in Azure Function App](https://awesomeopensource.com/project/mathieu-benoit/dot-net-on-azure-function-app)

[Aspnetcore N Tier ⭐ 6](https://awesomeopensource.com/project/aghayeffemin/aspnetcore-n-tier)

[.NET Core N-Tier architecture Web Api sample project.](https://awesomeopensource.com/project/aghayeffemin/aspnetcore-n-tier)

[Backofficebase ⭐ 5](https://awesomeopensource.com/project/alirizaadiyahsi/BackOfficeBase)

[ASP.NET Core Web API Startup Template](https://awesomeopensource.com/project/alirizaadiyahsi/BackOfficeBase)

[Mxlogger ⭐ 5](https://awesomeopensource.com/project/dshe/MXLogger)

[A minimal Microsoft.Extensions.Logging provider for test frameworks such as MSTest, xUnit and NUnit.](https://awesomeopensource.com/project/dshe/MXLogger)

[Gherkinspec ⭐ 5](https://awesomeopensource.com/project/GivePenny/GherkinSpec)

[True .NET Standard Gherkin test adapter](https://awesomeopensource.com/project/GivePenny/GherkinSpec)

[F1wm ⭐ 5](https://awesomeopensource.com/project/pevel/f1wm)

[Extracting web API of f1wm.pl, piece by piece](https://awesomeopensource.com/project/pevel/f1wm)

[Test Driven Development ⭐ 5](https://awesomeopensource.com/project/meanin/test-driven-development)

[Introduction into TDD](https://awesomeopensource.com/project/meanin/test-driven-development)

[Fsharp Hedgehog Xunit ⭐ 5](https://awesomeopensource.com/project/dharmaturtle/fsharp-hedgehog-xunit)

[Hedgehog with convenience attributes for xUnit.net](https://awesomeopensource.com/project/dharmaturtle/fsharp-hedgehog-xunit)
 