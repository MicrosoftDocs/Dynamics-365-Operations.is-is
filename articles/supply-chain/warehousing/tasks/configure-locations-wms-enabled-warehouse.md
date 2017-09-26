--- 
title: "Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi"
description: "Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 044da854273345877be92c9eab787f4edf0bba5b
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli). Ferlið er yfirleitt gert af stjórnanda vöruhúss. Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF eða í eigin gögnum. Forkröfur eru að minnsta kosti eitt svæði sé grunnstillt.


## <a name="create-a-new-warehouse"></a>Stofna nýtt vöruhús
1. Fara í Vöruhús.
2. Smellið á „Nýtt“.
3. Í reitinn vöruhús skal slá inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Svæði skal slá inn gildi.
6. Stækka eða fella saman hlutann Vöruhús.
7. Stilltu valkostinn Nota ferli vöruhúsastjórnunar á Já.
    * Þessi stilling leyfir þér að keyra ítarleg vöruhúsaferli með því að nota vöruhúsavinnu og fartæki.  
8. Lokið síðunni.

## <a name="define-a-location-format"></a>Skilgreina snið staðsetningar
1. Fara á staðsetningarsnið.
    * Staðsetningarsnið eru nafngiftarkerfi sem eru notuð til að stofna einkvæm og samræmd heiti fyrir aðrar staðsetningu karfa stöður notað innan vöruhúss. Það getur verið gagnlegt að nota skiltákn sem hluta af staðsetningarsniði til að auðvelda auðkenningu íhluta staðsetningar eins og númer gangs. Í þessu dæmi stofnum við heiti með fjórum íhlutum. Til dæmis, þetta gæti verið gangur, rekki, hilla og karfa.  
2. Smellið á „Nýtt“.
3. Í reitinn staðsetningarsnið skal slá inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Lýsing hluta skal slá inn gildi.
    * Það lýsir því fyrir hvað fyrsti íhluti heitis staðsetningar stendur. Til dæmis, gæti það verið Gangur.  
6. Í reitinn Lengd skal slá inn númer.
    * Þetta ákvarðar hversu margir stafir verða að vera í þessum hluta af nafni staðsetningar. Athugið að samtala allra íhluta í heiti, þar á meðal skiltákn, má ekki fara yfir 10 staftákn.  
7. Í reitinn Skiltákn skal slá inn gildi.
    * Þetta ákveður hvaða stafur eða tákn er notað á milli fyrsta og annars íhluta í heiti.  
8. Smellið á „Nýtt“.
9. Í reitinn Lýsing hluta skal slá inn gildi.
10. Í reitinn Lengd skal slá inn númer.
11. Í reitinn Skiltákn skal slá inn gildi.
12. Smellt er á Nýtt.
13. Í reitinn Lýsing hluta skal slá inn gildi.
14. Í reitinn Lengd skal slá inn númer.
15. Í reitinn Skiltákn skal slá inn gildi.
16. Smellt er á Nýtt.
17. Í reitinn Lýsing hluta skal slá inn gildi.
18. Í reitinn Lengd skal slá inn númer.
19. Smellið á „Vista“.
20. Lokið síðunni.

## <a name="define-location-types"></a>Skilgreina staðsetningagerðir
1. Fara í Gerðir staðsetninga.
    * Hægt er að nota gerðir staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Sem lágmark þarf að stofna staðsetningagerðir sviðsetninga og endanlegra sendinga til að skilgreina stjórnunarferli á útleið í vöruhúsi.  
2. Smellið á „Nýtt“.
3. Í reitinn Gerð staðsetningar skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Lokið síðunni.

## <a name="define-location-profile"></a>Skilgreina forstillingu staðsetningar
1. Fara í Forstillingar staðsetningar.
    * Skilgreining á forstillingum staðsetningar er mjög mikilvæg. Hægt er að stýra afkastagetu flokkaðra staðsetninga hér, ásamt reglum sem tengjast hvaða birgðir eru vistaðar og hvernig þær eru vistaðar. Hægt er að nota forstillingar staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Sem lágmark verður að stofna forstillingu fyrir staðsetningu notanda til að virkja ferli vöruhúsakerfis.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Kenni forstillingar staðsetningar.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitnum Staðsetningarsnið skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum Gerð staðsetningar skal smella a fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Merkja eða afmerkja gátreitinn Heimila blandaða birgðastöðu.
    * Virkja þennan valkost ef óskað er að heimila stöðugildi blandaðra birgða í staðsetningum sem eru flokkaðar eftir þessa forstillingu staðsetningar.  
12. Merkja eða afmerkja gátreitinn Hnekkja reglum fyrir runudaga.
    * Virkja þennan valkost til að hnekkja reglu fyrir hversu marga daga lokadaga birgðir runuvinnslu getur verið önnur, til að leyfa blöndun birgðaruna sem hlýðir þessari reglu ekki.  
13. Merkja eða afmerkja gátreitinn Leyfa reglulega talningu.
    * Virkja þennan valkost til að leyfa vinnslu reglulegrar talningar í öllum staðsetningum sem verða flokkaðar eftir þessar staðsetningarforstillingu.  
14. Stækka eða fella saman hlutann Víddir.
    * Flipinn Víddir gerir kleift að skilgreina færibreytur og aðferðir til að virkja nákvæmari útreikninga á afkastagetu innan hverrar staðsetningar.  
15. Lokið síðunni.

## <a name="enable-warehouse-management-parameters"></a>Virkja færibreytur vöruhúsakerfis
1. Færibreytur fyrir Fara í vöruhúsakerfi.
    * Til að geta keyrt vöruhúsavinnu þarf að setja upp færibreytur fyrir forstillingu notandastaðsetningar af staðsetningu sviðsetningar og endanlegri gerð sendingarstaðsetningar Um leið og færslum á útleið lýkur á endanlegum sendingarstað sem þú skilgreinir eru tengdar færslur á útleið uppfærðar í ‚Tekið til‘.  
2. Stækka eða fella saman hlutann Forstillingar staðsetningar.
3. Í reitnum Staðsetning notanda skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Stækka eða fella saman hlutann Gerð staðsetningar.
6. Í reitnum Gerð sviðsetningarstaðsetningar skal smella a fellilistahnappinn til að opna leitina.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum Gerð endanlegs sendingarstaðar skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Lokið síðunni.

## <a name="define-warehouse-zone-groups"></a>Skilgreina vöruhúsastaðaflokka
1. Fara í Vöruhúsastaðaflokka.
    * Hægt er að nota vöruhúsastaði sem síur til að stýra mismunandi vöruhúsakerfisferlum. Það þarf að stofna tímabeltaflokk áður en hægt er að tilgreina svæði.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Auðkenni svæðisflokks.
4. Færa inn gildi í reitnum Heiti svæðahóps.
5. Lokið síðunni.

## <a name="define-warehouse-zones"></a>Skilgreina vöruhúsastaði
1. Farið í Svæði.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Kenni svæðisauðkennis.
4. Í reitinn Heiti umdæmis skal slá inn gildi.
5. Í reitnum Auðkenni svæðisflokks skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Lokið síðunni.

## <a name="create-locations-using-the-location-setup-wizard"></a>Stofna staðsetningar með því að nota uppsetningarforrit staðsetningar
1. Fara í leiðsagnarforrit uppsetningar Staðsetningar.
2. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum Svæðisauðkenni skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum Kenni lýsingar skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Í listanum skal merkja valda línu.
12. Í reitinn Frá númeri skal slá inn númer.
    * Reitirnir Frá númeri og Til númers skilgreina hversu margar staðsetningar verða stofnaðar. Til dæmis, ef þú stilltir Frá númer á 1 og Til númers á 3 fyrir allar fjórar línur í staðsetningarsniðinu verða 81 staðsetningar stofnaðar (3x3x3x3).  
13. Í reitinn Til númers skal slá inn númer.
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Í reitinn Frá númeri skal slá inn númer.
16. Í reitinn Til númers skal slá inn númer.
17. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
18. Í reitinn Frá númeri skal slá inn númer.
19. Í reitinn Til númers skal slá inn númer.
20. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
21. Í reitinn Frá númeri skal slá inn númer.
22. Í reitinn Til númers skal slá inn númer.
23. Smellið á „Stofna“.

## <a name="create-locations-manually"></a>Stofna staðsetningar handvirkt
1. Fara í Staðsetningar.
    * Auðvelt er að stofna staðsetningar í vöruhúsi á handvirkan hátt. Heiti staðsetningar og Auðkenni forstillingar staðsetningar eru áskilin gildi.  
2. Smellið á „Nýtt“.
3. Í reitinn vöruhús skal slá inn gildi.
4. Í reitinn staðsetning skal slá inn gildi.
    * Athugaðu að þú ert að stofna nýja staðsetningu hér, svo að nauðsynlegt er að slá inn nýtt einkvæmt heiti frekar en að velja gamalt.  
5. Færa inn gildi í reitnum Kenni forstillingar staðsetningar.
6. Lokið síðunni.

## <a name="define-pack-size-categories"></a>Skilgreina stærðarflokka umbúða
1. Fara í Stærðarflokka umbúða.
    * Stærðarflokka er hægt að nota til að flokka vörur sem hafa svipaðar efnislegar pökkunarstærðir. Í þessu dæmi verður flokkur pökkunarstærða notaður til að stjórna afköstum á tiltektarstaðsetningum innan tiltekin svæðis vöruhússins. Vinsamlegast athugið að úthluta verður auðkenni pökkunarstærðarflokks á útgefna afurð einingar til að nota sem hluta af vinnslu birgðamarka.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Auðkenni stærðarflokks umbúða.
4. Færa inn gildi í reitnum Heiti stærðarflokks umbúða.
5. Lokið síðunni.

## <a name="define-location-stocking-limits"></a>Skilgreina birgðamörk staðsetningar
1. Fara í Birgðamörk staðsetningar.
    * Birgðamörk staðsetningar hjálpa við að tryggja að vinna sé ekki stofnuð til að biðja um að birgðir séu settar á staðsetningu sem er ekki með efnislega afkastagetu til að taka við birgðunum.  
2. Smellið á „Nýtt“.
3. Í reitinn vöruhús skal slá inn gildi.
4. Færa inn gildi í reitnum Kenni forstillingar staðsetningar.
5. Færa inn gildi í reitnum Auðkenni stærðarflokks umbúða.
6. Færið inn númer í reitnum „Magn“.
7. Smellið á „Vista“.
8. Lokið síðunni.

## <a name="define-fixed-picking-locations"></a>Skilgreinið fastar tiltektarstaðsetningar
1. Farið í Fastar staðsetningar.
    * Hægt er að skilgreina staðsetningar sem nota á hverja afurð eða á afurðarafbrigði. Hægt er að stofna margar fastar staðsetningar fyrir sömu afurð innan sama vöruhúss.  
2. Smellið á „Nýtt“.
3. Í reitnum Vörunúmer skal slá inn gildi.
4. Í reitinn vöruhús skal slá inn gildi.
5. Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Lokið síðunni.


