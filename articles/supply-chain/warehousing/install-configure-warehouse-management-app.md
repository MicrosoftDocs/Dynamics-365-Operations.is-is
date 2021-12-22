---
title: Setja upp og tengja farsímaforrit vöruhúsakerfis
description: Þetta efnisatriði útskýrir hvernig á að setja upp farsímaforrit Vöruhúsakerfa á fartækjum og grunnstilla það til að tengja það við Microsoft Dynamics 365 Supply Chain Management-umhverfið.
author: Mirzaab
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b1687b24f499f4d226406a0035f8ea70b6046167
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901990"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Setja upp og tengja farsímaforrit vöruhúsakerfis

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Þetta efnisatriði lýsir því hvernig á að skilgreina nýja farsímaforrit vöruhúsakerfisins. Ef leitað er upplýsinga um hvernig eigi að skilgreina gamla vöruhúsaforritið (nú úrelt) skal skoða [Setja upp og tengja vöruhúsaforrit](../../supply-chain/warehousing/install-configure-warehousing-app.md).

Þetta efnisatriði útskýrir hvernig á að sækja og setja upp farsímaforrit Vöruhúsakerfis og grunnstilla forritið til að tengja það við stjórnunarumhverfi Supply Chain Management. Hægt er að grunnstilla hvert tæki handvirkt eða flytja inn tengingarstillingar í gegnum skrá eða með því að skanna QR-kóða.

## <a name="system-requirements"></a>Kerfiskröfur

Farsímaforrit vöruhúsakerfisins er í boði fyrir bæði stýrikerfi Windows og Google Android. Til að nota forritið þarf eitt af eftirfarandi stýrikerfum að vera uppsett í fartækjunum:

- Windows 10 (Universal Windows Platform \[UWP\]) október 2018 uppfærsla 1809 (smíði 10.0.17763) eða nýrri
- Android 4.4 eða nýrra

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Áður en hægt er að nota forritið verður að vera kveikt á eiginleikanum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið*

## <a name="get-the-warehouse-management-mobile-app"></a>Sækja farsímaforrit vöruhúsakerfis

Fyrir smærri uppsetningar er yfirleitt sett upp forritið á hverju tæki úr viðkomandi verslun á hverju tæki og grunnstilla tenginguna sjálfkrafa í því umhverfi sem notað er.

Fyrir stærri uppsetningar er hægt að gera uppsetningu og/eða grunnstillingu forrits sjálfvirka, sem getur reynst hentugara ef verið er að stýra mörgum tækjum. Til dæmis gætu verið notaðar fartækjastjórnunar- og farsímaforritastjórnunarlausnir á borð við [Microsoft Intune](/mem/intune/fundamentals/what-is-intune). Upplýsingar um hvernig á að nota Intune til að bæta við forritum eru í [Bæta forritum við Microsoft Intune](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Setja upp forritið úr forritsverslun

Auðveldasta leiðin til að setja upp forritið á einu tæki er að setja það upp úr forritsverslun sem býður alltaf upp á nýjustu útgáfu sem er í boði. Microsoft Intune getur einnig sótt forrit úr forritaverslunum. Notaðu einn eftirfarandi tengla til að sækja forritið úr forritaversluninni og setja það upp:

- **Windows (UWP):** [Vöruhúsakerfi í Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Vöruhúsakerfi á Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Sækja forritið úr forritamiðstöð Microsoft

Í stað þess að setja upp í gegnum forritaverslun er hægt að sækja forritið frá forritamiðstöð Microsoft. Forritamiðstöðin býður upp á uppsetningarpakka sem hægt er að hlaða milli tækja. Til viðbótar við núverandi útgáfu gerir forritamiðstöðin einnig kleift að sækja eldri útgáfur og gæti boðið upp á forútgáfur af væntanlegum eiginleikum sem hægt er að prófa. Til að sækja núverandi eða eldri útgáfu eða forútgáfur af fartækjaforriti vöruhúsakerfisins úr forritamiðstöð Microsoft skal nota einn af eftirfarandi tenglum:

- **Windows (UWP):** [Vöruhúsakerfi (Windows)](https://go.microsoft.com/fwlink/?linkid=2154406)  
    Leiðbeiningar um hvernig á að setja upp sóttan pakka í Windows-tæki og síðan setja upp áskilin leyfi er að finna í [Setja upp smíð frá forritastöð](/appcenter/distribution/installation).

- **Android:** [Vöruhúsakerfi (Android)](https://go.microsoft.com/fwlink/?linkid=2154613)  
    Ef forútgáfa forritsins er sótt þarf að fara í gegnum nokkur aukaskref til að setja það upp. Frekari upplýsingar er að finna í [Prófun Android-forrita](/appcenter/distribution/testers/testing-android).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Búa til vefþjónustuforrit í Azure Active Directory

Til að virkja farsímaforrit Vöruhúsakerfis til að eiga samskipti við tiltekin þjón Supply Chain Management þarf að skrá vefþjónustuforrit fyrir aðfangakeðjustjórnun í Azure Active Directory (Azure AD). Eftirfarandi ferli sýnir eina leið til að ljúka þessu verki. Ítarlegar upplýsingar og aðra valkosti er að finna í tenglum eftir ferlið.

1. Opnaðu vafra og farðu á [https://portal.azure.com](https://portal.azure.com/).
1. Færið inn heiti og aðgangsorð notanda með aðgang að Azure-áskrift.
1. Í Azure-gáttinni, á vinstra yfirlitssvæðinu, skal velja **Azure Active Directory**.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Ganga skal úr skugga um að unnið sé með tilvik Azure AD sem eru notuð af Supply Chain Management.
1. Á listanum **Stjórna** skal velja **Forritsskráningar**.

    ![Skráning forrits.](media/app-connect-azure-register.png "Skráning forrits")

1. Á tækjastikunni skal velja **Ný skráning** til að opna leiðsögnina **Skrá forrit**.
1. Slá skal inn heiti fyrir forritið, velja **Aðeins lyklar í skráasafni þessa fyrirtækis** og síðan velja **Skrá**.

    ![Skrá leiðsagnarforrit.](media/app-connect-azure-register-wizard.png "Skrá leiðsagnarforrit")

1. Nýja forritaskráningin er opnuð. Munið gildi **Kenni forrits (biðlari)** því það þarf að nota það síðar. Þetta auðkenni verður nefnt síðar í þessu efnisatriði sem *biðlarakennið*.

    ![Kenni forrits (biðlara).](media/app-connect-azure-app-id.png "Kenni forrits (biðlari)")

1. Á listanum **Stjórna** skal velja **Vottorð og leyniorð**. Næst skal velja einn af eftirfarandi hnöppum, allt eftir því hvernig á að grunnstilla forritið fyrir sannvottun. (Frekari upplýsingar er að finna í hlutanum [Sannvotta með vottorði eða leyniorði biðlara](#authenticate) síðar í þessu efnisatriði.)

    - **Hlaða upp vottorði** – Hlaða upp vottorði til að nota sem leyniorð. Við mælum með þessari nálgun vegna þess að hún er öruggari og getur einnig verið sjálfvirk að fullu. Ef verið er að nota farsímaforrit Vöruhúsakerfis á Windows-tækjum skal skrá niður gildið **Fingrafar** sem er sýnt eftir að búið er að hlaða upp vottorðinu. Þú þarft þetta gildi þegar þú grunnstillir vottorð í Windows-tækjum.
    - **Nýtt leyniorð biðlara** – Stofnið lykil með því að slá inn lyklalýsingu og lengd í hlutanum **Aðgangsorð** og veljið **Bæta við**. Taktu afrit af lyklinum og geymdu það á öruggum stað.

    ![Vottorð og leyniorð.](media/app-connect-azure-authentication.png "Vottorð og leyniorð")

Frekari upplýsingar um hvernig vefþjónustuforrit eru sett upp eru í Azure AD, sjá eftirfarandi tilföng:

- Leiðbeiningar um nota má Windows PowerShell til að setja upp vefþjónustuforrit í Azure AD er að finna í [hvernig á að nota: Azure PowerShell til að stofna þjónustueiningu með vottorði](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Tæmandi upplýsingar um hvernig á að stofna vefþjónustuforrit handvirkt í Azure AD er að finna í eftirfarandi efnisatriðum:

    - [Stuttar leiðbeiningar: Skráið forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app)
    - [Hvernig á að: Nota gáttina til að stofna Azure AD-forrit og þjónustueiningu með aðgang að tilföngum](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Stofnaðu og skilgreindu notandareikning í Supply Chain Management

Til að virkja Supply Chain Management til að nota Azure AD-forritið skal fylgja þessum skrefum.

1. Stofnið notanda sem samsvarar notandaskilríkjum í farsímaforrit Vöruhúsakerfis:

    1. Í Supply Chain Management skal fara á **Kerfisstjórnun \> notendur \> notendur**.
    1. Stofna notanda.
    1. Úthlutaðu notandanum hlutverkinu *Fartækjanotandi í vöruhúsi*.

    ![Úthluta fartækjanotanda í vöruhúsi.](media/app-connect-app-users.png "Úthluta fartækjanotanda í vöruhúsi")

1. Tengið Azure AD-forritið við notanda farsímaforrits vöruhúsakerfis:

    1. Opnið **Kerfisstjórnun \> Uppsetning \> Azure Active Directory forrita**.
    1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.
    1. Í reitinn **Biðlarakenni** skal færa inn biðlarakennið sem þú skrifaðir niður í hlutanum hér á undan.
    1. Færið inn lýsandi nafn í reitinn **Heiti**.
    1. Í reitnum **Notandakenni** skal velja notandakennið sem var verið að búa til.

    ![Azure Active Directory-forrit.](media/app-connect-aad-apps.png "Forrit Azure Active Directory")

> [!TIP]
> Ein leið til að nota þessar stillingar er að búa til biðlarakenni í Azure fyrir sérhvert tæki og síðan bæta hverju biðlarakenni við síðuna **Azure Active Directory forrit**. Ef tæki týnist er lítið mál að fjarlægja aðgang þess að Supply Chain Management með því að fjarlægja biðlarakennið af síðunni. (Þessi aðferð virkar vegna þess að innskráningarupplýsingar tengingar sem eru vistaðar á hverju tæki tilgreina einnig biðlarakennið eins og lýst er síðar í þessum hluta.)
>
> Að auki eru stillingar fyrir sjálfgefið tungumál, númerasnið og tímabelti fyrir sérhvert biðlarakenni ákvarðaðar með þeim kjörstillingum sem eru stilltar fyrir gildi **Biðlarakennis** sem er varpað hér. Þess vegna getur þú notað þessar kjörstillingar til að setja upp sjálfgefnar stillingar fyrir hvert tæki eða safn tækja samkvæmt biðlarakenninu. Þessar sjálfgefnu stillingar verða hinsvegar hunsaðar ef þær eru einnig skilgreindar fyrir *notandareikning vöruhúsaforrit* sem starfskraftur notar til að skrá sig inn á tækið. (Frekari upplýsingar er að finna í [Notendareikningar fartækis](mobile-device-work-users.md).)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Sannvotta með því að nota vottorð eða leyniorð biðlara

Sannvottun með Azure AD býður upp á örugga leið til að tengja fartæki við Supply Chain Management. Hægt er að sannvotta með því að nota annaðhvort leyniorð biðlara eða vottorð. Ef fluttar eru inn tengingarstillingar mælum við með að notað sé vottorð í stað leyniorðs biðlara. Þar sem vista þarf leyniorð biðlara á öruggan máta er ekki hægt að flytja það inn úr tengistillingaskrá eða QR-kóða eins og lýst er síðar í þessu efnisatriði.

Hægt er að nota vottorð sem leyniorð til að sanna auðkenni forrits þegar beðið er um tákn. Almennum hluta vottorðsins er hlaðið upp í forritaskráninguna í Azure-gáttinni en setja verður fullt vottorð upp á öllum tækjum sem eru með farsímaforrit vöruhúsakerfis uppsett. Fyrirtækið er ábyrgt fyrir því að hafa umsjón með vottorðinu hvað varðar skipti og þess háttar. Hægt er að nota sjálfskráð vottorð en alltaf ætti að nota óframseljanleg vottorð.

Nauðsynlegt er að gera vottorð aðgengilegt staðbundið á hverju tæki sem keyrir farsímaforrit Vöruhúsakerfis. Upplýsingar um hvernig á að stjórna vottorðum fyrir Intune-stýrð tæki, ef verið er að nota Intune, eru í [Nota vottorð fyrir sannvottun í Microsoft Intune](/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Grunnstilla forritið með því að flytja inn tengingarstillingar

Til að auðvelda viðhald og uppsetningu á forritinu í mörgum fartækjum er hægt að flytja inn tengistillingar í stað þess að færa þær handvirkt inn í hvert tæki. Þessi hluti útskýrir hvernig á að búa til og flytja inn stillingarnar.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Stofna tengingarstillingaskrá eða QR-kóða

Hægt er að flytja inn tengingarstillingar annaðhvort úr skrá eða QR-kóða. Fyrst þarf að búa til stillingaskrá sem notar JavaScript Object Notation (JSON) sniðmát og setningaskipan. Skráin verður að innihalda tengilista sem inniheldur einstakar tengingar sem bæta þarf við. Eftirfarandi tafla inniheldur samantekt á færibreytum sem þarf að tilgreina í skránni fyrir tengingarstillingar.

| Færibreyta | lýsing |
|---|---|
| ConnectionName | Tilgreindu heiti tengistillinga. Hámarkslengd er 20 stafir. Vegna þess að þetta gildi er einkvæmt kennimerki fyrir tengistillingu skal ganga úr skugga um að það sé einkvæmt á listanum. Ef tenging sem er með sama heiti er þegar til í tækinu verður henni hnekkt af stillingunum úr innfluttu skránni. |
| ActiveDirectoryClientAppId | Tilgreinið auðkenni biðlarans sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service). |
| ActiveDirectoryResource | Tilgreina rótarvefslóð fyrir Supply Chain Management. |
| ActiveDirectoryTenant | Tilgreindu Azure AD lénsheiti sem á að nota með netþjón Supply Chain Management. Gildið er á sniðinu `https://login.windows.net/<your-Azure-AD-domain-name>`. Eftirfarandi er dæmi: `https://login.windows.net/contosooperations.onmicrosoft.com`. Frekari upplýsingar um hvernig á að finna Azure AD lénsheitið þitt eru í [Finna mikilvæg auðkenni fyrir notanda](/partner-center/find-ids-and-domain-names). |
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

Algengast er að nota verkfæri eða forskrift fyrir tækjastjórnun til að senda tengingarstillingarskrár í öll tæki sem verið er að stjórna. Ef sjálfgefið heiti og staðsetning eru notuð þegar tengingarstillingaskrá er vistuð á hvert tæki flytur farsímaforrit Vöruhúsakerfis hana sjálfkrafa inn, jafnvel við fyrstu keyrslu eftir að forritið hefur verið sett upp. Ef sérsniðið heiti eða staðsetning er notuð fyrir skrána verður notandi forritsins að tilgreina gildin í fyrstu keyrslu. Forritið mun hins vegar halda áfram að nota tilgreint heiti og staðsetningu eftir það.

Í hvert sinn sem forritið er ræst mun það flytja tengingarstillingarnar frá fyrri staðsetningu inn aftur til að ákvarða hvort einhverjar breytingar hafa verið gerðar. Forritið uppfærir aðeins tengingar sem hafa sama heiti og tengingarnar í skránni fyrir tengingarstillingar. Tengingar sem notandi hefur búið til sem nota önnur heiti verða ekki uppfærðar.

Ekki er hægt að fjarlægja tengingu með því að nota stillingaskrá tengingar.

Sjálfgefið skráarnafn er *connections.json*. Sjálfgefin skráarstaðsetning veltur á því hvort verið er að nota Windows-tæki eða Android tæki:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Yfirleitt eru slóðir sjálfkrafa búnar til eftir fyrstu keyrslu forritsins. Hins vegar er hægt að stofna þær handvirkt ef flytja þarf skrá tengingarstillinga í tækið fyrir uppsetningu.

> [!NOTE]
> Ef forritið er fjarlægt er sjálfgefna slóðin og efni hennar fjarlægð.

### <a name="import-the-connection-settings"></a>Flytja inn tengistillingarnar

Fylgið eftirfarandi skrefum til að flytja inn tengingarstillingar úr skrá eða QR-kóða.

1. Ræsið farsímaforrit vöruhúsakerfisins í fartækinu. Í fyrsta skipti sem forritið ræsist birtast opnunarskilaboð. Veljið **Velja tengingu**.

    ![Opnunarkveðja.](media/app-configure-welcome-screen.png "Opnunarkveðja")

1. Ef verið er að flytja inn tengistillingar úr skrá og sjálfgefið heiti og staðsetning var notuð þegar skráin var vistuð, þá kann að vera að forritið hafi þegar fundið skrána. Í þessu tilvikum skal fara næst í skref 4. Að öðrum kosti skal velja **Setja upp tengingu** og fara síðan í þriðja skref.

    ![Setja upp tengingu.](media/app-configure-set-up-connection.png "Setja upp tengingu")

1. Í svarglugganum **Uppsetning tengingar** skal velja **Bæta við úr skrá** eða **Bæta við úr QR-kóða**, allt eftir því hvernig á að flytja inn stillingarnar:

    - Ef verið er að flytja inn tengistillingarnar úr skrá skal velja **Bæta við úr skrá**, fletta skránni upp á staðbundnu tæki og velja hana. Ef valin staðsetning er sérsniðin mun forritið geyma hana og nota sjálfkrafa næst.
    - Ef verið er að flytja inn tengingarstillingarnar með því að skanna QR-kóða skal velja **Bæta við úr QR-kóða**. Forritið biður um heimild til að nota myndavél tækisins. Þegar heimild hefur verið veitt er myndavélin ræst þannig að hægt er að nota hana fyrir skönnun. Erfitt getur reynst að ná réttri skönnun en það veltur á gæðum myndavélar tækisins og því hversu flókinn QR-kóðinn er. Í því tilviki þarf að reyna að minnka flækjustig QR-kóðans með því að mynda aðeins eina tengingu á hvern QR-kóða. (Eins og er er aðeins hægt að nota myndavél tækisins til að skanna QR-kóðann.)

    ![Uppsetningarvalmynd tengingar.](media/app-configure-connection-setup-flyout.png "Uppsetningarvalmynd tengingar")

1. Þegar tengistillingar hafa verið hlaðnar er valin tenging sýnd.

    ![Tengistillingum hlaðið.](media/app-configure-select-connection.png "Tengistillingum hlaðið")

1. Ef þú ert að nota Android tæki og notar vottorð fyrir sannvottun birður tækið þig um að velja vottorðið.

    ![Velja vottorðskvaðningu á Android-tæki.](media/app-configure-select-certificate.png "Velja vottorðskvaðningu í Android-tæki")

1. Forritið tengist þjóni Supply Chain Management og sýnir innskráningarsíðuna.

    ![Innskráningarsíða.](media/app-configure-sign-in-page.png "Innskráningarsíða")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Skilgreina forritið handvirkt

Ef hvorki skrá né QR-kóði er til staðar er hægt að skilgreina forritið handvirkt í tækinu þannig að það tengist þjóni Supply Chain Management í gegnum Azure AD-forritið.

1. Ræsið farsímaforrit vöruhúsakerfisins í fartækinu.
1. Ef forritið er ræst í **Sýnistillingu** skal velja **Tengistillingar**. Ef síðan **Innskráning** birtist þegar forritið er ræst skal velja **Breyta tengingu**.
1. Veljið **Setja upp tengingu**.

    ![Setja upp tengingu.](media/app-configure-set-up-connection.png "Setja upp tengingu")

1. Veljið **Setja inn handvirkt**.

    ![Uppsetningarvalmynd tengingar.](media/app-configure-connection-setup-flyout.png "Uppsetningarvalmynd tengingar")

    Síðan **Ný tenging** birtist og sýnir stillingarnar sem þarf til að færa handvirkt inn tengiupplýsingarnar.

    ![Handvirk tengisvæði.](media/app-configure-input-manually.png "Handvirkir tengireitir")

1. Færi inn eftirfarandi upplýsingar:

    - **Nota leyniorð biðlara** – Stillið þennan valkost á _Já_ til að nota leyniorð biðlara til að sannvotta með Supply Chain Management. Stillið hann á _Nei_ til að nota vottorð fyrir sannvottun. (Frekari upplýsingar er að finna í hlutanum [Búa til vefþjónustuforrit í Azure Active Directory](#create-service) fyrr í þessu efnisatriði.)
    - **Heiti tengingar** – Sláðu inn heiti fyrir nýja tengingu. Þetta heiti birtist í reitnum **Velja tengingu** næst þegar tengingarstillingar eru opnaðar. Heitið sem fært er inn verður að vera einkvæmt. (Með öðrum orðum, það verður að vera frábrugðið öllum öðrum tengingarheitum sem eru geymd í tækinu, ef önnur tengingarheiti eru geymd þar.)
    - **Biðlarakenni Active Directory** – Færið inn auðkenni biðlarans sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Leyniorð biðlara Active Directory** – Þessi reitur er aðeins í boði þegar valkosturinn **Nota leyniorð biðlara** er stilltur á _Já_. Færið inn leyniorð biðlara sem skráð var þegar verið var að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Fingrafar Active Directory-vottorðs** – Þessi reitur er aðeins í boði fyrir Windows-tæki þegar valkosturinn **Nota leyniorð biðlara** er stilltur á _Nei_. Sláið inn fingrafar vottorðsins sem þú skráðir þegar þú varst að setja upp Azure AD í hlutanum [Stofna vefþjónustuforrit í Azure Active Directory](#create-service).
    - **Tilfang Active Directory** – Tilgreina rótarvefslóð fyrir Supply Chain Management.

        > [!IMPORTANT]
        > Ekki enda þetta gildi á skástriki (/).

    - **Active Directory leigjandi** – Færðu inn Azure AD lénsheitið sem á að nota með netþjóni Supply Chain Management. Gildið er á sniðinu `https://login.windows.net/<your-Azure-AD-domain-name>`. Eftirfarandi er dæmi: `https://login.windows.net/contosooperations.onmicrosoft.com`. Frekari upplýsingar um hvernig á að finna Azure AD lénsheitið þitt eru í [Finna mikilvæg auðkenni fyrir notanda](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Ekki enda þetta gildi á skástriki (/).

    - **Fyrirtæki** - Færðu inn lögaðila (fyrirtæki) í Supply Chain Management sem forritið á að tengjast við.

1. Velja skal hnappinn **Vista** efst í hægra horninu á síðunni.
1. Ef þú ert að nota Android tæki og notar vottorð fyrir sannvottun birður tækið þig um að velja vottorðið.
1. Forritið tengist þjóni Supply Chain Management og sýnir innskráningarsíðuna.

## <a name="remove-access-for-a-device"></a>Fjarlægja aðgang fyrir tæki

Ef tæki týnist eða hefur orðið fyrir árás þarf að fjarlægja aðgang þess að Supply Chain Management. Eftirfarandi skref lýsa ráðlögðu ferli við að til að fjarlægja aðgang.

1. Opnið **Kerfisstjórnun \> Uppsetning \> Azure Active Directory forrita**.
1. Eyddu línunni sem samsvarar tækinu sem á að fjarlægja aðgang fyrir. Mundu biðlararkennið sem er notað fyrir tækið þar sem þú þarft það síðar.

    Ef aðeins eitt biðlarakenni hefur verið skráð og mörg tæki nota sama biðlarakenni þarf að senda út nýjar tengistillingar í þessi tæki. Annars glata þær aðgangi.

1. Skráðu þig inn á Azure-gáttina á [https://portal.azure.com](https://portal.azure.com/).
1. Í hægra yfirlitssvæðinu skal velja **Active Directory** og ganga skal úr skugga um rétt skráasafn sé notað.
1. Á listanum **Stjórna** skal velja **Forritaskráningar** og svo forritið til að grunnstilla. Síðan **Stillingar** birtist og sýnir grunnstillingarupplýsingar.
1. Ganga skal úr skugga um að biðlarakenni forritsins passi við biðlarakenni í skrefi 2.
1. Á tækjastikunni skal velja **Eyða**.
1. Í staðfestingarskilaboðum sem birtist velurðu **Já**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Notandastillingar fartækis](mobile-device-user-settings.md)
- [Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið](step-icons-titles.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
