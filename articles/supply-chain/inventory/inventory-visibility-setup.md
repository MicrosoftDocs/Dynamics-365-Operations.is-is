---
title: Setja upp innbót birgðasýnileika
description: Þetta efnisatriði lýsir því hvernig á að setja upp innbót birgðasýnileika fyrir Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2b85f533a3318701ed08857b899cf9bdd103863
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474821"
---
# <a name="install-and-set-up-inventory-visibility"></a>Setja upp sýnileika birgða

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp innbót birgðasýnileika fyrir Microsoft Dynamics 365 Supply Chain Management.

Þú verður að nota Microsoft Dynamics Lifecycle Services (LCS) til að setja upp innbót birgðasýnileika. LCS er samstarfsgátt sem býður upp á umhverfi ásamt safni af reglulega uppfærðum þjónustum sem hjálpa til við að stjórna líftíma forrits fyrir fjármála- og rekstrarforritin þín.

Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Skilyrði birgðasýnileika

Áður en þú setur upp birgðasýnileika verður þú að ljúka eftirfarandi verkum:

- Fáðu LCS-innleiðingarverk þar sem a.m.k. eitt umhverfi er uppsett.
- Vertu viss um að lokið hafi verið við skilyrðin fyrir uppsetningu innbóta. Upplýsingar um þessar forsendur er að finna í [Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Sýnileiki birgða krefst ekki tengingu tvöföldrar skráningar.
- Hafa skal samskipti við teymi birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá eftirfarandi áskidlar áskildar skrár:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (ef útgáfan af Supply Chain Management sem er keyrð er eldri en útgáfa 10.0.18)

> [!NOTE]
> Löndin og svæðin sem nú eru studd eru Kanada (CCA, ECA), Bandaríkin (WUS, ESB), Evrópusambandið (NEU, WEU), Bretland (SUK, Wuk), Ástralía (EAU, SEAU), Japan (EJP, WJP) og Brasilía (SBR, SCUS).

Ef einhverjar spurningar vakna um þessi skilyrði skaltu hafa samband við vöruteymi birgðasýnileika.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Setja upp Dataverse

Til að setja upp Dataverse þannig að hægt sé að nota það með birgðasýnileika skaltu nota Package Deployer til að setja upp pakka birgðasýnileika. Eftirfarandi undirhlutar lýsa því hvernig á að ljúka hverju verki.

> [!NOTE]
> Sem stendur eru aðeins Dataverse umhverfi studd sem hafa verið búin til með því að nota LCS. Ef Dataverse umhverfið þitt var búið til á einhvern annan hátt (til dæmis með því að nota Power Apps stjórnendamiðstöðina) og ef það er tengt við umhverfi Supply Chain Management verður þú fyrst að hafa samband við vöruteymi birgðasýnileika til að leysa úr vandamáli vörpunar. Þá er hægt að setja upp birgðasýnileika.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Flytja úr gamalli útgáfu af Dataverse lausninni

Ef þú hefur sett upp eldri útgáfu af lausn Dataverse birgðasýnileika skatlu nota þessar leiðbeiningar til að uppfæra útgáfuna þína. Tvö tilfelli eru til staðar:

- **Tilfelli 1:** Ef þú setur `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` upp handvirkt með því að flytja inn Dataverse lausnina skaltu fylgja þessum skrefum:

    1. Sæktu eftirfarandi þrjár skrár:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Flyttu handvirkt `InventoryServiceBase_managed.cab` og `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` inn í Dataverse með því að fylgja þessum skrefum:

        1. Opnið vefslóð Dataverse umhverfisins.
        1. Opnaðu síðuna **Lausnir**.
        1. Velja **Innflutningur**.

    1. Notaðu Package Deployer til að setja upp `InventoryServiceApplication.PackageDeployer.zip` pakkann. Fyrir leiðbeiningar skaltu skoða hlutann [Notaðu Package Deployer til að setja upp pakkann](#deploy-package) síðar í þessu efnisatriði.

- **Tilfelli 2:** Ef þú setur upp Dataverse með því að nota Package Deployer áður en þú settir upp eldri `.*PackageDeployer.zip` pakkann, skaltu sækja `InventoryServiceApplication.PackageDeployer.zip` og gera uppfærslu. Fyrir leiðbeiningar skaltu skoða hlutann [Nota Package Deployer til að setja upp pakkann](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Nota Package Deployer til að setja upp pakkann

1. Setja upp verkfæri þróunaraðila eins og lýst er í [Sækja verkfæri frá NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Aflæstu `InventoryServiceApplication.PackageDeployer.zip` skránni sem þú sóttir úr Teams-hópnum með því að fylgja þessum skrefum:

    1. Veldu og haltu inni skránni (eða hægrismelltu á hana) og veldu síðan **Eiginleikar**.
    1. Í svarglugganum **Eiginleikar**, í flipanum **Almennt**, skaltu finna hlutann **Öryggi**, velja **Aflæsa** og setja breytinguna á. Ef það er enginn **Öryggishluti** í flipanum **Almennt** er skráin ekki útilokuð. Ef svo er skaltu fara yfir í næsta skref.

    ![Afblokka sótta skrá](media/unblock-file.png "Afblokka sótta skrá")

1. Afþjappaðu `InventoryServiceApplication.PackageDeployer.zip` til að finna eftirfarandi atriði:

    - `InventoryServiceApplication`-mappa
    - `[Content_Types].xml`-skrá
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`-skrá

1. Afritaðu hvert þessara atriða í `.\Tools\PackageDeployment` skráasafnið. (Þetta skráasafn var búið til þegar þú settir upp verkfæri þróunaraðila.)
1. Keyrðu `.\Tools\PackageDeployment\PackageDeployer.exe` og fylgdu leiðbeiningunum á skjánum til að flytja inn lausnirnar.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Setja upp innbót birgðasýnileika

Áður en þú setur upp innbótina skaltu skrá forrit og bæta leyniorði biðlara við Azure Active Directory (Azure AD) undir Azure-áskriftinni þinni. Leiðbeiningar er að finna í [Skrá forrit](/azure/active-directory/develop/quickstart-register-app) og [Bæta við leyniorði biðlara](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Vertu viss um að skrá hjá þér gildin fyrir **Kenni forrits (biðlara)**, **Leyniorð biðlara** og **Kenni leigjanda** því þú þarft á þeim halda síðar.

Eftir að þú hefur skráð forrit og bætt leyniorði biðlara við Azure AD skaltu fylgja þessum skrefum til að setja upp innbót birgðasýnileika.

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com/Logon/Index).
1. Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.
1. Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.
1. Á heimasíðu umhverfisins skal fletta niður þar til þú finnur hlutann **Innbætur umhverfis** í hlutanum **Power Platform samþætting**. Þar má finna heiti Dataverse umhverfisins.
1. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.

    ![Heimasíða umhverfis í LCS](media/inventory-visibility-environment.png "Heimasíða umhverfis í LCS")

1. Veldu tengilinn **Setja upp nýja innbót**. Listi yfir tiltækar innbætur birtist.
1. Í listanum skal velja **Birgðasýnileika**.
1. Stilltu eftirfarandi reiti fyrir umhverfið þitt:

    - **Auðkenni AAD-forritsins (biðlara)** – Sláðu inn Azure AD forritskennið sem þú bjóst til og skráðir hjá þér hér á undan.
    - **AAD-leigjandakenni** – Sláðu inn leigjandakennið sem þú skráðir hjá þér hér á undan.

    ![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")

1. Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.
1. Velja **Setja upp**. Staða innbótar er sýnd sem **Í uppsetningu**. Þegar uppsetningunni er lokið skaltu endurhlaða síðuna. Staðan ætti að breytast í **Uppsett**.

> [!IMPORTANT]
> Ef þú ert með fleiri en eitt LCS-umhverfi skaltu búa til annað Azure AD forrit fyrir hvert umhverfi. Ef þú notar sama forritskennið og leigjandakennið til að setja upp innbót birgðasýnileika fyrir mismunandi umhverfi mun koma upp vandamál varðandi lykla fyrir eldri umhverfi. Aðeins það síðasta sem var sett upp verður tekið gilt.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Fjarlægja innbót birgðasýnileika

Til að fjarlægja innbót birgðasýnileika skaltu velja **Fjarlægja** á LCS-síðunni. Fjarlægingarferlið eyðir innbót birgðasýnileika, afskráir innbótina úr LCS og eyðir öllum tímabundnum gögnum sem eru geymd í skyndiminni fyrir innbót birgðasýnileika. Hins vegar er helstu birgðagögnunum sem geymd eru í Dataverse áskriftinni þinni ekki eytt.

Til að fjarlægja birgðagögnin sem geymd eru í Dataverse áskriftinni skal opna [Power Apps](https://make.powerapps.com), velja **Umhverfi** í yfirlitsstikunni og velja Dataverse umhverfin sem eru bundin við LCS-umhverfið þitt. Farðu því næst í **Lausnir** og eyddu eftirfarandi fimm lausnum:

- Festa lausn fyrir forrit birgðasýnileika í lausnum Dynamics 365
- Forritslausnir birgðasýnileika í Dynamics 365 FNO SCM
- Skilgreining birgðaþjónustu
- Sjálfstæður birgðasýnileiki
- Grunnlausn birgðasýnileika í Dynamics 365 FNO SCM

Þegar þú eyðir þessum lausnum er gögnum sem geymd eru í töflum einnig eytt.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Setja upp birgðasýnileika í Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Nota samþættingarpakka birgðasýnileika

Ef keyrð er útgáfa 10.0.17 eða eldri af Supply Chain Management skal hafa samband við stuðningshóp vegna innleiðingar birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá skráarpakkann. Virkjaðu svo pakkann í LCS.

> [!NOTE]
> Ef villa vegna misræmis útgáfu kemur upp í uppsetningunni þarf að flytja inn handvirkt X++ verkið í þróunarumhverfið. Síðan skal stofna virkjanlega pakkann í þróunarumhverfinu og setja hann upp í þróunarumhverfinu.
>
> Kóðinn fylgir með Supply Chain Management útgáfu 10.0.18. Ef sú útgáfa eða nýrri er keyrð þarf ekki uppsetningu.

Gangið úr skugga um að kveikt sé á eftirfarandi eiginleikum í umhverfi Supply Chain Management. (Sjálfgefið er að kveikt sé á þessu.)

| Lýsing eiginleika | Kóðaútgáfa | Skipta milli klasa |
|---|---|---|
| Gera notkun birgðavídda í InventSum-töflu virka eða óvirka      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Gera notkun birgðavídda í InventSumDelta-töflu virka eða óvirka | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Setja upp samþættingu fyrir Sýnileika birgða

Þegar þú hefur sett upp innbótina skaltu undirbúa kerfi Supply Chain Management til að vinna með það með því að fara í gegnum eftirfarandi skref.

1. Í Supply Chain Management skal opna vinnusvæðið **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og kveikja á eftirfarandi eiginleikum:
    - *Samþætting sýnileika birgða* – Áskilið.
    - *Samþætting birgðasýnileika með mótbókun frátekningar* – Ráðlagt en valfrjálst. Krefst útgáfu 10.0.22 eða nýrri. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Opnaðu flipann **Almennt** og gerðu eftirfarandi stillingar:
    - **Endastöð sýnileika birgða** – Færðu inn vefslóð umhverfisins þar sem þú keyrir birgðasýnileika. Frekari upplýsingar er að finna í [Finna endastöð þjónustu](inventory-visibility-configuration.md#get-service-endpoint).
    - **Hámarksfjöldi færslna í einni beiðni** – Stilltu á hámarksfjölda færslna sem á að hafa með í einni beiðni. Þú verður að færa inn jákvæða heiltölu sem er minna en eða jafnt og 1000. Sjálfgildið er 512. Við mælum eindregið með því að halda sjálfgefna gildinu nema þú hafir fengið ráðgjöf frá notendaþjónustu Microsoft eða sért á annan hátt viss um að þú þurfir að breyta því.

1. Ef þú virkjaðir valfrjálsa eiginleikann *Samþætting birgðasýnileika með mótbókun frátekningar* skaltu opna flipann **Mótbókun frátekningar** og gera eftirfarandi stillingar:
    - **Virkja mótbókun frátekningar** – Stilltu á *Já* til að virkja þessa virkni.
    - **Breytilykill fyrir mótbókun frátekningar** – Veldu stöðu birgðafærslu sem mun mótbóka frátekningar sem gerðar eru í birgðasýnileika. Þessi stilling ákvarðar stöðu pöntunarúrvinnslu sem setur af stað mótbókanir. Staða á birgðafærslu pöntunar sér um að rekja stigið. Veljið um eitt af eftirfarandi:
        - *Í pöntun* – Fyrir stöðuna *Í færslu* mun pöntun senda beiðni um mótbókun þegar hún er stofnuð. Magn mótbókunar verður magn stofnaðrar pöntunar.
        - *Taka frá* – Fyrir stöðuna *Taka frá pantaða færslu* mun pöntun senda beiðni um mótbókun þegar hún er tekin frá, tínd, fylgiseðill bókaður eða hún reikningsfærð. Beiðnin verður aðeins sett af stað í eitt skipti fyrir fyrsta skrefið þegar uppgefið ferli á sér stað. Magn mótbókunar verður magnið þar sem staða birgðafærslu breyttist úr *Í pöntun* í *Frátekið pantað* (eða síðari staða) í samsvarandi pöntunarlínu.

1. Farið í **Birgðastjórnun \> Reglubundið \> Samþætting sýnileika birgða** og virkjið verkið. Öll tilvik birgðabreytinga úr Supply Chain Management verða nú bókuð í birgðasýnileika.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
