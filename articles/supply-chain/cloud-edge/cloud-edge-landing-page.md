---
title: Einingarkvarðar í dreifðri blandaðri grannfræði
description: Þetta efnisatriði veitir upplýsingar um einingarkvarðar fyrir ský og jaðra fyrir vinnuálag framleiðslu og vöruhúsakerfis
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3111de1f9862cbf926e763f963c86059f4121fc0
ms.sourcegitcommit: 4b7e9d074e368a08d2f75482b722dce0c69a4bbd
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/02/2021
ms.locfileid: "7733440"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Einingarkvarðar í dreifðri blandaðri grannfræði

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Boðið er upp á möguleika einingarkvarða fyrir Microsoft Dynamics 365 Supply Chain Management samkvæmt skilmálunum sem ná utan um notkun þjónustunnar. Nánari upplýsingar eru í [Microsoft Dynamics Lagalegar upplýsingar](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Þegar einingarkvarðar fyrir ský og edge eru virkjaðir verður þú beðin(n) að staðfesta að þú skiljir að sum gögn sem tengjast skilgreiningu og úrvinnslu einingarkvarða í skýi og edge kunni að vera geymd í gagnamiðstöðvum sem eru staðsettar í Bandaríkjunum. Frekari upplýsingar um úrvinnslu gagna fyrir einingarkvarða skýs og jaðars er að finna í hlutanum [Gagnavinnsla við stjórnun einingarkvarða](#data-processing-management) síðar í þessu efnisatriði.

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Tillaga um megingildi fyrir dreifða blandaða grannfræði

Fyrirtæki sem vinna með framleiðslu og dreifingu verða að geta keyrt helstu viðskiptaferla allan sólarhringinn án truflana og á eðlilegum hraða. Dreifð blönduð grannfræði gerir fyrirtækjum kleift að keyra mikilvægustu framleiðslu- og vöruhúsaferla án truflana, jafnvel þegar koma upp stöku vandamál tengd nettengingu eða biðtíma.

Dreifð blönduð grannfræði kynnir hugmyndina um *einingakvarða* sem virkjar dreifingu á vinnuálagi vinnusalar eða vöruhúsakeyrslu á meðan mismunandi umhverfa. Þessi virkni getur hjálpað til við að auka afköst, koma í veg fyrir truflun á þjónustu og hámarkað uppitíma. Boðið er upp á einingarkvarða í gegnum eftirfarandi innbætur fyrir áskriftina að Supply Chain Management:

- Viðbót Cloud Scale Unit fyrir Dynamics 365 Supply Chain Management
- Viðbót Edge Scale Unit fyrir Dynamics 365 Supply Chain Management

Verið er að gefa út möguleika vinnuálags jafnt og þétt í gegnum stigvaxandi viðbætur.

## <a name="scale-units-and-dedicated-workloads"></a>Einingarkvarðar og úthlutað vinnuálag

Einingarkvarðar stækka umhverfi Supply Chain Management miðstöðvarinnar með því að bæta við úthlutaðri úrvinnslugetu. Hægt er að keyra einingarkvarða í skýinu. Að öðrum kosti er hægt að keyra þá í jaðrinum á vinnustaðnum.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 með einingarkvörðum.":::

Einingarkvarðar bjóða upp á sveigjanleika, áreiðanleika og skölun fyrir úthlutað vinnuálag. Hægt er að aftengja tímabundið einingarkvarða jaðars frá umhverfi skýjamiðstöðvar og starfsfólk heldur áfram að vinna í úthlutuðu vinnuálagi í jaðrinum.

*Vinnuálag* er skilgreint safn viðskiptavirkni sem hægt er að taka til greina og úthluta til einingarkvarða. Þótt búið sé að gefa út vinnuálagið fyrir vöruhúsakerfið, er vinnuálagið fyrir framkvæmd framleiðslu enn í forútgáfu.

Hægt er að stilla umhverfi miðstöðvar og einingarkvarða skýs fyrir valið vinnuálag með því að nota [Stjórnandagátt einingarkvarða](https://sum.dynamics.com). Einnig er hægt að úthluta fleiri en einu vinnuálagi á hvern einingarkvarða. Frekari upplýsingar um skilyrði og takmarkanir einingarkvarða skýs í núverandi útgáfu er að finna í hlutanum [Skilyrði og takmarkanir einingarkvarða í skýi](#cloud-scale-unit-prerequisites) síðar í þessu efnisatriði.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Úthlutaðir möguleikar vinnuálags í vöruhúsakerfi í einingarkvarða

Vinnuálag vöruhúsastjórnunar gerir þér kleift að keyra vöruhúsastjórnunarferli á einangruðu uppsetningu.
Frekari upplýsingar eru í [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Úthlutað vinnuálag fyrir framkvæmd framleiðslu í einingarkvarða

Framleiðsluálagið skilar eftirfarandi getu:

- Stjórnandi véla og eftirlitsmenn vinnusalar fá aðgang að framleiðsluáætlun.
- Stjórnendur vél geta uppfært áætlunina með því að keyra afmarkað og verk framleiðsluferlis.
- Umsjónarmaður vinnusalar getur breytt starfsáætluninni.
- Starfskraftar geta opnað tíma og viðveru til innstimplunar og útstimplunar á jaðrinum til að tryggja réttan útreikning launa starfsmanna.

Frekari upplýsingar eru í [Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Það sem hafa ber í huga áður en dreifð blönduð grannfræði er virkjuð fyrir Supply Chain Management

Með því að virkja dreifða, blandaða grannfræði er skýjaumhverfi Supply Chain Management breytt þannig að það virki eins og miðstöð. Einnig er hægt að tengja frekari umhverfi við sem eru skilgreind sem einingarkvarðar í skýinu eða jaðrinum.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a> Skilyrði og takmarkanir fyrir einingarkvarða

Í núgildandi útgáfu fyrir einingarkvarða eru sumir möguleikar ekki enn tiltækir, en þeim gæti verið bætt við í væntanlegum útgáfum.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Þú verður að vera með leyfi fyrir Supply Chain Management

Til að geta tekið þátt í dreifðri grannfræði þarf að vera með leyfi fyrir Supply Chain Management. Núverandi skýjaumhverfi verður miðstöðin í blönduðu grannfræðinni. Hægt er að gefa upp bæði sandkassaumhverfi og framleiðsluumhverfi sem umhverfi miðstöðvar og hægt er að bæta við einingarkvörðum samkvæmt innbótunum sem þér áskotnast.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Stjórna þarf núverandi verki í gegnum almenna fyrirtækisútgáfu af LCS

Núverandi verk Microsoft Dynamics Lifecycle Services (LCS) verður að uppfylla eftirfarandi kröfur útgáfunnar:

- Stjórna þarf verkinu í gegnum almenna fyrirtækisútgáfu af LCS á [lcs.dynamics.com](https://lcs.dynamics.com).
- Staðbundnar útgáfur af LCS (svo sem [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) og [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) eru ekki studdar.
- LCS-skýjaútgáfur yfirvalda eru ekki studdar.
- Mooncake-útgáfa LCS er ekki studd.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Núverandi framleiðsluumhverfi verður að vera af sjálfsafgreiðslugerðinni í LCS

Núverandi framleiðsluumhverfi verður að vera merkt með gerðinni **Sjálfsafgreiðsla** í LCS. Þessi gerð gefur til kynna að leigjanda LCS-verksins hafi þegar verið breytt þannig að hann styðji hýsingarlíkanið Azure Service Fabric.

> [!IMPORTANT]
> Umhverfisgerðir sem keyra sem IaaS-þjónusta eru ekki studdar. Þessi umhverfi eru venjulega merkt með **Microsoft Managed** gerðinni í LCS. Ef þú ert með umhverfi af þessari gerð skaltu hafa samband við tengilið þinn hjá Microsoft til að komast að tímalínu á flutningi yfir í gerðina **Sjálfsafgreiðsla**.

Microsoft er að vinna að því að flytja öll skýjaumhverfi Supply Chain Management úr IaaS-líkani í grannfræði sem hýst er í Service Fabric. Þessi flutningur eykur sveigjanleika og stuðlar að auðveldari þjónustustjórnun. Fyrir vikið verða uppsetningar- og viðhaldsaðgerðir hraðari. Einnig er verið að flytja þjónustuíhluti yfir í örþjónustur og hýsingarlíkan þjónustunnar mun [breytast](/virtualization/windowscontainers/about/containers-vs-vm) úr líkani sýndarvélar og yfir í létta hólfahönnun.

Fyrir vikið mun sama hólfaða þjónustukerfi sem byggir á Service Fabric knýja bæði skýja- og jaðratilvik þjónustunnar burtséð frá því hvort tilvik sé miðstöð í skýinu eða einingarkvarði í skýinu eða jaðrinum.

Áður en hægt er að færa sig yfir í blandaða grannfræði sem styður einingarkvarða, þarf að flytja leigjanda verksins yfir í líkanið sem Service Fabric hýsir. Auk þess þarf að breyta öllum umhverfum sem virka eins og miðstöð.

> [!TIP]
> Til að spyrjast fyrir um stöðu leigjanda LCS-verks skal fletta upp á gerð umhverfisins í [LCS](https://lcs.dynamics.com/) eða hafa samband við samstarfsaðila eða tengilið hjá Microsoft.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Staðbundin umhverfi viðskiptagagna (á staðnum) eru ekki studd sem miðstöðvar fyrir einingarkvarða

Innanhússumhverfi geta ekki virkað sem miðstöðvar fyrir einingarkvarða. Umhverfi miðstöðvar verður alltaf að vera hýst í skýinu.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Stjórnunarmöguleikar einingarkvarða eru takmarkaðir

Stjórnunarmöguleikar sem geta hjálpað til við flutning vinnuálags eru takmarkaðir. Sumar stjórnunaraðgerðir eru ekki studdar í sjálfsafgreiðslu og hugsanlega þarf að óska eftir stuðningi í gegnum samstarfsaðila eða tengilið hjá Microsoft. Sem dæmi má nefna nokkrir flutningar vinnuálags á milli einingarkvarða og tímabundinna tilfallandi flutninga í alvarlegum aðstæðum.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Mælikvarðar og mælingar liggja ekki enn fyrir

Mælikvarðar og mælingar sem geta hugsanlega hjálpað til við að velja forritið fyrir einingarkvarðana eru ekki enn í boði. Starfið með tengilið ykkar hjá Microsoft eða samstarfsaðila innleiðingar til að velja gagnlegasta forritið.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a> Gagnavinnsla við stjórnun einingarkvarða

Þegar umhverfi Dynamics 365 er virkjað til að styðja dreifða blandaða grannfræði fyrir einingarkvarða skýs og jaðra munu sumar stýringarþjónustur eingöngu verða hýstar í Bandaríkjunum rétt eins og fyrir LCS. Þessi hegðun hefur áhrif á flutning og geymslu einhverra stjórnunar- og grunnstillingarupplýsinga sem [Stjórnandagátt einingarkvarða](https://sum.dynamics.com) notar. Hér eru nokkur dæmi:

- Heiti og auðkenni leigjenda
- LCS-verkkenni
- Netföng stjórnanda og verkeiganda sem notuð eru fyrir innskráningu
- Umhverfiskenni fyrir miðstöð og einingarkvarða
- Skilgreiningar vinnuálags, þ.m.t. heiti og aðsetur lögaðila og starfsstöðva, þannig að hægt sé að sýna grannfræði þína á landakorti
- Uppsafnaðar mælingar (á borð við biðtíma og gegnumstreymi) sem verða sýndar á greiningarsíðu kortsins til að auðvelda þér að velja hagkvæmustu notkun einingarkvarðanna

Gögnum sem eru flutt til og geymd í bandarískum gagnamiðstöðvum verður eytt í samræmi við reglur Microsoft um gagnavarðveislu. Persónuvernd þín skiptir Microsoft máli. Til að fá nánari upplýsingar skaltu lesa [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboarding-in-two-stages"></a>Innleiðing yfir tvö stig

Ferlið við innleiðingu dreifðrar blandaðrar grannfræði felur í sér tvö stig. Á fyrsta stiginu þarf að staðfesta sérstillingar til að ganga úr skugga um að þær virki í dreifðri grannfræði sem er með einingarkvarða. Sandkassa- og framleiðsluumhverfi eru aðeins flutt á seinna stiginum.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>Stig 1: Meta sérstillingar í heildrænu þróunarumhverfi

Áður en hafist er handa við að innleiða sandkassa- eða framleiðsluumhverfi er mælt með því að kanna einingarkvarða í þróunaruppsetningu, t.d. heildrænu umhverfi (einnig þekkt sem 1 lags umhverfi) þannig að hægt sé að staðfesta ferla, sérstillingar og lausnir. Á þessu stigi verða gögn og sérstillingar sett inn í heildræn umhverfi. Annað umhverfið tekur að sér hlutverk miðstöðvarinnar og hitt að sér hlutverk einingarkvarðans. Þessi uppsetning býður upp á bestu leiðina til að bera kennsl á og lagfæra vandamál. Nýjasta smíð snemmbúins aðgangs (PEAP) er einnig hægt að nota til að ljúka þessu stigi.

Fyrir stig 1 skal nota [uppsetningarverkfæri einingarkvarða fyrir heildræn þróunarumhverfi](https://github.com/microsoft/SCMScaleUnitDevTools). Þessi verkfæri gera kleift að skilgreina miðstöð og einingarkvarða í einu eða tveimur aðskildum heildrænum umhverfum. Boðið er upp á verkfærin sem tvíundarútgáfu og í frumkóða í GitHub. Kynnið ykkur verkið wiki, sem inniheldur [Ítarlega notkunarleiðbeiningu](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) sem lýsir því hvernig verkfærin eru notuð.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>Stig 2: Sækja innbætur og setja inn í sandkassa- og framleiðsluumhverfi

Til að innleiða eitt af sandkassa- eða framleiðslumhverfunum í nýju grannfræðina þarf að verða sér úti um viðbætur fyrir einn eða fleiri einingarkvarða (og fyrir einingarkvarða jaðars í framtíðinni). Innbæturnarr munu veita samsvarandi verk- og umhverfishólf í [LCS](https://lcs.dynamics.com/) þannig að hægt verði að setja upp umhverfi einingarkvarða.

> [!NOTE]
> Innbætur einingarkvarðans eru ekki tengdar við takmarkaðan fjölda notenda, en hvaða notandi sem er getur notað þær í núgildandi áskrift samkvæmt hlutverkunum sem stjórnandinn úthlutar.

Boðið er upp á einingarkvarða í mörgum birgðahaldseiningum og valkostum verðlagningar. Þar af leiðandi er hægt að velja þann valkost sem hentar best áætluðu færslumagni á mánuði og kröfum um afköst.

Birgðahaldseining á færslustigi er þekkt sem *Grunnur* og afkastameiri birgðahaldseiningin er þekkt sem *Venjuleg*. Hverri birgðahaldseiningu er hlaðið fyrirfram með tilteknum fjölda af mánaðarlegum færslum. Hins vegar er hægt að auka fjárhagsáætlun mánaðarlegra færslna með því bæta við gjaldfellingarinnbót fyrir hverja birgðahaldseiningu.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Innbætur fyrir einingarkvarða í skýi.":::

> [!TIP]
> Til að finna út hvaða stærð hentar best þínum kröfum skaltu starfa með samstarfsaðila þínum og Microsoft til að komast að mánaðarlegri færslustærð sem þú þarft á að halda.

Kaup á hverri innbót einingarkvarða veitir þér ekki einungis mánaðarmagn af færslum heldur færðu einnig aðgang að tilteknum fjölda umhverfishólfa í LCS. Fyrir hverja innbót einingarkvarða í skýinu færðu aðgang að einu nýju framleiðsluhólfi og einu nýju sandkassahólfi. Á meðan á innleiðingarferlinu stendur verður nýju LCS-verki bætt við þessi hólf. Notkunarheimildir fyrir hólfin eru bundin þannig að nota þarf hólfin sem einingarkvarða sem eru með miðstöð í skýinu.

Gjaldfellingarinnbætur veita þér ekki rétt á nýjum umhverfishólfum.

Ef þú vilt fá fleiri sandkassaumhverfi geturðu keypt fleiri venjuleg sandkassahólf. Microsoft getur þá aðstoðað þig við að virkja þessi hólf sem einingakvarðar sandkassa fyrir blönduðu grannfræðina.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Innleiða dreifða blandaða grannfræði fyrir Supply Chain Management

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Veljið leigjanda LCS-verks og ítarlegt innleiðingarferlið

Þegar búið er að áætla hvernig innleiðingu dreifðrar blandaðrar grannfræði fyrir Supply Chain Management verður háttað, verður [Stjórnandagátt einingarkvarða](https://aka.ms/SCMSUM) notuð til að hefja innleiðingarferlið. Í gáttinni skal velja flipann **Leigjendur Dynamics 365**. Þessi flipi sýnir lista yfir leigjendur sem reikningurinn þinn er hluti af og þar sem þú ert eigandi eða stjórnandi umhverfis fyrir LCS-verk.

Ef leigjandinn sem leitað er að er ekki á listanum skaltu fara í [LCS](https://lcs.dynamics.com/v2) og ganga úr skugga um að þú sért annaðhvort stjórnandi umhverfis eða verkeigandi LCS-verks fyrir þann leigjanda. Aðeins Azure Active Directory (Azure AD) reikningar frá völdum leigjanda mega ljúka skráningarferlinu.

> [!NOTE]
> Þegar búið er að gera breytingarnar á LCS gæti það tekið allt að 30 mínútur fyrir listann yfir leigjendur að sýna breytingarnar.

Listinn sýnir innleiðingarstöðuna fyrir hvern leigjanda fyrir sig.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Listi yfir leigjendur í flipa Dynamics 365-leigjenda.":::

Veljið **Smellið hér til að hefjast handa** til að óska eftir innleiðingu fyrir LCS-leigjandann. Samþykkja verður skilmálana. Einnig þarf að gefa upp tölvupóstfang fyrirtækis þar sem Microsoft getur sent samskipti sem tengjast nýliðunarferli.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Innsending nýskráningar fyrir leigjanda.":::

Microsoft mun fara yfir beiðnina og tilkynna um næstu skref með því að senda tölvupóst á netfangið sem gefið var upp á nýskráningareyðublaðinu. Microsoft mun starfa náið með þér til að virkja einingarkvarða í blandaðri grannfræði fyrir rekstraraðstæður þínar.

Þegar innleiðingu lýkur er hægt að nota gáttina til að skilgreina einingarkvarða og vinnuálag.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a> Hafa umsjón með mælieiningum og vinnuálagi með því að nota gáttina Scale Unit Manager

Farið í [Gátt Scale Unit Manager](https://aka.ms/SCMSUM) og skráið ykkur inn með leigjandareikningnum. Á síðunni **Skilgreina einingarkvarða** er hægt að bæta við umhverfi miðstöðvar ef það er ekki þegar í boði. Síðan er hægt að velja miðstöðina sem á að skilgreina með einingarkvörðum og vinnuálagi.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Gátt fyrir kvarðaeiningastjórnun, síðu Stilla mælieiningar.":::

Til að bæta við einum eða fleiri einingarkvörðum sem eru í boði í áskrift þinni, skal velja **Bæta við einingarkvörðum**.

Í flipanum **Skilgreint vinnuálag** skal nota hnappinn **Stofna vinnuálag** til að bæta vinnuálagi vöruhúsakerfis við einn einingarkvarðann. Fyrir hvert vinnuálag þarf að tilgreina samhengi ferlanna sem vinnuálagið verður í. Fyrir vinnuálag vöruhúsakerfis er samhengið tiltekið vöruhús á tilteknu svæði og lögaðila.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Valmynd til að skilgreina vinnuálag.":::

#### <a name="manage-workloads"></a>Stjórna vinnuálagi

Þegar ein eða fleiri vinnuálag eru virkjuð skaltu nota **Stjórna vinnuálagi** möguleika á að hefja og stjórna ferlum eins og þeim sem eru skráð í eftirfarandi töflu.

| Vinna | Lýsing |
|---|---|
| Gera hlé á samskiptum mælieininga | Gera hlé á leiðsluskilaboðum milli miðstöðvarinnar og mælieininga. Þetta ferli mun stöðva samskiptin og tæma gagnaleiðsluna milli miðstöðvarinnar og mælieininga. Þú verður að keyra þetta ferli áður en þú keyrir Supply Chain Management þjónustuaðgerð á annað hvort miðstöðina eða mælikvarðaeininguna, en þú getur líka notað þetta við aðrar aðstæður. |
| Haltu áfram samskiptum við mælieiningu | Halda áfram leiðsluskilaboðum milli miðstöðvarinnar og mælieininga. Þú gætir þurft að nota þetta ferli, til dæmis, eftir að þú hefur keyrt Supply Chain Management þjónustuaðgerð á annað hvort miðstöðina eða mælikvarðaeininguna. |
| Uppfærðu vinnuálag | Samstilltu nýja virkni á milli vinnuálags miðstöðvarinnar og mælieiningar. Þú gætir þurft að nota þetta ferli, til dæmis þegar þjónusta hefur valdið breytingum á gagnaskiptafyrirspurnum og/eða hefur bætt nýjum töflum eða reitum við vinnuálagið. |
| Flytja vinnuálag yfir á kvarðaeiningu | Tímasettu vinnuálag sem er í gangi á miðstöðinni til að flytja það yfir í mælieiningu. Þegar þetta ferli er keyrt mun samstilling gagna streyma og bæði miðstöðin og kvarðaeiningin verða stillt til að breyta eignarhaldi vinnuálagsins. |
| Flyttu kvarðaeiningu yfir á miðstöðina | Tímasettu vinnuálag sem nú er í gangi á mælikvarðaeiningu til að flytja í miðstöðina. Þegar þetta ferli er keyrt mun samstilling gagna streyma og bæði miðstöðin og kvarðaeiningin verða stillt til að breyta eignarhaldi vinnuálagsins.
| Neyðarskipti yfir í miðstöð | <p>Flyttu núverandi vinnuálag strax yfir á miðstöðina. *Þetta ferli mun aðeins breyta eignarhaldi þeirra gagna sem eru tiltæk á miðstöðinni.*</p><p><strong>Viðvörun:</strong> Þetta ferli getur valdið gagnatapi vegna ósamstilltra gagna og bilunar í viðskiptavinnslu. Þess vegna ætti það aðeins að nota í neyðartilvikum, þar sem vinna þarf úr viðskiptaferlum á miðstöðinni vegna þess að mælieiningin hefur bilun sem ekki er hægt að draga úr innan hæfilegs tíma.</p> |
| Dreifð svæðisfræði úr notkun | Fjarlægðu dreifingu mælieiningar og keyrðu aðeins á miðstöðinni, án vinnuálagsvinnslu. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Stjórnun einingarkvarða og vinnuálags.":::

> [!TIP]
> Með tímanum verða stigvaxandi viðbótum bætt við stjórnunarviðmót einingarkvarða til að gera aðgerðir líftímastjórnunar auðveldari. Tilteknir möguleikar fyrir núverandi útgáfu eru skráðir í handbók innleiðingar sem er í boði fyrir viðskiptavini sem hafa hafið innleiðingu dreifingar blandaðrar grannfræði fyrir Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
