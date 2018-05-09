---
title: "Bæta greiningu við vinnusvæði með Power BI Embedded"
description: "Þetta efnisatriði sýnir hvernig á að fella inn Power BI-skýrslu á flipann Greiningar á vinnusvæði."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1d4243d56828430bc04dfb24a287e6acdd572b5f
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="264ac-103">Bæta greiningu við vinnusvæði með Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="264ac-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="264ac-104">Þessi eiginleiki er studdur í Dynamics 365 tfor Finance and Operations (útgáfu 7.2 og seinni).</span><span class="sxs-lookup"><span data-stu-id="264ac-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="264ac-105">Inngangur</span><span class="sxs-lookup"><span data-stu-id="264ac-105">Introduction</span></span>
<span data-ttu-id="264ac-106">Þetta efnisatriði sýnir hvernig á að fella inn Microsoft Power BI-skýrslu á flipann **Greiningar** á vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="264ac-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="264ac-107">Í dæminu sem er gefið hér stækkum við vinnusvæðið **Stjórnun bókana** í forritinu Bílaflotastjórnun til að fella inn greiningarvinnusvæði á  **Greiningarflipa**.</span><span class="sxs-lookup"><span data-stu-id="264ac-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="264ac-108">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="264ac-108">Prerequisites</span></span>
+ <span data-ttu-id="264ac-109">Aðgangur að þróunarumhverfi sem keyrir á Verkvangsuppfærslu 8 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="264ac-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="264ac-110">Greiningarskýrsla (.pbix skrá) sem var búin til með Microsoft Power BI Desktop, og sem er með gagnalíkan sem kemur úr gagnagrunni Einingarverslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="264ac-111">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="264ac-111">Overview</span></span>
<span data-ttu-id="264ac-112">Hvort sem þú útvíkkar fyrirliggjandi forritsvinnusvæði eða býrð til þitt eigið vinnusvæði geturðu notað innfelld greiningaryfirlit til að fá skýrt og gagnvirkt yfirlit yfir viðskiptagögnin þín.</span><span class="sxs-lookup"><span data-stu-id="264ac-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="264ac-113">Ferlið til að bæta við greiningarvinnusvæðisflipa er í fjórum skrefum.</span><span class="sxs-lookup"><span data-stu-id="264ac-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="264ac-114">Bættu við .pbix file sem Dynamics 365 tilfangi.</span><span class="sxs-lookup"><span data-stu-id="264ac-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="264ac-115">Skilgreindu greiningarsvinnusvæðisflipa.</span><span class="sxs-lookup"><span data-stu-id="264ac-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="264ac-116">Felldu inn .pbix tilfangið á vinnusvæðisflipanum.</span><span class="sxs-lookup"><span data-stu-id="264ac-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="264ac-117">Valfrjálst: Bættu við skrárendingum til að sérsníða yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="264ac-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="264ac-118">Nánari upplýsingar um hvernig á að búa til greiningarskýrslur er að finna íí [Hafist handa með Power BI skjáborð](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="264ac-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="264ac-119">Á þessari síðu er hægt að nálgast upplýsingar sem geta hjálpað þér að búa til áhugaverðar greiningarskýrslulausnir.</span><span class="sxs-lookup"><span data-stu-id="264ac-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="264ac-120">Bættu við .pbix file sem tilfangi</span><span class="sxs-lookup"><span data-stu-id="264ac-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="264ac-121">Áður en hafist er handa þarf að stofna eða sækja Power BI skýrsluna sem þú munt fella inn í vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="264ac-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="264ac-122">Nánari upplýsingar um hvernig á að búa til greiningarskýrslur er að finna íí [Hafist handa með Power BI skjáborð](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="264ac-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="264ac-123">Fylgdu eftirfarandi skrefum til að bæta við .pbix skrá sem Visual Studio verkgervingu.</span><span class="sxs-lookup"><span data-stu-id="264ac-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="264ac-124">Stofna nýtt verk í viðeigandi líkani.</span><span class="sxs-lookup"><span data-stu-id="264ac-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="264ac-125">Veldi verkið í Solution Explorer, hægrismelltu og veldu svo **Bæta við** > **Nýtt atriði**.</span><span class="sxs-lookup"><span data-stu-id="264ac-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="264ac-126">Í svarglugganum **Bæta við nýju atriði**, undir **Aðgerðagervingar**, velurðu sniðmátið **Tilföng**.</span><span class="sxs-lookup"><span data-stu-id="264ac-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="264ac-127">Færðu inn heiti sem verður notað til að vísa til skýrslunnar í X++ lýsigögnum, og smelltu svo á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="264ac-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Bættu við svarglugga fyrir Nýtt atriði](media/analytical-workspace-add.png)

5. <span data-ttu-id="264ac-129">Finndu .pbix skrána sem inniheldur skilgreininguna á greiningarskýrslunnu og smelltu síðan á **Opna**.</span><span class="sxs-lookup"><span data-stu-id="264ac-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Veldu svarglugga Tilfangaskrár](media/analytical-workspace-select-resource.png)

<span data-ttu-id="264ac-131">Nú þegar þú hefur bætt við .pbix skránni sem Dynamics 365 tilfangi geturðu fellt skýrslurnar inn í vinnusvæði og bætt við beinum tenglum með því að nota valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="264ac-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="264ac-132">Bættu flipastýringu við forritsvinnusvæðinu</span><span class="sxs-lookup"><span data-stu-id="264ac-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="264ac-133">Í þessu dæmi víkkum við út vinnusvæðið **Stjórnun bókana** í Bílaflotastjórnunarlíkaninu með því að bæta flipanum **Greiningar** við skilgreininguna á skjámyndinni **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="264ac-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="264ac-134">Eftirfarandi skýringarmynd sýnir hvernig skjámyndin **FMClerkWorkspace** lítur út í hönnuðinum í Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="264ac-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![FMClerkWorkspace skjámynd fyrir breytingar](media/analytical-workspace-definition-before.png)

<span data-ttu-id="264ac-136">Fylgið eftirfarandi skrefum til að víkka út skjámyndarskilgreininguna fyrir vinnusvæðið **Stjórnun bókana**.</span><span class="sxs-lookup"><span data-stu-id="264ac-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="264ac-137">Opnið skjámyndarhönnuðinn til að víkka út hönnunarskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="264ac-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="264ac-138">Í hönnunarskilgreiningunni velurðu efstu eininguna sem er merkt **Design | Pattern: Workspace Operational**.</span><span class="sxs-lookup"><span data-stu-id="264ac-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="264ac-139">Hægrismelltu og veldu svo **Nýtt** > **Flipi** til að bæta við nýrri stýringu sem heitir **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="264ac-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="264ac-140">Veldu **FormTabControl1** í skjámyndarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="264ac-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="264ac-141">Hægrismelltu og veldu síðan **Ný flipasíða** til að bæta við nýrri flipasíðu.</span><span class="sxs-lookup"><span data-stu-id="264ac-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="264ac-142">Gefðu flipasíðunni nýtt og auðskilið heiti, eins og **Vinnusvæði**.</span><span class="sxs-lookup"><span data-stu-id="264ac-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="264ac-143">Veldu **FormTabControl1** í skjámyndarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="264ac-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="264ac-144">Hægrismelltu og veldu svo **Ný flipasíða**.</span><span class="sxs-lookup"><span data-stu-id="264ac-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="264ac-145">Gefðu flipasíðunni nýtt og auðskilið heiti, eins og **Greiningar**.</span><span class="sxs-lookup"><span data-stu-id="264ac-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="264ac-146">Veldu **Greiningar (Flipasíða)** í skjámyndarhönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="264ac-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="264ac-147">Stilltu eiginleikann **Myndatexti** á **Greiningar**.</span><span class="sxs-lookup"><span data-stu-id="264ac-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="264ac-148">Hægrismelltu á stýringuna og veldu svo **Nýtt** > **Hópur** til að bæta við nýrri skjámyndarhópsstýringu.</span><span class="sxs-lookup"><span data-stu-id="264ac-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="264ac-149">Gefðu skjámyndarhópnum nýtt og auðskilið heiti, eins og **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="264ac-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="264ac-150">Veldu **PanoramaBody (Flipi)** í skjámyndarhönnuðinum, og dragðu svo stýringuna á flipann **Vinnusvæði**.</span><span class="sxs-lookup"><span data-stu-id="264ac-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="264ac-151">Í hönnunarskilgreiningunni velurðu efstu eininguna sem er merkt **Design | Pattern: Workspace Operational**.</span><span class="sxs-lookup"><span data-stu-id="264ac-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="264ac-152">Hægrismelltu og veldu svo **Fjarlægja mynstur**.</span><span class="sxs-lookup"><span data-stu-id="264ac-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="264ac-153">Hægrismelltu aftur og veldu síðan **Bæta við mynstri** > **Vinnusvæði á flipa**.</span><span class="sxs-lookup"><span data-stu-id="264ac-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="264ac-154">Framkvæmdu byggingu til að sannreyna breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="264ac-155">Eftirfarandi skýringarmynd sýnir hvernig hönnunin lítur út eftir að breytingarnar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="264ac-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace eftir breytingar](media/analytical-workspace-definition-after.png)

<span data-ttu-id="264ac-157">Nú þegar þú hefur bætt við skjámyndarstýringunum sem verða notaðar til að fella inn vinnusvæðisskýrsluna, verður þú að skilgreina stærð yfirstýringarinnar svo hún ráði við útlitið.</span><span class="sxs-lookup"><span data-stu-id="264ac-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="264ac-158">Sjálfgefið er að bæði síðan **Síurúða** og síðan **Flipi** verða sýnilegar á skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="264ac-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="264ac-159">Hins vegar er hægt að breyta sýnileika þessara stýringa eftir þörfum fyrir markneytanda skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="264ac-160">Fyrir innfelld vinnusvæði mælum við með að nota skrárendingar til að fela bæði síðuna **Síurúða** og síðuna **Flipi**, til að tryggja stöðugleika.</span><span class="sxs-lookup"><span data-stu-id="264ac-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="264ac-161">Nú hefurðu klárað það verk að útvíkka skilgreiningu umsóknareyðublaðsins.</span><span class="sxs-lookup"><span data-stu-id="264ac-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="264ac-162">Frekari upplýsingar um hvernig á að nota skrárendingar til að sérsníða er að finna á  [Sérsnið: yfirlögn og skrárendingar](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="264ac-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="264ac-163">Bættu við X++ viðskiptagrunni til að fella inn yfirlitsstýringu</span><span class="sxs-lookup"><span data-stu-id="264ac-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="264ac-164">Fylgdu eftirfarandi skrefum til að bæta við viðskiptagrunni sem virkjar skýrsluyfirlitsstýringuna sem er innfelld í vinnusvæðinu  **Stjórnun bókana**.</span><span class="sxs-lookup"><span data-stu-id="264ac-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="264ac-165">Opnaðu skjámyndarhönnuðinn **FMClerkWorkspace** til að víkka út hönnunarskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="264ac-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="264ac-166">Ýttu á F7 til að opna kóðann á bak við kóðaskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="264ac-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="264ac-167">Bættu við eftirfarandi X++ kóða.</span><span class="sxs-lookup"><span data-stu-id="264ac-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="264ac-168">Framkvæmdu byggingu til að sannreyna breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="264ac-169">Nú hefurðu lokið því verki að bæta við viðskiptagrunni til að virkja innfellda skýrsluyfirlitsstýringu.</span><span class="sxs-lookup"><span data-stu-id="264ac-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="264ac-170">Eftirfarandi skýringarmynd sýnir hvernig vinnusvæðið lítur út eftir að breytingarnar eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="264ac-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Skýrsla felld inn í vinnusvæðið](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="264ac-172">Hægt að opna fyrirliggjandi rekstraryfirlit með því að nota vinnusvæðisflipana fyrir neðan titil síðunnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="264ac-173">Tilvísun</span><span class="sxs-lookup"><span data-stu-id="264ac-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="264ac-174">PBIReportHelper.initializeReportControl aðferð</span><span class="sxs-lookup"><span data-stu-id="264ac-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="264ac-175">Þessi hluti veitir upplýsingar um hjálparklasann sem er notaður til að fella inn Power BI skýrslu (.pbix tilfang) í skjámyndarhópsstýringu.</span><span class="sxs-lookup"><span data-stu-id="264ac-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="264ac-176">Málskipun</span><span class="sxs-lookup"><span data-stu-id="264ac-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="264ac-177">Færibreytur</span><span class="sxs-lookup"><span data-stu-id="264ac-177">Parameters</span></span>

|       <span data-ttu-id="264ac-178">Nafn</span><span class="sxs-lookup"><span data-stu-id="264ac-178">Name</span></span>       |                                                              <span data-ttu-id="264ac-179">lýsing</span><span class="sxs-lookup"><span data-stu-id="264ac-179">Description</span></span>                                                               |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="264ac-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="264ac-180">resourceName</span></span>   |                                                    <span data-ttu-id="264ac-181">Heiti .pbix tilfangsins.</span><span class="sxs-lookup"><span data-stu-id="264ac-181">The name of the .pbix resource.</span></span>                                                     |
| <span data-ttu-id="264ac-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="264ac-182">formGroupControl</span></span> |                                    <span data-ttu-id="264ac-183">Skjámyndarhópsstýring til að nota Power BI skýrslustýringuna á.</span><span class="sxs-lookup"><span data-stu-id="264ac-183">The form group control to apply the Power BI report control to.</span></span>                                     |
| <span data-ttu-id="264ac-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="264ac-184">defaultPageName</span></span>  |                                                         <span data-ttu-id="264ac-185">Sjálfgefið síðuheiti.</span><span class="sxs-lookup"><span data-stu-id="264ac-185">The default page name.</span></span>                                                         |
|  <span data-ttu-id="264ac-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="264ac-186">showFilterPane</span></span>  |   <span data-ttu-id="264ac-187">Boole-gildi sem gefur til kynna hvort síusvæðið ætti að vera sýnt (<strong>satt</strong>) eða falið (<strong>ósatt</strong>).</span><span class="sxs-lookup"><span data-stu-id="264ac-187">A Boolean value that indicates whether the filter pane should be shown (<strong>true</strong>) or hidden (<strong>false</strong>).</span></span>   |
|   <span data-ttu-id="264ac-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="264ac-188">showNavPane</span></span>    | <span data-ttu-id="264ac-189">Boole-gildi sem gefur til kynna hvort yfirlitssvæði ætti að vera sýnt (<strong>satt</strong>) eða falið (<strong>ósatt</strong>).</span><span class="sxs-lookup"><span data-stu-id="264ac-189">A Boolean value that indicates whether the navigation pane should be shown (<strong>true</strong>) or hidden (<strong>false</strong>).</span></span> |
|  <span data-ttu-id="264ac-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="264ac-190">defaultFilters</span></span>  |                                              <span data-ttu-id="264ac-191">Sjálfgefnar síur Power BI skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="264ac-191">The default filters for the Power BI report.</span></span>                                              |


