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
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fc8102d945faf9ad533f57ec1a45b0e0dc344963
ms.openlocfilehash: d36abbf7c08c56d84ed83dbec1bfa33f30b47ef5
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Bæta greiningu við vinnusvæði með Power BI Embedded

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Þessi eiginleiki er studdur í Dynamics 365 tfor Finance and Operations (útgáfu 7.2 og seinni).

# <a name="introduction"></a>Inngangur
Þetta efnisatriði sýnir hvernig á að fella inn Microsoft Power BI-skýrslu á flipann **Greiningar** á vinnusvæði. Í dæminu sem er gefið hér stækkum við vinnusvæðið **Stjórnun bókana** í forritinu Bílaflotastjórnun til að fella inn greiningarvinnusvæði á  **Greiningarflipa**.

# <a name="prerequisites"></a>Frumskilyrði
+ Aðgangur að þróunarumhverfi sem keyrir á Verkvangsuppfærslu 8 eða nýrri.
+ Greiningarskýrsla (.pbix skrá) sem var búin til með Microsoft Power BI Desktop, og sem er með gagnalíkan sem kemur úr gagnagrunni Einingarverslunarinnar.

# <a name="overview"></a>Yfirlit
Hvort sem þú útvíkkar fyrirliggjandi forritsvinnusvæði eða býrð til þitt eigið vinnusvæði geturðu notað innfelld greiningaryfirlit til að fá skýrt og gagnvirkt yfirlit yfir viðskiptagögnin þín. Ferlið til að bæta við greiningarvinnusvæðisflipa er í fjórum skrefum.

1. Bættu við .pbix file sem Dynamics 365 tilfangi.
2. Skilgreindu greiningarsvinnusvæðisflipa.
3. Felldu inn .pbix tilfangið á vinnusvæðisflipanum.
4. Valfrjálst: Bættu við skrárendingum til að sérsníða yfirlitið.

> [!NOTE]
> Nánari upplýsingar um hvernig á að búa til greiningarskýrslur er að finna íí [Hafist handa með Power BI skjáborð](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/). Á þessari síðu er hægt að nálgast upplýsingar sem geta hjálpað þér að búa til áhugaverðar greiningarskýrslulausnir.

# <a name="add-a-pbix-file-as-a-resource"></a>Bættu við .pbix file sem tilfangi
Áður en hafist er handa þarf að stofna eða sækja Power BI skýrsluna sem þú munt fella inn í vinnusvæðið. Nánari upplýsingar um hvernig á að búa til greiningarskýrslur er að finna íí [Hafist handa með Power BI skjáborð](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).
 
Fylgdu eftirfarandi skrefum til að bæta við .pbix skrá sem Visual Studio verkgervingu.

1. Stofna nýtt verk í viðeigandi líkani.
2. Veldi verkið í Solution Explorer, hægrismelltu og veldu svo **Bæta við** > **Nýtt atriði**.
3. Í svarglugganum **Bæta við nýju atriði**, undir **Aðgerðagervingar**, velurðu sniðmátið **Tilföng**.
4. Færðu inn heiti sem verður notað til að vísa til skýrslunnar í X++ lýsigögnum, og smelltu svo á **Bæta við**.

    ![Bættu við svarglugga fyrir Nýtt atriði](media/analytical-workspace-add.png)

5. Finndu .pbix skrána sem inniheldur skilgreininguna á greiningarskýrslunnu og smelltu síðan á **Opna**.

    ![Veldu svarglugga Tilfangaskrár](media/analytical-workspace-select-resource.png)
  
Nú þegar þú hefur bætt við .pbix skránni sem Dynamics 365 tilfangi geturðu fellt skýrslurnar inn í vinnusvæði og bætt við beinum tenglum með því að nota valmyndaratriði.

# <a name="add-a-tab-control-to-an-application-workspace"></a>Bættu flipastýringu við forritsvinnusvæðinu
Í þessu dæmi víkkum við út vinnusvæðið **Stjórnun bókana** í Bílaflotastjórnunarlíkaninu með því að bæta flipanum **Greiningar** við skilgreininguna á skjámyndinni **FMClerkWorkspace**.
 
Eftirfarandi skýringarmynd sýnir hvernig skjámyndin **FMClerkWorkspace** lítur út í hönnuðinum í Microsoft Visual Studio.

![FMClerkWorkspace skjámynd fyrir breytingar](media/analytical-workspace-definition-before.png)

Fylgið eftirfarandi skrefum til að víkka út skjámyndarskilgreininguna fyrir vinnusvæðið **Stjórnun bókana**.

1. Opnið skjámyndarhönnuðinn til að víkka út hönnunarskilgreininguna.
2. Í hönnunarskilgreiningunni velurðu efstu eininguna sem er merkt **Design | Pattern: Workspace Operational**.
3. Hægrismelltu og veldu svo **Nýtt** > **Flipi** til að bæta við nýrri stýringu sem heitir **FormTabControl1**.
4. Veldu **FormTabControl1** í skjámyndarhönnuðinum.
5. Hægrismelltu og veldu síðan **Ný flipasíða** til að bæta við nýrri flipasíðu.
6. Gefðu flipasíðunni nýtt og auðskilið heiti, eins og **Vinnusvæði**.
7. Veldu **FormTabControl1** í skjámyndarhönnuðinum.
8. Hægrismelltu og veldu svo **Ný flipasíða**.
9. Gefðu flipasíðunni nýtt og auðskilið heiti, eins og **Greiningar**.
10. Veldu **Greiningar (Flipasíða)** í skjámyndarhönnuðinum.
11. Stilltu eiginleikann **Myndatexti** á **Greiningar**.
12. Hægrismelltu á stýringuna og veldu svo **Nýtt** > **Hópur** til að bæta við nýrri skjámyndarhópsstýringu.
13. Gefðu skjámyndarhópnum nýtt og auðskilið heiti, eins og **powerBIReportGroup**.
14. Veldu **PanoramaBody (Flipi)** í skjámyndarhönnuðinum, og dragðu svo stýringuna á flipann **Vinnusvæði**.
15. Í hönnunarskilgreiningunni velurðu efstu eininguna sem er merkt **Design | Pattern: Workspace Operational**.
16. Hægrismelltu og veldu svo **Fjarlægja mynstur**.
17. Hægrismelltu aftur og veldu síðan **Bæta við mynstri** > **Vinnusvæði á flipa**.
18. Framkvæmdu byggingu til að sannreyna breytingarnar.
 
Eftirfarandi skýringarmynd sýnir hvernig hönnunin lítur út eftir að breytingarnar eru gerðar.

![FMClerkWorkspace eftir breytingar](media/analytical-workspace-definition-after.png)

Nú þegar þú hefur bætt við skjámyndarstýringunum sem verða notaðar til að fella inn vinnusvæðisskýrsluna, verður þú að skilgreina stærð yfirstýringarinnar svo hún ráði við útlitið. Sjálfgefið er að bæði síðan **Síurúða** og síðan **Flipi** verða sýnilegar á skýrslunni. Hins vegar er hægt að breyta sýnileika þessara stýringa eftir þörfum fyrir markneytanda skýrslunnar.
 
> [!NOTE]
> Fyrir innfelld vinnusvæði mælum við með að nota skrárendingar til að fela bæði síðuna **Síurúða** og síðuna **Flipi**, til að tryggja stöðugleika.
 
Nú hefurðu klárað það verk að útvíkka skilgreiningu umsóknareyðublaðsins. Frekari upplýsingar um hvernig á að nota skrárendingar til að sérsníða er að finna á  [Sérsnið: yfirlögn og skrárendingar](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Bættu við X++ viðskiptagrunni til að fella inn yfirlitsstýringu
Fylgdu eftirfarandi skrefum til að bæta við viðskiptagrunni sem virkjar skýrsluyfirlitsstýringuna sem er innfelld í vinnusvæðinu  **Stjórnun bókana**.

1. Opnaðu skjámyndarhönnuðinn **FMClerkWorkspace** til að víkka út hönnunarskilgreininguna.
2. Ýttu á F7 til að opna kóðann á bak við kóðaskilgreininguna.
3. Bættu við eftirfarandi X++ kóða.

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

4. Framkvæmdu byggingu til að sannreyna breytingarnar.

Nú hefurðu lokið því verki að bæta við viðskiptagrunni til að virkja innfellda skýrsluyfirlitsstýringu. Eftirfarandi skýringarmynd sýnir hvernig vinnusvæðið lítur út eftir að breytingarnar eru gerðar.

![Skýrsla felld inn í vinnusvæðið](media/analytical-workspace-final.png)

> [!NOTE]
> Hægt að opna fyrirliggjandi rekstraryfirlit með því að nota vinnusvæðisflipana fyrir neðan titil síðunnar.

# <a name="reference"></a>Tilvísun

## <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl aðferð
Þessi hluti veitir upplýsingar um hjálparklasann sem er notaður til að fella inn Power BI skýrslu (.pbix tilfang) í skjámyndarhópsstýringu.

### <a name="syntax"></a>Málskipun
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>Færibreytur

| Nafn | lýsing |
|---|---|
| resourceName | Heiti .pbix tilfangsins. |
| formGroupControl | Skjámyndarhópsstýring til að nota Power BI skýrslustýringuna á. |
| defaultPageName | Sjálfgefið síðuheiti. |
| showFilterPane | Boole-gildi sem gefur til kynna hvort síusvæðið ætti að vera sýnt (**satt**) eða falið (**ósatt**). |
| showNavPane | Boole-gildi sem gefur til kynna hvort yfirlitssvæði ætti að vera sýnt (**satt**) eða falið (**ósatt**). |
| defaultFilters | Sjálfgefnar síur Power BI skýrslunnar. |

