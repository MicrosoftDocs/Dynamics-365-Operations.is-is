---
title: Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi
description: Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4e3322bbeb64472bdcd27f9ff571fe45ef87d1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574114"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi

[!include [banner](../../includes/banner.md)]

Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli). Ferlið er yfirleitt gert af stjórnanda vöruhúss. Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF eða í eigin gögnum. Forkröfur eru að minnsta kosti eitt svæði sé grunnstillt.


## <a name="create-a-new-warehouse"></a>Stofna nýtt vöruhús
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Birgðastýring > Uppsetning > Niðurbrot birgða > Vöruhús**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Vöruhús** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Svæði** skal slá inn gildi.
6. Víkkið út hlutann **Vöruhús**.
7. Stilltu valkostinn **Nota ferli vöruhúsastjórnunar** á Já. Þessi stilling leyfir þér að keyra ítarleg vöruhúsaferli með því að nota vöruhúsavinnu og fartæki.
8. Lokið síðunni.

## <a name="define-a-location-format"></a>Skilgreina snið staðsetningar
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningarsnið**. Staðsetningarsnið eru nafngiftarkerfi sem eru notuð til að stofna einkvæm og samræmd heiti fyrir aðrar staðsetningu karfa stöður notað innan vöruhúss. Það getur verið gagnlegt að nota skiltákn sem hluta af staðsetningarsniði til að auðvelda auðkenningu íhluta staðsetningar eins og númer gangs. Í þessu dæmi stofnum við heiti með fjórum íhlutum. Til dæmis, þetta gæti verið gangur, rekki, hilla og karfa.
2. Smellt er á **Nýtt**.
3. Í reitinn **Staðsetningarsnið** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Lýsing hluta** skal slá inn gildi. Það lýsir því fyrir hvað fyrsti íhluti heitis staðsetningar stendur. Til dæmis, gæti það verið „Gangur“.
6. Í reitinn **Lengd** skal slá inn tölu. Þetta ákvarðar hversu margir stafir verða að vera í þessum hluta af nafni staðsetningar. Athugið að samtala allra íhluta í heiti, þar á meðal skiltákn, má ekki fara yfir 10 staftákn.    
7. Í reitinn **Skiltákn** skal slá inn gildi. Þetta ákveður hvaða stafur eða tákn er notað á milli fyrsta og annars íhluta í heiti.  
8. Í kaflanum **Upplýsingar** skaltu smella á **Nýtt**.
9. Í reitinn **Lýsing hluta** skal slá inn gildi.
10. Í reitinn **Lengd** skal slá inn tölu.
11. Í reitinn **Skiltákn** skal slá inn gildi.
12. Í kaflanum **Upplýsingar** skaltu smella á **Nýtt**.
13. Í reitinn **Lýsing hluta** skal slá inn gildi.
14. Í reitinn **Lengd** skal slá inn tölu.
15. Í reitinn **Skiltákn** skal slá inn gildi.
16. Í kaflanum **Upplýsingar** skaltu smella á **Nýtt**.
17. Í reitinn **Lýsing hluta** skal slá inn gildi.
18. Í reitinn **Lengd** skal slá inn tölu.
19. Smellt er á **Vista**.
20. Lokið síðunni.

## <a name="define-location-types"></a>Skilgreina staðsetningagerðir
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningargerðir**. Hægt er að nota gerðir staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Sem lágmark þarf að stofna staðsetningagerðir sviðsetninga og endanlegra sendinga til að skilgreina stjórnunarferli á útleið í vöruhúsi. 
2. Smellt er á **Nýtt**.
3. Í gerðarreitinn **Staðsetning** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Lokið síðunni.

## <a name="define-location-profile"></a>Skilgreina forstillingu staðsetningar
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningarforstillingar**. Skilgreining á forstillingum staðsetningar er mjög mikilvæg. Hægt er að stýra afkastagetu flokkaðra staðsetninga hér, ásamt reglum sem tengjast hvaða birgðir eru vistaðar og hvernig þær eru vistaðar. Hægt er að nota forstillingar staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum. Sem lágmark verður að stofna forstillingu fyrir staðsetningu notanda til að virkja ferli vöruhúsakerfis.
2. Smellt er á **Nýtt**.
3. Í reitnum **Kenni staðsetningarforstillingar**.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Staðsetningarsnið** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum **Gerð staðsetningar** skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Merktu eða afmerktu gátreitinn **Heimila blandaða birgðastöðu**. Virkja þennan valkost ef óskað er að heimila stöðugildi blandaðra birgða í staðsetningum sem eru flokkaðar eftir þessa forstillingu staðsetningar. 
12. Merkja eða afmerkja gátreitinn **Hnekkja reglum fyrir runudaga**. Virkjaðu þennan valkost til að hnekkja reglu fyrir hversu marga daga lokadaga birgðir runuvinnslu getur verið önnur, til að leyfa blöndun birgðaruna sem hlýðir þessari reglu ekki.  
13. Merkja eða afmerkja gátreitinn **Leyfa reglulega talningu**. Virkja þennan valkost til að leyfa vinnslu reglulegrar talningar í öllum staðsetningum sem verða flokkaðar eftir þessar staðsetningarforstillingu. 
14. Stækka eða fella saman hlutann **Víddir**. Flipinn Víddir gerir kleift að skilgreina færibreytur og aðferðir til að virkja nákvæmari útreikninga á afkastagetu innan hverrar staðsetningar.  
15. Lokið síðunni.

## <a name="enable-warehouse-management-parameters"></a>Virkja færibreytur vöruhúsakerfis
1. Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Færibreytur vöruhúsakerfis**. Til að geta keyrt vöruhúsavinnu þarf að setja upp færibreytur fyrir forstillingu notandastaðsetningar af staðsetningu sviðsetningar og endanlegri gerð sendingarstaðsetningar Um leið og færslum á útleið lýkur á endanlegum sendingarstað sem þú skilgreinir eru tengdar færslur á útleið uppfærðar í „Tekið til“.
2. Stækka eða fella saman hlutann **Forstillingar staðsetningar**.
3. Í reitnum **Staðsetning notanda** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Stækka eða fella saman hlutann **Gerðir staðsetningar**.
6. Í reitnum **Gerð sviðsetningarstaðsetningar** skal smella a fellilistahnappinn til að opna leitina.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum **Gerð endanlegs sendingarstaðar** skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Lokið síðunni.

## <a name="define-warehouse-zone-groups"></a>Skilgreina vöruhúsastaðaflokka
1. Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðarflokkar vöruhúsakerfis**. Hægt er að nota vöruhúsastaði sem síur til að stýra mismunandi vöruhúsakerfisferlum. Það þarf að stofna tímabeltaflokk áður en hægt er að tilgreina svæði.   
2. Smellt er á **Nýtt**.
3. Í reitinn **Auðkenni staðarflokks** skal færa inn gildi.
4. Í reitinn **Heiti staðarflokks** skal slá inn gildi.
5. Lokið síðunni.

## <a name="define-warehouse-zones"></a>Skilgreina vöruhúsastaði
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðir**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Auðkenni staðar** skal færa inn gildi.
4. Í reitinn **Heiti staðar** skal slá inn gildi.
5. Í reitnum **Auðkenni staðarflokks** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Lokið síðunni.

## <a name="create-locations-using-the-location-setup-wizard"></a>Stofna staðsetningar með því að nota uppsetningarforrit staðsetningar
1. Farðu í **Skoðunnarúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Vöruhús > Uppsetningarforrit staðsetningar**.
2. Í reitnum **Vöruhús** skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum **Auðkenni staðar** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum **Auðkenni forstillingar staðsetningar** skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Í listanum skal merkja valda línu.
12. Í reitinn **Frá númeri** skal slá inn númer. Reitirnir Frá númeri og Til númers skilgreina hversu margar staðsetningar verða stofnaðar. Til dæmis, ef þú stilltir Frá númer á 1 og Til númers á 3 fyrir allar fjórar línur í staðsetningarsniðinu verða 81 staðsetningar stofnaðar (3x3x3x3).   
13. Í reitinn **Til númers** skal slá inn númer.
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Í reitinn **Frá númeri** skal slá inn númer.
16. Í reitinn **Til númers** skal slá inn númer.
17. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
18. Í reitinn **Frá númeri** skal slá inn númer.
19. Í reitinn **Til númers** skal slá inn númer.
20. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
21. Í reitinn **Frá númeri** skal slá inn númer.
22. Í reitinn **Til númers** skal slá inn númer.
23. Smellið á „Stofna“.

## <a name="create-locations-manually"></a>Stofna staðsetningar handvirkt
1. Farðu í **Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningar**. Auðvelt er að stofna staðsetningar í vöruhúsi á handvirkan hátt. Heiti staðsetningar og Auðkenni forstillingar staðsetningar eru áskilin gildi. 
2. Smellt er á **Nýtt**.
3. Í reitinn **Vöruhús** skal slá inn gildi.
4. Í reitinn **Staðsetning** skal slá inn gildi. Athugaðu að þú ert að stofna nýja staðsetningu hér, svo að nauðsynlegt er að slá inn nýtt einkvæmt heiti frekar en að velja gamalt.
5. Í reitnum **Kenni staðsetningarforstillingar**.
6. Lokið síðunni.

## <a name="define-pack-size-categories"></a>Skilgreina stærðarflokka umbúða
1. Farðu í **Vöruhúsakerfi > Uppsetning > Vöruhús > Stærðarflokkar umbúða**. Stærðarflokka er hægt að nota til að flokka vörur sem hafa svipaðar efnislegar pökkunarstærðir. Í þessu dæmi verður flokkur pökkunarstærða notaður til að stjórna afköstum á tiltektarstaðsetningum innan tiltekin svæðis vöruhússins. Vinsamlegast athugið að úthluta verður auðkenni pökkunarstærðarflokks á útgefna afurð einingar til að nota sem hluta af vinnslu birgðamarka.  
2. Smellt er á **Nýtt**.
3. Í reitinn **Auðkenni stærðarflokks umbúða** skal færa inn gildi.
4. Í reitinn **Heiti stærðarflokks umbúða** skal slá inn gildi.
5. Lokið síðunni.

## <a name="define-location-stocking-limits"></a>Skilgreina birgðamörk staðsetningar
1. Farðu í **Vöruhúsakerfi > Uppsetning > Vöruhús > Birgðamörk staðsetningar**. Birgðamörk staðsetningar hjálpa við að tryggja að vinna sé ekki stofnuð til að biðja um að birgðir séu settar á staðsetningu sem er ekki með efnislega afkastagetu til að taka við birgðunum.  
2. Smellt er á **Nýtt**.
3. Í reitinn **Vöruhús** skal slá inn gildi.
4. Í reitnum **Kenni staðsetningarforstillingar**.
5. Í reitinn **Auðkenni stærðarflokks umbúða** skal færa inn gildi.
6. Í reitnum **Magn** slærðu inn tölu.
7. Smellt er á **Vista**.
8. Lokið síðunni.

## <a name="define-fixed-picking-locations"></a>Skilgreinið fastar tiltektarstaðsetningar
1. Farðu í **Vöruhúsakerfi > Uppsetning > Vöruhús > Fastar staðsetningar**. Hægt er að skilgreina staðsetningar sem nota á hverja afurð eða á afurðarafbrigði. Hægt er að stofna margar fastar staðsetningar fyrir sömu afurð innan sama vöruhúss.     
2. Smellt er á **Nýtt**.
3. Í reitnum **Vörunúmer** skal slá inn gildi.
4. Í reitinn **Vöruhús** skal slá inn gildi.
5. Í reitnum **Staðsetning** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]