Unit testing C# with NUnit and .NET Core
========================================

As far as NUnit vs. XUnit vs. MSTest is concerned, the biggest difference between xUnit and the other two test frameworks (NUnit and MSTest) is that xUnit is much more extensible when compared to NUnit and MSTest. The [Fact] attribute is used instead of the [Test] attribute. Non-parameterized tests are implemented under the [Fact] attribute, whereas the [Theory] attribute is used if you plan to use parameterized tests.

In NUnit and MSTest, the class that contains the tests is under the [TestClass] attribute. This was not a very robust approach hence [TestClass] attribute was also removed in xUnit. Instead, intelligence is built in the xUnit framework so that it can locate the test methods, irrespective of the location of the tests.

Shown below are the most popular attributes/annotations used in the xUnit framework:
 

### In this article

1.  [Prerequisites](#prerequisites)
2.  [Creating the source project](#creating-the-source-project)
3.  [Creating the test project](#creating-the-test-project)
4.  [Creating the first test](#creating-the-first-test)
5.  [Adding more features](#adding-more-features)

This tutorial takes you through an interactive experience building a sample solution step-by-step to learn unit testing concepts. If you prefer to follow the tutorial using a pre-built solution, [view or download the sample code](https://github.com/dotnet/samples/blob/main/core/getting-started/unit-testing-using-nunit/) before you begin. For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/#view-and-download-samples).

This article is about testing a .NET Core project. If you're testing an **ASP.NET Core** project, see [Integration tests in ASP.NET Core](/en-us/aspnet/core/test/integration-tests#test-app-prerequisites).

[](#prerequisites)Prerequisites
-------------------------------

*   [.NET Core 2.1 SDK](https://dotnet.microsoft.com/download) or later versions.
*   A text editor or code editor of your choice.

[](#creating-the-source-project)Creating the source project
-----------------------------------------------------------

Open a shell window. Create a directory called _unit-testing-using-nunit_ to hold the solution. Inside this new directory, run the following command to create a new solution file for the class library and the test project:

.NET CLI Copy

    dotnet new sln
    

Next, create a _PrimeService_ directory. The following outline shows the directory and file structure so far:

Console Copy

    /unit-testing-using-nunit
        unit-testing-using-nunit.sln
        /PrimeService
    

Make _PrimeService_ the current directory and run the following command to create the source project:

.NET CLI Copy

    dotnet new classlib
    

Rename _Class1.cs_ to _PrimeService.cs_. You create a failing implementation of the `PrimeService` class:

C# Copy

    using System;
    
    namespace Prime.Services
    {
        public class PrimeService
        {
            public bool IsPrime(int candidate)
            {
                throw new NotImplementedException("Please create a test first.");
            }
        }
    }
    

Change the directory back to the _unit-testing-using-nunit_ directory. Run the following command to add the class library project to the solution:

.NET CLI Copy

    dotnet sln add PrimeService/PrimeService.csproj
    

[](#creating-the-test-project)Creating the test project
-------------------------------------------------------

Next, create the _PrimeService.Tests_ directory. The following outline shows the directory structure:

Console Copy

    /unit-testing-using-nunit
        unit-testing-using-nunit.sln
        /PrimeService
            Source Files
            PrimeService.csproj
        /PrimeService.Tests
    

Make the _PrimeService.Tests_ directory the current directory and create a new project using the following command:

.NET CLI Copy

    dotnet new nunit
    

The [dotnet new](../tools/dotnet-new) command creates a test project that uses NUnit as the test library. The generated template configures the test runner in the _PrimeService.Tests.csproj_ file:

XML Copy

    <ItemGroup>
      <PackageReference Include="nunit" Version="3.13.2" />
      <PackageReference Include="NUnit3TestAdapter" Version="4.2.0" />
      <PackageReference Include="Microsoft.NET.Test.Sdk" Version="17.0.0" />
    </ItemGroup>
    

The test project requires other packages to create and run unit tests. `dotnet new` in the previous step added the Microsoft test SDK, the NUnit test framework, and the NUnit test adapter. Now, add the `PrimeService` class library as another dependency to the project. Use the [`dotnet add reference`](../tools/dotnet-add-reference) command:

.NET CLI Copy

    dotnet add reference ../PrimeService/PrimeService.csproj
    

You can see the entire file in the [samples repository](https://github.com/dotnet/samples/blob/main/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService.Tests.csproj) on GitHub.

The following outline shows the final solution layout:

Console Copy

    /unit-testing-using-nunit
        unit-testing-using-nunit.sln
        /PrimeService
            Source Files
            PrimeService.csproj
        /PrimeService.Tests
            Test Source Files
            PrimeService.Tests.csproj
    

Execute the following command in the _unit-testing-using-nunit_ directory:

.NET CLI Copy

    dotnet sln add ./PrimeService.Tests/PrimeService.Tests.csproj
    

[](#creating-the-first-test)Creating the first test
---------------------------------------------------

You write one failing test, make it pass, then repeat the process. In the _PrimeService.Tests_ directory, rename the _UnitTest1.cs_ file to _PrimeService\_IsPrimeShould.cs_ and replace its entire contents with the following code:

C# Copy

    using NUnit.Framework;
    using Prime.Services;
    
    namespace Prime.UnitTests.Services
    {
        [TestFixture]
        public class PrimeService_IsPrimeShould
        {
            private PrimeService _primeService;
    
            [SetUp]
            public void SetUp()
            {
                _primeService = new PrimeService();
            }
    
            [Test]
            public void IsPrime_InputIs1_ReturnFalse()
            {
                var result = _primeService.IsPrime(1);
    
                Assert.IsFalse(result, "1 should not be prime");
            }
        }
    }
    

The `[TestFixture]` attribute denotes a class that contains unit tests. The `[Test]` attribute indicates a method is a test method.

Save this file and execute [`dotnet test`](../tools/dotnet-test) to build the tests and the class library and then run the tests. The NUnit test runner contains the program entry point to run your tests. `dotnet test` starts the test runner using the unit test project you've created.

Your test fails. You haven't created the implementation yet. Make this test pass by writing the simplest code in the `PrimeService` class that works:

C# Copy

    public bool IsPrime(int candidate)
    {
        if (candidate == 1)
        {
            return false;
        }
        throw new NotImplementedException("Please create a test first.");
    }
    

In the _unit-testing-using-nunit_ directory, run `dotnet test` again. The `dotnet test` command runs a build for the `PrimeService` project and then for the `PrimeService.Tests` project. After building both projects, it runs this single test. It passes.

[](#adding-more-features)Adding more features
---------------------------------------------

Now that you've made one test pass, it's time to write more. There are a few other simple cases for prime numbers: 0, -1. You could add new tests with the `[Test]` attribute, but that quickly becomes tedious. There are other NUnit attributes that enable you to write a suite of similar tests. A `[TestCase]` attribute is used to create a suite of tests that execute the same code but have different input arguments. You can use the `[TestCase]` attribute to specify values for those inputs.

Instead of creating new tests, apply this attribute to create a single data driven test. The data driven test is a method that tests several values less than two, which is the lowest prime number:

C# Copy

    [TestCase(-1)]
    [TestCase(0)]
    [TestCase(1)]
    public void IsPrime_ValuesLessThan2_ReturnFalse(int value)
    {
        var result = _primeService.IsPrime(value);
    
        Assert.IsFalse(result, $"{value} should not be prime");
    }
    

Run `dotnet test`, and two of these tests fail. To make all of the tests pass, change the `if` clause at the beginning of the `Main` method in the _PrimeService.cs_ file:

C# Copy

    if (candidate < 2)
    

Continue to iterate by adding more tests, more theories, and more code in the main library. You have the [finished version of the tests](https://github.com/dotnet/samples/blob/main/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.cs) and the [complete implementation of the library](https://github.com/dotnet/samples/blob/main/core/getting-started/unit-testing-using-nunit/PrimeService/PrimeService.cs).

You've built a small library and a set of unit tests for that library. You've structured the solution so that adding new packages and tests is part of the normal workflow. You've concentrated most of your time and effort on solving the goals of the application.



 
 
 

[Nunit ⭐ 2,126](https://awesomeopensource.com/project/nunit/nunit)

[NUnit 3 Framework](https://awesomeopensource.com/project/nunit/nunit)

[Specflow ⭐ 1,836](https://awesomeopensource.com/project/SpecFlowOSS/SpecFlow)

[#1 .NET BDD Framework. SpecFlow automates your testing & works with your existing code. Find Bugs before they happen. Behavior Driven Development helps developers, testers, and business representatives to get a better understanding of their collaboration](https://awesomeopensource.com/project/SpecFlowOSS/SpecFlow)

[Tdd Katas ⭐ 654](https://awesomeopensource.com/project/garora/TDD-Katas)

[This repository contains Hands on Test Driven Development Katas (C#)](https://awesomeopensource.com/project/garora/TDD-Katas)

[Bunit ⭐ 626](https://awesomeopensource.com/project/bUnit-dev/bUnit)

[bUnit is a testing library for Blazor components that make tests look, feel, and runs like regular unit tests. bUnit makes it easy to render and control a component under test’s life-cycle, pass parameter and inject services into it, trigger event handlers, and verify the rendered markup from the component using a built-in semantic HTML comparer.](https://awesomeopensource.com/project/bUnit-dev/bUnit)

[Docs ⭐ 603](https://awesomeopensource.com/project/nunit/docs)

[Documentation for all active NUnit projects](https://awesomeopensource.com/project/nunit/docs)
 

[Mockqueryable ⭐ 344](https://awesomeopensource.com/project/romantitov/MockQueryable)

[Moking Entity Framework Core operations such ToListAsync, FirstOrDefaultAsync etc](https://awesomeopensource.com/project/romantitov/MockQueryable)

[Fsunit ⭐ 322](https://awesomeopensource.com/project/fsprojects/FsUnit)

[FsUnit makes unit-testing with F# more enjoyable. It adds a special syntax to your favorite .NET testing framework.](https://awesomeopensource.com/project/fsprojects/FsUnit)

[Ocaramba ⭐ 247](https://awesomeopensource.com/project/ObjectivityLtd/Ocaramba)

[C# Framework to automate tests using Selenium WebDriver](https://awesomeopensource.com/project/ObjectivityLtd/Ocaramba)

[Lightbdd ⭐ 238](https://awesomeopensource.com/project/LightBDD/LightBDD)

[BDD framework allowing to create easy to read and maintain tests.](https://awesomeopensource.com/project/LightBDD/LightBDD)

[Nunit Console ⭐ 184](https://awesomeopensource.com/project/nunit/nunit-console)

[NUnit Console runner and test engine](https://awesomeopensource.com/project/nunit/nunit-console)

[Csharp.webdriver ⭐ 105](https://awesomeopensource.com/project/sayems/csharp.webdriver)

[Browser test automation using Selenium WebDriver in C#](https://awesomeopensource.com/project/sayems/csharp.webdriver)

[Nbi ⭐ 95](https://awesomeopensource.com/project/Seddryck/NBi)

[NBi is a testing framework (add-on to NUnit) for Business Intelligence and Data Access. The main goal of this framework is to let users create tests with a declarative approach based on an Xml syntax. By the means of NBi, you don't need to develop C# or Java code to specify your tests! Either, you don't need Visual Studio or Eclipse to compile your test suite. Just create an Xml file and let the framework interpret it and play your tests. The framework is designed as an add-on of NUnit but with the possibility to port it easily to other testing frameworks.](https://awesomeopensource.com/project/Seddryck/NBi)

[Beef ⭐ 86](https://awesomeopensource.com/project/Avanade/Beef)

[Business Entity Execution Framework](https://awesomeopensource.com/project/Avanade/Beef)

[Format Pester ⭐ 75](https://awesomeopensource.com/project/equelin/Format-Pester)

[Powershell module for documenting Pester's results](https://awesomeopensource.com/project/equelin/Format-Pester)

[Meissa ⭐ 68](https://awesomeopensource.com/project/AutomateThePlanet/Meissa)

[Cross-platform Distributed Test Runner. Executes tests in parallel, time balanced on multiple machines.](https://awesomeopensource.com/project/AutomateThePlanet/Meissa)

[N Tier Architecture ⭐ 68](https://awesomeopensource.com/project/nuyonu/N-Tier-Architecture)

[This is a n-layer architecture based on Common web application architectures.](https://awesomeopensource.com/project/nuyonu/N-Tier-Architecture)

[Nunit.analyzers ⭐ 53](https://awesomeopensource.com/project/nunit/nunit.analyzers)

[Roslyn analyzers for writing unit tests with NUnit](https://awesomeopensource.com/project/nunit/nunit.analyzers)

[Chainingassertion ⭐ 49](https://awesomeopensource.com/project/neuecc/ChainingAssertion)

[Method Chaining base UnitTesting Extension Methods and Dynamic Private Accessor for MSTest, NUnit, xUnit.net.](https://awesomeopensource.com/project/neuecc/ChainingAssertion)

[Nunit.testlogger ⭐ 48](https://awesomeopensource.com/project/spekt/nunit.testlogger)

[NUnit logger for vstest platform](https://awesomeopensource.com/project/spekt/nunit.testlogger)

[Ghpr.core ⭐ 46](https://awesomeopensource.com/project/GHPReporter/Ghpr.Core)

[Easy-to-use .NET Html QA Reporting framework (Core repository)](https://awesomeopensource.com/project/GHPReporter/Ghpr.Core)

[Seleniumwithspecflow ⭐ 45](https://awesomeopensource.com/project/executeautomation/SeleniumWithSpecflow)

[In this sample project we will demonstrate how to execute Specflow test in parallel using Selenium and NUnit 3](https://awesomeopensource.com/project/executeautomation/SeleniumWithSpecflow)

[

Sponsored by Microsoft Azure

Essayer Azure (gratuit)

Migrez vers le nuage de manière sécurisée et efficace, à votre façon.

![](https://cdn4.buysellads.net/uu/1/106122/1640617847-Microsoft-logo_rgb_c-wht-250x100.png)





](//srv.buysellads.com/ads/click/x/GTND42JWCV7I45QNCYS4YKQNCE7DV2QIFTYDLZ3JCYBD6K7ICW7I6KJKCASIKK7NCA7I5KQWCVYIEK3WCTBICK7KC6SDVKJLF6ADVK3EHJNCLSIZ?segment=placement:awesomeopensourcecom; "Essayer Azure (gratuit)")![](https://ad.doubleclick.net/ddm/trackimp/N572608.452584BUYSELLADS.COM/B26936539.323082640;dc_trk_aid=515333555;dc_trk_cid=157783975;ord=1642299637;dc_lat=;dc_rdid=;tag_for_child_directed_treatment=;tfua=;gdpr=$;gdpr_consent=$;ltd=?)![](https://pixel.adsafeprotected.com/rfw/st/901515/59187633/skeleton.gif?gdpr=$&gdpr_consent=$&gdpr_pd=$&ias_dspID=64&network=BUYSELLADS)

[Rest.api.test ⭐ 43](https://awesomeopensource.com/project/sayems/rest.api.test)

[Simple REST API Test Framework](https://awesomeopensource.com/project/sayems/rest.api.test)

[Allure Nunit ⭐ 38](https://awesomeopensource.com/project/unickq/allure-nunit)

[Allure adapter for NUnit framework.](https://awesomeopensource.com/project/unickq/allure-nunit)

[Difido Reports ⭐ 38](https://awesomeopensource.com/project/Top-Q/difido-reports)

[This project aims to provide a generic implementation for HTML test reports.](https://awesomeopensource.com/project/Top-Q/difido-reports)

[Aspnetcore Tests Sample ⭐ 37](https://awesomeopensource.com/project/giggio-samples/aspnetcore-tests-sample)

[A project to help demonstrate how to do unit, integration and acceptance tests with an web api project using ASP.NET Core and Angular 7 front end.](https://awesomeopensource.com/project/giggio-samples/aspnetcore-tests-sample)

[Ghpr.nunit ⭐ 32](https://awesomeopensource.com/project/GHPReporter/Ghpr.NUnit)

[Adapter for NUnit 3 (generate HTML report for NUnit 3)](https://awesomeopensource.com/project/GHPReporter/Ghpr.NUnit)

[Guitestsharp ⭐ 32](https://awesomeopensource.com/project/PlasticSCM/GuiTestSharp)

[An extensible multiplatform framework to test GUIs in WinForms, WPF, GtkSharp and Xamarin.Mac.](https://awesomeopensource.com/project/PlasticSCM/GuiTestSharp)

[Nspectator ⭐ 24](https://awesomeopensource.com/project/novikov-school/NSpectator)

[Agile development with .NET code specifications](https://awesomeopensource.com/project/novikov-school/NSpectator)

[Kekiri ⭐ 18](https://awesomeopensource.com/project/chris-peterson/kekiri)

[A .NET framework that supports writing low-ceremony BDD tests using Gherkin language](https://awesomeopensource.com/project/chris-peterson/kekiri)

[Allure.nunit ⭐ 17](https://awesomeopensource.com/project/Noksa/Allure.NUnit)

[C# NUnit Allure with improvements and SpecFlow3 adapter](https://awesomeopensource.com/project/Noksa/Allure.NUnit)

[Gradle Nunit Plugin ⭐ 16](https://awesomeopensource.com/project/Itiviti/gradle-nunit-plugin)

[A gradle plugin for launching NUnit tests](https://awesomeopensource.com/project/Itiviti/gradle-nunit-plugin)

[Testcontainers Dotnet ⭐ 16](https://awesomeopensource.com/project/isen-ng/testcontainers-dotnet)

[dotnet port of testcontainers-java](https://awesomeopensource.com/project/isen-ng/testcontainers-dotnet)

[Nunit\_cshaprp\_cheatsheet ⭐ 14](https://awesomeopensource.com/project/sanneabhilash/Nunit_CShaprp_CheatSheet)

[Example implementations of each attribute available in Nunit2 unit Testing Framework using C# .NET.](https://awesomeopensource.com/project/sanneabhilash/Nunit_CShaprp_CheatSheet)

[Sampleseleniumpomframework ⭐ 14](https://awesomeopensource.com/project/AmolLearning/SampleSeleniumPOMFramework)

[Sample Selenium Webdriver framework with C# build using Page Object Model approach, C# and NUnit.](https://awesomeopensource.com/project/AmolLearning/SampleSeleniumPOMFramework)

[Waveshare.epaperdisplay ⭐ 14](https://awesomeopensource.com/project/eXoCooLd/Waveshare.EPaperDisplay)

[.Net Core Library to show images on Waveshare E-Paper Displays](https://awesomeopensource.com/project/eXoCooLd/Waveshare.EPaperDisplay)

[Parameterizednunit ⭐ 14](https://awesomeopensource.com/project/avraampiperidis/parameterizednunit)

[Parameterized test example in .NET core using NUnit](https://awesomeopensource.com/project/avraampiperidis/parameterizednunit)

[Paralleltestingsample Dotnet Core ⭐ 13](https://awesomeopensource.com/project/idubnori/ParallelTestingSample-dotnet-core)

[Sample for running dotnet core tests in parallel across multiple agents in Azure DevOps](https://awesomeopensource.com/project/idubnori/ParallelTestingSample-dotnet-core)

[Signalr\_unittestingsupport ⭐ 13](https://awesomeopensource.com/project/NightAngell/SignalR_UnitTestingSupport)

[Easy to use, small, SignalR Core unit testing support with NUnit, xUnit, MSTest and Moq. It\`s also possibility to use it with custom testing engine. (Docs ready to use)](https://awesomeopensource.com/project/NightAngell/SignalR_UnitTestingSupport)

[Fakeiteasy.autofakeit ⭐ 13](https://awesomeopensource.com/project/akamud/FakeItEasy.AutoFakeIt)

[A very simple, yet flexible, "AutoFaker" for FakeItEasy to easily auto generate classes with faked dependencies.](https://awesomeopensource.com/project/akamud/FakeItEasy.AutoFakeIt)

[Smarttests ⭐ 11](https://awesomeopensource.com/project/LudovicDubois/SmartTests)

[Smart Tests is a library and a Visual Studio Analyzer to simplify Unit Testing](https://awesomeopensource.com/project/LudovicDubois/SmartTests)

[Cloudbackupactors ⭐ 10](https://awesomeopensource.com/project/kevinmcfarlane/CloudBackupActors)

[An Application That Backs Up Files To Cloud Storage Using Akka.NET](https://awesomeopensource.com/project/kevinmcfarlane/CloudBackupActors)

[Specflow.selenium.plugin ⭐ 10](https://awesomeopensource.com/project/unickq/SpecFlow.Selenium.Plugin)

[SpecFlow WebDriver instances generator plugin. Annotate scenario with @Browser:Chrome and run you tests!](https://awesomeopensource.com/project/unickq/SpecFlow.Selenium.Plugin)

[Sampleprogram ⭐ 10](https://awesomeopensource.com/project/OpenTouryoProject/SampleProgram)

[いろいろなサンプルプログラムが格納されています。(A variety of sample programs are stored.)](https://awesomeopensource.com/project/OpenTouryoProject/SampleProgram)

[Gradle Dotnet Plugin ⭐ 9](https://awesomeopensource.com/project/Itiviti/gradle-dotnet-plugin)

[Gradle plugin for interacting with dotnet cli](https://awesomeopensource.com/project/Itiviti/gradle-dotnet-plugin)

[Mvvmcrossstarterkit ⭐ 9](https://awesomeopensource.com/project/wcoder/MvvmCrossStarterKit)

[The starter project to develop apps with Xamarin + MvvmCross](https://awesomeopensource.com/project/wcoder/MvvmCrossStarterKit)

[

Sponsored by Microsoft Azure

Essayer Azure (gratuit)

Créez des expériences client personnalisées avec Azure AI.

![](https://cdn4.buysellads.net/uu/1/106122/1640617847-Microsoft-logo_rgb_c-wht-250x100.png)





](//srv.buysellads.com/ads/click/x/GTND42JWCV7I45QNCYS4YKQNCE7DV2QIFTYDLZ3JCYBD6K7ICW7ILK7KCASIKK7NCA7I5KQWCVYIEK3WCTBICK7KC6SDVKJLF6ADVK3EHJNCLSIZ?segment=placement:awesomeopensourcecom; "Essayer Azure (gratuit)")![](https://ad.doubleclick.net/ddm/trackimp/N572608.452584BUYSELLADS.COM/B26936539.323082640;dc_trk_aid=515505990;dc_trk_cid=157782568;ord=1642299637;dc_lat=;dc_rdid=;tag_for_child_directed_treatment=;tfua=;gdpr=$;gdpr_consent=$;ltd=?)![](https://pixel.adsafeprotected.com/rfw/st/901515/59187639/skeleton.gif?gdpr=$&gdpr_consent=$&gdpr_pd=$&ias_dspID=64&network=BUYSELLADS)

[Kata Quickstarter ⭐ 8](https://awesomeopensource.com/project/teamneusta/kata-quickstarter)

[In this repo, you find several projects, to kickstart a code kata - in a programming language you like - quick and easy.](https://awesomeopensource.com/project/teamneusta/kata-quickstarter)

[Samples ⭐ 8](https://awesomeopensource.com/project/pvlakshm/Samples)

[Sample code for various features](https://awesomeopensource.com/project/pvlakshm/Samples)

[Dotnet Core Postgresql Boilerplate ⭐ 8](https://awesomeopensource.com/project/mzrimsek/dotnet-core-postgresql-boilerplate)

[A .NET Core MVC boilerplate project with Entity Framework Core, PostgreSQL, and NUnit.](https://awesomeopensource.com/project/mzrimsek/dotnet-core-postgresql-boilerplate)

[Dynamicspecs ⭐ 8](https://awesomeopensource.com/project/HerrLoesch/DynamicSpecs)

[An easy to use specfication framework as extension for NUnit and MSTest.](https://awesomeopensource.com/project/HerrLoesch/DynamicSpecs)

[Oktatas Hft ⭐ 7](https://awesomeopensource.com/project/siposm/oktatas-hft)

[💻 A Haladó Fejlesztési Technikák tárgyhoz tartozó laboranyagok, házi és gyakorló feladatok kódjai.](https://awesomeopensource.com/project/siposm/oktatas-hft)

[Tddbook Code ⭐ 7](https://awesomeopensource.com/project/dariusz-wozniak/TddBook-Code)

[📘 Repozytorium dla książki "TDD. Techniki programowania sterowanego testami".](https://awesomeopensource.com/project/dariusz-wozniak/TddBook-Code)

[Spiralmatrixsharp ⭐ 7](https://awesomeopensource.com/project/bangjunyoung/SpiralMatrixSharp)

[Arguably the world's most advanced spiral matrix generator written in F#.](https://awesomeopensource.com/project/bangjunyoung/SpiralMatrixSharp)

[Moqassist ⭐ 7](https://awesomeopensource.com/project/omeerkorkmazz/MoqAssist)

[A Lightweight Mocking Assistant for Moq Library in .NET Platforms.](https://awesomeopensource.com/project/omeerkorkmazz/MoqAssist)

[Nunit Test Video Recorder ⭐ 6](https://awesomeopensource.com/project/endless-qa/nunit-test-video-recorder)

[](https://awesomeopensource.com/project/endless-qa/nunit-test-video-recorder)

[Gherkinspec ⭐ 5](https://awesomeopensource.com/project/GivePenny/GherkinSpec)

[True .NET Standard Gherkin test adapter](https://awesomeopensource.com/project/GivePenny/GherkinSpec)

[Test Driven Development ⭐ 5](https://awesomeopensource.com/project/meanin/test-driven-development)

[Introduction into TDD](https://awesomeopensource.com/project/meanin/test-driven-development)

[Testrail.nunit.integration ⭐ 5](https://awesomeopensource.com/project/AshleyDhevalall/TestRail.NUnit.Integration)

[This project enables you to add the results of tests executed in NUnit to TestRail.](https://awesomeopensource.com/project/AshleyDhevalall/TestRail.NUnit.Integration)

[Mxlogger ⭐ 5](https://awesomeopensource.com/project/dshe/MXLogger)

[A minimal Microsoft.Extensions.Logging provider for test frameworks such as MSTest, xUnit and NUnit.](https://awesomeopensource.com/project/dshe/MXLogger)

[Ftss ⭐ 4](https://awesomeopensource.com/project/heidarbozorg/FTSS)

[Fast, Testable, Secure, and Scalable restful APIs by C# .Net Core](https://awesomeopensource.com/project/heidarbozorg/FTSS)

[Let.cs ⭐ 4](https://awesomeopensource.com/project/BaylorRae/Let.cs)

[Add convention to your unit tests.](https://awesomeopensource.com/project/BaylorRae/Let.cs)

[Ghpr.console ⭐ 4](https://awesomeopensource.com/project/GHPReporter/Ghpr.Console)

[Console application to convert NUnit and MSTest test result files into Ghpr HTML Report](https://awesomeopensource.com/project/GHPReporter/Ghpr.Console)

[Giveth ⭐ 4](https://awesomeopensource.com/project/mcintyre321/Giveth)

[The less annoying BDD / Gherkin library for .NET](https://awesomeopensource.com/project/mcintyre321/Giveth)

[Nunittestordering ⭐ 3](https://awesomeopensource.com/project/Sebazzz/NUnitTestOrdering)

[Allows to use hierarchical (integration) test ordering in NUnit and supports workflow based testing](https://awesomeopensource.com/project/Sebazzz/NUnitTestOrdering)

[Ts Unit ⭐ 3](https://awesomeopensource.com/project/alveflo/ts-unit)

[typescript testing framework for the c# dudes](https://awesomeopensource.com/project/alveflo/ts-unit)

[Aspnetcoredevops ⭐ 3](https://awesomeopensource.com/project/iAmBipinPaul/AspNetCoreDevOps)

[Building, Testing , Containerizing and pushing to Docker Registry Nuke Build and Cake Build Updated to .NET 5 🛠⚒🔨](https://awesomeopensource.com/project/iAmBipinPaul/AspNetCoreDevOps)

[Channeladam.testframeworks ⭐ 3](https://awesomeopensource.com/project/channeladam/ChannelAdam.TestFrameworks)

[DEPRECATED - .NET libraries that provide handy functionality for writing automated tests and reading their output, using Moq and MSTest.](https://awesomeopensource.com/project/channeladam/ChannelAdam.TestFrameworks)

[Nvalidate ⭐ 3](https://awesomeopensource.com/project/horia141/nvalidate)

[Business logic validation library](https://awesomeopensource.com/project/horia141/nvalidate)

[Chainingassertion.core ⭐ 3](https://awesomeopensource.com/project/acple/ChainingAssertion.Core)

[Method Chaining base UnitTesting Extensions](https://awesomeopensource.com/project/acple/ChainingAssertion.Core)

[Saucery ⭐ 3](https://awesomeopensource.com/project/Sauceforge/Saucery)

[The SauceLabs DesiredOption factory](https://awesomeopensource.com/project/Sauceforge/Saucery)

[Unittestgenerator ⭐ 3](https://awesomeopensource.com/project/dlmcdonald/UnitTestGenerator)

[Visual studio for Mac extension to generate unit tests from a method](https://awesomeopensource.com/project/dlmcdonald/UnitTestGenerator)

[Template Netcore Domain ⭐ 3](https://awesomeopensource.com/project/DustinChristians/template-netcore-domain)

[A .NET Core 3.1 CRUD template for new projects. (C#, .NET Core 3.1, .NET Standard 2.1, Entity Framework Core, AutoMapper, Hangfire, NUnit, Serilog)](https://awesomeopensource.com/project/DustinChristians/template-netcore-domain)

[Blazereport ⭐ 3](https://awesomeopensource.com/project/LeoVen/BlazeReport)

[A minimal example of a Blazor App with NUnit, Selenium, SpecFlow and ExtentReports (.NET Core 3)](https://awesomeopensource.com/project/LeoVen/BlazeReport)

[Automockhelper ⭐ 3](https://awesomeopensource.com/project/markjsc/AutoMockHelper)

[Speed up your unit test writing by using this helper that leverages AutoMocker to automatically mock dependencies.](https://awesomeopensource.com/project/markjsc/AutoMockHelper)

[Willyos C ⭐ 3](https://awesomeopensource.com/project/thewillyhuman/willyOS-c)

[TPP Course from Prof. Jose Manuel Redondo at University of Oviedo](https://awesomeopensource.com/project/thewillyhuman/willyOS-c)

[Testing ⭐ 3](https://awesomeopensource.com/project/LeapingGorillaLTD/Testing)

[Leaping Gorilla's testing framework for BDD style Given/When/Then without the ceremony](https://awesomeopensource.com/project/LeapingGorillaLTD/Testing)

[Akka.testkit.nunit ⭐ 3](https://awesomeopensource.com/project/akkadotnet/Akka.TestKit.NUnit)

[Akka.NET TestKit integration plugin for NUnit](https://awesomeopensource.com/project/akkadotnet/Akka.TestKit.NUnit)

[Dotnet Core Postgresql React Redux Boilerplate ⭐ 2](https://awesomeopensource.com/project/mzrimsek/dotnet-core-postgresql-react-redux-boilerplate)

[A .NET Core MVC boilerplate project with Entity Framework Core, PostgreSQL, and NUnit using React as the view layer.](https://awesomeopensource.com/project/mzrimsek/dotnet-core-postgresql-react-redux-boilerplate)

[Specflow.contrib.variants ⭐ 2](https://awesomeopensource.com/project/TotalTest/SpecFlow.Contrib.Variants)

[SpecFlow plugin to allow variants of a test to be run using tags e.g. against different browsers](https://awesomeopensource.com/project/TotalTest/SpecFlow.Contrib.Variants)

[Commonfixtures ⭐ 2](https://awesomeopensource.com/project/CanerPatir/CommonFixtures)

[A toolkit contains essential test fixtures for .net core and asp.net core projects.](https://awesomeopensource.com/project/CanerPatir/CommonFixtures)

[Nunit.applicationdomain ⭐ 2](https://awesomeopensource.com/project/zastrowm/NUnit.ApplicationDomain)

[Run NUnit tests in separate application domains for better isolation.](https://awesomeopensource.com/project/zastrowm/NUnit.ApplicationDomain)

[Http Mock Player ⭐ 2](https://awesomeopensource.com/project/igudkova/http-mock-player)

[.NET library for recording and playing HTTP mock requests](https://awesomeopensource.com/project/igudkova/http-mock-player)

[Dotnet Test Split ⭐ 2](https://awesomeopensource.com/project/javiertuya/dotnet-test-split)

[Splits dotnet test trx files into a separate junit xml files like those generated by maven surefire report plugin. The trx files can be generated from MSTest, NUnit or Xunit.](https://awesomeopensource.com/project/javiertuya/dotnet-test-split)

[Nunitextras Hierarchicalcategories ⭐ 2](https://awesomeopensource.com/project/YevgeniyShunevych/nunitextras-hierarchicalcategories)

[Hierarchical categories for NUnit](https://awesomeopensource.com/project/YevgeniyShunevych/nunitextras-hierarchicalcategories)

[Bdd\_specflow\_nunit ⭐ 2](https://awesomeopensource.com/project/gauravkarvir/bdd_specflow_nunit)

[\# BDD SpecFlow Webdriver Nunit Framework ### Uses: + SpecFlow 2 (Cucumber BDD) + Selenium (WebDriver) + NUnit + specflow-report-templates + pickles (documentation generator for features and scenarios) + utilises Page Object Model pattern + can be run using Jenkins + runs tests locally or in saucelabs (account required) and reports results back to the Jenkins job + takes screenshots on failure of web tests](https://awesomeopensource.com/project/gauravkarvir/bdd_specflow_nunit)

[Xam Gradle Plugins ⭐ 2](https://awesomeopensource.com/project/oliviergauthier/xam-gradle-plugins)

[Set of Gradle plugins to build Xamarin mobile application (iOS/Android) and Nuget librairies](https://awesomeopensource.com/project/oliviergauthier/xam-gradle-plugins)

[Testingwithneo4j ⭐ 2](https://awesomeopensource.com/project/DotNet4Neo4j/TestingWithNeo4j)

[Examples of testing against a Neo4j instance that is started on the fly, using NUnit, XUnit and MSTest](https://awesomeopensource.com/project/DotNet4Neo4j/TestingWithNeo4j)

[Testy ⭐ 2](https://awesomeopensource.com/project/rebus-org/Testy)

[🔬 Nifty opinionated test helpers for NUnit](https://awesomeopensource.com/project/rebus-org/Testy)

[Nunit.dependencyinjection ⭐ 2](https://awesomeopensource.com/project/kalebpederson/nunit.dependencyinjection)

[Add support to NUnit for constructor injection using an inversion control container, such as Unity or Autofac.](https://awesomeopensource.com/project/kalebpederson/nunit.dependencyinjection)

[Specter Code ⭐ 2](https://awesomeopensource.com/project/darkmusic/specter-code)

[A behaviour-driven development framework for .NET and Mono](https://awesomeopensource.com/project/darkmusic/specter-code)

[Logofx Client Testing Integration Nunit ⭐ 2](https://awesomeopensource.com/project/LogoFX/logofx-client-testing-integration-nunit)

[Base integration tests and builder registration service implementation for NUnit](https://awesomeopensource.com/project/LogoFX/logofx-client-testing-integration-nunit)

[Cleanarchitecture.us ⭐ 2](https://awesomeopensource.com/project/musmanbit/CleanArchitecture.US)

[Clean Architecture](https://awesomeopensource.com/project/musmanbit/CleanArchitecture.US)

[Nconstraints ⭐ 2](https://awesomeopensource.com/project/saturdaymp/NConstraints)

[Additional constraints for NUnit.](https://awesomeopensource.com/project/saturdaymp/NConstraints)

[Questioner ⭐ 1](https://awesomeopensource.com/project/henriq-toledo/questioner)

[Questioner is a web application that test using questions and answers about a theme to help studying. Developed to be responsive to run in the PC web browser or mobile web browser.](https://awesomeopensource.com/project/henriq-toledo/questioner)

[Uml Drawer ⭐ 1](https://awesomeopensource.com/project/Vukan-Markovic/UML-drawer)

[Windows form application for drawing UML diagrams](https://awesomeopensource.com/project/Vukan-Markovic/UML-drawer)

[Microservices Passenger Management Csharp 2 2020 ⭐ 1](https://awesomeopensource.com/project/panaitescu-paul/Microservices-Passenger-Management-CSharp-2-2020)

[Microservice Architecture - Passenger Management Service](https://awesomeopensource.com/project/panaitescu-paul/Microservices-Passenger-Management-CSharp-2-2020)

[Awesome Automated Testing ⭐ 1](https://awesomeopensource.com/project/berkayalcin/awesome-automated-testing)

[Automated-Testing Exampled With NUnit Test Runner](https://awesomeopensource.com/project/berkayalcin/awesome-automated-testing)

[Selenium Page Object Model Csharp ⭐ 1](https://awesomeopensource.com/project/osandadeshan/selenium-page-object-model-csharp)

[This is the demo project on Selenium + Page Object Model Design Pattern + NUnit + C#.](https://awesomeopensource.com/project/osandadeshan/selenium-page-object-model-csharp)

[Unittesting ⭐ 1](https://awesomeopensource.com/project/MatthiWare/UnitTesting)

[Unit Testing Basics with xUnit and NUnit](https://awesomeopensource.com/project/MatthiWare/UnitTesting)

[Protractor Page Object Model Csharp ⭐ 1](https://awesomeopensource.com/project/osandadeshan/protractor-page-object-model-csharp)

[This is the demo project on Protractor + Selenium + Page Object Model Design Pattern + NUnit + C#.](https://awesomeopensource.com/project/osandadeshan/protractor-page-object-model-csharp)
 