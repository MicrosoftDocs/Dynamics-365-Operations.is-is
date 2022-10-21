---
title: Aðstæður fyrir vélarstöðu
description: Þessi grein lýsir stöðu atburðarásar vélarinnar, sem gerir þér kleift að nota skynjaragögn til að fylgjast með framboði á búnaði þínum.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689640"
---
# <a name="the-machine-status-scenario"></a>Aðstæður fyrir vélarstöðu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

The *stöðu vélarinnar* atburðarás gerir þér kleift að nota skynjaragögn til að fylgjast með framboði á búnaði þínum. Ef þú setur upp skynjara sem sendir merki þegar framleiðsluverk á vélaauðlind framleiðir úttak, en ekkert skynjaramerki er móttekið innan tiltekins bils, birtist tilkynning á mælaborði umsjónarmanns.

## <a name="scenario-dependencies"></a>Ósjálfstæði sviðsmynda

The *stöðu vélarinnar* atburðarás hefur eftirfarandi ósjálfstæði:

- Aðeins er hægt að kveikja á tilkynningu ef framleiðsluverk er í gangi á kortlagðri vél.
- Merki sem táknar a *hluta út* merki verður að senda til IoT miðstöðina.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Undirbúa kynningargögn fyrir stöðu vélarinnar

Ef þú vilt nota kynningarkerfi til að prófa *stöðu vélarinnar* atburðarás, notaðu kerfi þar sem [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er uppsett skaltu velja *USMF* lögaðila (fyrirtæki), og undirbúa viðbótar kynningargögn eins og lýst er í þessum hluta. Ef þú ert að nota þína eigin skynjara og gögn geturðu sleppt þessum hluta.

### <a name="set-up-a-sensor-simulator"></a>Settu upp skynjarahermi

Ef þú vilt prófa þessa atburðarás án þess að nota líkamlegan skynjara geturðu sett upp hermi til að búa til nauðsynleg merki. Fyrir frekari upplýsingar, sjá [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Staðfestu að tilföng 3118 sé notuð fyrir vöru P0111

Framleiðslupöntun verður áætluð og gefin út. Þess vegna losnar framleiðsluverk til tilföngs *3118* (*Froðuskurðarvél*). Fylgdu þessum skrefum til að staðfesta það tilfang *3118* er notað fyrir vöru *P0111* í kynningargögnunum þínum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu vöruna þar sem **Vörunúmer** reiturinn er stilltur á *P0111*.
1. Á aðgerðarrúðunni, á **Verkfræðingur** flipa, í **Útsýni** hópur, veldu **Leið**.
1. Á **Leið** síðu, á **Yfirlit** flipann neðst á síðunni, veldu línuna þar sem **Óper. Nei.** Reiturinn er stilltur á *30*.
1. Á **Auðlindaþörf** flipann neðst á síðunni, vertu viss um að tilföngin *3118* (*Froðuskurðarvél*) tengist aðgerðinni.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Stofna og gefa út framleiðslupöntun fyrir vöru P0111

Fylgdu þessum skrefum til að stofna og gefa út framleiðslupöntun fyrir vöru *P0111*.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á **Allar framleiðslupantanir** síðu, á aðgerðarrúðunni, veldu **Ný lotupöntun**.
1. Í **Búðu til lotu** valmynd, stilltu eftirfarandi gildi:

    - **Vörunúmer:** *P0111*
    - **Magn:** *10*

1. Veldu **Búa til** til að búa til pöntunina og fara aftur í **Allar framleiðslupantanir** síðu.
1. Nota **Sía** reit til að leita að framleiðslupöntunum þar sem **Vörunúmer** reiturinn er stilltur á *P0111*. Finndu síðan og veldu framleiðslupöntunina sem þú varst að búa til.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í **Áætlun** valmynd, veldu **Allt í lagi** til að keyra matið.
1. Á aðgerðarrúðunni, á **Framleiðslupöntun** flipa, í **Ferli** hópur, veldu **Gefa út**.
1. Í **Gefa út** í glugganum skaltu skrifa niður númer lotupöntunarinnar sem þú bjóst til.
1. Veldu **Allt í lagi** að gefa út pöntunina.

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Þú munt nota framkvæmdarviðmót framleiðslugólfs til að hefja verkið sem var áætlað og gefið út fyrir vörunúmer *P0111* í fyrri hlutanum. Fylgdu þessum skrefum til að stilla framkvæmdarviðmót framleiðslugólfs.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Ef þú hefur ekki áður sett upp viðmótið birtist innskráningarsíða. Færðu inn skilríki
1. Á opnunarsíðunni velurðu **Stilla** að opna **Stilla tæki** galdramaður.
1. Á **Stilla tæki - Skref 1 - Veldu stillingar** síðu, veldu *Sjálfgefið* uppsetningu.
1. Veljið **Næst**.
1. Á **Stilla tæki - Skref 2 - Skilgreina gólfflöt framleiðslunnar** síðu, stilltu **Auðlind** sviði til *3118*.
1. Veldu **Í lagi**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a> Virkjaðu leitarmöguleikann í framkvæmdarviðmóti framleiðslugólfs

Til að gera það auðveldara að finna framleiðsluverkið fyrir framleiðslupöntunina sem var gefin út fyrr, fylgdu þessum skrefum til að virkja leitarvalkostinn í framkvæmdarviðmóti framleiðslugólfs.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Veldu *Sjálfgefið* uppsetningu.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á **Almennt** flýtiflipann, stilltu **Virkja leit** valmöguleika til *Já*.
1. Lokið síðunni.

### <a name="start-the-first-job-in-the-batch-order"></a>Byrjaðu fyrsta verkið í runupöntuninni

Fylgdu þessum skrefum til að hefja verkið sem áætlað er á tilfangi *3118*.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í **Merki auðkenni** reit, slá inn *123*. Veldu síðan **skrá inn**.
1. Ef þú ert beðinn um fjarvistarástæðu skaltu velja eitt af kortunum fyrir fjarveru og síðan velja **Allt í lagi**.
1. Í **Leita** reit, sláðu inn lotupöntunarnúmerið sem þú skráðir áður. Veldu síðan **Til baka** lykill.
1. Veldu pöntunina og veldu síðan **Byrja starf**.
1. Í **Byrja starf** valmynd, veldu **Byrjaðu**.

## <a name="set-up-the-machine-status-scenario"></a>Settu upp stöðuatburðarás vélarinnar

Fylgdu þessum skrefum til að setja upp *stöðu vélarinnar* atburðarás í Supply Chain Management.

1. Fara til **Framleiðslueftirlit \> Uppsetning \> Sensor Data Intelligence \> Sviðsmyndir**.
1. Í **Staða vélarinnar** atburðarás kassi, veldu **Stilla** til að opna uppsetningarhjálpina fyrir þessa atburðarás.
1. Á **Skynjarar** síðu, veldu **Nýtt** til að bæta skynjara við ristina. Stilltu síðan eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn auðkenni skynjarans sem þú ert að nota. (Ef þú ert að nota Raspberry PI Azure IoT Online Simulator og hefur sett hann upp eins og lýst er í [Settu upp herma skynjara til að prófa](sdi-set-up-simulated-sensor.md), koma inn *Vélarstaða* .)
    - **Lýsing á skynjara** – Sláðu inn lýsingu á skynjaranum.

1. Endurtaktu fyrra skref fyrir hvern viðbótarskynjara sem þú vilt bæta við núna. Þú getur komið aftur og bætt við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á **Kortlagning viðskiptaskráa** síðu, í **Skynjarar** kafla, veldu skrána fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í **Kortlagning viðskiptaskráa** kafla, veldu **Nýtt** til að bæta línu við ristina.
1. Á nýju röðinni skaltu stilla **Viðskiptaskrá** reitnum við auðlindina sem þú notar valinn skynjara til að fylgjast með. (Ef þú ert að nota kynningargögnin sem þú bjóst til fyrr í þessari grein skaltu stilla reitinn á *3118, Froðuskurðarvél* .)
1. Veljið **Næst**.
1. Á **Vélarstöðuþröskuldur** síðu, tilgreindu hversu lengi eftir síðasta *hluta út* gefa til kynna að kerfið ætti að senda tilkynningu um stöðu vélarinnar. Það eru tvær leiðir til að skilgreina þröskuldinn:

    - **Sjálfgefinn þröskuldur (mínútur)** – Stilltu þennan reit til að skilgreina sjálfgefna þröskuldinn. Gildið mun þá gilda um allar auðlindir þar sem **Þröskuldur til að ákvarða vél svarar ekki (mínútur)** reiturinn er stilltur á tvær mínútur eða minna. Lágmarksgildið er *2* (mínútur).
    - **Þröskuldur til að ákvarða vél svarar ekki (mínútur)** – Fyrir hverja tilföng í hnitanetinu sem þú vilt ekki nota sjálfgefna þröskuldinn fyrir skaltu slá inn hnekkjagildi í þessum reit. Tilföng sem eru stillt á að nota þröskuld upp á tvær mínútur eða minna munu nota **Sjálfgefinn þröskuldur (mínútur)** stilling í staðinn.

    > [!NOTE]
    > Venjulega muntu nota a *hluta út* merki til að fylgjast með stöðu vélarinnar. Þess vegna ættir þú að ganga úr skugga um að þröskuldurinn fyrir hverja vélaauðlind sé lengri en vélin þarfnast til að framleiða hvern hluta.

1. Veljið **Næst**.
1. Á **Virkjaðu skynjara** síðu, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkjaðu**. Fyrir hvern virkan skynjara í ristinni birtist gátmerki í **Virkur** dálki.
1. Veljið **Ljúka**.

## <a name="work-with-the-machine-status-scenario"></a>Vinna með stöðu vélarinnar

Eftir að þú hefur sett upp skynjarana þína og stillt atburðarásina geturðu skoðað stöðuatburði véla í Supply Chain Management. Þessi hluti lýsir hvar og hvernig á að skoða þessar upplýsingar.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Skoðaðu gögn um stöðu vélarinnar á síðunni Tilfangsstaða

Á **Auðlindastaða** síðu, umsjónarmenn geta fylgst með tímalínu á *hluta út* merki sem er móttekið frá skynjurum sem eru kortlagðar á hverja vélaauðlind. Fylgdu þessum skrefum til að stilla tímalínuna.

1. Fara til **Framleiðslueftirlit \> Framleiðsluframkvæmd \> Auðlindastaða**.
1. Í **Stilla** valmynd, stilltu eftirfarandi reiti:

    - **Auðlind** - Veldu úrræði sem þú vilt fylgjast með. (Ef þú ert að vinna með kynningargögnin skaltu velja *3118* .)
    - **Tímaröð 1** – Veldu færsluna (mælingarlykill) sem hefur eftirfarandi snið fyrir nafnið: *MachineReporting Status:&lt; Skynjari&gt;*
    - **Birta nafn** - Koma inn *Hlutar út merki*.

Eftirfarandi mynd sýnir dæmi um stöðuupplýsingar vélar á vélinni **Auðlindastaða** síðu í hefðbundnum rekstri.

![Vélarstöðugögn á síðunni Tilfangsstaða við venjulega notkun.](media/sdi-resource-status-downtime-up.png "Vélarstöðugögn á síðunni Tilfangsstaða við venjulega notkun")

Eftirfarandi mynd sýnir dæmi um stöðuupplýsingar vélar þegar niðurtími greinist.

![Vélarstöðugögn á síðunni Tilfangsstaða þegar niðurtími greinist.](media/sdi-resource-status-downtime-down.png "Vélarstöðugögn á síðunni Tilfangsstaða þegar niðurtími greinist")

### <a name="view-machine-status-on-the-notifications-page"></a>Skoðaðu stöðu vélarinnar á tilkynningasíðunni

Á **Tilkynningar** síðu geta umsjónarmenn skoðað þær tilkynningar sem myndast þegar of langur tími er liðinn frá því skynjarinn sendi síðast frá sér *hluta út* merki. Hver tilkynning veitir yfirlit yfir framleiðsluverkið sem verður fyrir áhrifum af biluninni og gefur möguleika á að endurúthluta viðkomandi verki til annars tilföngs.

Til að opna **Tilkynning** síðu, farðu á **Framleiðslueftirlit \> Fyrirspurnir og skýrslur \> Skynjargagnagreind \> Tilkynningar**.

Eftirfarandi mynd sýnir dæmi um tilkynningu um stöðu vélarinnar.

![Dæmi um tilkynningu um stöðu vélar.](media/sdi-resource-status-downtime-notification.png "Dæmi um tilkynningu um stöðu vélar")
