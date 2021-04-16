---
title: Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka
description: Þetta efnisatriði lýsir hvernig á að endurnýta núverandi forritaskrár í grunnstillingu rafrænnar skýrslugerðar (ER) með því að kalla á nauðsynlegar aðferðir við forritaflokka.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37cf01ac4b23717ebddaaefe6bcb06be0ff82dc6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752509"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Hanna segðir rafrænnar skýrslugerðar til að kalla á aðferðir forritaflokka

[!include [banner](../../includes/banner.md)]

Þessi handbók veitir upplýsingar um hvernig á að endurnýta núverandi forritaskrár í grunnstillingu rafrænnar skýrslugerðar (ER) með því að kalla á nauðsynlegar aðferðir við forritaflokka í segðum rafrænnar skýrslugerðar. Hægt er að skilgreina gildi frumbreyta fyrir köllunarflokka á keyrslutíma: Til dæmis byggt á upplýsingum í þáttunarskjalinu til að tryggja réttmæti þess. Í þessum leiðbeiningum mun notandi stofna þær grunnstillingar rafrænnar skýrslugerðar sem krafist er fyrir sýnifyrirtækið Litware, Inc. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar. 

Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er. Þú verður líka að hlaða niður og vista eftirfarandi skrá staðbundið: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð Stofna skilgreiningaveitu og merkja hana sem virka.“

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Sannprófið að grunnstillingarveita fyrir sýnifyrirtækið Litware, Inc. sé tiltæk og merkt sem virk. Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.   
    * Þú ert að hanna aðferð til að þátta bankayfirlit á innleið fyrir uppfærslu á umsóknargögnum. Þú færð bankayfirlit á innleið sem TXT skrár sem innihalda IBAN kóða. Sem hluti af innflutningsaðferð bankayfirlits þarft þú að sannreyna réttmæti þessa IBAN númera með því að nota rökfræði sem er nú þegar í boði.   

## <a name="import-a-new-er-model-configuration"></a>Flytja inn nýja grunnstillingu líkans í Rafræn skýrslugerð
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja skal Microsoft reitinn.  
2. Smella á Geymslur.
3. Smellt er á Sýna síur.
4. Bæta við síureit „Gerð heitis“. Í svæðinu heiti skal færa inn gildið „tilföng“, velja síuna „inniheldur“ og smella svo á Nota.
5. Smellt er á Opin.
6. Í trénu skal velja „Greiðslulíkan“.
    * Ef innflutningshnappurinn á flýtiflipa Versions er ekki virkur hefur útgáfa 1 af stillingum „Greiðslulíkan“ rafrænnar skýrslugerðar þegar verið flutt inn. Þú mátt sleppa þeim skrefum sem eftir eru í þessu undirverkefni.   
7. Smelltu á Flytja inn.
8. Smella á Já.
9. Lokið síðunni.
10. Lokið síðunni.

## <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð
1. Smelltu á Grunnstillingar skýrslugerðar
    * Bæta við nýju sniði fyrir rafræna skýrslugerð til að þátta bankayfirlit á innleið á TXT-sniði.  
2. Í trénu skal velja „Greiðslulíkan“.
3. Smellt er á Stofna skilgreiningu til að opna svarglugga.
4. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.
5. Í reitnum Heiti skal færa inn „Innflutningssnið bankayfirlits (dæmi)“.
    * Innflutningssnið bankayfirlits (dæmi)  
6. Velja Já í svæði Styður gagnainnflutning.
7. Smelltu á Stofna skilgreiningu.

## <a name="design-the-er-format-configuration---format"></a>Veljið grunnstillingu rafrænnar skýrslugerðar - snið
1. Smellið á Hönnuður.
    * Uppsetta sniðið stendur fyrir væntanlega uppbyggingu ytri skráar á TXT-sniði.  
2. Smelltu á Bæta við rót til að opna svargluggann.
3. Í trénu skal velja 'Text\Sequence'.
4. Í reitnum Heiti skal færa inn ‚rót'.
    * Rót  
5. Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".
    * Valkosturinn „Ný lína - Windows (CR LF)“ hefur verið valinn í reitnum „sérstafir“. Byggt á þessari stillingu telst sérhver lína í þáttunarskrá aðskilin færsla.  
6. Smellið á „Í lagi“.
7. Smelltu á Bæta við til að opna felligluggann.
8. Í trénu skal velja 'Text\Sequence'.
9. Í svæðið Heiti skal slá inn „Raðir“.
    * Línur  
10. Veljið „Einn margir“ í svæðinu Margfeldi.
    * Valkosturinn „Einn margir“ hefur verið valinn í svæðinu „Margfeldi“. Byggt á þessari stillingu er gert ráð fyrir að minnsta kosti ein lína verði kynnt í þáttunarskránni.  
11. Smellið á „Í lagi“.
12. Í trénu skal velja „Rót\Raðir“.
13. Smellið á „Bæta við röð“.
14. Í svæðið Heiti skal slá inn „Svæði“.
    * Svæði  
15. Veljið „Akkúrat einn“ í svæðinu Margfeldi.
16. Smellið á „Í lagi“.
17. Í trénu skal velja „Rót\Raðir\Reitir“.
18. Smelltu á Bæta við til að opna felligluggann.
19. Í trénu skal velja ‚Texti/Strengur'.
20. Í svæðið Heiti, færðu inn ‚IBAN-númer'.
    * IBAN-númer  
21. Smellið á „Í lagi“.
    * Það hefur verið stillt á að hver lína í þáttunarskrá innihaldi eina IBAN kóðann.  
22. Smellið á „Vista“.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Veljið grunnstillingu rafrænnar skýrslugerðar - vörpun í gagnalíkan
1. Smellt er á Varpa sniði á líkan.
2. Smellið á „Nýtt“.
3. Í svæði Skilgreining skal slá inn „BankToCustomerDebitCreditNotificationInitiation“.
    * BankToCustomerDebitCreditNotificationInitiation  
4. „Leysa úr“ breytir skilgreiningu.
5. Í reitnum Heiti skal færa inn „Vörpun í gagnalíkan“.
    * Vörpun í gagnalíkan  
6. Smellið á „Vista“.
7. Smellið á Hönnuður.
8. Í trénu skal velja 'Dynamics 365 for Operations\Class'.
9. Smella á bæta Við rót.
    * Bæta nýjum gagnagjafa við fyrirliggjandi forritsgrunn fyrir sannprófun IBAN-númera.  
10. Í svæðið Heiti skal slá inn „check_codes“.
    * check_codes  
11. Í reitinn klasi skal færa inn „ISO7064“.
    * ISO7064  
12. Smellið á „Í lagi“.
13. Í trénu skal víkka út „snið“.
14. Í trénu skal víkka út „snið\Rót: Röð(Rót)“.
15. Í trénu skal velja „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)“.
16. Smelltu á Binda.
17. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)“.
18. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)\Reitir: Röð 1..1 (Reitir)“.
19. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)\Reitir: Röð 1..1 (Reitir)\IBAN: Strengur(IBAN)“.
20. Í trénu skal víkka út „Payments = format.Root.Rows“.
21. Í trénu skal víkka út „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)“.
22. Í trénu skal víkka út „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)\Sannkennsl“.
23. Í trénu skal velja „Payments = format.Root.Rows\Reikningur lánveitanda(CreditorAccount)\Sannkennsl\IBAN“.
24. Smelltu á Binda.
25. Smellt er á flipann Sannprófanir.
26. Smellið á „Nýtt“.
    * Bættu við nýrri villuleitarreglu sem sýnir villu fyrir hvaða línu sem er í þáttunarskránni sem inniheldur ógildan IBAN kóða.  
27. Breyta skilyrði.
28. Í trénu skal víkka út „check_codes“.
29. Í trénu skal velja „check_codes\verifyMOD1271_36“.
30. Smellt er á Bæta við gagnagjafa.
31. Í Formúlureitinn skal slá inn „check_codes.verifyMOD1271_36('.
    * check_codes.verifyMOD1271_36(  
32. Í trénu skal víkka út „snið“.
33. Í trénu skal víkka út „snið\Rót: Röð(Rót)“.
34. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)“.
35. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)\Reitir: Röð 1..1 (Reitir)“.
36. Í trénu skal víkka út „snið\Rót: Röð(Rót)\Raðir: Röð 1..* (Raðir)\Reitir: Röð 1..1 (Reitir)\IBAN: Strengur(IBAN)“.
37. Smellt er á Bæta við gagnagjafa.
38. Í Formúlureitinn skal slá inn „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)“.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Smellið á „Vista“.
40. Lokið síðunni.
    * Villuleitarskilyrði hafa verið stillt til að skila FALSE fyrir hvaða ógildan IBAN kóða með því að kalla núverandi aðferð „verifyMOD1271_36“ umsóknarflokksins „ISO7064“. Athugaðu að gildi IBAN-kóðans er skilgreindt gagnvirkt á keyrslutíma sem frumbreyta köllunaraðferðarinnar, byggt á innihaldi TXT þáttunarskráarinnar.   
41. Smellt er á Breyta skilaboðum.
42. Í Formúlureitinn skal slá inn „CONCATENATE("Invalid IBAN code has been found: format.Root.Rows.Fields.IBAN)“.
    * CONCATENATE(„Ógildur IBAN-kóði fannst: “, format.Root.Rows.Fields.IBAN)  
43. Smellið á „Vista“.
44. Lokið síðunni.
45. Smellið á „Vista“.
46. Lokið síðunni.

## <a name="run-the-format-mapping"></a>Keyra vörpun sniðs
Til að prófa, skal framkvæma vörpun sniðs með SampleIncomingMessage.txt-skránni sem þú sóttir. Myndað úttak inniheldur gögn sem verða flutt inn úr valinni TXT-skrá og fyllt út í sérstillt gagnalíkan í rauninnflutningi.   
1. Smellið á „Keyra“.
    * Smellt er á Fletta og flett á skrána SampleIncomingMessage.txt sem áður var sótt.  
2. Smellið á „Í lagi“.
    * Farið yfir úttak í XML-sniði, sem stendur fyrir gögn sem hafa verið innflutt úr valinni skrá og tengd við gagnalíkan. Athugaðu að aðeins 3 línur af innfluttri TXT-skrá voru unnar. IBAN-númerið á línu 4 sem er ógilt var sleppt og villuskilaboð eru veitt í Infolog.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]