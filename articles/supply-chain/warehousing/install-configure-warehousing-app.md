---
title: Setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing
description: "Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations – Warehousing."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: 0f83735ec42e945c5e0abf8d72b83936e076e60e
ms.contentlocale: is-is
ms.lasthandoff: 02/27/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing

[!include[banner](../includes/banner.md)]


> [!NOTE]

> Þetta efnisatriði lýsir því hvernig eigi að grunnstilla vörugeymslur fyrir virkjun skýs. Ef þú ert að leita að því hvernig eigi að grunnstilla vöruhús fyrir virkjun á staðnum, vinsamlegast skoðaðu [Vöruhús fyrir virkjun á staðnum](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations – Warehousing.

Finance and Operations - Warehousing er forrit sem er hægt að sækja á Google Play Store og Windows Store. Fyrir núverandi útgáfu Finance and Operations er þetta forrit útvegað sem stakur þáttur, sem þýðir að það er notað sjálfstætt á tækjum sem eru notuð við vöruhúsaaðgerðir. Til að nota forritið í þínu Finance and Operations umhverfi verður að sækja forritið fyrir hvert tæki og grunnstilla það til að geta tengst við þitt Finance and Operations umhverfi. Þetta efnisatriði lýsir því hvernig á að setja upp forritið á þínum tækjum. Það lýsir líka hvernig á að grunnstilla forritið til að tengjast þínu Finance and Operations umhverfi.

## <a name="prerequisites"></a>Frumskilyrði
Forritið er tiltækt fyrir Android og Windows stýrikerfi. Til að nota forritið verður þú að hafa sett upp eitt af eftirfarandi stýrikerfum á þínu tæki. Þú þarft einnig að vera með eina eftirfarandi studdra útgáfa af Finance and Operations. Notið upplýsingar í eftirfarandi töflu til að ákvarða hvort þitt umhverfi í fastbúnaði og hugbúnaði er tilbúið til að styðja uppsetninguna.

| Kerfi                    | Útgáfa                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (allar útgáfur)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, útgáfa 1611 <br>-eða- <br>Microsoft Dynamics Dynamics AX útgáfa 7.0/7.0.1 og Microsoft Dynamics AX verkvangsuppfærsla 2 með bráðabót KB 3210014 |

## <a name="get-the-app"></a>Sækja forritið
-   Windows (UWP)
     - [Finance and Operations - Warehousing í Windows store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Warehousing í Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Warehousing á Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Stofna vefþjónustuforrit í Azure Active Directory
Til að virkja forritið til að eiga samskipti við tiltekinn þjón fyrir Finance and Operations verður að skrá vefþjónustuforrit í Azure Active Directory fyrir leigjanda Finance and Operations. Af öryggisástæðum ráðleggjum við að búa til vefþjónustuforrit fyrir hvert tæki sem þú notar. Til að stofna vefþjónustuforrit í Azure Active Directory (Azure AD) skal fylgja eftirfarandi skrefurm:

1.  Opnaðu vafra og farðu á <https://portal.azure.com>.
2.  Færið inn heiti og aðgangsorð fyrir notandi með aðgang að Azure-áskrift.
3.  Í Azure gátt, í vinstri yfirlitssvæðinu, smelltu á **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Tryggðu að Active Directory tilvikið sé það sem er notað af Finance and Operations.
5.  Smelltu á **forritsskráningar** í listanum. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Í efsta glugganum skaltu smella á **Nýja forritsskráningu**. **Bæta við forriti** leiðsagnarforrit er ræst.
7.  Sláðu inn heiti forritsins og veldu **Vefforrit/vef-API**. Sláðu inn innskráningarvefslóð, sem er þín vefslóð fyrir vefforit. Vefslóðin er sú sama og vefslóð uppsetningar þinnar, en oauth er bætt við fyrir aftan. Smellið á **Stofna**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Veldu nýja forritið á listanum. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Mundu **kenni forrits**, þú munt þurfa á því að halda síðar. **Kenni forritsins** verður síðar vísað til sem **kenni biðlara**.
10. Smelltu á **Lyklar** í **Stillingarglugganum**. Stofnaðu lykil með því að slá inn lyklalýsingu og lengd í **lykilorða** hlutanum. 
11. Smelltu á **Vista** og afritaðu lykilinn. Seinna verður vísað til þessa lykils sem **Leynilikill biðlara**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Stofnaðu og skilgreindu notandareikning í Finance and Operations
Til að virkja Finance and Operations til að nota Azure AD forritið þitt þarf að ljúka eftirfarandi skilgreiningarskrefum:

1.  Stofna nýjan notandareikning í Azure Active Directory fyrir leigjanda Finance and Operations. Tilgangur þessa notandareiknings er að fá aðgang að tiltekinni sérstilltri þjónustu í vöruhúsaforritinu sem Finance and Operations þjónninn birtir. Þegar þessu skrefi er lokið verður þú með skilríki WMDP-notanda, sem eru WMDP-nettfang og WMDP-aðgangsorð. Frekari upplýsingar um grunnskref við að bæta notendum við Azure AD og Finance and Operations, eru í þessu kennsluefni: [Skráning í áskrift að Finance and Operations](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Stofnaðu Finance and Operations notanda sem samsvarar notandaskilríkjum í vöruhússforriti.
    1.  Í Finance and Operations er farið í **Kerfisstjórnun** &gt; **Almennt** &gt; **Notendur**.
    2.  Stofnaðu nýjan notanda
    3.  Úthlutaðu notanda Vöruhús í fartæki, eins og sýnt er á eftirfarandi skjáskoti. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Tengdu Azure Active Directory forritið þitt við notanda vöruhússforrits fyrir fartæki.
    1.  Í Finance and Operations er farið í **Kerfisstjórnun** &gt; **Uppsetning** &gt; **Azure Active Directory forrit**.
    2.  Stofnið nýja línu.
    3.  Færið inn **Biðlarakenni** (útvegað í síðasta hluti), gefðu því heiti og veldu notandann sem var búið að stofna. Við mælum með því að þú merkir öll tækin þín til að auðvelt sé að fjarlægja aðgang þeirra að Finance and Operations af þessari síðu ef þau týnast. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Skilgreina forritið
Það verður að grunnstilla forritið á tækinu til að tengjast þjóni Finance and Operations í gegnum Azure AD forritið. Það er gert með því að ljúka við eftirfarandi ferli:

1.  Í forritinu, opna **Tengingarstillingar**.
2.  Hreinsa svæðið **Sýnistilling**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Færi inn eftirfarandi upplýsingar: 
    + **Biðlarakenni Azure Active-skráasafns** - Biðlarakennið er fengið í skrefi 9 „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + **Leyndarmál biðlara Azure Active-skráasafns** - Leyndarmál biðlara er fengið í skrefi 11 í „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + **Tilföng Azure Active-skráasafns** - Tilföng Azure Active-skráasafns tilgreina rót vefslóðar Finance and Operations. **Athugið**: Látið þennan reit ekki enda á framvísandi skástriki (/). 
    + **Azure Active directory leigjandi** - Azure AD directory leigjandi sem er notaður með Finance and Operations þjóni: `https://login.windows.net/your-AD-tenant-ID`. Til dæmis: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Athugið**: Látið þennan reit ekki enda á framvísandi skástriki (/). 
    + **Fyrirtæki** - Færðu inn þann lögaðila í Finance and Operations sem þú vilt að tengist forritinu. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Veldu hnappinn **Til baka** í efra vinstra horni forritsins Þá tengist forritið þínum Finance and Operations þjóni og innskráningarskjár fyrir starfsmenn í vöruhúsi birtist. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki
Ef tæki týnist eða öryggi þess er ógnað verður þú að fjarlægja aðgang að Finance and Operations fyrir það tæki. Eftirfarandi skref lýsa ráðlögðu ferli við að fjarlægja aðgangur.

1.  Í Finance and Operations er farið í **Kerfisstjórnun** &gt; **Uppsetning** &gt; **Azure Active Directory forrit**.
2.  Eyddu línunni sem samsvarar tækinu sem á að fjarlægja aðgang úr. Mundu **biðlararkennið** sem er notað fyrir fjarlægða tækið, þú þarft það síðar.
3.  Skráðu þig inn á Azure-gáttina á <https://portal.azure.com>.
4.  Smelltu á **Active Directory** táknið á vinstri valmyndinni og vertu viss um að þú sért í réttu skráasafni.
5.  Í listanum smelltu á **forritsskráningar** og smelltu síðan á forritið sem þú vilt skilgreina. **Stillingar** síðan birtist með grunnstillingarupplýsingum.
6.  Vertu viss um að **biðlarakenni** forritsins sé það sama og í skrefi 2 í þessum kafla.
7.  Smelltu á hnappinn **Eyða** efst í glugganum.
8.  Í staðfestingarglugganum smellirðu á **Já**.

