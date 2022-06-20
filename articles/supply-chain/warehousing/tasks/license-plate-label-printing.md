---
title: Virkja prentun merkis á númeraplötu
description: Þessi grein sýnir hvernig á að virkja sjálfvirka prentun merkimiða raðflutningsgámakóða (SSCC) eftir að síðasta vara er tínd úr birgðum í sölutínsluvinnuferli.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dec552cac505b3fdc24dd453dbf723fa1d009ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903667"
---
# <a name="enable-license-plate-label-printing"></a>Virkja prentun merkis á númeraplötu

[!include [banner](../../includes/banner.md)]

Þessi grein sýnir hvernig á að virkja sjálfvirka prentun merkimiða raðflutningsgámakóða (SSCC) eftir að síðasta vara er tínd úr birgðum í sölutínsluvinnuferli. Hægt er að keyra þetta ferli fyrir sýnigögn fyrirtækisins USMF. Ef verið er að keyra hana með eigin gögn, þarf að hafa sett upp númeraröð fyrir númeraplötur. Þarf að setja upp merkimiði prentarinn áður en byrjað er að þetta verkefni. Fara á fyrirtækisstjórnun > Uppsetning > Prentarar á neti. Á aðgerðasvæðinu er smellt á Valkostir og svo á uppsetningarhnapp fyrir niðurhal skjals leiðarfulltrúa. Keyra uppsetningarforritið og gangið úr skugga um að þú hefur virkan prentara á neti stilltan áður en haldið er áfram með ferlið.


## <a name="set-up-the-gs1-company-prefix"></a>Setja upp GS1-fyrirtækjaforskeyti
1. Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Færibreytur vöruhúsakerfis**.
2. Í svæðinu **Forskeyti GS1 fyrirtækis** skaltu færa inn 7 tölur fyrir GS1 númer fyrirtækis þíns .
3. Veljið **Vista**.
4. Lokið síðunni.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Setja upp númeraröð SSCC númeraplötu
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Fyrirtækjastjórnun > Númeraraðir > Númeraraðir**.
2. Í reitnum **Svæði** skal velja valkost.
3. Í reitnum **Tilvísun** skal velja valkost.
4. Í reitinn **Fyrirtæki** skal slá inn gildi.
5. Stækkaðu hlutann **Hlutar**.
6. Veljið **Breyta**.
7. Í töflunni **Hlutar** skal velja fyrstu línuna
8. Veldu **Fjarlægja**.
9. Veldu **Fjarlægja**.
10. Veljið **Vista**.
11. Lokið síðunni.

## <a name="create-the-document-route-layout"></a>Stofna útlit leið skjals
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Skjalaleið > Útlit skjalaleiðar**. Virkja SSCC útlit.  
2. Veljið **Nýtt**.
3. Í reitnum **Kenni útlits** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Veldu **Setja inn aftan við texta**.
6. Veljið **Vista**.
7. Lokið síðunni.

## <a name="set-up-the-document-routing"></a>Setja upp skjalaleið
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Skjalaleið > Skjalaleið**.
2. Í reitnum **Gerð verkbeiðni** skal velja valkost.
3. Veljið **Nýtt**.
4. Í reitinn **Vöruhús** skal slá inn gildi.
5. Í reitinn **Heiti** skal slá inn gildi.
6. Veljið **Nýtt**.
7. Í reitinn **Útlit kennis** skal slá inn eða velja gildi.
8. Í reitnum **Heiti** skal færa inn heiti prentarans sem á að nota.
9. Veljið **Vista**.
10. Lokið síðunni.

## <a name="create-mobile-device-menu"></a>Stofna Valmynd fartækja
1. Farðu í **Skoðunarrúðuna > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmyndaratriði fartækis**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti valmyndaratriðis** skal færa inn gildi.
4. Í reitinn **Titill** skal slá inn gildi.
5. Í reitnum **Hamur** velurðu valkost.
6. Velja skal **Já** í reitnum **Nota fyrirliggjandi vinnu**.
7. Velja skal **Já** í reitnum **Mynda númeraplötu**.
8. Útvíkkaðu hlutann **Vinnuklasar**.
9. Veljið **Nýtt**.
10. Í reitinn **Kenni vinnuklasa** skal færa inn gildi.
11. Veljið **Vista**.
12. Lokið síðunni.
13. Farðu í **skoðunarrúðuna > Kerfiseiningar > Vöruhúsakerfi > Uppsetning > Fartæki > Valmynd fartækis**.
14. Í trénu, skal velja þau valmyndaratriði sem voru stofnuð áður.
15. Veljið **Breyta**.
16. Veldu örina til að bæta valmyndaratriði við valmyndina.
17. Veljið **Vista**.
18. Lokið síðunni.

## <a name="update-a-work-template"></a>Uppfæra sniðmát verks
1. Farðu í **Skoðunarrúðu > Kerfi > Vöruhúsakerfi > Uppsetning > Vinna > Vinnusniðmát**.
2. Veljið **Breyta**.
3. Veljið **Nýtt**.
4. Í reitnum **Gerð vinnu** skal velja **Prenta**.
5. Í reitnum **Kenni vinnuklasa** skal færa inn eða velja gildi.
6. Veldu **Færa upp**.
7. Veljið **Vista**.
8. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]