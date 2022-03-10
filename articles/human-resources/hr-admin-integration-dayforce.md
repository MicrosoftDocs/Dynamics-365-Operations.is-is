---
title: Skilgreina samþættingu við Dayforce
description: Þetta efnisatriði lýsir nauðsynlegum stilliskrefum fyrir samþættingu milli Microsoft Dynamics 365 Human Resources og Ceridian Dayforce.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e2043e75aa647e21f3e0816247dcf651be64730
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067077"
---
# <a name="configure-integration-with-dayforce"></a>Skilgreina samþættingu við Dayforce


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Samþættingin milli Microsoft Dynamics 365 Human Resources og Ceridian Dayforce er byggir á nokkrum skilgreiningarskrefum sem er fjallað um í þessu efnisatriði. Nauðsynlegt er að skilgreina samþættinguna bæði í Human Resources og Dayforce áður en hafist er handa við að afgreiða launakeyrslu.

Þegar þjónusta eins og Dayforce er notuð til að ljúka launakeyrslum verður að virkja samþættinguna í Human Resources. Samþættingin krefst tilgreindra gagna frá Human Resources. Þess vegna þarf að staðfesta að gögn sem varpað er á Dayforce séu skilgreind í Human Resources á þann hátt sem styður samþættingu. Samþættingin notar eftirfarandi víðtæka flokka gagna:

- Mannauðsgögn
- Launagögn
- Launagögn, svo sem greiðsluferli, greiðslutímabil og tekjukóðar
- Starfsmannagögn

Þetta efnisatriði fjallar um skrefin sem verður að fylgja til að virkja samþættinguna og útskýrir hvers konar gagnagerðir og upplýsingar um skilgreiningu samþættingin þarfnast.

## <a name="enable-the-integration"></a>Virkja samþættingu

Í Human Resources er nauðsynlegt að kveikja á samþættingu og slá inn skilgreiningarupplýsingar til að tengjast Dayforce. Ef þú vilt að fjárhagsfærslan sem er búin til verði flutt inn í Microsoft Dynamics 365 Finance þarf einnig að setja upp Microsoft Azure-geymslureikning og slá inn tengistreng Azure-geymslu í Finance.

Til að kveikja á samþættingu í Human Resources skal fylgja þessum skrefum.

1. Á síðunni **Kerfisstjórnun** skal velja **Skilgreining samþættingar**.
2. Sláðu inn öruggu FTP-endastöðina (File Transfer Protocol) og öruggu FTP-möppuslóðina.
3. Sláðu inn notandanafn og aðgangsorð þess notanda sem mun hafa aðgang að FTP-endastöð og möppuslóð.
4. Prófaðu tenginguna, eftir því sem þörf krefur, og stilltu valkostinn **Virkja launasamþættingu** á **Já**.

Þegar kveikt er á samþættingunni eru gagnaútflutningspakki og skrár búnar til og tíðnin er stillt. Hægt er að breyta tíðninni eftir þörfum.

Frekari upplýsingar um Azure-geymslureikninga og tengistrengi Azure-geymslu er að finna í eftirfarandi efnisatriðum Azure:

- [Um Azure-geymslureikninga](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Skilgreina tengistrengi Azure-geymslu](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Tæknilýsing þegar launasamþætting er virk

Að kveikja á launasamþættingu hefur aðallega tvennt í för með sér:

- Gagnaútflutningsverk sem heitir "Útflutningur launasamþættingar" er búið til. Þetta verk inniheldur þær einingar og reiti sem þarf fyrir launasamþættinguna. Til að skoða verkið skaltu fara í **Kerfisstjórnun**, velja reitinn **Gagnastjórnun** og opna síðan gagnaverkið af listanum yfir verk.
- Þessi runuvinnsla keyrir gagnaútflutningsverkið, dulkóðar gagnapakkann sem fylgir því og flytur gagnapakkaskrána á SFTP-endastöðina sem er skilgreind á skjánum **Skilgreining samþættingar**.

> [!NOTE]
> Gagnapakkinn sem er fluttur til SFTP-endastöðvarinnar er dulkóðaður með lykli sem er einkvæmur fyrir pakkann. Lykillinn er í Azure-lykageymslu er aðeins aðgengileg af Ceridian. Ekki er hægt að afkóða og skoða innihald gagnapakka. Ef þú þarft að skoða innihald gagnapakka þarftu að flytja út gagnaverkið „Útflutningur launasamþættingar“ handvirkt, hlaða niður því og opna það síðan. Handvirkur útflutningur mun ekki beita dulkóðun eða flytja pakkann.

## <a name="configure-your-data"></a>Skilgreina gögnin þín 

Til að afgreiða laun þarf að skilgreina mannauðsgögn í Human Resources. Þú verður að setja upp skipulagsgögn, svo sem störf og stöður, ásamt upplýsingum um fríðindi og laun. Þessar upplýsingar veita upplýsingar um starf, laun og frádrátt sem þarf til að búa til starfsmannalaun.

### <a name="human-resource-data"></a>Mannauðsgögn

#### <a name="benefits"></a>Fríðindi 

Mannauður veitir verkfæri fyrir uppsetningu og viðhald á fríðindum, frádrætti og launafyrirkomulagi starfsmanns sem fyrirtæki býður upp á eða afgreiðir fyrir starfsfólk sitt.

Þegar fríðindi eru búin til skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.

##### <a name="benefit-plans"></a>Fríðindaáætlanir

- Áætlun (krafist)
- Gerð (krafist)
- Áhrif á launaskrá (krafist)
- Endurheimta vangoldnar greiðslur
- Frádráttaraðferð
- Frádráttarforgangur
- Takmörkunartímabil
- Takmarka upphæð

##### <a name="benefits"></a>Fríðindi

- Áætlun (krafist)
- Gerð (krafist)
- Valkostur (krafist)
- Fríðindaauðkenni (krafist)
- Tíðni
- Grunnur
- Upphæð eða taxti
- Tekjukóði

##### <a name="supported-frequencies"></a>Studdar tíðnir 

- Vikulega
- Hálfsmánaðarlega
- Hálfsmánaðarlega
- Mánaðarlega

##### <a name="supported-bases"></a>Studdir grunnar 

- Föst upphæð
- Prósenta af tekjum
- Virkar vinnustundir

Dayforce býr til eftirfarandi frádrætti sem byggjast á áhrifum launaskrár sem er skilgreind í fríðindaáætluninni.

| Val í Human Resources        | Niðurstaða í Dayforce                            |
|----------------------------|-----------------------------------------------|
| Enginn                       | Enginn frádráttur er búinn til.                      |
| Eingöngu frádráttur             | Frádráttur starfsmanns er búinn til.             |
| Eingöngu framlag          | Frádráttur vinnuveitanda er búinn til.             |
| Frádráttur og framlag | Frádrættir starfsmanns og vinnuveitanda eru búnir til. |

Frekari upplýsingar um hvernig á að skilgreina og stjórna fríðindaáætlun er að finna í eftirfarandi efnisatriðum:

- [Leggja fram fríðindaáætlun starfsmanns](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Stofna ný fríðindi](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Skilgreina reglur og stefnur um hæfi til fríðinda](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Skrá og fjarlægja fríðindi starfsmanna](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Laun 

Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar. Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa. Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.

Dayforce notar launaupplýsingar til að reikna út tíma- og árskaup starfsmanns. Krafist er umreikninga á launafyrirkomulagi fastra launa og launataxta. Starfsmenn verða að tengjast launafyrirkomulagi fastra launa.

Frekari upplýsingar um launafyrirkomulag er hægt að finna í eftirfarandi efnisatriðum:

- [Launafyrirkomulag fastra launa stofnað](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Launafyrirkomulag breytilegra launa](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Þróa uppbyggingu launa og launafyrirkomulag](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Launaútreikningur](/dynamics365/unified-operations/talent/process-compensation)
- [Skilgreina launavinnslu og reikna niðurstöður](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Skrá starfsmann í launafyrirkomulag fastra launa](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Skrá starfsmann í launafyrirkomulag breytilegra launa](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Störf 

Verk er safn verkefna og ábyrgðarsviða sem er ætlast til af einstaklings sem framkvæmir verkið. Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Setja upp íhluta verks](/dynamics365/unified-operations/talent/create-job)
- [Skilgreina ný störf](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Stöður

Staða er sérstakt tilvik starfs. Til dæmis er staðan „Sölustjóri (Austur)“ ein af stöðunum sem tengjast verkinu „Sölustjóri“. Staða er til í deild. Einungis einn starfsmaður getur tengst hverri stöðu.

Hafðu eftirfarandi gögn og skilgreiningar í huga þegar þú setur upp stöður:

- Staða (krafist)
- Lýsing (krafist)
- Starf (krafist)
- Deild (krafist)
- Stöðugerð (krafist)
- Jafngildi fulls starfs
- Reglulegar árlegar vinnustundir (krafist)
- Greitt eftir lögaðila (krafist)
- Greiðsluferli (krafist)
- Sjálfgefin fjárhagsvídd - Kostnaðarstaður (krafist)
- Úthlutun starfsmanns - Starfsmaður, upphaf úthlutunar, endir úthlutunar, ástæðukóði

Ef margar stöður í sömu deild eru tengdar við sama starfið eru þær sameinaðar í eina stöðu í Dayforce.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Vinnuafl skipulagt með notkun deilda, starfa og staða](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Setja upp stöður](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Deildir

Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði. Hægt er að nota deildir til að gefa skýrslur um virk svið. Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Stofnun deildar og tenging hennar við deildastigveldið](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Skilgreina nýjar deildir](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Greiðsluferli og launatímabil

Greiðsluferli ákvarðar hversu oft launaskrá er keyrð og þá daga þegar starfsmenn fá greitt. Til dæmis gæti greiðsluferli verið mánaðarlega og starfsmenn gætu fengið greitt á síðasta degi mánaðarins. Að öðrum kosti gæti greiðsluferli verið vikulega og starfsmenn gætu fengið greitt á þriðjudegi eftir að launatímabili lýkur. Greiðsluferlum er úthlutað á stöður til að stjórna því þegar starfsmenn í þessum stöðum fá greitt.

Eftir að þú hefur stofnað greiðsluferli getur þú búið til launatímabil fyrir hvert ferli. Hvert launatímabil inniheldur sjálfgefinn greiðsludag sem byggist á upplýsingum sem þú gefur upp. Þú getur hins vegar breytt sjálfgefnum greiðsludegi í launatímabili til að leyfa undantekningar, t.d. þegar greiðsludagur lendir á frídegi.

Eftirfarandi upplýsingar eru notaðar í Dayforce:

- Greiðsluferli (krafist)
- Tíðni greiðsluferlis (krafist)
- Upphafsdagsetning tímabils (fyrsta launatímabils er krafist)
- Sjálfgefin dagsetning greiðslu (fyrsta launatímabils er krafist)

Þessar upplýsingar eru felldar inn í Dayforce sem greiðsluhóp og eru aðgreindar eftir landi eða svæði fyrir hvert greiðsluferli. Það verður að búa til að minnsta kosti eitt launatímabil fyrir samþættingu. Dayforce býr til dagatöl greiðsluhópa og greiðsludaga sem byggjast á upphafsdagsetningu fyrsta launatímabilsins og sjálfgefnum greiðsludegi sem er sett upp í Human Resources.

#### <a name="earning-codes"></a>Tekjukóðar

Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær. Kóðarnir eru með ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu.

Eftirfarandi upplýsingar eru notaðar í Dayforce:

- Tekjukóði (krafist)
- lýsing
- Mælieining
- Framleiðni

### <a name="worker-data"></a>Starfsmannagögn

Færslur fyrir ýmsar gerðir starfsmanna sem þú hefur eru mikilvægar mannauðs- og launakerfinu þínu. Hægt er að nota upplýsingarnar sem voru slegnar inn til að fylgjast með starfsmönnum og persónulegum upplýsingum.

Hægt er að viðhalda eftirfarandi upplýsingum fyrir starfsmenn:

- **Grunnur** - Viðhalda grunnupplýsingum um starfsmann, svo sem upplýsingar um tengiliði, lýðfræðilegar upplýsingar, auðkennisupplýsingar, upplýsingar um fjölskyldu, staða herþjónustu, upplýsingar um starfsmann í öðru landi og persónulega tengiliði og ættingjaupplýsingar.
- **Starf** - Viðhalda upplýsingum um starf starfsmanns, t.d. fyrirtækja- eða stofnanatengsl, stöðuverkefni, upphafs- og lokadagsetningar, vinnuhæfni, ráðningarskilmálar og upplýsingar um lífeyri, orlof og búsetubreytingar.
- **Leyfi og fjarvistir** - Viðhalda upplýsingum um fjarvistir starfsmanns, t.d. verkdagatöl, fjarvistarfærslur og uppsetningu fjarvista.
- **Laun og launaskrá** - Viðhalda upplýsingum um launafyrirkomulag og launaskrá starfsmanns, t.d. skráningu áætlunar, verðlaun, frammistöðu, sölulaun, skattaupplýsingar, starfslok og launafrádrátt.

Þegar starfsmannaupplýsingar eru færðar inn skal hafa í huga eftirfarandi gögn og skilgreiningar sem eru notaðar í Dayforce.

#### <a name="general-information"></a>Almennar upplýsingar

- Númer starfsmanns (krafist)
- Fornafn (krafist)
- Eftirnafn (krafist)
- Millinafn
- Starfsaldursdagsetning
- Þekkt sem

#### <a name="personal-information"></a>Persónulegar upplýsingar

- Hjúskaparstaða (krafist)
- Fæðingardagur (krafist)
- Kyn (krafist)
- Einstaklingur sem á við fötlun að stríða
- Þjóðerni land svæði (aðeins fyrir Mexíkó)

#### <a name="address-information"></a>Upplýsingar um aðsetur

- Aðalaðsetur (krafist)
- Land/svæði (krafist)
- Póstnúmer (krafist)
- Götunúmer (krafist) (aðeins fyrir Mexíkó)
- Viðbygging (aðeins fyrir Mexíkó)
- Borg (krafist)
- Ríki (krafist)
- Sýsla (krafist)

#### <a name="contact-information"></a>Samskiptaupplýsingar 

- Aðalaðsetur (krafist)
- Símanúmer tengiliðar (krafist)
- Skráarending

#### <a name="payroll-information-and-earning-codes"></a>Launaupplýsingar og tekjukóðar

Starfsmönnum kann að vera úthlutað tilgreindum tekjum fyrir tiltekna greiðslutíðni og vera með greiðslumáta sem óskað er eftir. Eftirfarandi reitir eru notaðir í Dayforce til að tryggja að þessar óskir og stillingar séu notaðar.

##### <a name="earning-codes"></a>Tekjukóðar

- Staða (krafist)
- Tekjukóði (krafist)
- Tíðni (krafist)
- Upphæð (áskilin)

##### <a name="payroll-information"></a>Launaupplýsingar

- Greiðsluháttur
- Efnahagssvæði (krafist)
- Kenni fyrir fríðindi starfsmanna
- Kennitala (krafist)
- Hernaðarþjónustunúmer
- Auðkenni vaktar (krafist)
- Skattanúmer (krafist)
- Auðkenni stéttarfélags (krafist)
- Vinnudagskenni (krafist)
- Vinnuleyfisnúmer

> [!NOTE]
> Hvað varðar greiðslumáta þá styður Mexíkó **Reiðufé**, **Ávísun** (raunverulega ávísun fyrirtækis) og **Rafræna greiðslu**. Ef enginn greiðslumáti er tilgreindur er **Ávísun** notuð að sjálfgefnu.

#### <a name="employment-details"></a>Atvinnuupplýsingar

Upplýsingar um atvinnuferil notaðar sem lykilupplýsingar til að búa til ráðningar-, starfsloka- og endurráðningarstöður starfsmanns í Dayforce. Dayforce styður aðeins eina starfsferilsskrá í einu.

- Upphafsdagsetning ráðningar (krafist)
- Dagsetning starfsloka
- Fyrsti vinnudagur
- Breyttur fyrsti starfsdagur
- Dagsetning starfsloka (krafist við starfslok)
- Ástæða starfsloka (krafist við starfslok)

Helstu dagsetningar starfsmanns eru fengnar með eftirfarandi upplýsingum.

| Mannauður                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Nýlegasti ráðningardagurinn | Upphaf ráðningar fyrir núgildandi atvinnuferil sem ekki er lokið                                 |
| Starfslokadagur      | Starfslokadagur fyrir núgildandi atvinnuferil sem ekki er lokið                                 |
| Fyrsti vinnudagur            | Leiðréttur upphafsdagur, upphafsdagur eða upphaf ráðningar fyrir núgildandi óvirkan atvinnuferil |
| Upprunaleg ráðningardagsetning    | Upphaf ráðningar fyrir elsta atvinnuferil                                               |

#### <a name="compensation"></a>Laun

Launafyrirkomulag fastra launa verður að tengjast hverri aðalstöðu starfsmanns í gegnum ráðningartímabil. Þetta tímabil hefst þann dag sem starfsmaðurinn var ráðinn (eða upphafsdagur atvinnu) og heldur áfram fram að starfslokum.

- Gildisdagsetning (krafist)
- Gildistími
- Launataxti (krafist)
- Umreikningur launataxta (krafist)
- Árlegt jafngildi (krafist)
- Klukkutíma jafngildi (krafist)

Ef starfsmaður á tímakaupi gegnir mörgum stöðum eru föstu laun aðalstöðunnar flutt inn í Dayforce sem grunntaxti/-laun starfsmanns. Fyrir stöður sem ekki eru aðalstöður er tímakaupið vistað í samsvarandi stöðu í Dayforce.

Ef launþegi gegnir mörgum stöðum er uppsafnað tímakaup og árslaun yfir allar virkar stöður búið til og notað sem grunntaxti/-laun starfsmanns.

#### <a name="identification-numbers"></a>Auðkennisnúmer

##### <a name="social-security-identifier"></a>Auðkenni kennitölu 

Sérhver starfsmaður verður að hafa eitt aðalauðkenni. Þetta auðkenni verður að vera af auðkennisgerðinni **Kennitala**. Í Dayforce er það fengið sjálfkrafa þar sem krafist er kennitölu starfsmanns fyrir ráðningu.

- Aðalauðkenni (krafist)
- Gerð auðkennis = „Kennitala“
- Útgáfudagsetning
- Lokadagur

Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Kennitala**. Hins vegar er aðeins skráin sem merkt er sem **Aðal** samþætt í Dayforce, óháð því hvort númerið er virkt eða útrunnið.

#### <a name="bank-accounts-and-disbursements"></a>Bankareikningar og útborganir

Slá þarf inn gildar bankareikningsupplýsingar fyrir hvern þann starfsmann sem kýs að fá greitt með millifærslu á bankareikningi.

| Mannauður                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankareikningsnúmer (krafist) |                                                                                                             |
| SWIFT-kóði (krafist)          | Reiturinn **Bankakenni** notaður við vinnslu launaskráar í Mexíkó.                                                             |
| Númer útibús (krafist)       |                                                                                                             |
| Gerð bankareiknings (krafist)   | Reiturinn **Gerð reiknings** notaður við vinnslu launaskráar í Mexíkó. Studd gildi innihalda **Athugun** og **Launaskrá**. |

> [!NOTE]
> Starfsmenn sem kjósa að fá greitt með millifærslu á bankareikningi verða að gefa tengil á eftirstöðvarreikning sem er undir lögaðila sem hefur aðalaðsetrið í Mexíkó og tengist gildum bankareikningi í mexíkönskum banka. Allir aðrir reikningar eru hunsaðir.

#### <a name="address-information"></a>Upplýsingar um aðsetur

Sérhver starfsmaður verður að hafa eina aðalstaðsetningu. Í Dayforce er þessi staðsetning notuð til að ákvarða aðalbúsetu starfsmanns í skattalegum tilgangi.

- Aðalauðkenni (krafist)
- Land/svæði (krafist)
- Póstnúmer (krafist)
- Gata (krafist)
- Götunúmer (krafist)
- Býr til viðbót
- Borg (krafist)
- Ríki (krafist)
- Sýsla (krafist)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Skilgreindu gögnin þín til að búa til launaskrá fyrir Bandaríkin og Kanada

Ef þú ert að búa til laun fyrir starfsmenn í Bandaríkjunum og Kanada, þarf að skilgreina eftirfarandi þætti:

- Deildir eru nauðsynlegar fyrir stöður.
- Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.

> [!NOTE] 
> Þú getur stillt Human Resources til að krefjast þess að stöður tilgreini deild. Til að gera þetta skal fara í **Samnýttar stöður mannauðs > Stöður > Krefjast deilda á stöðum**. Við mælum með að þessari stillingu sé framfylgt fyrir samþættinguna.

### <a name="job-types"></a>Starfsgerðir

Starfsgerðir eru notaðar til að flokka svipuð störf í flokka. Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Bandaríkjunum og Kanada. Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup. Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.

Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.

| Starfsgerð   | lýsing |
|------------|-------------|
| Tímar     | Tímar      |
| Föst laun   | Föst laun    |

### <a name="position-types"></a>Stöðugerðir 

Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað. Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.

Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.

| Gerð stöðu   | lýsing        |
|-----------------|--------------------|
| Fullt starf       | Starfsmaður í fullu starfi |
| Hlutastarf       | Starfsmaður í hlutastarfi |

### <a name="reason-codes"></a>Ástæðukóðar

Ástæðukóðar veita upplýsingar um stöðu starfsmanns. Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.

Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.

| Ástæðukóði    | lýsing      | Tiltækar sviðsmyndir |
|----------------|------------------|----------------------|
| UPPSÖGN    | Uppsögn      | Segja starfskrafti upp     |
| STARFSLOK    | Lok      | Segja starfskrafti upp     |
| STARFSLOK SÖKUM ALDURS     | Starfslok       | Segja starfskrafti upp     |
| ANNAÐ          | Aðrar ástæður    | Segja starfskrafti upp     |
| DAUÐI          | Dauði            | Segja starfskrafti upp     |
| FJARVISTARLEYFI | Fjarvistarleyfi | Segja starfskrafti upp     |
| SAMNINGSLOK    | Lok á samningi  | Segja starfskrafti upp     |
| LAUNABREYTINGAR   | Breyting launa | Laun         |

### <a name="marital-status"></a>Hjúskaparstaða

Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.

| Mannauður                 | Dayforce             |
|------------------------|----------------------|
| Gift(ur)                | Gift(ur)              |
| Ein                 | Ein               |
| Ekkja/ekkill                | Ekkja/ekkill              |
| Fráskilin(n)               | Fráskilin(n)             |
| Skráð hjónaband | Sambúð |
| None                   | None                 |
| Í sambúð             | Í sambúð           |

### <a name="gender"></a>Kyn

Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.

| Mannauður       | Dayforce        |
|--------------|-----------------|
| Karl         | Karl            |
| Kona       | Kona          |
| Ótilgreint | *Ekki stutt* |

### <a name="earning-codes"></a>Tekjukóðar

Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær. Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu. Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.

#### <a name="supported-frequencies"></a>Studdar tíðnir

- Allir
- ALLAR LAUNAGREIÐSLUR
- SÉRHVERT LAUNATÍMABIL
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR - LASTOFQTR
- LASTMTHOFQTR - LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR - LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Aðsetur

Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á. Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.

| Mannauður          | Dayforce              |
|-----------------|-----------------------|
| Land/svæði  | Landsnúmer          |
| Póstnúmer | Póstnúmer           |
| Ríki           | Ríkiskóði            |
| Póststöð            | Póststöð                  |
| Sýsla          | Sýsla (sveitarfélag) |
| Gata          | Heimilisfang, lína 1        |

### <a name="tax-regions"></a>Skattumdæmi

Skattumdæmi eru notuð til að ákvarða viðeigandi skatt sem á að beita við myndun launagreiðslna. Skattasvæðum er varpað í Dayforce sem staðsetningaraðsetrum. Sjálfgefið skattumdæmi verður að vera tengt við virka stöðu starfsmannsins. 

- Skattumdæmi (krafist)
- Land/svæði (krafist)
- Ríki (krafist)
- Sýsla 
- Borg (krafist)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Skilgreindu gögnin þín til að búa til launaskrá fyrir Mexíkó

Ef þú ert að búa til laun fyrir starfsmenn í Mexíkó, þarf að skilgreina eftirfarandi þætti:

- Deildir eru nauðsynlegar fyrir stöður.
- Kostnaðarstaðir verða að vera stilltir sem fjárhagsvíddir og verða að vera fyrsti þátturinn í sjálfgefnum fjárhagsvíddarstreng.

### <a name="job-types"></a>Vinnslugerðir

Starfsgerðir eru notaðar til að flokka svipuð störf í flokka. Starfsgerðir eru nauðsynlegar til að vinna úr launaskrá í Mexíkó. Dæmi um starfsgerðir eru fullt starf og hlutastarf, eða föst laun og tímakaup. Starfsgerðum er varpað í Dayforce sem launagerðum sem gefa til kynna hvort starfsmaður sé á tímakaupi eða föstum launum.

Eftirfarandi starfsgerðir og lýsingar eru nauðsynlegar.

| Starfsgerð   | lýsing |
|------------|-------------|
| Tímar     | MX tímakaup   |
| Föst laun   | MX föst laun |

### <a name="position-types"></a>Stöðugerðir 

Þú notar stöðugerðir til að lýsa því hvort staðan er fullt starf, hlutastarf eða eitthvað annað. Stöðugerðum er varpað í Dayforce sem launaflokkum sem gefa til kynna hvort starfsmaður sé í fullu starfi eða hlutastarfi.

Eftirfarandi stöðugerðir og lýsingar eru nauðsynlegar.

| Gerð stöðu   | lýsing        |
|-----------------|--------------------|
| Fullt starf       | Starfsmaður í fullu starfi |
| Hlutastarf       | Starfsmaður í hlutastarfi |

### <a name="reason-codes"></a>Ástæðukóðar

Ástæðukóðar veita upplýsingar um stöðu starfsmanns. Ástæðukóðum er varpað í Dayforce sem stöðuástæðum sem gefa til kynna ástæðuna fyrir breytingum á stöðu sem starfsmaður gegnir eða stöðu á starfsmanni.

Eftirfarandi ástæðukóðar og lýsingar eru nauðsynlegar.

| Ástæðukóði            | lýsing                    | Tiltækar sviðsmyndir |
|------------------------|--------------------------------|----------------------|
| BROTTFÖR Á UNDAN LAUNAGREIÐSLU | Brottför á undan launum | Segja starfskrafti upp     |
| UPPSÖGN            | Uppsögn                    | Segja starfskrafti upp     |
| LÍFEYRIR                | Lífeyrir                        | Segja starfskrafti upp     |
| STARFSLOK            | Lok                    | Segja starfskrafti upp     |
| STARFSLOK SÖKUM ALDURS             | Starfslok                     | Segja starfskrafti upp     |
| FJARVERA               | Fjarvera                       | Segja starfskrafti upp     |
| ANNAÐ                  | Aðrar ástæður                  | Segja starfskrafti upp     |
| LOKUN                | Viðskiptalokun               | Segja starfskrafti upp     |
| DAUÐI                  | Dauði                          | Segja starfskrafti upp     |
| FJARVISTARLEYFI         | Fjarvistarleyfi               | Segja starfskrafti upp     |
| SAMNINGSLOK            | Lok á samningi                | Segja starfskrafti upp     |
| LAUNABREYTINGAR           | Breyting launa               | Laun         |

### <a name="terms-of-employment"></a>Ráðningarskilmálar

Ráðningarskilmálar eru notaðir til að búa til flokka fyrir skilmála ráðningar. Skilmálunum er varpað í Dayforce sem gildum starfsmannavísis.

Eftirfarandi ráðningarskilmálar og lýsingar eru nauðsynlegar.

| Ráðningarskilmálar   | lýsing |
|-----------------------|-------------|
| Venjuleg               | Venjuleg     |
| Beint                | Beint      |
| Starfsnám            | Starfsnám  |
| Fast             | Fast   |

### <a name="marital-status"></a>Hjúskaparstaða

Gildi hjúskaparstöðu er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

Eftirfarandi tafla sýnir hvernig gildum hjúskaparstöðu er varpað í Dayforce.

| Mannauður                 | Dayforce                  |
|------------------------|---------------------------|
| Gift(ur)                | Gift(ur)                   |
| Ein                 | Ein                    |
| Ekkja/ekkill                | Ekkja/ekkill                   |
| Fráskilin(n)               | Fráskilin(n)                  |
| Skráð hjónaband | Sambúð      |
| None                   | *Ekki stutt af Mexíkó* |
| Í sambúð             | *Ekki stutt af Mexíkó* |

### <a name="gender"></a>Kyn

Merki kyns er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

Eftirfarandi tafla sýnir hvernig kynjamerkingu er varpað í Dayforce.

| Mannauður       | Dayforce                  |
|--------------|---------------------------|
| Karl         | Karl                      |
| Kona       | Kona                    |
| Ótilgreint | *Ekki stutt af Mexíkó* |

### <a name="payment-method"></a>Greiðslumáti

Greiðslumátar bjóða starfsmanni og fyrirtæki upp á leið til að lýsa því hvernig starfsmenn fá greitt. Greiðslumátum er varpað í Dayforce og þýtt, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

Eftirfarandi tafla sýnir hvernig greiðslumátum er varpað í Dayforce.

| Mannauður             | Dayforce                  |
|--------------------|---------------------------|
| Innlausn               | Innlausn                      |
| Rafræn greiðsla | Flutningur                  |
| Villuleit              | Ávísun                    |
| Bankaávísun         | *Ekki stutt af Mexíkó* |
| Annað              | *Ekki stutt af Mexíkó* |

### <a name="bank-account-type"></a>Gerð bankareiknings

Gerðir bankareikninga eru notaðar fyrir rafrænar greiðslur til starfsmanna. Gerðum bankareikninga er varpað í Dayforce sem upplýsingum um millifærslureikninga. Gerðir bankareikninga eru þýddar, eftir því sem við á, yfir í samþykkt gildi við samþættingu.

| Mannauður            | Dayforce                  |
|-------------------|---------------------------|
| Ávísanareikningur  | CheckingAccount           |
| Launareikningur   | PayrollAccount            |
| Sparnaðarreikningur   | *Ekki stutt af Mexíkó* |
| BankGirot-reikningur | *Ekki stutt af Mexíkó* |
| PlusGirot-reikningur | *Ekki stutt af Mexíkó* |

### <a name="earning-codes"></a>Tekjukóðar

Tekjukóðar auðkenna með einkvæmum hætti allar gerðir af tekjum sem starfsmaður fær. Kóðarnir ná yfir ýmsar færibreytur sem tengjast tekjum, svo sem bókhaldsreglum, skattalögum, skýrslukröfum og hækkunargetu. Ef óþekkt tíðni er notuð er tíðnin **Sérhver launagreiðsla** notuð sjálfgefið fyrir útreikning.

#### <a name="supported-frequencies"></a>Studdar tíðnir

- Allir
- ALLAR LAUNAGREIÐSLUR
- SÉRHVERT LAUNATÍMABIL
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR - LASTOFQTR
- LASTMTHOFQTR - LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR - LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Aðsetur

Að bera kennsl á kóða tiltekins lands eða svæðis, ríkis og fylkis (sveitarfélags) krefst sérstakra sniða sem Dayforce og innlendir veitendur/svæðisveitendur geta borið kennsl á. Þótt snið fyrir borgir sé sveigjanlegt, verður hver borg að vera tengd ríki.

| Mannauður              | Dayforce              |
|---------------------|-----------------------|
| Land/svæði      | Landsnúmer          |
| Póstnúmer     | Póstnúmer           |
| Ríki               | Ríkiskóði            |
| Póststöð                | Póststöð                  |
| Sýsla              | Sýsla (sveitarfélag) |
| Gata              | Heimilisfang, lína 1        |
| Húsnúmer       | Heimilisfang, lína 2        |
| Býr til viðbót | Heimilisfang, lína 5        |

### <a name="passport-number"></a>Vegabréfsnúmer

Starfsmenn geta gefið upp vegabréfsupplýsingar. Þessar upplýsingar eru af auðkennisgerðinni **Vegabréf** og eru samþættar í Dayforce sem hluti af tilteknum mexíkönskum upplýsingum starfsmanns.

- Gerð auðkennis = „Vegabréf“
- Útgáfudagsetning
- Lokadagur

Starfsmenn geta gefið upp mörg auðkennisnúmer af auðkennisgerðinni **Vegabréf**. Hins vegar er aðeins núverandi virka færslan samþætt í Dayforce. Ef allar vegabréfsfærslur eru útrunnar verður vegabréfið sem síðast var gefið út samþætt í Dayforce.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
