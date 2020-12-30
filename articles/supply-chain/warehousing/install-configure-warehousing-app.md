---
title: Setja upp og tengja vöruhúsaforrit
description: Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit á fartækjum og grunnstilla það til að tengja það við Microsoft Dynamics 365 Supply Chain Management-umhverfið. Hægt er að grunnstilla hvert tæki handvirkt eða flytja inn tengingarstillingar í gegnum skrá eða með því að skanna QR-kóða.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/25/2020
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
ms.openlocfilehash: 88bce09a6d3bf154592955a6fb2dada6247f1993
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430549"
---
# <a name="install-and-connect-the-warehouse-app"></a>Setja upp og tengja vöruhúsaforrit

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Þetta efnisatriði lýsir því hvernig eigi að grunnstilla vörugeymslur fyrir virkjun skýs. Ef þú ert að leita að því hvernig eigi að grunnstilla vöruhús fyrir virkjun á staðnum skaltu skoða [Vöruhús fyrir virkjun á staðnum](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Vöruhúsaforritið er í boði í Google Play Store og Microsoft Store. Það er gefið út sem sjálfstæður hluti. Þess vegna þarf að sækja það í hvert tæki og stilla það svo á tengingu við Microsoft Dynamics 365 Supply Chain Management -umhverfið.

Þetta efnisatriði útskýrir hvernig á að setja upp vöruhúsaforrit á fartækjum og grunnstilla það til að tengja það við stjórnunarumhverfi Supply Chain Management. Hægt er að grunnstilla hvert tæki handvirkt eða flytja inn tengingarstillingar í gegnum skrá eða með því að skanna QR-kóða.

## <a name="system-requirements"></a>Kerfiskröfur

Vöruhúsaforritið er í boði fyrir bæði Windows- og Android-stýrikerfi. Til að nota nýjustu útgáfu forritsins þarf eitt af eftirfarandi stýrikerfum að vera uppsett á fartækjum notanda:

- Windows 10 (Universal Windows Platform \[UWP\]) haustuppfærsla 1709 (smíði 10.0.16299) eða nýrri
- Android 4.4 eða nýrra

> [!NOTE]
> Ef styðja þarf við eldri Windows-tæki sem ekki geta keyrt nýjustu útgáfu af Windows er enn hægt að sækja útgáfu 1.6.3.0 af vöruhúsaforritinu úr Microsoft Store. Sú útgáfa mun keyra á Windows 10 (UWP) nóvemberuppfærslu 1511 (smíði 10.0.10586) eða nýrri. Hins vegar skal hafa í huga að þessi útgáfa vöruhúsaforritsins styður ekki fjöldauppsetningu tengingarstillinga. Þess vegna þarf að [skilgreina tenginguna handvirkt](#config-manually) í hverju tæki sem keyrir þessa útgáfu forritsins.

## <a name="get-the-warehouse-app"></a>Sækja vöruhúsaforrit

Notaðu einn eftirfarandi tengla til að sækja forritið:

- **Windows (UWP):** [Dynamics 365 for Finance and Operations - Vöruhúsakerfi á Microsoft Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Warehousing - Dynamics 365 á Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Fyrir smærri uppsetningar er hægt að setja upp forritið úr viðkomandi verslun á hverju tæki og grunnstilla tenginguna sjálfkrafa í því umhverfi sem notað er. Í útgáfu 1.7.0.0 og nýrri útgáfum vöruhúsaforritsins er hins vegar hægt að gera uppsetningu og/eða grunnstillingu forrits sjálfvirka. Hugsanlega er þessi nálgun þægilegri ef verið er að vinna með mörg tæki og verið er að nota fartækjastjórnunar- og farsímaforritastjórnunarlausnir á borð við [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune). Upplýsingar um hvernig á að nota Intune til að bæta við forritum eru í [Bæta forritum við Microsoft Intune](https://docs.microsoft.com/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Búa til vefþjónustuforrit í Azure Active Directory

Til að virkja vöruhúsaforritið til að eiga samskipti við tiltekin þjón Supply Chain Management þarf að skrá vefþjónustuforrit fyrir aðfangakeðjustjórnun í Azure Active Directory (Azure AD). Eftirfarandi ferli sýnir eina leið til að ljúka þessu verki. Ítarlegar upplýsingar og aðra valkosti er að finna í tenglum eftir ferlið.

1. Opnaðu vafra og farðu á [https://portal.azure.com](https://portal.azure.com/).
1. Færið inn heiti og aðgangsorð notanda með aðgang að Azure-áskrift.
1. Í Azure-gáttinni, á vinstra yfirlitssvæðinu, skal velja **Azure Active Directory**.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Ganga skal úr skugga um að unnið sé með tilvik Azure AD sem eru notuð af Supply Chain Management.
1. Á listanum **Stjórna** skal velja **Forritsskráningar**.

    ![Skráning forrits](media/app-connect-azure-register.png "Skráning forrits")

1. Á tækjastikunni skal velja **Ný skráning** til að opna leiðsögnina **Skrá forrit**.
1. Slá skal inn heiti fyrir forritið, velja **Aðeins lyklar í skráasafni þessa fyrirtækis** og síðan velja **Skrá**.

    ![Skrá leiðsagnarforritið](media/app-connect-azure-register-wizard.png "Skrá leiðsagnarforrit")

1. Nýja forritaskráningin er opnuð. Munið gildi **Kenni forrits (biðlari)** því það þarf að nota það síðar. Þetta auðkenni verður nefnt síðar í þessu efnisatriði sem *biðlarakennið*.

    ![Kenni forrits (biðlari)](media/app-connect-azure-app-id.png "Kenni forrits (biðlari)")

1. Á listanum **Stjórna** skal velja **Vottorð og leyniorð**. Næst skal velja einn af eftirfarandi hnöppum, allt eftir því hvernig á að grunnstilla forritið fyrir sannvottun. (Frekari upplýsingar er að finna í hlutanum [Sannvotta með vottorði eða leyniorði biðlara](#authenticate) síðar í þessu efnisatriði.)

    - **Hlaða upp vottorði** – Hlaða upp vottorði til að nota sem leyniorð. Við mælum með þessari nálgun vegna þess að hún er öruggari og getur einnig verið sjálfvirk að fullu. Ef verið er að nota vöruhúsaforritið á Windows-tækjum skal skrá niður gildið **Fingrafar** sem er sýnt eftir að búið er að hlaða upp vottorðinu. Þú þarft þetta gildi þegar þú grunnstillir vottorð í Windows-tækjum.
    - **Nýtt leyniorð biðlara** – Stofnið lykil með því að slá inn lyklalýsingu og lengd í hlutanum **Aðgangsorð** og veljið **Bæta við**. Taktu afrit af lyklinum og geymdu það á öruggum stað.

    ![Vottorð og leyniorð](media/app-connect-azure-authentication.png "Vottorð og leyniorð")

Frekari upplýsingar um hvernig vefþjónustuforrit eru sett upp eru í Azure AD, sjá eftirfarandi tilföng:

- Leiðbeiningar um nota má Windows PowerShell til að setja upp vefþjónustuforrit í Azure AD er að finna í [hvernig á að nota: Azure PowerShell til að stofna þjónustueiningu með vottorði](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Tæmandi upplýsingar um hvernig á að stofna vefþjónustuforrit handvirkt í Azure AD er að finna í eftirfarandi efnisatriðum:

    - [Stuttar leiðbeiningar: Skráið forrit með auðkenningarverkvangi Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Hvernig á að: Nota gáttina til að stofna Azure AD-forrit og þjónustueiningu með aðgang að tilföngum](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Stofnaðu og skilgreindu notandareikning í Supply Chain Management

Til að virkja Supply Chain Management til að nota Azure AD-forritið skal fylgja þessum skrefum.

1. Stofnið notanda sem samsvarar notandaskilríkjum í vöruhúsaforriti:

    1. Í Supply Chain Management skal fara á **Kerfisstjórnun \> notendur \> notendur**.
    1. Stofna notanda.
    1. Úthluta fartækjanotanda í vöruhúsi.

    ![Úthluta fartækjanotanda í vöruhúsi](media/app-connect-app-users.png "Úthluta fartækjanotanda í vöruhúsi")

1. Tengdu Azure AD forritið þitt við notanda vöruhúsaforrits fyrir fartæki:

    1. Opnið **Kerfisstjórnun \> Uppsetning \> Azure Active Directory forrita**.
    1. Stofna línu.
    1. Færa skal inn biðlarakennið sem skráð var niður í hlutanum á undan, gefa því heiti og velja notandann sem var stofnaður. Við mælum með því að öll tækin þín séu merkt. Ef þau glatast er auðvelt að fjarlægja aðgang þeirra að Supply Chain Management á þessari síðu.

    ![Azure Active Directory-forrit](media/app-connect-aad-apps.png "Forrit Azure Active Directory")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Sannvotta með því að nota vottorð eða leyniorð biðlara

Sannvottun með Azure AD býður upp á örugga leið til að tengja fartæki við Supply Chain Management. Hægt er að sannvotta með því að nota annaðhvort leyniorð biðlara eða vottorð. Ef fluttar eru inn tengingarstillingar mælum við með að notað sé vottorð í stað leyniorðs biðlara. Þar sem vista þarf leyniorð biðlara á öruggan máta er ekki hægt að flytja það inn úr tengistillingaskrá eða QR-kóða eins og lýst er síðar í þessu efnisatriði.

Hægt er að nota vottorð sem leyniorð til að sanna auðkenni forrits þegar beðið er um tákn. Almennum hluta vottorðsins er hlaðið upp í forritaskráninguna í Azure-gáttinni en setja verður fullt vottorð upp á öllum tækjum sem eru með vöruhúsaforritið uppsett. Fyrirtækið er ábyrgt fyrir því að hafa umsjón með vottorðinu hvað varðar skipti og þess háttar. Hægt er að nota sjálfskráð vottorð en alltaf ætti að nota óframseljanleg vottorð.

Nauðsynlegt er að gera vottorð aðgengilegt staðbundið á hverju tæki sem keyrir vöruhúsaforritið. Upplýsingar um hvernig á að stjórna vottorðum fyrir Intune-stýrð tæki, ef verið er að nota Intune, eru í [Nota vottorð fyrir sannvottun í Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Grunnstilla forritið með því að flytja inn tengingarstillingar

Til að auðvelda viðhald og uppsetningu á forritinu í mörgum fartækjum er hægt að flytja inn tengistillingar í stað þess að færa þær handvirkt inn í hvert tæki. Þessi hluti útskýrir hvernig á að búa til og flytja inn stillingarnar.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Stofna tengingarstillingaskrá eða QR-kóða

Hægt er að flytja inn tengingarstillingar annaðhvort úr skrá eða QR-kóða. Fyrst þarf að búa til stillingaskrá sem notar JavaScript Object Notation (JSON) sniðmát og setningaskipan. Skráin verður að innihalda tengilista sem inniheldur einstakar tengingar sem bæta þarf við. Eftirfarandi tafla inniheldur samantekt á færibreytum sem þarf að tilgreina í skránni fyrir tengingarstillingar.

| Færibreyta | lýsing |
| --- | --- |
| ConnectionName | Tilgreindu heiti tengistillinga. Hámarkslengd er 20 stafir. Vegna þess að þetta gildi er einkvæmt kennimerki fyrir tengistillingu skal ganga úr skugga um að það sé einkvæmt á listanum. Ef tenging sem er með sama heiti er þegar til í tækinu verður henni hnekkt af stillingunum úr innfluttu skránni. |
| ActiveDirectoryClientAppId | Tilgreinið auðkenni biðlarans sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Tilgreina rótarvefslóð fyrir Supply Chain Management. |
| ActiveDirectoryTenant | Tilgreinið Azure AD leigjanda sem á að nota með net fyrir Supply Chain Management. Gildið er á sniðinu `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Eftirfarandi er dæmi: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
| Fyrirt.   | Tilgreinið lögaðilann í Supply Chain Management sem forritið á að tengjast við. |
| ConnectionType | (Valfrjálst) Tilgreinið hvort tengistillingin eigi að nota vottorð eða leyniorð biðlara til að tengjast umhverfi. Gild gildi eru *"certificate"* og *"clientsecret"*. Sjálfgefið gildi er *"certificate"*.<p>**Athugið:** ekki er hægt að flytja inn leyniorð biðlara.</p> |
| IsEditable | (Valfrjálst) Tilgreinið hvort forritsnotandinn eigi að geta breytt tengistillingunni. Gild gildi eru *„rétt“* og *„rangt“*. Sjálfgefið gildi er *„rétt“*. |
| IsDefault | (Valfrjálst) Tilgreinið hvort tengingin er sjálfgefin tenging. Tenging sem er stillt sem sjálfgefin tenging verður sjálfkrafa forvalin þegar forritið er opnað. Aðeins er hægt að velja eina tengingu sem sjálfgefna tengingu. Gild gildi eru *„rétt“* og *„rangt“*. Sjálfgefið gildi er *„rangt“*. |
| CertificateThumbprint | (Valfrjálst) Í Windows-tækjum er hægt að tilgreina fingrafar vottorðs fyrir tenginguna. Í Android tækjum þarf forritsnotandi að velja vottorð í fyrsta skipti sem tenging er notuð. |

Eftirfarandi dæmi sýnir gilda stillingaskrá tengingar sem inniheldur tvær tengingar. Eins og hægt er að sjá er tengingarlisti (sem nefnist *„ConnectionList"* í skránni) hlutur sem er með fylki sem vistar hverja tengingu sem hlut. Hver hlutur verður að vera innan hornklofa ({}) og aðskilin með kommu, og fylkið verður að vera innan sviga (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Annaðhvort er hægt að vista upplýsingarnar sem JSON-skrá eða mynda QR-kóða sem er með sama efni. Ef upplýsingarnar eru vistaðar sem skrá er mælt með því að vista þær með sjálfgefna heitinu, *connections.json*, sérstaklega ef hún er vistuð á sjálfgefinni staðsetningu í öllum fartækjum.

### <a name="save-the-connection-settings-file-on-each-device"></a>Vista tengingarstillingaskrá í öllum tækjum

Algengast er að nota verkfæri eða forskrift fyrir tækjastjórnun til að senda tengingarstillingarskrár í öll tæki sem verið er að stjórna. Ef sjálfgefið heiti og staðsetning eru notuð þegar tengingarstillingaskrá er vistuð á hvert tæki flytur vöruhúsaforritið hana sjálfkrafa inn, jafnvel við fyrstu keyrslu eftir að forritið hefur verið sett upp. Ef sérsniðið heiti eða staðsetning er notuð fyrir skrána verður notandi forritsins að tilgreina gildin í fyrstu keyrslu. Forritið mun hins vegar halda áfram að nota tilgreint heiti og staðsetningu eftir það.

Í hvert sinn sem forritið er ræst mun það flytja tengingarstillingarnar frá fyrri staðsetningu inn aftur til að ákvarða hvort einhverjar breytingar hafa verið gerðar. Forritið uppfærir aðeins tengingar sem hafa sama heiti og tengingarnar í skránni fyrir tengingarstillingar. Tengingar sem notandi hefur búið til sem nota önnur heiti verða ekki uppfærðar.

Ekki er hægt að fjarlægja tengingu með því að nota stillingaskrá tengingar.

Sjálfgefið skráarnafn er *connections.json*. Sjálfgefin skráarstaðsetning veltur á því hvort verið er að nota Windows-tæki eða Android tæki:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Yfirleitt eru slóðir sjálfkrafa búnar til eftir fyrstu keyrslu forritsins. Hins vegar er hægt að stofna þær handvirkt ef flytja þarf skrá tengingarstillinga í tækið fyrir uppsetningu.

> [!NOTE]
> Ef forritið er fjarlægt er sjálfgefna slóðin og efni hennar fjarlægð.

### <a name="import-the-connection-settings"></a>Flytja inn tengistillingarnar

Fylgið eftirfarandi skrefum til að flytja inn tengingarstillingar úr skrá eða QR-kóða.

1. Opnið vöruhúsaforritið á fartækinu.
1. Farðu í **Stillingar tengingar**.
1. Stillið **Nota sýnisstillingu** valkostinn á _Nei_.

    ![Nota valkost sýnistillingu](media/app-connect-app-demo-mode.png "Nota valkost sýnikennslu")

1. Veljið **Velja skrá** eða **Skanna QR-kóða**, allt eftir því hvernig á að flytja inn stillingar:

    - Ef verið er að flytja inn tengingarstillingar úr skrá kann forritið þegar að hafa fundið skrána ef sjálfgefna heitið og sjálfgefna staðsetningin voru notuð þegar hún var vistuð. Annars skal velja **Velja skrá**, fletta á skrána í staðbundna tækinu og velja hana. Ef valin staðsetning er sérsniðin mun forritið geyma hana og nota sjálfkrafa næst.
    - Ef verið er að flytja inn tengingarstillingarnar með því að skanna QR-kóða skal velja **Skanna QR-kóða**. Forritið biður um heimild til að nota myndavél tækisins. Þegar heimild hefur verið veitt er myndavélin ræst þannig að hægt er að nota hana fyrir skönnun. Erfitt getur reynst að ná réttri skönnun en það veltur á gæðum myndavélar tækisins og því hversu flókinn QR-kóðinn er. Í því tilviki þarf að reyna að minnka flækjustig QR-kóðans með því að mynda aðeins eina tengingu á hvern QR-kóða. (Eins og er er aðeins hægt að nota myndavél tækisins til að skanna QR-kóðann.)

    ![Flytja inn tengistillingar](media/app-connect-app-select-file.png "Flytja inn tengistillingar")

1. Þegar tengistillingar hafa verið sóttar er hnappurinn **Til baka** (vinstri ör) valinn í efst til vinstri á síðunni.

    ![Tengistillingum hlaðið](media/app-connect-app-settings-loaded.png "Tengistillingum hlaðið")

1. Ef þú ert að nota Android tæki og notar vottorð fyrir sannvottun birður tækið þig um að velja vottorðið.

    ![Veljið vottorðskvaðningu á Android-tæki](media/app-connect-app-choose-cert.png "Veljið vottorðskvaðningu á Android tæki")

1. Forritið tengist þjóni Supply Chain Management og sýnir innskráningarsíðuna.

    ![Innskráningarsíða](media/app-connect-sign-in.png "Innskráningarsíða")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Skilgreina forritið handvirkt

Hægt er að skilgreina forritið handvirkt í tækinu þannig að það tengist þjóni Supply Chain Management í gegnum Azure AD-forritið.

1. Opnið vöruhúsaforritið á fartækinu.
1. Farðu í **Stillingar tengingar**.
1. Stillið **Nota sýnisstillingu** valkostinn á _Nei_.

    ![Slökkt á sýnistillingu](media/app-connect-app-select-file.png "Slökkt á sýnistillingu")

1. Snertið reitinn **Velja tengingu** til að stækka stillingarnar sem eru nauðsynlegar til að færa handvirkt inn upplýsingar um tenginguna.

    ![Handvirk tengisvæði](media/app-connect-manual-connect.png "Handvirkir tengireitir")

1. Færi inn eftirfarandi upplýsingar:

    - **Nota leyniorð biðlara** – Stillið þennan valkost á _Já_ til að nota leyniorð biðlara til að sannvotta með Supply Chain Management. Stillið hann á _Nei_ til að nota vottorð fyrir sannvottun. (Frekari upplýsingar er að finna í [Búa til vefþjónustuforrit í Azure Active Directory](#create-service).)
    - **Heiti tengingar** – Sláðu inn heiti fyrir nýja tengingu. Þetta heiti birtist í reitnum **Velja tengingu** næst þegar tengingarstillingar eru opnaðar. Heitið sem fært er inn verður að vera einkvæmt. (Með öðrum orðum, það verður að vera frábrugðið öllum öðrum tengingarheitum sem eru geymd í tækinu, ef önnur tengingarheiti eru geymd þar.)
    - **Biðlarakenni Active Directory** – Færið inn auðkenni biðlarans sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Leyniorð biðlara Active Directory** – Þessi reitur er aðeins í boði þegar valkosturinn **Nota leyniorð biðlara** er stilltur á _Já_. Færið inn leyniorð biðlara sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Fingrafar Active Directory-vottorðs** – Þessi reitur er aðeins í boði fyrir Windows-tæki þegar valkosturinn **Nota leyniorð biðlara** er stilltur á _Nei_. Sláið inn fingrafar vottorðsins sem þú skráðir þegar þú varst að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Tilfang Active Directory** – Tilgreina rótarvefslóð fyrir Supply Chain Management.

        > [!NOTE]
        > Ekki enda þetta gildi á skástriki (/).

    - **Active Directory leigjanda** – Færið inn þann Azure AD leigjanda sem á að nota með netþjóni Supply Chain Management. Gildið er á sniðinu `https://login.windows.net/<your-Azure-AD-tenant-ID>`. Eftirfarandi er dæmi: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Ekki enda þetta gildi á skástriki (/).

    - **Fyrirtæki** - Færðu inn lögaðila í Supply Chain Management sem forritið á að tengjast við.

1. Velja skal hnappinn **Vista** efst í hægra horninu á síðunni.
1. Ef þú ert að nota Android tæki og notar vottorð fyrir sannvottun birður tækið þig um að velja vottorðið.
1. Forritið tengist þjóni Supply Chain Management og sýnir innskráningarsíðuna.

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki

Ef tæki týnist eða öryggi þess er ógnað verður þú að fjarlægja aðgang að Supply Chain Management fyrir það tæki. Eftirfarandi skref lýsa ráðlögðu ferli við að til að fjarlægja aðgang.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Azure Active Directory forrita**.
1. Eyddu línunni sem samsvarar tækinu sem á að fjarlægja aðgang fyrir. Mundu biðlararkennið sem er notað fyrir fjarlægða tækið þar sem þú þarft það síðar.

    Ef aðeins eitt biðlarakenni hefur verið skráð og mörg tæki nota sama biðlarakenni þarf að senda út nýjar tengistillingar í þessi tæki. Annars glata þær aðgangi.

1. Skráðu þig inn á Azure-gáttina á [https://portal.azure.com](https://portal.azure.com/).
1. Í hægra yfirlitssvæðinu skal velja **Active Directory** og ganga skal úr skugga um rétt skráasafn sé notað.
1. Á listanum **Stjórna** skal velja **Forritaskráningar** og svo forritið til að grunnstilla. Síðan **Stillingar** birtist og sýnir grunnstillingarupplýsingar.
1. Ganga skal úr skugga um að biðlarakenni forritsins passi við biðlarakenni í skrefi 2.
1. Á tækjastikunni skal velja **Eyða**.
1. Í staðfestingarskilaboðum sem birtist velurðu **Já**.
