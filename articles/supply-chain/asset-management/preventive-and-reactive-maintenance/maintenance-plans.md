---
title: Viðhaldsáætlanir
description: Þetta efni útskýrir viðhaldsáætlanir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 28c00b5a2485ffcc01a316d2a39e7259fb563d1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430368"
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

Fyrst býrðu til viðhaldsáætlanir sem þú þarft fyrir forvirk viðhaldsverk og velur eignategundir, eignir, gerðir virkra staðsetninga og virkar staðsetningar sem ættu að tengjast hverri viðhaldsáætlun. Síðan, ef þess er krafist, geturðu einnig bætt viðhaldsáætlunum við eign eða virka staðsetningu, sem gert er í **Allar eignir** > velja eign > flýtiflipann **Viðhaldsáætlanir eigna** eða **Allar virkar staðsetningar** > velja virka staðsetningu > flýtiflipann **Viðhaldsáætlanir**.

Ef þú bætir viðhaldsáætlun við eignategundir eða gerðir virkrar staðsetningar þýðir það að þegar þú býrð til nýjar eignir eða virkar staðsetningar með þessum eignategundum eða virkum staðartegundum verður eigninni eða virkri staðsetningu sjálfkrafa bætt við viðhaldsáætlunina. Upphafsdagur tengslum við viðhaldsáætlun verður núverandi dagsetning, sem gæti þurft að laga.

## <a name="set-up-maintenance-plans"></a>Setja upp viðhaldsáætlanir

Þessi hluti lýsir því hvernig á að setja upp viðhaldsáætlunarlínur og gefur dæmi um hvernig hægt er að nota þær.

1. Smelltu á **Eignastjórnun** > **Uppsetning** > **Forvirkt viðhald** > **Viðhaldsáætlanir**.

2. Smellt er á **Ný** til að búa til nýja röð.

3. Settu inn auðkenni í reitinn **Viðhaldsröð** og teljaraheiti í reitinn **Heiti**.

4. Í reitinn **Áætlunardagsetning** skaltu setja inn upphafsdagsetninguna sem hægt er að gera áætlun viðhaldsáætluninni frá. Athugaðu að tímabundnar viðhaldsáætlunarlínur geta verið með aðrar áætlunardagsetningar.

5. Veldu "Já" á skiptihnappnum **Virkt** til að virkja viðhaldsáætlun.

>[!NOTE]
>Ef þú afvirkjar viðhaldsáætlun verða engir áætlunarpóstar stofnaðir í viðhaldsskemanu þegar þú keyrir tímasetninarvinnslu viðhaldsáætlunar.

6. Reitirnir **Vikmörk dögum áður** og **Vikmörk dögum á eftir** varða viðhaldsáætlunarlínur þar sem gátreiturinn **Þjappa viðhaldsverk sem skarast** er valinn (sjá skref 17). Reitirnir „Vikmörk“ eru notaðir til að lengja bilið á dögum þar sem, ef nokkrar viðhaldsáætlanir skarast, umfangsmesta / stærsta starfið er stofnað sem viðhaldsskemalína við tímasetningu viðhaldsáætlana, en tíðari verkum sem skarast er sleppt meðan á tímasetningu viðhaldsáætlunar stendur. Settu fjölda daga í reitinn **Vikmörk dögum áður**, til dæmis „2“.

7. Ef þú hefur sett gildi inn í **Vikmörk dögum áður** skaltu einnig setja inn fjölda daga í reitinn **Vikmörk dögum á eftir**, til dæmis „2“.

>[!NOTE]
>Dæmið sem lýst er í þessu og fyrra skrefi þýðir að ef nokkrar viðhaldsáætlunarlínur skarast, og **Þjappa viðhaldsverkum sem skarast** er valið fyrir eina eða fleiri línur er tímabilið þar sem viðhaldsskemalínum er sleppt framlengt í samtals fimm daga (áætlaður upphafsdagur á viðhaldsskemalínunni *og* tveimur dögum áður *og* tveimur dögum eftir þann dag).

8. Reitirnir í hópnum **Upplýsingar** á flýtiflipanum **Upplýsingar** sýnir fjölda viðhaldsáætlanalína sem settar eru upp í viðhaldsáætluninni, og fjölda eigna og virkra staðsetninga sem tengjast viðhaldsáætluninni.

9. Á flýtiflipanum **Línur** smellirðu á **Bæta við tímalínu** eða **Bæta við eignateljaralínu** til að búa til nýja viðhaldsáætlunarlínu.

10. Færið inn lýsingu á línunni í reitnum **Lýsing verkbeiðni**. Lýsingin er flutt yfir í skyldar verkbeiðnir.

11. Í reitnum **Tegund viðhaldsverka** velurðu gerð vinnslu sem viðhaldsáætlunarlínan tengist.

12. Í reitnum **Tegundaafbrigði viðhaldsverka** og **Viðskipti** skal velja afbrigðið og viðskiptin sem tengjast gerð viðhaldsverks.

13. Í reitunum **Ljúka innan daga** og **Ljúka innan klukkustunda** er hægt að setja inn áætlaða lokadagsetningu í dögum eða klukkustundum. Væntanlegur lokadagur er settur inn miðað við áætlaðan upphafsdag, sem reiknaður er þegar línur viðhaldsskema eru búnar til. Til dæmis er hægt að setja „7“ í reitinn **Ljúka innan daga** til að gefa til kynna að skyldri vinnslu skuli vera lokið innan viku frá áætluðum upphafsdegi.

14. Í reitnum **Gerð millibils** skaltu velja gerð bilsins sem á að nota á viðhaldsáætlunarlínunni, til dæmis, "Endurtekið..." eða "Einu sinni...". Sjá töfluna [Yfirlit millibilsgerða](## Interval types overview) hér að neðan til að lýsa tengslum á milli tegunda bila og línutegunda.

15. Reiturinn **Tímabil** snýr aðeins að tímatengdum línutegundum. Veldu tímabilsgerð sem tengist tíðnistímabilinu.

16. Í reitinn **Tímabilstíðni** skal setja inn fjölda skipta sem nota skal línuna til að skipuleggja forvirk viðhaldsverk. Dæmi: Ef þú hefur búið til línu af gerðinni "Teljari", og teljarinn þinn er framleiðslumagn, og þú setur inn númerið "20000" í þennan reit, eru nýjar viðhaldsraðarlínur búnar til við fyrirbyggjandi viðhaldsáætlun í hvert skipti sem þú ert búinn að framleiða 20.000 vörur í viðbót.

17. Gátreiturinn **Þjappa viðhaldsverk sem skarast** snýr að tímabyggðum sem og teljarabyggðum línutegundum. Veldu gátreitinn til að eyða færslum viðhaldsáætlana sem eru búnar til á sama degi. Þetta skiptir máli ef þú hefur til dæmis búið til 1 mánaða skoðunarlínu, 6 mánaða skoðunarlínu og 1 árs skoðunarlínu. Fyrir 1 árs skoðunina viltu aðeins að skoðunin verði gerð, ekki hinar tvær skoðanirnar, sem einnig passa inn í tímarammann. Til að setja upp þetta dæmi rétt setur þú upp 1 árs skoðunarlínu sem fyrstu línuna, 6 mánaða línuna sem aðra línuna og 1 mánaðar línuna sem þriðju línuna og þú velur gátreitinn **Þjappa viðhaldsverkum sem skarast** fyrir 1 mánaðar og 6 mánaða línur. Þannig tryggirðu að þegar þú nærð 1 árs merkinu er skoðunum í einn mánuð og sex mánuði sleppt og viðhaldsáætlunarlína er aðeins búin til fyrir 1 árs skoðunarlínu.

>[!NOTE]
>Dæmið sem lýst er í þessu skrefi sýnir að alltaf ætti að setja ítarlegasta starfið, sem inniheldur mesta fjölda verkefna og er ekki gert svo oft, sem fyrstu línuna. Tíðari vinnslurnar eru síðan settar inn sem aðskildar línur í röð tíðninnar og tíðasta vinnslan er sett neðst á listann.

18. Reiturinn **Teljari** snýr aðeins að teljaratengdum línutegundum. Veldu teljaragerð sem á að nota á línunni. Ef teljaragerð er ekki virk á tengdri eign er viðhaldsáætlunarlínunni sleppt.

19. Reiturinn **Tímamörk eignateljara í döum** snýr eingöngu að teljarabyggðum línutegundum. Settu inn tölu sem skilgreinir hve marga daga aftur í tímann teljaraskráningar eru athugaðar þegar tímasetning viðhaldsáætlunar er gerð. Þetta þýðir hversu langt aftur gögn (fyrirliggjandi teljaraskráningar) eru notuð sem grundvöllur til að reikna út þróunina sem ákvarðar hversu margar viðhaldsáætlunarlínur eru búnar til.

>*Dæmi:* Ef búist er við að teljaraskráningar verði gerðar einu sinni í mánuði geturðu sett númerið '365' inn í þennan reit vegna þess að tímasetning viðhaldsáætlana mun alltaf byggjast á síðustu 12 mánuðum og búa því til viðhaldsáætlunarlínur út frá þróun síðasta árs. Aftur á móti, ef þú setur töluna '10' inn í þennan reit, þá býstu við að teljaraskráningar verði gerðar oftar, til dæmis daglega. Þetta þýðir að þegar þú skipuleggur viðhaldsáætlun eru teljaraskráningar síðustu 10 daga notaðar sem grunnur fyrir tímasetningu viðhaldsáætlunarlína.

20. Reiturinn **Áætlunardags.** snýr aðeins að tímatengdum línutegundum. Ef viðhaldsáætlunarlínan hefur annan áætlunardag en öll viðhaldsáætlunin skaltu velja dagsetningu í reitnum **Áætlunardagsetning** á línunni.

21. Í reitnum **Þjónustustig** geturðu valið þjónustustig verkbeiðni sem frekari afmörkun á viðhaldsáætlunarlínunni - til að nota sem þjónustustig í verkbeiðnum.

22. Veldu gátreitinn **Stofna sjálfkrafa** ef þú vilt að verkpöntun verði sjálfkrafa stofnuð samkvæmt valinni viðhaldsáætlunarlínu við tímasetningu viðhaldsáætlana.

23. Ef þú hefur valið gátreitinn **Stofna sjálfkrafa** er hægt að velja gerð verkpöntunar fyrir sjálfvirkt stofnaða verkbeiðni í reitnum **Gerð verkbeiðni**. Ef þú hefur valið gátreitinn **Stofna sjálfkrafa** og þú velur ekki verkpöntunargerð í þessum reit er verkbeiðnigerðin sem var valin í tenglinum **Eignastýring** > **Uppsetning** > **Færibreytur eignastjórnunar** > **Verkbeiðnir** > reitnum **Gerð fyrirbyggjandi verkbeiðni** notaður.

24. Notaðu reitina **Árstíð frá** og **Árstíð til** til að búa til endurtekna tímabundna viðhaldsáætlunarlínu innan 12 mánaða tímabils. *Dæmi:* Búnaður sem notaður er til að viðhalda grænum svæðum þarf þjónustu á hverju vori á fyrirframskilgreindu tímabili. Settu upphafsdagsetningu tímabilsins sem á að endurtaka í reitnum **Árstíð frá**.

25. Settu lokadagsetningu tímabilsins sem á að endurtaka í reitnum **Árstíð til**.

26. Í reitnum **Niðurstöðutímabil** er núverandi tímabil sem á að endurtaka sýnt. Þegar núverandi tímabil er liðið og þú byrjar nýtt ár verður tímabilið sem sýnt er í þessum reit uppfært til að endurspegla næsta tímabil í endurtekningarröðinni.

27. Á flýtiflipanum **Eignir** veldu þá eignir sem eiga að tengjast viðhaldsáætluninni.

28. Á flýtiflipanum **Eignagerðir** velurðu þær eignagerðir sem eiga að tengjast viðhaldsáætluninni.

29. Á flýtiflipanum **Virkar staðsetningar** velurðu þær virku staðsetningar sem eiga að tengjast viðhaldsáætluninni. Ef þess er krafist geturðu gert uppsetninguna nákvæmari með því að velja tengda eignategund, framleiðanda og tegund.

30. Á flýtiflipanum **Gerðir virkra staðsetninga** velurðu þær gerðir virkra staðsetninga sem eiga að tengjast viðhaldsáætluninni.

>[!NOTE]
>Þegar verkbeiðnir eru búnar til handvirkt á eignum sem falla undir ábyrgð lánadrottins er sýndur gluggi til að gera notandanum grein fyrir ábyrgðinni. Þá er hægt að hætta við að búa til verkbeiðnina. Hætt er við athugun á ábyrgðartengslum vegna verkbeiðna sem eru búnar til sjálfkrafa.

## <a name="interval-types-overview"></a>Yfirlit millibilsgerða

| Gerð millibils og lýsing                                                                                                                                                                                                                                                                                                                                                                                                       | Línugerð: Tími                                                                                                                                                                                                                                                                                                                                                           | Línugerð: Teljari                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Gerð millibils: Endurtekin frá áætlunardegi** Talningin byrjar frá áætlunardeginum sem notaður var. Þegar þú skipuleggur viðhaldsáætlanir eru viðhaldsáætlunarlínur stofnaðar þegar bilinu er náð.                                                                                                                                                                                                                | **Áætlunardagsetningin** á viðhaldsáætlunarlínunni er notuð. Ef engin áætlunardagsetning er valin á línunni er **Áætlunardagsetningin** fyrir viðhaldsáætlun notuð. Dæmi: Ef númerið "3" er sett inn í reitinn **Tímabilstíðni** og „Ár“ er valið í reitnum **Tímabil** verður ný viðhaldsskemalína stofnuð á þriggja ára fresti.                             | **Áætlunardagsetningin** fyrir viðhaldsáætlunina er notuð. Ef skipt hefur verið um teljarann er nýjasta skiptidagsetningin notuð sem áætlunardagsetningin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Gerð millibils: Endurtekin frá upphafsdegi** Talningin hefst frá upphafsdegi eignatengslanna. Dagsetningin er valin í upplýsingasýninni **Allar eignir** > flýtiflipanum **Viðhaldsáætlanir eigna** > reitnum **Upphafsdagur**, eða í upplýsingasýninni **Allir virkir staðir** > flýtiflipanum **Viðhaldsáætlanir** > reitnum **Upphafsdagur**. Þegar þú skipuleggur viðhaldsáætlanir verður til viðhaldsáætlunarlína þegar bilinu er náð. | Upphafsdagur viðhaldsáætlunarlínunnar á eign eða virkri staðsetningu er notaður. Ef þessi reitur er auður er **Áætlunardagsetning** fyrir viðhaldsáætlun notuð.                                                                                                                                                                                                 | Upphafsdagur viðhaldsáætlunarlínunnar á eign eða virkri staðsetningu er notaður. Ef þessi reitur er auður er **Áætlunardagsetning** fyrir viðhaldsáætlun notuð.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Gerð millibils: Endurtekin úr síðustu verkbeiðni** Talningin byrjar frá raunverulegum lokadegi og -tíma síðustu verkbeiðni sem lokið var á eigninni með þeirri tilteknu samsetningu af gerð viðhaldsverks / gerðarafbrigðis viðhaldsverks / viðskipta. Sú dagsetning og tími eru sýnd í reitnum **Raunverulegur endir** í upplýsingasýninni **Allar verkbeiðnir**.                                                                                                                                 | Raunverulegur lokadagur og tími verkbeiðni sem lokið er við eignina með þeirri tilteknu samsetningu af gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. Ef engin fullunnin verkbeiðni finnst er í staðinn notuð ein af dagsetningunum sem notaðar voru í bilgerðinni „Endurtekið frá upphafsdegi“ sem lýst er hér að ofan.                                                                                             | Raunverulegur lokadagur og tími verkbeiðni sem lokið er við eignina *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti. er notað. Ef lokadagsetning og -tími var haft autt í verkbeiðninni er í staðinn notuð ein af dagsetningunum sem notaðar voru í bilgerðinni „Endurtekið frá upphafsdegi“ sem lýst er hér að ofan.                                                                                                                                                                                                                                                                                                                                                                           |
| **Gerð millibils: Einu sinni frá áætlunardegi** Sjá lýsingu fyrir tímabilið „Endurtekið frá áætlunardegi“ hér að ofan. Eini munurinn er sá að þessi millibilsgerð er aðeins notuð einu sinni.                                                                                                                                                                                                                                                   | Sjá lýsingu fyrir „Endurtekið frá áætlunardegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf.                                                                                                                                                                                                                             | Sjá lýsingu fyrir „Endurtekið frá áætlunardegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. **Athugasemd 1:** Þessi millibilsgerð skiptir aðeins máli ef skipt er um teljarann í hvert skipti sem þú annast viðhalds- eða þjónustustörf. Ef af einhverjum ástæðum hefur verið skipt um teljara fyrir lok fyrirhugaðs tíma er reiknaður nýr tími fyrir vinnsluna frá þeim tíma sem teljara var skipt út. **Athugasemd 2:** Ef skipt er um teljarann þegar lokið er við viðhalds- eða þjónustuvinnslu, þá virkar þessi millibilsgerð sem „Endurtekin frá áætlunardegi“ bilinu hér að ofan.                                             |
| **Gerð millibils: Einu sinni frá upphafsdegi** Sjá lýsingu fyrir tímabilið „Endurtekið frá upphafsdegi“ hér að ofan. Eini munurinn er sá að þessi millibilsgerð er aðeins notuð einu sinni.                                                                                                                                                                                                                                                 | Sjá lýsingu fyrir „Endurtekið frá upphafsdegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf.                                                                                                                                                                                                                            | Sjá lýsingu fyrir „Endurtekið frá upphafsdegi“ millibilsgerð hér að ofan. Þetta bil er venjulega notað í stök viðhalds- eða þjónustustörf. **Athugasemd 1** hér að ofan á einnig við um þessa millibilsgerð. **Athugasemd 3:** Ef skipt er um teljarann þegar lokið er við viðhalds- eða þjónustuvinnslu, þá virkar þessi millibilsgerð sem „Endurtekin frá upphafsdegi“ bilinu hér að ofan.                                                                                                                                                                                                                                                                                                |
| **Gerð millibils: Þegar náð hér að ofan** Þessi bilstegund snýr aðeins að teljurum og er notuð til að gefa til kynna efri mörk sett upp á viðhaldsáætlunarlínunni. Færslur í viðhaldsskema verða með áætlaðan upphafsdag og -tíma teljaraskráningar, sem þýðir að þessar færslur verða búnar til með áætluðum upphafsdegi sem er jafnt og eða á undan kerfisdagsetningu.                                                | Á ekki við                                                                                                                                                                                                                                                                                                                                                                       | Teljarabilið gefur til kynna efri mörk. Ef farið er yfir þessi mörk þegar þú býrð til teljaraskráningu verður til viðhaldsskemalína þegar þú áætlar forvirkt viðhald.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Gerð millibils: Þegar náð hér að neðan** Þessi bilstegund snýr aðeins að teljurum og er notuð til að gefa til kynna neðri mörk sett upp á viðhaldsáætlunarlínunni. Færslur í viðhaldsskema verða með áætlaðan upphafsdag og -tíma teljaraskráningar, sem þýðir að þessar færslur verða búnar til með áætluðum upphafsdegi sem er jafnt og eða á undan kerfisdagsetningu.                                                 | Á ekki við                                                                                                                                                                                                                                                                                                                                                                       | Teljarabilið gefur til kynna neðri mörk. Ef farið er framyfir þessi mörk þegar þú býrð til teljaraskráningu verður til viðhaldsskemalína þegar þú áætlar forvirkt viðhald.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Gerð millibils: Tengt frá upphafsdegi** Þessi millibilsgerð býr aðeins til viðhaldsáætlunarlínu einu sinni. Viðhaldsáætlun getur innihaldið fleiri línur viðhaldsáætlunar sem nota þessa millibilsgerð og þær línur eru tengdar. Venjulega muntu stofna viðhaldsáætlun sem inniheldur línur af aðeins þessu millibili. Viðhaldsskemalínur eru búnar til með því að bera kennsl á viðhaldsáætlunarlínuna sem hefur fyrsta áætlaðan upphafsdag og tíma.                                                                                                                                                                                                                                                                                                                                                                                           | Sjá lýsingu fyrir „Einu sinni frá upphafsdegi“ millibilsgerð hér að ofan. Dæmi: Þú býrð til tvær línur í viðhaldsáætlun fyrir þjónustuverk á bíl: eina tímamiðaða línu með 1 árs tímabili, og eina teljarabyggða línu með 25.000 km mark. Viðhaldsáætlunarlína er búin til fyrir mörkin sem nást fyrst. Fyrir þessa línugerð býrðu til línuna með 1 árs tímabilinu.                                                                                                                                                                                   | Sjá lýsingu fyrir „Einu sinni frá upphafsdegi“ millibilsgerð hér að ofan. Dæmi: Þú býrð til tvær línur í viðhaldsáætlun fyrir þjónustuverk á bíl: eina tímamiðaða línu með 1 árs tímabili, og eina teljarabyggða línu með 25.000 km mark. Viðhaldsáætlunarlína er búin til fyrir mörkin sem nást fyrst. Fyrir þessa línugerð býrðu til línuna með 25,000 km marki. Dæmi um stofnun tveggja teljaralína: Þú getur líka sett upp viðhaldsáætlun með tveimur tengdum, teljarasniðnum línum þar sem fyrsta línan er með 10.000 framleitt vörumagn og önnur línan snýr að vélinni eða vinnumiðstöðinni sem þarfnast þjónustu eftir keyrslu í 3.000 klukkustundir.                                                                                                                                                           |
| **Gerð millibils: Tengt úr síðustu verkbeiðni** Þessi millibilsgerð býr til nýjar viðhaldsáætlunarlínur eftir hverja fullunna vinnupöntun. Viðhaldsáætlun getur innihaldið fleiri línur sem nota þessa millibilsgerð og þær línur eru tengdar. Venjulega muntu stofna viðhaldsáætlun sem inniheldur línur viðhaldsáætlunar af aðeins þessu millibili. Viðhaldsskemalínur eru búnar til með því að bera kennsl á viðhaldsáætlunarlínuna sem hefur fyrsta áætlaðan upphafsdag og tíma.                                                                                                                                                                                                                                                                        | Þessi millibilstegund virkar í grundvallaratriðum sem „Tengt frá upphafsdegi“ sem lýst er hér að ofan. Eini munurinn er dagsetningin sem gerð bils er byggð á. Notuð dagsetning er raundagsetning og -tími á síðustu verkbeiðni sem lokið er við á eigninni *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti.                                                                                                                                                                                                                                                           | Þessi millibilstegund virkar í grundvallaratriðum sem „Tengt frá upphafsdegi“ sem lýst er hér að ofan. Eini munurinn er dagsetningin sem gerð bils er byggð á. Notuð dagsetning er raundagsetning og -tími á síðustu verkbeiðni sem lokið er við á eigninni *og* samsetninguna gerð viðhaldsverks / gerðarafbrigði viðhaldsverks / viðskipti.                                                                                                                   |


>[!NOTE]
>Þegar viðhaldsskemalínur eru búnar til fyrir tímabundnar viðhaldsáætlunarlínur er áætlaður tími alltaf í byrjun dags. Fyrir teljarabyggðar viðhaldsáætlunarlínur getur áætlaðaður tími verið hvenær sem er á daginn.

Hér að neðan er að finna dæmi um uppsetningu tímabyggðra og teljarabyggðra viðhaldsáætlanalína:

**Dæmi 1 - Tímabyggð viðhaldsáætlunarlína:** Smurningarvinnslu má setja upp með föstu millibili sem kemur fyrir einu sinni í viku. Veldu í því skyni „Endurtekið frá áætlunardegi“ í reitnum **Gerð millibils**. Sjá dæmi í eftirfarandi mynd.

![Mynd 1](media/02-preventive-maintenance.png)

**Dæmi 2 - Tímabundin viðhaldsáætlunarlína:** Heimilt er að setja upp skoðunarverk til að framkvæma um það bil einu sinni í viku. Veldu í því skyni „Endurtekið frá síðustu verkbeiðni“ í reitnum **Gerð millibils**. Sjá dæmi í eftirfarandi mynd.

![Mynd 2](media/03-preventive-maintenance.png)

**Dæmi 3 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir klukkutímateljara sem ný viðhaldsskemalína er stofnuð fyrir í hvert skipti sem 250 klukkustundir eru liðnar. Millibilstegund fyrir þessa teljaralínu er „Endurtekin frá upphafsdegi“. Upphafsdagsetningin er upphafsdagur tengdra eigna í upplýsingasýninni **Allar eignir** > flýtiflipanum **Viðhaldsáætlanir eigna** > reitnum **Upphafsdagur**, eða í upplýsingasýninni **Virk staðsetning** > flýtiflipanum **Viðhaldsáætlanir** > reitnum **Upphafsdagur**. Þetta er dæmi um *fyrirbyggjandi* viðhaldsáætlun vegna þess að viðhaldsskemalínan er sjálfkrafa búin til í hvert skipti sem þröskuldinum (+ 250) er náð.

![Mynd 3](media/04-preventive-maintenance.png)


**Dæmi 4 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir lækkun á teljaravirði, sem mælir slit á hemlapúða. Viðhaldsskemalína er búin til þegar teljaraskráning undir 20 mm er búin til á bremsuklossanum. Bilið fyrir þessa teljarabyggðu línu er „Þegar náð að neðan“ eða „Einu sinni frá síðasta upphafsdegi“. Þetta er dæmi um *viðbragðs* viðhaldsáætlun vegna þess að viðhaldsskemalínan er ekki búin til í fyrr en mæling undir 20 mm er skráð.

![Mynd 4](media/05-preventive-maintenance.png)


**Dæmi 5 - Teljarabyggð viðhaldsáætlunarlína:** Eftirfarandi myndræn skýringarmynd sýnir teljara með þröskuldinn -18 ° á Celsíus. Viðhaldsskemalína er búin til þegar teljaraskráning yfir -18 ° á Celsius er gerð. Millibilstegund fyrir þessa teljaralínu er „Þegar náð fyrir ofan“. Þetta er dæmi um *viðbragðs* viðhaldsáætlun vegna þess að viðhaldsskemalínan er ekki búin til í fyrr en mæling sem er hærri en -18 á Celsius er skráð.

![Mynd 5](media/06-preventive-maintenance.png)

- Þegar þú býrð til nýja eign og sú eign notar eignategund sem tengist viðhaldsáætlun er viðhaldsáætlunin sjálfkrafa sett inn í **Allir hlutir** > **Viðhaldáætlanir eigna** flýtiflipanum. Einnig, í **Sjálfgildi eignagerða**, á flýtiflipanum **Viðhaldsáætlanir**, verða skyldar viðhaldsáætlanir sjálfkrafa settar inn.  
- Ef þú bætir við eða fjarlægir eignategundir eða gerðir virkra staðsetningar í **Viðhaldsáætlunum** mun sú breyting aðeins endurspegla nýjar eignir sem stofnað var til eftir að þú gerðir breytinguna.  
- Ef þú bætir við eða fjarlægir eignir eða virkar staðsetningar í **Viðhaldsáætlanir**, verður sú breyting sjálfkrafa uppfærð í **Allar eignir** > **Viðhald eigna** flýtiflipanum, eða í **Allar virkar staðsetningar** > **Viðhaldsáætlanir** flýtiflipanum.  

Eftirfarandi mynd sýnir dæmi um viðhaldsáætlun „Vörubílaþjónusta“ á síðunni **Viðhaldsáætlanir**.

![Mynd 6](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>Bættu viðhaldsáætlun við eign

1. Smelltu á **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir** eða **Virkar eignir**.

2. Veldu eignina sem þú vilt setja upp viðhaldsáætlun á og smelltu á **Breyta**.

3. Á flýtiflipanum **Viðhaldsáætlanir eigna** velurðu **Bæta við línu** til að bæta við viðhaldsáætlun við eignina.

4. Í reitnum **Viðhaldsáætlun** skaltu velja viðeigandi viðhaldsáætlun.

5. Í reitnum **Upphafsdagsetning** skaltu velja dagsetninguna sem hægt er að áætla forvirk viðhaldsverk frá. 

6. Smellt er á **Vista**. Reiturinn **Virkur** er sjálfkrafa uppfærður.

Eftirfarandi mynd sýnir dæmi um viðhaldsáætlanir settar upp á eign á síðunni **Allar eignir**.

![Mynd 7](media/08-preventive-maintenance.png)

