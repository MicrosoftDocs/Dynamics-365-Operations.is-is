---
title: Viðhaldsáætlanir
description: Þetta efni útskýrir viðhaldsáætlanir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09ae8b0ce56b08db0ba400b19676bd698c90a561
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500815"
---
# <a name="maintenance-plans"></a>Viðhaldsáætlanir

[!include [banner](../../includes/banner.md)]

Viðhaldsáætlun skilgreinir hvenær fyrirframskipulagt forvirkt viðhald á að fara fram á eign. Viðhaldsáætlanir geta verið tengdar eignum, eignategundum, virkum staðsetningum eða virkum staðartegundum, en fyrst býrðu til viðhaldsáætlanir sem nota á í fyrirtækinu.

Viðhaldsáætlun getur verið með margar viðhaldsáætlunarlínur. Tegund viðhaldsverks og bil eru tilgreind á viðhaldsáætlunarlínunni. Það eru tvenns konar línur viðhaldsáætlana:

- Tími
- Teljari

Línur viðhaldsáætlana af gerðinni „Tími“ eru notaðar til endurtekins áætlaðs viðhalds sem byggist á föstu tímabili. Línur viðhaldsáætlana af gerðinni „Teljari“ eru notaðar við áætlað viðhald eða viðbragðsviðhald byggt á eignateljaraskráningum. Viðhaldsáætlun getur innihaldið nokkrar viðhaldsáætlunarlínur af báðum gerðum.

>[!NOTE]
>Ef engin teljaragildi hafa verið skráð fyrir teljarategund á eign er viðhaldsáætlunarlínunum sleppt.

Fyrst býrðu til viðhaldsáætlanir sem þú þarft fyrir forvirk viðhaldsverk og velur eignategundir, eignir, gerðir virkra staðsetninga og virkar staðsetningar sem ættu að tengjast hverri viðhaldsáætlun. Eftir á, ef þörf krefur, er einnig hægt að bæta viðhaldsáætlunum við eign eða virka staðsetningu, sem er gert í flýtiflipanum **Allar eignir** \> velja eign \> **Viðhaldsáætlanir eignar** eða flýtiflipanum **Allar virkar staðsetningar** \> velja virka staðsetningu \> **Viðhaldsáætlanir**.

Ef þú bætir viðhaldsáætlun við eignategundir eða gerðir virkrar staðsetningar þýðir það að þegar þú býrð til nýjar eignir eða virkar staðsetningar með þessum eignategundum eða virkum staðartegundum verður eigninni eða virkri staðsetningu sjálfkrafa bætt við viðhaldsáætlunina. Upphafsdagur tengslum við viðhaldsáætlun verður núverandi dagsetning, sem gæti þurft að laga.

## <a name="set-up-maintenance-plans"></a>Setja upp viðhaldsáætlanir

Þessi hluti lýsir því hvernig á að setja upp viðhaldsáætlunarlínur og gefur dæmi um hvernig hægt er að nota þær.

1. Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.

1. Velja skal **Nýtt** til að búa til nýja röð.

1. Settu inn auðkenni í reitinn **Viðhaldsröð** og teljaraheiti í reitinn **Heiti**.

1. Í reitinn **Áætlunardagsetning** skaltu setja inn upphafsdagsetninguna sem hægt er að gera áætlun viðhaldsáætluninni frá. Athugaðu að tímabundnar viðhaldsáætlunarlínur geta verið með aðrar áætlunardagsetningar.

1. Veldu "Já" á skiptihnappnum **Virkt** til að virkja viðhaldsáætlun.

    >[!NOTE]
    >Ef slökkt er á viðhaldsáætlun verða engar bókanir tímasetninga stofnaðar í viðhaldsáætluninni þegar keyrt er tímasett verk viðhaldsáætlunar.

1. Reitirnir **Dagar vikmarka fyrir** og **Dagar vikmarka eftir** eiga við um línur viðhaldsáætlunar þar sem gátreiturinn **Fela viðhaldsverk sem skarast** er valinn (sjá skref 17). Reitirnir „Vikmörk“ eru notaðir til að lengja bilið á dögum þar sem, ef nokkrar viðhaldsáætlanir skarast, umfangsmesta / stærsta starfið er stofnað sem viðhaldsskemalína við tímasetningu viðhaldsáætlana, en tíðari verkum sem skarast er sleppt meðan á tímasetningu viðhaldsáætlunar stendur. Settu fjölda daga í reitinn **Vikmörk dögum áður**, til dæmis „2“.

1. Ef þú hefur sett gildi inn í **Vikmörk dögum áður** skaltu einnig setja inn fjölda daga í reitinn **Vikmörk dögum á eftir**, til dæmis „2“.

    >[!NOTE]
    >Dæmið sem lýst er í þessu skrefi og skrefinu á undan þýðir að ef nokkrar línur viðhaldsáætlunar skarast og **Fela viðhaldsverk sem skarast** er valið fyrir eina eða fleiri línur, verður tímabilið þar sem línum viðhaldsáætlunar er sleppt aukið um fimm daga (væntanleg upphafsdagsetning í línu viðhaldsáætlunar *og* tveir dagar fyrir *og* tveir dagar eftir þá dagsetningu).

1. Reitirnir í hópnum **Upplýsingar** á flýtiflipanum **Upplýsingar** sýnir fjölda viðhaldsáætlanalína sem settar eru upp í viðhaldsáætluninni, og fjölda eigna og virkra staðsetninga sem tengjast viðhaldsáætluninni.

1. Í flýtiflipanum **Línur** skal velja **Bæta við tímalínu** eða **Bæta við línu eignateljara** til að stofna nýja línu viðhaldsáætlunar.

1. Færið inn lýsingu á línunni í reitnum **Lýsing verkbeiðni**. Lýsingin er flutt yfir í skyldar verkbeiðnir.

1. Í reitnum **Tegund viðhaldsverka** velurðu gerð vinnslu sem viðhaldsáætlunarlínan tengist.

1. Í reitnum **Tegundaafbrigði viðhaldsverka** og **Viðskipti** skal velja afbrigðið og viðskiptin sem tengjast gerð viðhaldsverks.

1. Í reitunum **Ljúka innan daga** og **Ljúka innan klukkustunda** er hægt að setja inn áætlaða lokadagsetningu í dögum eða klukkustundum. Væntanlegur lokadagur er settur inn miðað við áætlaðan upphafsdag, sem reiknaður er þegar línur viðhaldsskema eru búnar til. Til dæmis er hægt að setja „7“ í reitinn **Ljúka innan daga** til að gefa til kynna að skyldri vinnslu skuli vera lokið innan viku frá áætluðum upphafsdegi.

1. Í reitnum **Gerð millibils** skaltu velja gerð bilsins sem á að nota á viðhaldsáætlunarlínunni, til dæmis, "Endurtekið..." eða "Einu sinni...". Sjá töfluna [Yfirlit millibilsgerða](#interval-types) hér að neðan til að lýsa tengslum á milli tegunda bila og línutegunda.

1. Reiturinn **Tímabil** snýr aðeins að tímatengdum línutegundum. Veldu tímabilsgerð sem tengist tíðnistímabilinu.

1. Í reitinn **Tímabilstíðni** skal setja inn fjölda skipta sem nota skal línuna til að skipuleggja forvirk viðhaldsverk. Dæmi: Ef þú hefur búið til línu af gerðinni "Teljari", og teljarinn þinn er framleiðslumagn, og þú setur inn númerið "20000" í þennan reit, eru nýjar viðhaldsraðarlínur búnar til við fyrirbyggjandi viðhaldsáætlun í hvert skipti sem þú ert búinn að framleiða 20.000 vörur í viðbót.

1. Gátreiturinn **Fela viðhaldsverk sem skarast** á við um tímamiðaðar jafnt sem talningarmiðaðar línugerðir. Veldu gátreitinn til að eyða færslum viðhaldsáætlana sem eru búnar til á sama degi. Þetta skiptir máli ef þú hefur til dæmis búið til 1 mánaða skoðunarlínu, 6 mánaða skoðunarlínu og 1 árs skoðunarlínu. Fyrir 1 árs skoðunina viltu aðeins að skoðunin verði gerð, ekki hinar tvær skoðanirnar, sem einnig passa inn í tímarammann. Til að hægt sé að setja upp þetta dæmi á réttan hátt skal setja upp eins árs eftirlitslínu sem fyrstu línuna, sex mánað línuna sem næstu línu og eins mánaðar línu sem þriðju línu og gátreiturinn **Fela viðhaldsverk sem skarast** er valinn fyrir eins mánaðar og sex mánaðar línurnar. Þannig tryggirðu að þegar þú nærð 1 árs merkinu er skoðunum í einn mánuð og sex mánuði sleppt og viðhaldsáætlunarlína er aðeins búin til fyrir 1 árs skoðunarlínu.

    >[!NOTE]
    >Dæmið sem lýst er í þessu skrefi sýnir að alltaf ætti að setja ítarlegasta starfið, sem inniheldur mesta fjölda verkefna og er ekki gert svo oft, sem fyrstu línuna. Tíðari vinnslurnar eru síðan settar inn sem aðskildar línur í röð tíðninnar og tíðasta vinnslan er sett neðst á listann.

1. Reiturinn **Teljari** snýr aðeins að teljaratengdum línutegundum. Veldu teljaragerð sem á að nota á línunni. Ef teljaragerð er ekki virk á tengdri eign er viðhaldsáætlunarlínunni sleppt.

1. Reiturinn **Tímamörk eignateljara í döum** snýr eingöngu að teljarabyggðum línutegundum. Settu inn tölu sem skilgreinir hve marga daga aftur í tímann teljaraskráningar eru athugaðar þegar tímasetning viðhaldsáætlunar er gerð. Þetta þýðir hversu langt aftur gögn (fyrirliggjandi teljaraskráningar) eru notuð sem grundvöllur til að reikna út þróunina sem ákvarðar hversu margar viðhaldsáætlunarlínur eru búnar til.

    >*Dæmi:* Ef búist er við að teljaraskráningar verði gerðar einu sinni í mánuði geturðu sett númerið '365' inn í þennan reit vegna þess að tímasetning viðhaldsáætlana mun alltaf byggjast á síðustu 12 mánuðum og búa því til viðhaldsáætlunarlínur út frá þróun síðasta árs. Aftur á móti, ef þú setur töluna '10' inn í þennan reit, þá býstu við að teljaraskráningar verði gerðar oftar, til dæmis daglega. Þetta þýðir að þegar þú skipuleggur viðhaldsáætlun eru teljaraskráningar síðustu 10 daga notaðar sem grunnur fyrir tímasetningu viðhaldsáætlunarlína.

1. Reiturinn **Áætlunardags.** snýr aðeins að tímatengdum línutegundum. Ef viðhaldsáætlunarlínan hefur annan áætlunardag en öll viðhaldsáætlunin skaltu velja dagsetningu í reitnum **Áætlunardagsetning** á línunni.

1. Í reitnum **Þjónustustig** geturðu valið þjónustustig verkbeiðni sem frekari afmörkun á viðhaldsáætlunarlínunni - til að nota sem þjónustustig í verkbeiðnum.

1. Veldu gátreitinn **Stofna sjálfkrafa** ef þú vilt að verkpöntun verði sjálfkrafa stofnuð samkvæmt valinni viðhaldsáætlunarlínu við tímasetningu viðhaldsáætlana.

1. Ef þú hefur valið gátreitinn **Stofna sjálfkrafa** er hægt að velja gerð verkpöntunar fyrir sjálfvirkt stofnaða verkbeiðni í reitnum **Gerð verkbeiðni**. Ef gátreiturinn **Stofna sjálfvirkt** er valinn og gerð verkbeiðni er ekki valin í þessum reit verður notuð gerð verkbeiðni sem valin er í reitnum **Eignastýring \> Uppsetning \> Færibreytur eignastýringar \> Verkbeiðnir** tengill \> **Fyrirbyggjandi verkbeiðnigerð**.

1. Notaðu reitina **Árstíð frá** og **Árstíð til** til að búa til endurtekna tímabundna viðhaldsáætlunarlínu innan 12 mánaða tímabils. *Dæmi:* Búnaður sem notaður er til að viðhalda grænum svæðum þarf þjónustu á hverju vori á fyrirframskilgreindu tímabili. Settu upphafsdagsetningu tímabilsins sem á að endurtaka í reitnum **Árstíð frá**.

1. Settu lokadagsetningu tímabilsins sem á að endurtaka í reitnum **Árstíð til**.

1. Í reitnum **Niðurstöðutímabil** er núverandi tímabil sem á að endurtaka sýnt. Þegar núverandi tímabil er liðið og þú byrjar nýtt ár verður tímabilið sem sýnt er í þessum reit uppfært til að endurspegla næsta tímabil í endurtekningarröðinni.

1. Á flýtiflipanum **Eignir** veldu þá eignir sem eiga að tengjast viðhaldsáætluninni.

1. Á flýtiflipanum **Eignagerðir** velurðu þær eignagerðir sem eiga að tengjast viðhaldsáætluninni.

1. Á flýtiflipanum **Virkar staðsetningar** velurðu þær virku staðsetningar sem eiga að tengjast viðhaldsáætluninni. Ef þess er krafist geturðu gert uppsetninguna nákvæmari með því að velja tengda eignategund, framleiðanda og tegund.

1. Á flýtiflipanum **Gerðir virkra staðsetninga** velurðu þær gerðir virkra staðsetninga sem eiga að tengjast viðhaldsáætluninni.

>[!NOTE]
>Þegar verkbeiðnir eru búnar til handvirkt á eignum sem falla undir ábyrgð lánadrottins er sýndur gluggi til að gera notandanum grein fyrir ábyrgðinni. Þá er hægt að hætta við að búa til verkbeiðnina. Hætt er við athugun á ábyrgðartengslum vegna verkbeiðna sem eru búnar til sjálfkrafa.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Yfirlit millibilsgerða

| Heiti og lýsing tímabils | Línugerð: Tími | Línugerð: Teljari |
|---|---|---|
| **Gerð millibils: Endurtekin frá áætlunardegi** Talningin byrjar frá áætlunardeginum sem notaður var. Þegar þú skipuleggur viðhaldsáætlanir eru viðhaldsáætlunarlínur stofnaðar þegar bilinu er náð. | **Áætlunardagsetningin** á viðhaldsáætlunarlínunni er notuð. Ef engin áætlunardagsetning er valin á línunni er **Áætlunardagsetningin** fyrir viðhaldsáætlun notuð. Dæmi: Ef númerið "3" er sett inn í reitinn **Tímabilstíðni** og „Ár“ er valið í reitnum **Tímabil** verður ný viðhaldsskemalína stofnuð á þriggja ára fresti. | **Áætlunardagsetningin** fyrir viðhaldsáætlunina er notuð. Ef skipt hefur verið um teljarann er nýjasta skiptidagsetningin notuð sem áætlunardagsetningin. |
| **Gerð millibils: Endurtekin frá upphafsdegi** Talningin hefst frá upphafsdegi eignatengslanna. Dagsetningin er valin í upplýsingayfirlitinu **Allar eignir** \> flýtiflipanum **Viðhaldsáætlanir eignar** \> reitnum **Upphafsdagsetning** eða í upplýsingayfirlitinu **Allar virkar staðsetningar** \> flýtiflipanum **Viðhaldsáætlanir** \> reitnum **Upphafsdagsetning**. Þegar þú skipuleggur viðhaldsáætlanir verður til viðhaldsáætlunarlína þegar bilinu er náð. | Upphafsdagur viðhaldsáætlunarlínunnar á eign eða virkri staðsetningu er notaður. Ef þessi reitur er auður er **Áætlunardagsetning** fyrir viðhaldsáætlun notuð. | Upphafsdagur viðhaldsáætlunarlínunnar á eign eða virkri staðsetningu er notaður. Ef þessi reitur er auður er **Áætlunardagsetning** fyrir viðhaldsáætlun notuð. |
| **Gerð millibils: Endurtekin úr síðustu verkbeiðni** Talningin byrjar frá raunverulegum lokadegi og -tíma síðustu verkbeiðni sem lokið var á eigninni með þeirri tilteknu samsetningu af gerð viðhaldsverks / gerðarafbrigðis viðhaldsverks / viðskipta. Sú dagsetning og tími eru sýnd í reitnum **Raunverulegur endir** í upplýsingasýninni **Allar verkbeiðnir**. | Raunverulegur lokadagur og tími verkbeiðni sem lokið er við eignina með þeirri tilteknu samsetningu af gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. Ef engin fullunnin verkbeiðni finnst er í staðinn notuð ein af dagsetningunum sem notaðar voru í bilgerðinni „Endurtekið frá upphafsdegi“ sem lýst er hér að ofan. | Raunverulegur lokadagur og tími verkbeiðni sem lokið er við eignina *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. er notað. Ef lokadagsetning og -tími var haft autt í verkbeiðninni er í staðinn notuð ein af dagsetningunum sem notaðar voru í bilgerðinni „Endurtekið frá upphafsdegi“ sem lýst er hér að ofan. |
| **Gerð millibils: Einu sinni frá áætlunardegi** Sjá lýsingu fyrir tímabilið „Endurtekið frá áætlunardegi“ hér að ofan. Eini munurinn er sá að þessi millibilsgerð er aðeins notuð einu sinni. | Sjá lýsingu fyrir „Endurtekið frá áætlunardegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. | Sjá lýsingu fyrir „Endurtekið frá áætlunardegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. **Athugasemd 1:** Þessi millibilsgerð skiptir aðeins máli ef skipt er um teljarann í hvert skipti sem þú annast viðhalds- eða þjónustustörf. Ef af einhverjum ástæðum hefur verið skipt um teljara fyrir lok fyrirhugaðs tíma er reiknaður nýr tími fyrir vinnsluna frá þeim tíma sem teljara var skipt út. **Athugasemd 2:** Ef skipt er um teljarann þegar lokið er við viðhalds- eða þjónustuvinnslu, þá virkar þessi millibilsgerð sem „Endurtekin frá áætlunardegi“ bilinu hér að ofan. |
| **Gerð millibils: Einu sinni frá upphafsdegi** Sjá lýsingu fyrir tímabilið „Endurtekið frá upphafsdegi“ hér að ofan. Eini munurinn er sá að þessi millibilsgerð er aðeins notuð einu sinni. | Sjá lýsingu fyrir „Endurtekið frá upphafsdegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. | Sjá lýsingu fyrir „Endurtekið frá upphafsdegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. **Athugasemd 1** hér að ofan á einnig við um þessa millibilsgerð. **Athugasemd 3:** Ef skipt er um teljarann þegar lokið er við viðhalds- eða þjónustuvinnslu, þá virkar þessi millibilsgerð sem „Endurtekin frá upphafsdegi“ bilinu hér að ofan. |
| **Gerð millibils: Þegar náð hér að ofan** Þessi bilstegund snýr aðeins að teljurum og er notuð til að gefa til kynna efri mörk sett upp á viðhaldsáætlunarlínunni. Færslur í viðhaldsskema verða með áætlaðan upphafsdag og -tíma teljaraskráningar, sem þýðir að þessar færslur verða búnar til með áætluðum upphafsdegi sem er jafnt og eða á undan kerfisdagsetningu. | Ekki tiltækt | Teljarabilið gefur til kynna efri mörk. Ef farið er yfir þessi mörk þegar þú býrð til teljaraskráningu verður til viðhaldsskemalína þegar þú áætlar forvirkt viðhald. |
| **Gerð millibils: Þegar náð hér að neðan** Þessi bilstegund snýr aðeins að teljurum og er notuð til að gefa til kynna neðri mörk sett upp á viðhaldsáætlunarlínunni. Færslur í viðhaldsskema verða með áætlaðan upphafsdag og -tíma teljaraskráningar, sem þýðir að þessar færslur verða búnar til með áætluðum upphafsdegi sem er jafnt og eða á undan kerfisdagsetningu. | Ekki tiltækt | Teljarabilið gefur til kynna neðri mörk. Ef farið er framyfir þessi mörk þegar þú býrð til teljaraskráningu verður til viðhaldsskemalína þegar þú áætlar forvirkt viðhald. |
| **Gerð millibils: Tengt frá upphafsdegi** Þessi millibilsgerð býr aðeins til viðhaldsáætlunarlínu einu sinni. Viðhaldsáætlun getur innihaldið fleiri línur viðhaldsáætlunar sem nota þessa millibilsgerð og þær línur eru tengdar. Venjulega muntu stofna viðhaldsáætlun sem inniheldur línur af aðeins þessu millibili. Viðhaldsskemalínur eru búnar til með því að bera kennsl á viðhaldsáætlunarlínuna sem hefur fyrsta áætlaðan upphafsdag og tíma. | Sjá lýsingu fyrir „Einu sinni frá upphafsdegi“ millibilsgerð hér að ofan. Dæmi: Þú býrð til tvær línur í viðhaldsáætlun fyrir þjónustuverk á bíl: eina tímamiðaða línu með 1 árs tímabili, og eina teljarabyggða línu með 25.000 km mark. Viðhaldsáætlunarlína er búin til fyrir mörkin sem nást fyrst. Fyrir þessa línugerð býrðu til línuna með 1 árs tímabilinu. | Sjá lýsingu fyrir „Einu sinni frá upphafsdegi“ millibilsgerð hér að ofan. Dæmi: Þú býrð til tvær línur í viðhaldsáætlun fyrir þjónustuverk á bíl: eina tímamiðaða línu með 1 árs tímabili, og eina teljarabyggða línu með 25.000 km mark. Viðhaldsáætlunarlína er búin til fyrir mörkin sem nást fyrst. Fyrir þessa línugerð býrðu til línuna með 25,000 km marki. Dæmi um stofnun tveggja teljaralína: Þú getur líka sett upp viðhaldsáætlun með tveimur tengdum, teljarasniðnum línum þar sem fyrsta línan er með 10.000 framleitt vörumagn og önnur línan snýr að vélinni eða vinnumiðstöðinni sem þarfnast þjónustu eftir keyrslu í 3.000 klukkustundir. |
| **Gerð millibils: Tengt úr síðustu verkbeiðni** Þessi millibilsgerð býr til nýjar viðhaldsáætlunarlínur eftir hverja fullunna vinnupöntun. Viðhaldsáætlun getur innihaldið fleiri línur sem nota þessa millibilsgerð og þær línur eru tengdar. Venjulega muntu stofna viðhaldsáætlun sem inniheldur línur viðhaldsáætlunar af aðeins þessu millibili. Viðhaldsskemalínur eru búnar til með því að bera kennsl á viðhaldsáætlunarlínuna sem hefur fyrsta áætlaðan upphafsdag og tíma. | Þessi millibilstegund virkar í grundvallaratriðum sem „Tengt frá upphafsdegi“ sem lýst er hér að ofan. Eini munurinn er dagsetningin sem gerð bils er byggð á. Notuð dagsetning er raundagsetning og -tími á síðustu verkbeiðni sem lokið er við á eigninni *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. | Þessi millibilstegund virkar í grundvallaratriðum sem „Tengt frá upphafsdegi“ sem lýst er hér að ofan. Eini munurinn er dagsetningin sem gerð bils er byggð á. Notuð dagsetning er raundagsetning og -tími á síðustu verkbeiðni sem lokið er við á eigninni *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. |
| **Gerð millibils: Endurtekið á uppsöfnuðu gildi (aðeins teljari)** Þegar viðhaldsáætlun er keyrð verður viðhaldsáætlunarlína stofnuð í hvert skipti sem uppsafnað gildi fyrir eignateljara nær upp í tímabilstíðnina eða margfeldi af henni. (Tímabilstíðni er skilgreind á línu viðhaldsáætlunar.)<p>Frekari upplýsingar um hvernig á að virkja og nota þessa virkni er að finna kaflanum [Viðbætur viðhalds sem byggir á teljara](#counter-based-maintenance) síðar í þessu efnisatriði. | Ekki tiltækt | **Dæmi:** Tímateljari er settur upp fyrir eign AK-101. Eignaáætlunarlína er einnig sett upp fyrir eignina. Millibilsgerð þessarar línu er *Endurtekið á uppsöfnuðu gildi (aðeins teljari)* og tímabilstíðnin er *1000*. Þegar viðhaldsáætlunin er keyrð er áætluð viðhaldslína búin til þegar samanlagt virði teljara er yfir 1.000 klukkustundir. Þegar uppsafnað gildi fyrir teljarann er umfram 2.000 stundir, verður til önnur lína viðhaldsáætlunar, og svo framvegis fyrir allar aðrar 1.000 klukkustundir. |
| **Gerð millibils: Einu sinni á uppsöfnuðu gildi (aðeins teljari)** Þegar viðhaldsáætlun er keyrð verður viðhaldsáætlunarlína stofnuð þegar uppsafnað gildi fyrir eignateljara nær upp í tímabilstíðnina sem skilgreind er í línu viðhaldsáætlunar.<p>Frekari upplýsingar um hvernig á að virkja og nota þessa virkni er að finna í [Viðbætur viðhalds sem byggir á teljara](#counter-based-maintenance). | Ekki tiltækt | **Dæmi:** Tímateljari er settur upp fyrir eign AK-101. Eignaáætlunarlína er einnig sett upp fyrir eignina. Millibilsgerð þessarar línu er *Einu sinni á uppsöfnuðu gildi (aðeins teljari)* og tímabilstíðnin er *1000*. Þegar viðhaldsáætlunin er keyrð er áætluð viðhaldslína búin til þegar samanlagt virði teljara er yfir 1.000 klukkustundir. |

>[!NOTE]
>Þegar viðhaldsskemalínur eru búnar til fyrir tímabundnar viðhaldsáætlunarlínur er áætlaður tími alltaf í byrjun dags. Fyrir teljarabyggðar viðhaldsáætlunarlínur getur áætlaðaður tími verið hvenær sem er á daginn.

Hér að neðan er að finna dæmi um uppsetningu tímabyggðra og teljarabyggðra viðhaldsáætlanalína:

**Dæmi 1 - Tímabyggð viðhaldsáætlunarlína:** Smurningarvinnslu má setja upp með föstu millibili sem kemur fyrir einu sinni í viku. Veldu í því skyni „Endurtekið frá áætlunardegi“ í reitnum **Gerð millibils**. Sjá dæmi í eftirfarandi mynd.

![Þjónustuverk sett upp á föstu tímabili, einu sinni í viku](media/02-preventive-maintenance.png "Þjónustuverk sett upp á föstu tímabili, einu sinni í viku")

**Dæmi 2 - Tímabundin viðhaldsáætlunarlína:** Heimilt er að setja upp skoðunarverk til að framkvæma um það bil einu sinni í viku. Veldu í því skyni „Endurtekið frá síðustu verkbeiðni“ í reitnum **Gerð millibils**. Sjá dæmi í eftirfarandi mynd.

![Eftirlitsverk sett upp framkvæmdar u.þ.b. einu sinni í viku](media/03-preventive-maintenance.png "Eftirlitsverk sett upp framkvæmdar u.þ.b. einu sinni í viku")

**Dæmi 3 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir klukkutímateljara sem ný viðhaldsskemalína er stofnuð fyrir í hvert skipti sem 250 klukkustundir eru liðnar. Millibilstegund fyrir þessa teljaralínu er „Endurtekin frá upphafsdegi“. Upphafsdagsetningin er upphafsdagsetning tengdra eigna í upplýsingayfirlitinu **Allar eignir** \> flýtiflipanum **Viðhaldsáætlanir eignar** \> reitnum **Upphafsdagsetning** eða í upplýsingayfirlitinu **Virk staðsetning** \> flýtiflipanum **Viðhaldsáætlanir** \> reitnum **Upphafsdagsetning**. Þetta er dæmi um *fyrirbyggjandi* viðhaldsáætlun vegna þess að viðhaldsskemalínan er sjálfkrafa búin til í hvert skipti sem þröskuldinum (+ 250) er náð.

![Tímateljari sem stofnar reglulega viðhaldsáætlunarlínur](media/04-preventive-maintenance.png "Tímateljari sem stofnar reglulega viðhaldsáætlunarlínur")

**Dæmi 4 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir lækkun á teljaravirði, sem mælir slit á hemlapúða. Viðhaldsskemalína er búin til þegar teljaraskráning undir 20 mm er búin til á bremsuklossanum. Bilið fyrir þessa teljarabyggðu línu er „Þegar náð að neðan“ eða „Einu sinni frá síðasta upphafsdegi“. Þetta er dæmi um *viðbragðs* viðhaldsáætlun vegna þess að viðhaldsskemalínan er ekki búin til í fyrr en mæling undir 20 mm er skráð.

![Lækkun á teljaragildi, mæling á sliti bremsuklossi](media/05-preventive-maintenance.png "Lækkun á teljaragildi, mæling á sliti bremsuklossa")

**Dæmi 5 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir teljara með þröskuldinn -18 ° á Celsíus. Viðhaldsskemalína er búin til þegar teljaraskráning yfir -18 ° á Celsius er gerð. Millibilstegund fyrir þessa teljaralínu er „Þegar náð fyrir ofan“. Þetta er dæmi um *viðbragðs* viðhaldsáætlun vegna þess að viðhaldsskemalínan er ekki búin til í fyrr en mæling sem er hærri en -18 á Celsius er skráð.

![Teljari með þröskuldi í -18° Celsius](media/06-preventive-maintenance.png "Teljari með þröskuldi í -18° Celsius")

- Þegar ný eign er stofnuð og sú eign notar eignagerð sem tengist viðhaldsáætlun, er viðhaldsáætlunin sjálfkrafa sett inn í flýtiflipann **Allir hlutir \> Viðhaldsáætlanir eignar**. Einnig, í **Sjálfgildi eignagerða**, á flýtiflipanum **Viðhaldsáætlanir**, verða skyldar viðhaldsáætlanir sjálfkrafa settar inn.
- Ef þú bætir við eða fjarlægir eignategundir eða gerðir virkra staðsetningar í **Viðhaldsáætlunum** mun sú breyting aðeins endurspegla nýjar eignir sem stofnað var til eftir að þú gerðir breytinguna.
- Ef eignum er bætt við eða fjarlægðar í **Viðhaldsáætlanir**, verður sú breyting sjálfkrafa uppfærð í flýtiflipanum **Allar eignir \> Viðhaldsáætlanir eignar** eða í flýtiflipanum **Allar virkar staðsetningar \> Viðhaldsáætlanir**.

Eftirfarandi mynd sýnir dæmi um viðhaldsáætlun „Vörubílaþjónusta“ á síðunni **Viðhaldsáætlanir**.

![Dæmi um viðhaldsáætlun vörubílaþjónustu](media/07-preventive-maintenance.png "Dæmi um viðhaldsáætlun vörubílaþjónustu")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Bættu viðhaldsáætlun við eign

1. Opnaðu **Eignastýringu \> Almennt \>Eignir \> Allar eignir** eða **Virkar eignir**.

1. Veljið eignina sem á að setja upp viðhaldsáætlun fyrir og veljið **Breyta**.

1. Í flýtiflipanum **Viðhaldsáætlanir eignar** skal velja **Bæta við línu** til að bæta viðhaldsáætlun við eignina.

1. Í reitnum **Viðhaldsáætlun** skaltu velja viðeigandi viðhaldsáætlun.

1. Í reitnum **Upphafsdagsetning** skaltu velja dagsetninguna sem hægt er að áætla forvirk viðhaldsverk frá. 

1. Veljið **Vista**. Reiturinn **Virkur** er sjálfkrafa uppfærður.

Eftirfarandi mynd sýnir dæmi um viðhaldsáætlanir settar upp á eign á síðunni **Allar eignir**.

![Dæmi um uppsetningu viðhaldsáætlana á eign](media/08-preventive-maintenance.png "Dæmi um uppsetningu viðhaldsáætlana á eign")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Viðbætur viðhalds sem byggir á teljara

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

*Viðbætur viðhalds sem byggir á teljara* eiginleiki kynnir eftirfarandi virkni:

- Valkosturinn til að setja sjálfkrafa inn teljara sem hefur gildið *0* (núll) þegar eign er stofnuð. Þessi valkostur getur komið að gagni þegar forspárviðhald er notað sem byggir á teljurum. Þegar eiginleikinn *Viðbætur viðhalds sem byggir á teljara* er ekki notaður, þarf að slá handvirkt inn teljara sem eru með gildið *0* (núll).
- Möguleikinn til að skilgreina teljara þannig að hann endurstilli sig sjálfkrafa þegar verkbeiðni er lokið. Þessi virkni er gagnleg þegar á að áætla viðhald út frá uppsöfnuðum gildum frá því að síðasta verkbeiðni var kláruð.
- Ný gerð af viðhaldsáætlunartímabili sem hefur heitið *Endurtekið á uppsöfnuðu gildi (aðeins teljari)*. Þessi gerð kveikir á viðhaldi í hvert sinn sem teljari nær stigvaxandi gildi. Til dæmis getur viðhald farið af stað á 10.000 klst. fresti. Frekari upplýsingar er að finna í [Yfirlit tímabilsgerða](#interval-types) fyrr í þessu efnisatriði.
- Önnur ný gerð af viðhaldsáætlunartímabili sem hefur heitið *Einu sinni á uppsöfnuðu gildi (aðeins teljari)*. Þessi gerð kveikir á viðhaldi þegar gildi teljara nær tilteknu gildi á borð við 8.000 klukkustundir. Sjá [Yfirlit tímabila](#interval-types) fyrir frekari upplýsingar

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Kveikja á eiginleika fyrir viðbætur viðhalds sem byggir á teljara

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining** *Kostnaðarstjórnun*
- **Heiti eiginleika:** *(Forskoðun) Viðbætur viðhalds sem byggir á teljara*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Stofna og frumstilla teljara þegar eign er stofnuð

Í hvert skipti sem eign er stofnuð er hægt að stofna sjálfkrafa eignateljara sem frumstilltir til að nota gildið *0* (núll), svo lengi sem kerfið er sett upp og eignin stofnuð á réttan hátt.

1. Opnaðu **Eignastýring \> Uppsetning \> Eignastýring**.
1. Gangið úr skugga um að eignagerð sé til staðar sem á við um nýja áætlaða eign. Stofna gerð eignar eins og nauðsynlegt er. Gangið úr skugga um að allir viðeigandi teljarar séu valdir á flýtiflipanum **Teljarar**.
1. Opnaðu **Eignastýringu \> Uppsetningu \> Færibreytur eignastýringar \> Teljarar**.
1. Fyrir hvern viðeigandi teljara skal ganga úr skugga um reiturinn **Heildarsamtala** sé stilltur á *Samtals*.
1. Stofnið eignina á síðunni **Allar eignir**.
1. Stillið reitnn **Eignagerð** á eignagerðina sem var tilgreind eða stofnuð í skrefi 2.
1. Ljúkið við að setja upp nýju eignina eins og nauðsynlegt er.
1. Fara í **Eignastjórnun \> Fyrirspurnir \> Eignir \> Teljarar**. Þú ættir að geta fundið frumstillta teljara sem settir eru upp fyrir nýju eignina.

> [!NOTE]
> Þegar frumstilltir eignateljarar eru stofnaðir er gert ráð fyrir að eignin hafi aldrei verið notuð áður en henni var bætt við kerfið. Þegar viðhaldsáætlunin er keyrð í fyrsta skipti notar útreikningurinn dagsetninguna og *0* (núll) teljaragildi sem grunnlínu til að reikna út viðhald í framtíðinni. Ef eignin var ekki ný þegar henni var bætt við kerfið er hægt að leiðrétta teljaragildið handvirkt þannig að það stemmi við raunverulegt teljaragildi. Til að leiðrétta teljaragildi skal opna tilheyrandi eign á síðunni **Allar eignir** og síðan á aðgerðasvæðinu í flipanum **Eign** í flokknum **Fyrirbyggjandi** skal velja **Teljarar**. Á síðunni **Eignateljarar** fyrir valda eign skal leiðrétta gildið í dálkinum **Gildi** fyrir upphaflega teljarafærslu eftir þörfum.

### <a name="automatically-reset-a-counter-value"></a>Endurstilla teljaragildi sjálfkrafa

Hægt er að skilgreina kerfið á að endurstilla teljara sjálfkrafa í hvert skipti sem viðkomandi verkbeiðni nær völdu stöðugildi.

1. Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.
1. Í listasvæðinu er viðhaldsáætlun valin. Endurstilling teljara gildir fyrir allar eignir sem nota þessa áætlun.
1. Í hlutanum **Línur** skal finna teljaralínu eignar sem á að endurstilla teljara fyrir og velja gátreitinn **Endurstilla teljara** fyrir þá línu. (Eignateljaralínur eru með gildi í dálknum **Teljandi**. Teljari sem er tilgreindur í þeim dálki er teljari sem verður endurstilltur fyrir viðeigandi eign.)
1. Farið í **Eignastýring \> Uppsetning \> Verkbeiðnir \> Líftímastöður**.
1. Í listasvæðinu skal velja líftímastöðu verkbeiðni sem endurstilla á viðeigandi teljara á.
1. Í flipanum **Almennt** skal stilla valkostinn **Endurstilla teljara** á *Já*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]