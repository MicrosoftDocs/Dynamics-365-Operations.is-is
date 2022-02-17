---
title: Frumstilla Commerce Scale Unit (ský)
description: Þetta efni útskýrir hvernig á að frumstilla Commerce Scale Unit (ský) í Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 84e70515accde161e7efa36755edec68d26be952
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092223"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Frumstilla Commerce Scale Unit (ský)

[!include[banner](../includes/banner.md)]

Þetta efni útskýrir hvernig á að frumstilla Commerce Scale Unit (ský) í Microsoft Dynamics 365 Commerce.

Ef þú ert að nota Tier-2 sandkassa eða framleiðsluumhverfi sem er með forritaútgáfu 8.1.2.x eða nýrri, verður þú að frumstilla Commerce Scale Unit (ský) áður en þú getur notað smásölurásarvirkni annað hvort fyrir sölustaða (POS) starfsemi eða fyrir rafræn viðskipti sem nota Retail Server í skýinu. Frumstilling mun dreifa viðskiptaskalaeiningu (skýi).

> [!IMPORTANT]
> Fyrir núverandi viðskiptavini sem nota smásölurásarvirkni í skýinu, til að tryggja áframhaldandi og óslitinn stuðning við fyrirtækið þitt, krefjumst við þess að þú uppfærir smásölurásirnar þínar til að nota Commerce Scale Unit. Nýtt umhverfi sem er notað án Commerce Scale Unit mun ekki lengur fá gæða- og þjónustuuppfærslur fyrir skýhýsta smásölurásarhluta. Engar aðgerða er krafist fyrir viðskiptavini sem nota eingöngu Commerce Scale Unit (sjálfhýst). Hafðu samband við Microsoft FastTrack lausnararkitektinn þinn ef þú þarft framlengingu.

## <a name="prerequisites"></a>Forkröfur

1. Settu upp Tier-2 sandkassa eða framleiðsluumhverfi sem hefur útgáfu 8.1.2.x eða nýrri.
2. Þú getur sjálfdreifað allt að 2 Commerce Scale Units í hverju umhverfi. Ef þú þarfnast fleiri en 2 Commerce Scale Units í hverju umhverfi, í Microsoft Dynamics Lifecycle Services (LCS), búðu til stuðningsbeiðni og sláðu inn **Beiðni um viðbótareiningu viðskiptaskala** og tilgreinið auðkenni umhverfisins, fjölda viðskiptakvarðaeininga og viðkomandi gagnaverasvæði. Beiðninni verður lokið innan fimm virkra daga. Ef þú þarft ekki meira en 2 Commerce Scale Units í hverju umhverfi þarftu ekki að búa til stuðningsbeiðni. 
3. Þú verður að hafa verkefniseigandaheimildir í Lifecycle Services áður en þú getur frumstillt Commerce Scale Unit.
4. Gakktu úr skugga um að stillingarlyklar fyrir smásöluleyfi séu virkir í umhverfi þínu. Fyrir frekari upplýsingar, sjá [Skýrsla um leyfiskóða og stillingarlykla](../sysadmin/license-codes-configuration-keys-report.md). Þú verður að hafa kveikt á eftirfarandi lyklum til að nota Commerce Scale Unit.

    - RetailBasic
    - RetaileCommerce - Ef þú ætlar að nota rafræn viðskipti fyrir Dynamics 365 Commerce.
    - RetailGiftCard - Ef þú ætlar að nota gjafakort.
    - RetailInvent - Ef þú ætlar að nota lager.
    - RetailModernPos - Ef þú ætlar að nota sölustað (POS).
    - RetailReplenishment - Ef þú ætlar að nota áfyllingar.
    - RetailScheduler
    - Smásöluverslanir - Ef þú ætlar að nota POS.


## <a name="region-availability"></a>Svæðisframboð
Commerce Scale Unit er fáanlegt til dreifingar á eftirfarandi svæðum.

| Staðsetning á heimsvísu | Svæði              | Framboð        |
|-----------------|---------------------|---------------------|
| BANDARÍKIN        | Austurhluti Bandaríkjanna             | Almennt tiltækt |
| BANDARÍKIN        | Austurhluti Bandaríkjanna 2           | Almennt tiltækt |
| BANDARÍKIN        | Norður- og miðríki Bandaríkjanna    | Almennt tiltækt |
| BANDARÍKIN        | Suður- og miðríki Bandaríkjanna    | Almennt tiltækt |
| BANDARÍKIN        | Miðríki Bandaríkjanna          | Almennt tiltækt |
| BANDARÍKIN        | Vesturhluti Bandaríkjanna             | Almennt tiltækt |
| BANDARÍKIN        | Vestur-Bandaríkin 2           | Almennt tiltækt |
| BANDARÍKIN        | Kanada Mið      | Takmarkað afkastageta    |
| BANDARÍKIN        | Kanada Austur         | Takmarkað afkastageta    |
| BANDARÍKIN        | Vestur Mið-Bandaríkin     | Takmarkað afkastageta    |
| APAC            | Austur-Ástralía      | Almennt tiltækt |
| APAC            | Suðaustur-Asía      | Almennt tiltækt |
| APAC            | Austur-Japan          | Almennt tiltækt |
| APAC            | Vestur-Japan          | Almennt tiltækt |
| APAC            | Suðaustur-Ástralía | Takmarkað afkastageta    |
| APAC            | Austur-Asía           | Takmarkað afkastageta    |
| APAC            | Indland suður         | Takmarkað afkastageta    |
| APAC            | Miðbær Indlands       | Takmarkað afkastageta    |
| EMEA            | Vestur-Evrópa         | Almennt tiltækt |
| EMEA            | Norður-Evrópa        | Almennt tiltækt |
| EMEA            | Bretland suður            | Takmarkað afkastageta    |
| EMEA            | Bretland vestur             | Takmarkað afkastageta    |

Dreifingargeta á svæðum með takmarkaða getu er mjög takmörkuð. Beiðnir um dreifingu eru metnar í hverju tilviki fyrir sig. Ef þú hefur sannfærandi viðskiptaþörf fyrir dreifingu á svæðum með takmarkaða afkastagetu geturðu lagt fram stuðningsbeiðni um að bætast á biðlistann.

![Kort sem sýnir framboð svæðis.](media/Commerce-Scale-Unit-Region-Availability.png "Kort sem sýnir framboð svæðis")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Frumstilla Commerce Scale Unit sem hluti af nýrri uppsetningu umhverfisins

Gakktu úr skugga um að höfuðstöðvarnar séu tiltækar. Þetta er nauðsynlegt til að skrá mælikvarðaeininguna hjá höfuðstöðvunum meðan á upphafsferlinu stendur. Ekki er mælt með því að frumstilla mælieiningu þegar höfuðstöðvarnar eru í þjónustu, þar sem hún gæti orðið ekki tiltæk á meðan á þjónustuferlinu stendur.

1. Gakktu úr skugga um að umhverfi höfuðstöðvanna sé tiltækt og ekki inni [Viðhaldsstilling](../sysadmin/maintenance-mode.md).
2. Í LCS, á upplýsingasíðu umhverfisins, veldu **Umhverfiseiginleikar \> Verslun**.
3. Á síðunni Uppsetning viðskiptauppsetningar velurðu **Frumstilla**.
4. Veldu útgáfu Commerce Scale Unit til að frumstilla.
5. Veldu svæði til að frumstilla Commerce Scale Unit í.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Stilltu rásir til að nota Commerce Scale Unit

Eftir að Commerce Scale Unit hefur verið dreift verður þú að tryggja að rásirnar þínar séu stilltar til að nota gagnagrunninn fyrir það. 

Til að stilla rásirnar þínar til að nota gagnagrunn Commerce Scale Unit skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Uppsetning höfuðstöðva \> Viðskiptaáætlun \> Rásar gagnagrunnur**.
1. Í vinstri glugganum skaltu velja rásargagnagrunn.
1. Á **Smásölurás** Flýtiflipi, veldu **Bæta við**, og veldu síðan smásölurásina þína í fellilistanum.
1. Veldu **Bæta við**, og veldu síðan netrásina þína í fellilistanum. 

Þegar þú ert búinn skaltu fara á **Verslun og verslun \> Upplýsingatækni í verslun og viðskiptum \> Dreifingaráætlun**, og keyra starf 9999.

> [!NOTE] 
> Job 9999 samstillir allar nýjar vörur og viðskiptavini við Commerce Scale Unit. Þetta ferli getur tekið langan tíma. Ef rásin verður að vera tiltæk bara fyrir uppsetningu e-verslunarsíðugerðar geturðu keyrt starf 1070 í stað vinnu 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Uppfærsla gagnagrunns og viðskiptakvarðaeiningar

Áður en þú byrjar skaltu ganga úr skugga um að þú þekkir til [Skref til að ljúka eftir endurnýjun gagnagrunns fyrir umhverfi sem nota viðskiptavirkni](../database/database-refresh.md).

Ekki er hægt að færa gagnagrunnsskrár mælieininga (á skjámynd Rásargagnagrunns) yfir umhverfi sem hluta af endurnýjun gagnagrunns. Þetta er vegna þess að færslurnar tákna umhverfissértæka uppsetningu.

Eftir endurnýjun gagnagrunns geturðu endurnýjað gagnagrunnsskrá mælikvarðaeiningarinnar með því að gefa út enduruppfærslu á mælieiningunni þinni í LCS. Allar dreifingar- eða þjónustuaðgerðir í vogareiningunni mun reyna að skrá vogareininguna hjá höfuðstöðvunum, ef skráningin er týnd.

Þú getur gefið út endurdreifingu á mælieiningunni, án þess að breyta neinum íhlutum, með því að velja að nota sömu útgáfuna sem mælieiningin þín er nú þegar á. Þetta er hægt að gera í LCS með eftirfarandi skrefum:

1. Í LCS, á upplýsingasíðu umhverfisins, veldu **Umhverfiseiginleikar \> Smásala**.
2. Á uppsetningardreifingarsíðunni skaltu velja mælikvarðaeininguna sem þú vilt endurútreiða.
3. Í aðgerðavalmynd kvarðaeiningarinnar velurðu **Uppfærsla**.
4. Á sleðann, á fellilistanum fyrir **Veldu útgáfu**, veldu valkostinn **Tilgreindu útgáfu**.
5. Á textareitnum undir **Tilgreindu útgáfu**, sláðu inn útgáfuna sem sýnd er fyrir kvarðaeininguna þína, sýnd fyrir utan **Núverandi útgáfa** merki.
6. Smelltu á **Uppfærsla** takki.

Þú þarft ekki að velja **Uppfærðu viðbætur**, jafnvel þótt þú hafir notað viðbætur áður, þar sem síðasti viðbótapakkinn sem notaður var á kvarðaeininguna er sjálfkrafa valinn þegar mælieining er uppfærð.

Ef þú ert með margar kvarðaeiningar þarftu að framkvæma aðgerðina hér að ofan fyrir hverja kvarðaeiningu. Þú getur framkvæmt þessar aðgerðir samhliða, ef þess er óskað.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Settu upp fleiri viðskiptakvarðaeiningar (valfrjálst)

Eftir að þú hefur frumstillt Commerce Scale Unit geturðu sjálfvirkt dreift annarri Scale Unit ef leyfið þitt veitir þér rétt til þess. Til að dreifa fleiri en tveimur mælieiningum verður þú að búa til stuðningsbeiðni. Í stuðningsbeiðninni skaltu tilgreina fjölda Commerce Scale Units sem þú þarfnast, heiti umhverfisins og viðkomandi svæði. Fyrir frekari upplýsingar um leyfisveitingar, sjá [Leyfisleiðbeiningar fyrir Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Fyrir hverja viðbótar Commerce Scale Unit sem þú setur upp mælum við með að þú stofnir sérstakan rásargagnagrunnshóp með því að fylgja þessum skrefum.

1. Í aðalskrifstofu Commerce, farðu til **Smásala og verslun >Retail Headquarters > Uppsetning smásöluáætlunar > Rásargagnagrunnshópur**.
2. Stofna nýjan gagnagrunnsflokk rásar.
3. Farðu í **Smásala og verslun >Retail Headquarters > Uppsetning smásöluáætlunar > Rásargagnagrunnur**, og veldu rásargagnagrunninn sem samsvarar nýstofnuðu Commerce Scale Unit.
4. Veldu **Breyta** og veldu nýja rásargagnagrunnshópinn.
5. Veldu **Vista**.
6. Veldu **Keyra fulla gagnasamstillingu** fyrir valinn rásargagnagrunn.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Viðbótarupplýsingar ef þú frumstillir verslunarrásaríhluti sem hýst er í skýi í núverandi umhverfi

Ef þú ert nú þegar að nota skýhýsta Commerce rásaríhluti í umhverfi mun frumstilling á Commerce Scale Unit hjálpa til við að draga úr niður í miðbæ þegar þessir íhlutir eru uppfærðir. Viðbótaráætlanagerð er nauðsynleg áður en Commerce Scale Unit er frumstillt.

Þegar þú frumstillir fyrstu Commerce Scale Unit í umhverfi sem notar skýhýst Commerce rás íhluti, mun frumstillingarferlið flytja rásirnar þínar sem tengjast skýhýstu rásaríhlutunum yfir í fyrstu mælikvarðaeininguna. Rásir sem tengjast Store Scale-einingum eru óbreyttar.

Flutningsferlið er gagnsætt fyrir rásirnar. Eftir að frumstilling mælieiningarinnar hefst eru eftirfarandi aðgerðir sjálfkrafa framkvæmdar:

1. Ný Commerce Scale Unit verður til og tengd umhverfinu.
2. The Commerce Scale Unit verður skráð sem tiltækur rásgagnagrunnur í höfuðstöðvunum.
3. Allar rásir kortlagðar á **Sjálfgefið** gagnagrunnur rása í höfuðstöðvunum verður uppfærður til að kortleggjast í nýja viðskiptaskalaeininguna.
4. A Commerce Data Exchange (CDX) full gagnasamstilling verður framkvæmd til að koma rásargögnunum yfir í nýju mælikvarðaeininguna.

**Skipulagning og prófun fyrir frumstillingu Commerce Scale Unit** Að jafnaði, þegar þú frumstillir Commerce Scale Unit, verður þú að skipuleggja fimm klukkustunda niðritíma fyrir verslunarrekstur sem og hvers kyns rafræn viðskipti sem nota Retail Server eða Cloud Point of Sale.

1. Framkvæmdu endurnýjun gagnagrunns úr framleiðsluumhverfi þínu yfir í sandkassa UAT umhverfi. 
2. Frumstilla Commerce Scale Unit í sandkassa UAT umhverfinu. 
3. Athugaðu upphafstímann sem á að ljúka fyrir Commerce Scale Unit. Þetta mun vera sambærilegt við þann tíma sem þessi aðgerð tekur í framleiðsluumhverfi þínu, þar sem verslunarrekstur og rafræn viðskipti verða ekki tiltæk.

Þú verður að framkvæma eftirfarandi viðbótarskref áður en þú frumstillir Commerce Scale Unit.

- **Lokaðu öllum POS vaktum** - Eftir flutning munu POS notendur ekki geta lokað neinum vöktum sem voru virkar á flutningsferlinu.
- **Staðfestu að öllum P-störfum hafi verið lokið** - Mælt er með því að P-störf til að samstilla færslur í bið hafi lokið áður en CSU er frumstillt.
- **Skráðu þig út úr öllum POS-tækjum** - POS aðgerðir eru ekki studdar meðan á flutningi stendur.
- **Innkalla og ógilda allar lokaðar færslur í POS** - Frestað viðskipti eru ekki varðveitt sem hluti af frumstillingunni.

> [!IMPORTANT]
> Sem hluti af frumstillingu Commerce Scale Unit munu fyrri stöðvuð viðskipti tapast og ekki er hægt að innkalla þær. 

Hér er það sem gerist á upphafstímabilinu:

- Skýhýstar viðskiptarásir virka ekki nema þú kveikir á POS offline getu.
- POS tæki með kveikt á nettengingu munu hafa skerta virkni.
- Allir viðskiptavinir rafrænna viðskipta sem eru háðir Retail Server verða fyrir truflunum.
- Rásir sem eru hýstar á Commerce Scale Units (sjálf-hýst) verða ekki fyrir áhrifum.
- Það hefur ekki áhrif á virkni aðalskrifstofunnar.

Hér er það sem gerist eftir að frumstillingu er lokið:

- Tækjavirkjunarstaða allra virkjaða POS-tækja er varðveitt, sem þýðir að ekki þarf að endurvirkja tækin.
- Sjálfstæðir vélbúnaðarstöðvar munu halda áfram að virka.
- Skýrslur POS rásar hliðar verða endurstilltar og munu ekki sýna gögn frá því fyrir frumstillingu.
- Sýna dagbókaraðgerð verður einnig endurstillt og mun ekki sýna gögn frá því fyrir frumstillingu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
