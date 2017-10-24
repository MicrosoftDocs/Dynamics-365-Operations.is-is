---
title: Setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing
description: "Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations – Warehousing."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 31e77b27d4bf95c997817b3a053b33119562adf8
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla Microsoft Dynamics 365 for Finance and Operations – Warehousing.

Finance and Operations - Warehousing er forrit sem er hægt að sækja á Google Play Store og Windows Store. Fyrir núverandi útgáfu Finance and Operations er þetta forrit útvegað sem stakur þáttur, sem þýðir að það er notað sjálfstætt á tækjum sem eru notuð við vöruhúsaaðgerðir. Til að nota forritið í þínu Finance and Operations umhverfi verður að sækja forritið fyrir hvert tæki og grunnstilla það til að geta tengst við þitt Finance and Operations umhverfi. Þetta efnisatriði lýsir því hvernig á að setja upp forritið á þínum tækjum. Það lýsir líka hvernig á að grunnstilla forritið til að tengjast þínu Finance and Operations umhverfi.

## <a name="prerequisites"></a>Frumskilyrði
Forritið er tiltækt fyrir Android og Windows stýrikerfi. Til að nota forritið verður þú að hafa sett upp eitt af eftirfarandi stýrikerfum á þínu tæki. Þú þarft einnig að vera með eina eftirfarandi studdra útgáfa af Finance and Operations. Notið upplýsingar í eftirfarandi töflu til að ákvarða hvort þitt umhverfi í fastbúnaði og hugbúnaði er tilbúið til að styðja uppsetninguna.

| Kerfi                    | Útgáfa                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (allar útgáfur)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations útgáfa 1611 <br>-eða- <br>Microsoft Dynamics Dynamics AX útgáfa 7.0/7.0.1 og Microsoft Dynamics AX verkvangsuppfærsla 2 með bráðabót KB 3210014 |

## <a name="get-the-app"></a>Sækja forritið
-   Windows (UWP): [Finance and Operations - Warehousing í Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations - Warehousing í Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Warehousing á Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Stofna vefþjónustuforrit í Active Directory
Til að virkja forritið til að eiga samskipti við tiltekinn þjón fyrir Finance and Operations verður að skrá vefþjónustuforrit í Azure Active Directory fyrir leigjanda Finance and Operations. Af öryggisástæðum ráðleggjum við að búa til vefþjónustuforrit fyrir hvert tæki sem þú notar. Til að stofna vefþjónustuforrit í Azure Active Directory (Azure AD) skal fylgja eftirfarandi skrefurm:

1.  Opnaðu vafra og farðu í <https://manage.windowsazure.com>.
2.  Færið inn heiti og aðgangsorð fyrir notandi með aðgang að Azure-áskrift.
3.  Í Azure gátt, í vinstri yfirlitssvæði, smellt er á **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Í hnitanetinu velurðu það Active Directory tilvik sem er notað af Finance and Operations.
5.  Á efri  tækjastika, Smellt er á  **Forrit**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Á neðra svæði, smelltu á **Bæta við**. **Bæta við forriti** leiðsagnarforrit er ræst.
7.  Færðu inn heiti forrits og veldu **Vefforrit og /eða vef-API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Sláðu inn innskráningarvefslóð, sem er þín vefslóð fyrir vefforit. Vefslóðin er sú sama og vefslóð uppsetningar þinnar, en oauth er bætt við fyrir aftan. Sláðu inn URI forritsauðkennis, þetta gildi er skyldubundið en er ekki nauðsynlegt fyrir sannvottun. Vertu viss um að þetta URI forritsauðkenni sé eftirlíkingar-URI eins og https://contosooperations/wmapp, þar sem notkun vefslóðar innleiðingar þinnar getur valdið vandamálum í öðrum AAD-forritum eins og í Excel-innbótinni. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  Farðu í flipann **Skilgreina**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Flettu niður þar til þú sérð hlutann **Heimildir fyrir önnur forrit**. Smellt er á **Bæta við forriti**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Veldu **Microsoft Dynamics ERP** á listanum Smellt er á the **Ljúka við könnun** hnappur í hægra horni síðu [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Í **Heimildir fulltrúa** listi, velja allar gátreitur. Smellið á **Vista**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Skráið niður eftirfarandi upplýsingar:
    -   **Biðlarakenni** - þegar þú flettir upp síðuna sérðu **Biðlarakenni**.
    -   **Lykill** - Í **Lykill** hluti, stofnaðu lykil með því að velja tímalengd og afritaðu lykilinn. Seinna verður vísað til þessa lykils sem **Leynilikill biðlara**.

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
    + **Biðlarakenni Azure Active-skráasafns** - Biðlarakennið er fengið í skrefi 13 „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + **Leyndarmál biðlara Azure Active-skráasafns** - Leyndarmál biðlara er fengið í skrefi 13 í „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + **Tilföng Azure Active-skráasafns** - Tilföng Azure Active-skráasafns tilgreina rót vefslóðar Finance and Operations. **Athugið**: Látið þennan reit ekki enda á framvísandi skástriki (/). 
    + **Leigjandi Azure Active-skráasafns** - Leigjandi Azure AD-skráasafns sem er notaður með þjóni Finance and Operations: https://login.windows.net/your-AD-tenant-ID. Til dæmis: https://login.windows.net/contosooperations.onmicrosoft.com.
    <br>**Athugið**: Látið þennan reit ekki enda á framvísandi skástriki (/). 
    + **Fyrirtæki** - Færðu inn þann lögaðila í Finance and Operations sem þú vilt að tengist forritinu. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Veldu hnappinn **Til baka** í efra vinstra horni forritsins Þá tengist forritið þínum Finance and Operations þjóni og innskráningarskjár fyrir starfsmenn í vöruhúsi birtist. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki
Ef tæki týnist eða öryggi þess er ógnað verður þú að fjarlægja aðgang að Finance and Operations fyrir það tæki. Eftirfarandi skref lýsa ráðlögðu ferli við að fjarlægja aðgangur.

1.  Í Finance and Operations er farið í **Kerfisstjórnun** &gt; **Uppsetning** &gt; **Azure Active Directory forrit**.
2.  Eyddu línunni sem samsvarar tækinu sem á að fjarlægja aðgang úr. Skráðu niður **biðlarakenni** sem notað er fyrir tækið sem er fjarlægt.
3.  Skrá inn í Azure classic gátt á <https://manage.windowsazure.com>.
4.  Smellt er á the **Active Directory** tákn á vinstri Valmynd, og svo smellt á æskilegt skráasafn.
5.  Á efstu valmynd, Smellt er á **forrit** og svo smellt er á forritið sem á að skilgreina. Síðan **Flýtiræsing** birtist með stakri innskráningu og öðrum skilgreiningarupplýsingum.
6.  Smellt er á flipann **Skilgreina** flett niður og tryggt að **Biðlarakenni**  forrits er sama og í skrefi 2 í þessum hluta.
7.  Smellið á hnappinn **Eyða** á skipanastiku
8.  Í staðfestingarglugganum smellirðu á **Já**.





