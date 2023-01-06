---
title: Frumstilla Commerce Scale Unit (ský)
description: Í þessari grein er því lýst hvernig á að frumstilla Commerce Scale Unit (ský) í Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: f9d21de3e498b293394835d5cf564899338b9c18
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474016"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Frumstilla Commerce Scale Unit (ský)

[!include[banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig á að frumstilla Commerce Scale Unit (ský) í Microsoft Dynamics 365 Commerce.

Ef þú ert að nota tveggja laga sandkassa- eða vinnsluumhverfi sem er með forritsútgáfuna 8.1.2.x eða nýrri þarftu að frumstilla Commerce Scale Unit (ský) áður en þú getur notað virkni smásölurásar annaðhvort fyrir sölustaðaraðgerðir eða fyrir aðgerðir rafrænna viðskipta sem nota Retail Server í skýinu. Frumstilling mun nota Commerce Scale Unit (ský).

> [!IMPORTANT]
> Fyrir núverandi viðskiptavini sem nota virkni smásölurásar í skýinu þarf að uppfæra smásölurásirnar til að nota Commerce Scale Unit til að tryggja áframhaldandi og óhindraða notendaþjónustu fyrir viðskiptin þín. Ný umhverfi sem notuð eru án Commerce Scale Unit fá ekki lengir gæða- og þjónustuuppfærslur fyrir þætti smásölurásar sem hýstir eru í skýinu. Ekki er krafist neinna aðgerða fyrir viðskiptavini sem eingöngu nota Commerce Scale Unit (hýsing á eigin vegum). Hafðu samband við hönnuð Microsoft FastTrack lausnarinnar ef þú þarft viðbót.

## <a name="prerequisites"></a>Forkröfur

1. Settu upp tveggja laga sandkassa- eða vinnsluumhverfi sem er með útgáfuna 8.1.2.x eða nýrri.
2. Hægt er að setja inn allt að tvær Commerce Scale Unit í hverju umhverfi. Ef þú þarft fleiri en 2 Commerce Scale Unit á umhverfi þá skal í Microsoft Dynamics Lifecycle Services (LCS) stofna þjónustubeiðni og fara í **Beiðni um aukalegt Commerce Scale Unit** og gefa upp umhverfiskenni, númer Commerce Scale Unit og æskileg svæði gagnamiðstöðvar. Beiðninni verður lokið innan fimm virkra daga. Ef þú þarf ekki fleiri en 2 Commerce Scale Unit á umhverfi þarf ekki að stofna þjónustubeiðni. 
3. Þú verður að hafa heimildir verkeiganda í Lifecycle Services áður en hægt er að frumstilla Commerce Scale Unit.
4. Gakktu úr skugga um að skilgreiningarlyklar Retail-leyfis séu virkir í umhverfinu. Frekari upplýsingar eru í [Leyfiskóðar og skilgreiningarlyklaskýrsla](../sysadmin/license-codes-configuration-keys-report.md). Kveikt verður á eftirfarandi lyklum til að nota Commerce Scale Unit.

    - RetailBasic
    - RetaileCommerce - Ef ætlunin er að nota rafræn viðskipti fyrir Dynamics 365 Commerce.
    - RetailGiftCard - Ef ætlunin er að nota gjafakort.
    - RetailInvent - Ef ætlunin er að nota birgðir.
    - RetailModernPos - Ef þú hyggst nota sölustað.
    - RetailReplenishment - Ef ætlunin er að nota áfyllingar.
    - RetailScheduler
    - RetailStores - Ef ætlunin er að nota sölustaði.


## <a name="region-availability"></a>Svæði í boði
Commerce Scale Unit er í boði til notkunar á eftirfarandi svæðum.

| Alþjóðlega staðsetning | Svæði              | Framboð        | Athugasemdir                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERÍKA        | Austurhluti Bandaríkjanna             | Almennt tiltækt |  Engar athugasemdir.                         |
| AMERÍKA        | Austurhluti Bandaríkjanna 2           | Almennt tiltækt |  Engar athugasemdir.                          |
| AMERÍKA        | Norður- og miðríki Bandaríkjanna    | Takmörkuð afkastageta    |  Engar athugasemdir.                            |
| AMERÍKA        | Suður- og miðríki Bandaríkjanna    | Takmörkuð afkastageta    |  Engar athugasemdir.                            |
| AMERÍKA        | Miðríki Bandaríkjanna          | Almennt tiltækt |  Engar athugasemdir.                            |
| AMERÍKA        | Vesturhluti Bandaríkjanna             | Almennt tiltækt |  Engar athugasemdir.                            |
| AMERÍKA        | Bandaríkin 2, vestur           | Almennt tiltækt |  Engar athugasemdir.                            |
| AMERÍKA        | Mið-Kanada      | Takmörkuð afkastageta    |  Engar athugasemdir.                            |
| AMERÍKA        | Austur-Kanada         | Takmörkuð afkastageta    |   Engar athugasemdir.                           |
| AMERÍKA        | Vestur- og miðríki Bandaríkjanna     | Takmörkuð afkastageta    |   Engar athugasemdir.                           |
| APAC            | Austur-Ástralía      | Almennt tiltækt |   Engar athugasemdir.                           |
| APAC            | Suðaustur-Asía      | Afköst takmörkuð | Engar uppsetningar leyfðar.    |
| APAC            | Austur-Japan          | Almennt tiltækt |  Engar athugasemdir.                            |
| APAC            | Vestur-Japan          | Almennt tiltækt |   Engar athugasemdir.                           |
| APAC            | Suðaustur-Ástralía | Almennt tiltækt |   Engar athugasemdir.                           |
| APAC            | Austur-Asía           | Takmörkuð afkastageta    |   Engar athugasemdir.                           |
| APAC            | Suður-Indland         | Afköst takmörkuð | Engar uppsetningar leyfðar.    |
| APAC            | Mið-Indland       | Takmörkuð afkastageta    | Krefst samþykktarferlis. |
| EMEA            | Vestur-Evrópa         | Almennt tiltækt    |  Engar athugasemdir. |
| EMEA            | Norður-Evrópa        | Almennt tiltækt    |  Engar athugasemdir. |
| EMEA            | Suður-Bretland            | Almennt tiltækt |    Engar athugasemdir.                          |
| EMEA            | Bretland, vestur             | Almennt tiltækt |    Engar athugasemdir.                          |
| Sameinuðu arabísku furstadæmin             | Sameinuðu arabísku furstadæmin, norður           | Takmörkuð afkastageta    | Krefst samþykktarferlis. |

Uppsetningargeta á svæðum með takmarkaðri afkastagetu er afar takmörkuð. Óskir um uppsetningu eru metnar í hverju tilviki fyrir sig. Ef þú ert með sannfærandi viðskiptaþörf fyrir uppsetningu á svæðum takmarkaðrar afkastagetu geturðu sent inn þjónustubeiðni sem bætt verður á biðlistann. Svæði með takmarkaða afkastagetu leyfa ekki uppsetningu Commerce Scale Unit sem stendur. 

![Kort sem sýnir framboð eftir svæðum.](media/Commerce-Scale-Unit-Region-Availability.png "Kort sem sýnir framboð svæðis")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Frumstilla Commerce Scale Unit sem hluta af nýju umhverfi

Gakktu úr skugga um að höfuðstöðvarnar séu tiltækar. Þetta er nauðsynlegt til að skrá kvörðunareininguna hjá höfuðstöðvum í frumstillingarferlinu. Ekki er mælt með að frumstilla kvörðunareiningu þegar viðhald stendur yfir á höfuðstöðvum því þær geta verið óstarfhæfar í viðhaldsferlinu.

1. Gættu þess að umhverfi höfuðstöðva sé tiltækt og ekki í [Viðhaldsstillingu](../sysadmin/maintenance-mode.md).
2. Í LCS á upplýsingasíðu umhverfisins skal velja **Eiginleikar umhverfis \> Commerce**.
3. Á síðunni Uppsetning Commerce skaltu velja **Frumstilla**.
4. Veldu útgáfu Commerce Scale Unit til að frumstilla.
5. Veldu svæði til að frumstilla Commerce Scale Unit í.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Skilgreina rásir til að nota Commerce Scale Unit

Eftir að Commerce Scale Unit hefur verið tekin í notkun verður að tryggja að rásir þínar séu skilgreindar til að nota gagnagrunninn fyrir hana. 

Til að skilgreina rásirnar á að nota gagnagrunn Commerce Scale Unit skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal opna **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Commerce-verkraðari \> Gagnagrunnur rásar**.
1. Veljið rásargagnagrunninn í vinstra svæðinu.
1. Í flýtiflipanum **Smásölurás** skal velja **Bæta við** og síðan velja smásölurásina í fellilistanum.
1. Veljið **Bæta við** og veljið netrásina á fellilistanum. 

Að því loknu skal opna **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun** og keyra verk 9999.

> [!NOTE] 
> Vinnsla 9999 samstillir allar nýjar afurðir og viðskiptavini við Commerce Scale Unit. Þetta ferli getur tekið langan tíma. Ef rásin verður að vera til taks bara fyrir skilgreiningu svæðissmiðs á rafrænum viðskiptum er hægt að keyra vinnslu 1070 í staðinn fyrir vinnslu 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Uppfærsla gagnagrunns og Commerce Scale Unit-einingar

Áður en þú hefst handa skaltu ganga úr skugga um að þú kannist við [Skref til að ljúka eftir uppfærslu gagnagrunns fyrir umhverfi sem nota Commerce-virknina](../database/database-refresh.md).

Ekki er hægt að færa gagnagrunnsfærslur fyrir rás kvörðunareiningar (í skjámynd gagnagrunns rásar) á milli umhverfa sem hluti af uppfærslu gagnagrunns. Það er vegna þess að skrárnar tákna skilgreiningu tiltekins umhverfis.

Eftir uppfærslu gagnagrunns er hægt að endurskapa gagnagrunn kvörðunareiningarrásar með því að setja kvörðunareininguna aftur upp í LCS. Allar uppsetningar eða þjónustuaðgerðir í kvörðunareiningunni munu reyna að skrá kvörðunareininguna með höfuðstöðvum ef tekið er eftir að skráningu vanti.

Hægt er að gera enduruppsetningu á kvörðunareiningu án þess að breyta neinum þáttum með því að velja að setja upp sömu útgáfuna og kvörðunareiningin er nú þegar í. Þetta er hægt að gera í LCS með eftirfarandi skrefum:

1. Í LCS á upplýsingasíðu umhverfisins skal velja **Eiginleikar umhverfis \> Retail**.
2. Á uppsetningarsíðunni skal velja kvörðunareiningu sem á að setja upp aftur.
3. Í aðgerðarvalmynd kvörðunareiningarinnar skal velja **Uppfæra**.
4. Á sleðanum, í fellilistanum fyrir **Velja útgáfu**, skal velja valkostinn **Tilgreina útgáfu**.
5. Í textahólfinu undir **Tilgreina útgáfu** skal slá inn útgáfuna sem sýnd er fyrir kvörðunareininguna, sýnd við hliðina á merkinu **Núverandi útgáfa**.
6. Smellið á hnappinn **Uppfæra**.

Ekki þarf að velja **Uppfæra viðbætur** jafnvel þótt þú hafir notað viðbætur áður, þar sem síðasti viðbótarpakkinn sem var notaður á kvörðunareininguna er sjálfkrafa valinn þegar kvörðunareining er uppfærð.

Ef þú ert með margar kvörðunareiningar þarftu að framkvæma ofangreinda aðgerð fyrir hverja kvörðunareiningu. Þú getur framkvæmt þessar aðgerðir samhliða ef þess er óskað.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Nota fleiri Commerce Scale Unit-einingar (valfrjálst)

Þegar þú hefur frumstillt Commerce Scale Unit geturðu sett upp aðra kvörðunareiningu sjálf(ur) ef leyfið dugar til. Ef nota á fleiri en tvær Scale Unit-einingar þarf að stofna þjónustubeiðni. Í þjónustubeiðninni skal gefa upp fjölda Commerce Scale Unit sem þú þarft á að halda, heiti umhverfisins og æskileg svæði. Nánari upplýsingar um leyfisveitingar má finna í [Leyfishandbók Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Fyrir hvert aukalegt Commerce Scale Unit sem sett er upp er mælt með að búa til aðskildan gagnagrunnsflokk rásar með því að fylgja þessum skrefum.

1. Á aðalskrifstofu Commerce skal fara í **Smásala og viðskipti > Retail Headquarters > Uppsetning verkraðara smásölu > Gagnagrunnsflokkur rásar**.
2. Stofna nýjan gagnagrunnsflokk rásar.
3. Farðu í **Smásala og viðskipti > Retail Headquarters > Uppsetning verkraðara smásölu > Gagnagrunnur rásar** og veldu gagnagrunn rásar sem samsvarar nýlega stofnuðu Commerce Scale Unit.
4. Velja **Breyta** og velja nýjan gagnagrunnsflokk rásar.
5. Veldu **Vista**.
6. Veldu **Keyra fulla samstillingu gagna** fyrir valinn gagnagrunn rásarinnar.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Viðbótaratriði ef þú frumstillir hluta skýjahýstrar Commerce-rásar í núverandi umhverfi

Ef þú ert þegar að nota þætti Commerce-rásar sem hýstir eru í skýinu í umhverfi mun frumstilling Commerce Scale Unit hjálpa til við að draga úr niðurtíma þegar þessi þættir eru uppfærðir. Frekari áætlanagerð er nauðsynleg áður en Commerce Scale Unit er notuð.

Þegar fyrsta Commerce Scale Unit er frumstillt í umhverfi sem notar þætti Commerce-rásar sem hýstir eru í skýinu mun frumstillingarferlið flytja rásirnar sem tengjast þáttum rásar sem hýst er í skýinu yfir í fyrstu kvörðunareininguna. Ekki er hægt að hafa áhrif á rásir sem tengjast Store Scale Unit.

Flutningsferlið er gagnsætt gagnvart rásunum. Eftir að frumstilling kvörðunareiningar hefst eru eftirfarandi aðgerðir sjálfkrafa framkvæmdar:

1. Ný Commerce Scale Unit verður stofnuð og tengist umhverfinu.
2. Commerce Scale Unit mun vera skráð sem tiltækur gagnagrunnur rásar í höfuðstöðvum.
3. Allar rásir sem varpað er í gagnagrunnsrásina **Sjálfgefið** í höfuðstöðvum verða uppfærðar til að varpa nýja Commerce Scale Unit.
4. Full gagnasamstilling Commerce Data Exchange (CDX) verður framkvæmd til að færa rásargögnin í nýju kvörðunareininguna.

**Áætlanagerð og prófanir fyrir frumstillingu Commerce Scale Unit** Sem almenn regla þegar Commerce Scale Unit er frumstillt þarf að gera ráð fyrir fimm klukkustunda niðurtíma fyrir verslunaraðgerðir ásamt öllum aðgerðum í rás rafrænna viðskipta sem notar Retail Server eða sölustað í skýinu.

1. Uppfærðu gagnagrunninn úr vinnsluumhverfinu í UAT-sandkassaumhverfi. 
2. Frumstilla Commerce Scale Unit í UAT-sandkassaumhverfi. 
3. Athugaðu frumstillingartíma fyrir Commerce Scale Unit. Þetta verður sambærilegt við tímann sem þessi gerð tekur í vinnsluumhverfinu, en þá verða verslunaraðgerðir og aðgerðir rafrænna viðskipta ekki í boði.

Framkvæma þarf eftirfarandi viðbótarskref áður en Commerce Scale Unit er frumstillt.

- **Loka öllum sölustaðarvöktum** – Eftir flutning geta sölustaðarnotendur ekki lokað vöktum sem voru virkar í flutningsferlinu.
- **Staðfesta að öllum P-vinnslum sé lokið** – Mælt er með að búið sé að ljúka við P-vinnslur sem samstilla biðfærslur áður en CSU er frumstillt.
- **Útskráning úr öllum sölustaðartækjum** – Sölustaðaraðgerðir eru ekki studdar við flutning.
- **Kalla aftur á og ógilda allar frestaðar færslur á sölustað** – Frestaðar færslur eru ekki geymdar sem hluti af frumstillingunni.

> [!IMPORTANT]
> Sem hluti af upphafssetningu Commerce Scale Unit uppsetningar munu fyrri færslur tapast og ekki er hægt að afturkalla þær. 

Þetta gerist á frumstillingartímabilinu:

- Viðskiptarásir sem hýstar eru í skýinu virka ekki nema kveikt sé á aðgerðafærni sölustaðar utan nets.
- Sölustaðartæki með kveikt á aðgerðarhæfni utan nets verða með skerta virkni.
- Allir netviðskiptavinir sem eru háðir Retail Server verða fyrir truflunum.
- Þetta hefur ekki áhrif á rásir sem eru hýstar í Commerce Scale Unit (sjálfshýstar).
- Virkni aðalskrifstofu verður ekki fyrir áhrifum.

Hér er það sem gerist eftir að frumstillingu er lokið:

- Haldið er utan um virkjunarstöðu tækis fyrir öll virk tæki sölustaðar, sem þýðir að ekki þurfi að endurvirkja tækin.
- Tilvik sjálfstæðra vélbúnaðarstöðva munu halda áfram að virka.
- Skýrslur á rás sölustaðar verða endurstilltar og munu ekki sýna gögn frá því fyrir frumstillingu.
- „Sýna færslubókaraðgerð“ verður einng endurstillt og sýnir ekki gögn frá því fyrir frumstillingu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
