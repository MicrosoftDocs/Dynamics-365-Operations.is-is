---
title: "Setja upp og skilgreina Microsoft Dynamics 365 fyrir Aðgerðir & #8211; Vöruhús"
description: "Í þessu efnisatriði er lýst hvernig eigi að setja upp og skilgreina Microsoft Dynamics 365 aðgerða - Vöruhús."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Setja upp og skilgreina Microsoft Dynamics 365 fyrir Aðgerðir & #8211; Vöruhús

Í þessu efnisatriði er lýst hvernig eigi að setja upp og skilgreina Microsoft Dynamics 365 aðgerða - Vöruhús.

Dynamics 365 aðgerða - Vöruhús er forrit tiltækur í Geymslueiningu fyrir Windows og Google Play Verslun. Gildandi útgáfu af Microsoft Dynamics 365 aðgerða, fylgir forritið sem stök íhlut, sem þýðir að self-virkjun á tæki sem eru notaðar fyrir vöruhús verkefni. Til að nota forritið þitt Dynamics 365 fyrir umhverfi Aðgerðir, verður að sækja forrit á hvert tæki og skilgreina hana til að tengjast við Dynamics 365 fyrir Aðgerðir umhverfi. Þetta efnisatriði lýsir hvernig setja forritið upp á við tæki. Hún líka skýrir skilgreina forrits til að tengjast við Dynamics 365 fyrir Aðgerðir umhverfi.

## <a name="prerequisites"></a>Forkröfur
Forritið er tiltæk á Android og Windows stýrikerfi. Til að nota forritið, þarf einn við eftirfarandi studd stýrikerfi uppsett á þitt tæki. Einnig þarf eitt af eftirfarandi studdar útgáfur af Dynamics 365 fyrir Aðgerðir. Notið upplýsingar í eftirfarandi töflu til að meta ef umhverfinu hug- og vélbúnaður er tilbúið til að styðja við uppsetningu.

| Kerfi                    | Útgáfa                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (allar útgáfur)                                                                                                                                                   |
| Dynamics 365 fyrir Aðgerðir | Svæðis í Microsoft Dynamics AX og Microsoft Dynamics 365 fyrir Aðgerðir útgáfu 1611 - eða - Microsoft Dynamics Dynamics AX 7,0/7.0.1 uppfæra 2 með bráðabót KB 3210014 |

## <a name="get-the-app"></a>Sækja forritið
-   Windows (UWP) - [Dynamics 365 aðgerða - Vöruhús í Geymslueiningu fyrir Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 aðgerða - Vöruhús á Google Play Verslunar](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Stofna þarf vefforrit þjónustu í Active Directory
Til að virkja forritið á að eiga samskipti við tiltekna Dynamics 365 fyrir Aðgerðir server, þarf að skrá þjónustuna vefforrit í Azure Active fyrir Dynamics 365 fyrir leigjanda Aðgerðir. Öryggisástæðum er mælt með því að stofna vefforrit þjónustu fyrir hverja tækið sem nota. Til að stofna þarf vefforrit þjónustu í Azure Active Directory (Azure AD), skal ljúka eftirfarandi skrefum:

1.  Í vefvafra, farið <https://manage.windowsazure.com>.
2.  Færið inn nafn og aðgangsorð fyrir notandann sem hefur aðgang að Azure áskrift.
3.  Í Azure Portal er í vinstri skoðunarrúðu smellt **Active Directory**. [](./media/wh-01-active-directory-example.png)[![wh-01-virk-directory-dæmi](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Veljið Active Directory-tilvik sem notar Dynamics 365 aðgerða í hnitanetinu.
5.  Smellið á efstu **Umsóknir**. [![wh-02-virk-directory-forrit](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Í neðri rúðunni er smellt á **Bæta**. Í **Bæta forritið** leiðsagnarforrit hefst.
7.  Færið inn heiti fyrir forritið og veljið **Vefforritið og/eða web API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Færið inn formerki á Vefslóð, sem er forritið Vefslóð í skal leigjanda rót SLÓÐ Aðgerða. Vefslóð formerki á er ekki virkri notuð sem stendur í sannvottun hugbúnaðarhlutaþjóninum forritið en er skyldusvæði. Færa inn sama Vefslóð í svæðinu URI Kenni Forrits. [![wh-04-ad-bæta-eiginleika](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Farið í **Skilgreina** flipa. [![wh-05-ad-skilgreina-forrits](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Fletta niður þar til að sjá á **Heimildir fyrir önnur forrit** hluta. Smellið á **Bæta forritið**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Velja **Microsoft Dynamics ERP** á listanum. Smellið á **Ljúka ávísun** hnappinn hægri horninu á síðunni. [![wh-07-ad-velja-heimildir](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Í því **Úthluta Heimildum** skal velja alla gátreiti. Click **Save**. [![wh-08-ad-úthluta-heimildir](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Skráið eftirfarandi upplýsingar:
    -   **Biðlarakenni** - eins Og að fletta upp á síðu sjást **Biðlarakenni** birt.
    -   **Lykill** - í það **Lykla** hlutanum stofna lykil með því að velja tímalengd og afrita lykillinn. Þessi lykill verður seinna að kallað á **Biðlara leyndarmál**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Stofna og skilgreina notandareikning í í Dynamics 365 fyrir Aðgerðir
Til að virkja Dynamics 365 aðgerða til að nota hugbúnaðinn Azure AD, þarf að ljúka við eftirfarandi afbrigði:

1.  Stofna nýjan lykil notanda Dynamics 365 fyrir leigjanda Aðgerðir í Azure Active Directory. Tilgangur þessa notandareikningurinn er til að nota ákveðna sérsniðna þjónustuna warehousing forrits sem birtir Dynamics 365 fyrir Aðgerðir þjóninum. Eftir að ljúka við þessi þrep er verður að hafa notendaheimildir WMDP, sem samanstanda af þarf WMDP netfang og lykilorð WMDP. Til að fræðast um grundvallarskref við til að bæta notendum í Azure AD og Dynamics 365 fyrir Aðgerðir í sýnikennsluna: [Innskráning í Microsoft Dynamics 365 fyrir Aðgerðir áskriftar](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Stofna Dynamics 365 Aðgerðir notanda sem samsvarar warehousing notendaheimildir forrits.
    1.  Í Dynamics 365 fyrir Aðgerðir, farið **kerfisstjórnun**&gt;**Algengar**&gt;**Notendur**.
    2.  Stofna nýjan notanda.
    3.  Úthluta notanda fartækis Vöruhúss, eins og sýnt er í eftirfarandi skjámyndir. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Tengja warehousing forrits notanda hugbúnaðinn Azure Active Directory.
    1.  Í Dynamics 365 aðgerða, farið **kerfisstjórnun**&gt;**Uppsetningu**&gt;**Azure Active Directory-forrit**.
    2.  Stofnið nýja línu.
    3.  Færa inn í **Biðlarakenni** (fengið í síðasta hluta,) gefa því heiti og valinn sá notandi sem hefur áður verið stofnaðar. Mælt er með að merkinu öll tæki svo að auðvelt fjarlægja má þeirra aðgang að Dynamics 365 fyrir Aðgerðir úr þessari síðu ef þær eru glatast. [![wh-10-ad-forrit-skjámynd](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Skilgreina forritið
Skilgreina forritið á tæki til að tengjast við Dynamics 365 þjóns Aðgerðir með Azure AD-forritið. Til þess að ljúka eftirfarandi skrefum.

1.  Í forriti, farið **tengingarstillingar**.
2.  Hreinsa skal **sýningarstillingu** svæði. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Færa inn eftirfarandi upplýsingar:- **Azure Active directory Biðlarakenni** -biðlara Kenni fæst í skref 13 í "Stofna vefforrit þjónustu í Active Directory". - **Azure Active directory biðlara leyndarmál** -biðlara leyndarmál fæst í skref 13 í "Stofna vefforrit þjónustu í Active Directory". - **Azure Active directory tilfanga** -directory tilfang Azure AD depicts Dynamics 365 fyrir Vefslóð rót Aðgerðir. **Athugasemd**: endar ekki þetta svæði með staf skástrik (/). - **Azure Active directory leigjanda** -leigjanda directory Azure AD notað með Dynamics 365 Aðgerðir server: https://login.windows.net/&lt;your-AD-leigjanda-Kenni&gt;. Til dæmis: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Athugasemd**: endar ekki þetta svæði með staf skástrik (/). - **Fyrirtæki** -færið Inn lögaðila í Dynamics 365 fyrir Aðgerðir sem óskað er eftir að umsókn til að tengjast. [![wh-12-forrits-tenging-stillingar](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Velja skal **Aftur** hnappinn efst í vinstra horni forritsins. Forritið mun nú tengjast við Dynamics 365 Aðgerðir þjóns og birtir skjánum innskráningu starfsmanns vöruhús. [![wh-13-innskráningu-skjánum](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki
Ef gefa týnda eða öryggi hættu tækis, verður að fjarlægja aðgang að Dynamics 365 aðgerða fyrir tækið. Eftirfarandi skrefum er lýst mælt er með ferlið til að fjarlægja aðgang.

1.  Í Dynamics 365 aðgerða, farið **kerfisstjórnun**&gt;**Uppsetningu**&gt;**Azure Active Directory-forrit**.
2.  Eyða línu sem samsvarar tækið sem óskað er að fjarlægja aðgang. Athugið niður í **Biðlarakenni** notaðir fyrir fjarlægð tækið.
3.  Skrá í Azure classic portal á <https://manage.windowsazure.com>.
4.  Smellið á **Active Directory** á vinstri valmynd og svo á æskilegt skráasafninu.
5.  Í efstu valmyndinni er smellt á **Umsóknir**, og smellið síðan á forritinu sem á að skilgreina. Í **Flýtiræsistikunni Ræsa** síða birtast með einni formerki á og aðrar upplýsingar um afbrigðið.
6.  Smellið á í **Skilgreina** valinn fletta niður og tryggja í **Biðlarakenni** forritsins er sú sama og í skrefi 2 í þessum hluta.
7.  Smellið á **Eyða** strikamerkjum skipana hnappinn.
8.  Smellið á **Já** í skilaboðunum staðfestingu.



