---
title: Yfirlit yfir uppsetningu og skilgreiningu vöruhúsaforrits
description: Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla forritið Dynamics 365 for Finance and Operations – Warehousing.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52882ef7542bfedebdae4a08de8404cddd01ed55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205599"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Yfirlit yfir uppsetningu og skilgreiningu vöruhúsaforrits

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Þetta efnisatriði lýsir því hvernig eigi að grunnstilla vörugeymslur fyrir virkjun skýs. Ef þú ert að leita að því hvernig eigi að grunnstilla vöruhús fyrir virkjun á staðnum, vinsamlegast skoðaðu [Vöruhús fyrir virkjun á staðnum](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla forritið Dynamics 365 for Finance and Operations – Warehousing.

Forritið Warehousing er fáanlegt í Google Play Store og Windows Store. Fyrir núverandi útgáfu af Dynamics 365 Supply Chain Management er þetta forrit útvegað sem stakur þáttur, sem þýðir að það er notað sjálfstætt á tækjum sem eru notuð við vöruhúsaaðgerðir. Til að nota forritið í þínu Finance and Operations umhverfi verður að sækja forritið fyrir hvert tæki og grunnstilla það til að geta tengst við þitt Supply Chain Management umhverfi. Þetta efnisatriði lýsir því hvernig á að setja upp forritið á þínum tækjum. Það lýsir líka hvernig á að grunnstilla forritið til að tengjast þínu Supply Chain Management umhverfi.

## <a name="prerequisites"></a>Forkröfur
Forritið er tiltækt fyrir Android og Windows stýrikerfi. Til að nota forritið verður þú að hafa sett upp eitt af eftirfarandi stýrikerfum á þínu tæki. Ein af eftirfarandi studdum útgáfum verður einnig að vera til staðar. Notið upplýsingar í eftirfarandi töflu til að ákvarða hvort þitt umhverfi í fastbúnaði og hugbúnaði er tilbúið til að styðja uppsetninguna.

| Kerfi                    | Útgáfa                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (allar útgáfur)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, útgáfa 1611 <br>-eða- <br>Microsoft Dynamics AX útgáfa 7.0/7.0.1 og Microsoft Dynamics AX verkvangur uppfærsla 2 með bráðabót KB 3210014 |

## <a name="get-the-app"></a>Sækja forritið
-   Windows (UWP)
     - [Finance and Operations - Warehousing í Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Warehousing í Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery er hætt, sem þýðir að ekki er hægt að hlaða niður forritinu frá þeim stað.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Stofna vefþjónustuforrit í Azure Active Directory
Til að virkja forritið til að eiga samskipti við tiltekinn Supply Chain Management þjón fyrir verður að skrá vefþjónustuforrit í Azure Active Directory fyrir leigjanda Supply Chain Management. Af öryggisástæðum ráðleggjum við að búa til vefþjónustuforrit fyrir hvert tæki sem þú notar. Til að stofna vefþjónustuforrit í Azure Active Directory (Azure AD) skal fylgja eftirfarandi skrefum:

1.  Opnaðu vafra og farðu á <https://portal.azure.com>.
2.  Færið inn heiti og aðgangsorð fyrir notandi með aðgang að Azure-áskrift.
3.  Í vinstra yfirlitssvæðinu í Azure Portal smellirðu á **Azure Active Directory**.

    [![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)

4.  Tryggðu að Active Directory tilvikið sé það sem er notað af Supply Chain Management.
5.  Smelltu á **forritsskráningar** í listanum. 

    [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)

6.  Í efsta glugganum skaltu smella á **Nýja skráningu**. Leiðsagnarforritið **Skrá forrit** er ræst.
7.  Sláðu inn heiti fyrir forritið og veldu **Reikningar í þessari skipulagsskrá eingöngu**. Smelltu á **Skráning**.  

    [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)

8.  Nýja forritaskráning þín opnast. 

    [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)

9.  Mundu **kenni forrits**, þú munt þurfa á því að halda síðar. **Kenni forritsins** verður síðar vísað til sem **kenni biðlara**.
10. Smelltu á **Vottorð og leyndarmál** í glugganum **Stjórna**. Smelltu á **Nýtt leyndarmál biðlara**. 

    [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

11. Stofnaðu lykil með því að slá inn lyklalýsingu og lengd í **lykilorða** hlutanum. Smelltu á **Bæta við** og afritaðu lykilinn. Seinna verður vísað til þessa lykils sem **Leynilikill biðlara**. 

    [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Stofnaðu og skilgreindu notandareikning í Supply Chain Management
Til að virkja Supply Chain Management til að nota Azure AD forritið þitt þarf að ljúka eftirfarandi skilgreiningarskrefum:

1.  Stofnaðu notanda sem samsvarar notandaskilríkjum í vöruhússforriti.
    1.  Farðu í **Kerfisstjórnun** &gt; **Sameiginlegt** &gt; **Notendur**.
    2.  Stofnaðu nýjan notanda
    3.  Úthlutaðu notanda Vöruhús í fartæki, eins og sýnt er á eftirfarandi skjáskoti. 
    
        [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Tengdu Azure Active Directory forritið þitt við notanda vöruhússforrits fyrir fartæki.
    1.  Í Supply Chain Management skal opna **Kerfisstjórnun** &gt; **Uppsetning** &gt; **Azure Active Directory forrit**.
    2.  Stofnið nýja línu.
    3.  Færið inn **Biðlarakenni** (útvegað í síðasta hluti), gefðu því heiti og veldu notandann sem var búið að stofna. Við mælum með því að þú merkir öll tækin þín til að auðvelt sé að fjarlægja aðgang þeirra að Supply Chain Management af þessari síðu ef þau týnast. 
    
        [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Skilgreina forritið
Það verður að skilgreina forritið á tækinu til að tengjast þjóni Supply Chain Management gegnum Azure AD forritið. Það er gert með því að ljúka við eftirfarandi ferli:

1.  Í forritinu, opna **Tengingarstillingar**.
2.  Hreinsa svæðið **Sýnistilling**. <br>

    [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)

3.  Færi inn eftirfarandi upplýsingar: 
    + **Biðlarakenni Azure Active-skráasafns** - Biðlarakennið er fengið í skrefi 9 „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + **Leyndarmál biðlara Azure Active-skráasafns** - Leyndarmál biðlara er fengið í skrefi 11 í „Stofnaðu vefþjónustuforrit í Active Directory“. 
    + - **Azure Active directory tilföng** - Azure AD skráasafnstilföng tilgreina vefslóð fyrir Supply Chain Management. 
    
        > [!NOTE]
        > Látið þennan reit ekki enda á framvísandi skástriki (/). 

    + **Azure Active directory leigjandi** - Azure AD skráasafnsleigjandi sem er notaður með Supply Chain Management þjóni: `https://login.windows.net/your-AD-tenant-ID`. Til dæmis: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    
        > [!NOTE]
        > Látið þennan reit ekki enda á framvísandi skástriki (/). 
    
    + **Fyrirtæki** - Færðu inn þann lögaðila í Supply Chain Management sem þú vilt að tengist forritinu. <br>
    
    [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)

4.  Veldu hnappinn **Til baka** í efra vinstra horni forritsins Þá tengist forritið þínum Supply Chain Management þjóni og innskráningarskjár fyrir starfsmenn í vöruhúsi birtist.

    [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Upplýsingar um hvernig eigi að setja upp vöruhúsaforrit til að skanna strikamerki með myndavél á fartæki er að finna í [Skanna strikamerki með myndavél í Dynamics 365 for Finance and Operations – forritið Warehousing](scan-bar-codes-using-a-camera.md).

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki
Ef tæki týnist eða öryggi þess er ógnað verður þú að fjarlægja aðgang að Supply Chain Management fyrir það tæki. Eftirfarandi skref lýsa ráðlögðu ferli við að fjarlægja aðgangur.

1.  Farðu í **Kerfisstjórnun** &gt; **Uppsetning** &gt; **Azure Active Directory forrit**.
2.  Eyddu línunni sem samsvarar tækinu sem á að fjarlægja aðgang úr. Mundu **biðlararkennið** sem er notað fyrir fjarlægða tækið, þú þarft það síðar.
3.  Skráðu þig inn á Azure-gáttina á <https://portal.azure.com>.
4.  Smelltu á **Active Directory** táknið á vinstri valmyndinni og vertu viss um að þú sért í réttu skráasafni.
5.  Í listanum smelltu á **forritsskráningar** og smelltu síðan á forritið sem þú vilt skilgreina. **Stillingar** síðan birtist með grunnstillingarupplýsingum.
6.  Vertu viss um að **biðlarakenni** forritsins sé það sama og í skrefi 2 í þessum kafla.
7.  Smelltu á hnappinn **Eyða** efst í glugganum.
8.  Í staðfestingarglugganum smellirðu á **Já**.
