---
title: Endurstilla númer kvittunar
description: Þessi grein lýsir því hvernig á að endurstilla kvittunarnúmerin sem eru notuð fyrir ýmsar aðgerðir á tiltekinni dagsetningu (til dæmis reikningsár eða almanaksár).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, Commerce
ms.search.form: ''
ms.openlocfilehash: 3034a1b8f1a9f304b8d8803a7f906418321d81d9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272742"
---
# <a name="reset-receipt-numbers"></a>Endurstilla númer kvittunar 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Við krefjumst þess að notandi velji eiginleikann **Sjálfstæð röð** fyrir allar kvittanategundir í virknireglunni áður en eiginleikinn er notaður. Einnig ætti tímabelti kerfisins, þar sem sölustaðurinn er notaður, að passa við samsvarandi tímabelti verslunarinnar. Vegna þessara takmarkana er mælt með því að nota ekki þennan eiginleika í framleiðslu á meðan unnið er að því að leysa þessi vandamál í framtíðarútgáfu. 

Söluaðilar búa til innhreyfingartölur fyrir ýmsar aðgerðir í versluninni, svo sem staðgreiddar færslur, skilafærslur, pantanir viðskiptavina, tilboð og greiðslur. Þrátt fyrir að smásalar skilgreini eigin innhreyfingarsnið, hafa sum lönd eða svæði reglur sem setja takmarkanir á þessi innhreyfingarsnið. Til dæmis gætu þessar reglugerðir takmarkað fjölda stafa í kvittuninni, krafist röð kvittunarnúmera, takmarkað einhverja sérstaka stafi eða krafist endurstillingar kvittunúmera í byrjun árs. Microsoft Dynamics 365 Commerce gerir stjórnunarferlið fyrir kvittunarnúmer sveigjanlegra, til að hjálpa smásölum að uppfylla kröfur vegna reglugerða. Þessi grein útskýrir hvernig á að nota virknina til að endurstilla kvittunarnúmer.

Í viðskiptum geta kvittunarsnið verið bókstafleg. Þú getur sett bæði fast efni og kvikt efni í það. Fast efni inniheldur stafrófsröð, tölur og sértákn. Kvikt efni inniheldur einn eða fleiri stafi sem tákna upplýsingar, svo sem verslunarnúmer, afgreiðslukassanúmer, dagsetningu, mánuð, ár og númeraröð sem hækkar sjálfkrafa. Sniðin eru skilgreind í **Númer kvittunar** hluti af virknireglunni. Eftirfarandi tafla lýsir stöfum sem tákna kvikt efni.

| Stafir | Lýsing |
|------------|-------------|
| L          | Stafurinn **S** er notað fyrir verslunarnúmerið. Til dæmis, ef verslun er númeruð HOUSTON1 sýnir sniðið **SSS** „ON1“ á kvittuninni. Sniðið **SSSSS** sýnir „STON1“ á kvittuninni. |
| T          | Stafurinn **T** er notað fyrir afgreiðslukassanúmerið. Til dæmis, ef afgreiðslukassi er með númerið 0001 sýnir sniðið **TTTT** „0001“ á kvittuninni. |
| K          | Stafurinn **C** er notað fyrir starfsmannakennisnúmerið. Til dæmis, ef starfsmaður er með auðkenni 000160 sýnir sniðið **CCCC** „0160“ á kvittuninni. |
| ddd        | Stafirnir **ddd** samsvara degi ársins, frá 1 til og með 366. Til dæmis, þann 15. janúar sýnir sniðið **ddd** „015“ á kvittuninni. |
| Vörpun líkans         | Stafirnir **MM** eru notaðir fyrir tveggja stafa mánuð. Til dæmis, í janúar sýnir sniðið **MM** „01“ á kvittuninni. |
| DD         | Stafirnir **DD** eru notaðir fyrir tveggja stafa mánaðardag. Til dæmis, þann 15. janúar sýnir sniðið **DD** „15“ á kvittuninni. |
| YY         | Stafirnir **YY** eru notaðir fyrir tveggja stafa ár. Til dæmis, í hvaða mánuði sem er á árinu 2020 sýnir sniðið **YY** „20“ á kvittuninni. |
| \#         | Tölumerki (**\#**) er notað við röðun. Til dæmis sýnir sniðið **####** „0001”, „0002”, 0003, o.s.frv., á kvittuninni. |

Þú getur endurstillt raðnúmer kvittunarinnar á tiltekinni dagsetningu. Síðan, í fyrslu færslunni sem á sér stað eftir klukkan 12:00 f.h. á völdum endurstillingardegi endurstillir kerfið númeraröð kvittunarinnar á 1. Þú getur einnig tilgreint hvort endurstilling á sér stað aðeins í eitt skipti, eða hvort hún endurtekur sig á hverju ári. Ef árleg endurtekning er tilgreind á sér stað endurstillingin sjálfkrafa á hverju ári þar til smásalinn kýs að stöðva það. 

Fylgdu þessum skrefum til að kveikja á endurstillingu.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**.
1. Á flýtiflipanum **Númer kvittunar**, veldu **Endurstilla endurstillingardag númers**.
1. Í fellivalmyndinni, í reitnum **Endurstilla dagsetningu**, veldu framtíðardagsetningu þegar núllstillingin ætti að eiga sér stað.
1. Í reitnum **Endurstilla tegund kvittunar**, veldu **Aðeins einu sinni** eða **Árlega**.
1. Veldu **Í lagi**.

![Val á endurstillingu dagsetningar kvittunar.](media/Enable_receipt_reset.png "Val á endurstillingu dagsetningar kvittunar")

Þegar þú hefur valið dagsetningu birtist hún í dálknum **Næsti endurstillingardagur kvittunarnúmera**. Endurstillingardagsetningin gildir fyrir allar gerðir kvittunarfærslna. Þess vegna verður kvittunarnúmeraröðin endurstillt fyrir allar gerðir kvittunar.

Þegar endurstillingardagsetning kemur er kvittunarnúmerið endurstillt fyrir fyrstu færslu af hverri gerð. Að auki, í virkni sniðinu, er núllstillingar dagsetningin færð úr dálknum **Næsti endurstillingardagur kvittunarnúmera** í dálkinn **Núverandi endurstillingardagsetning kvittunarnúmera**. Þessi breyting gefur til kynna að ef skrá er ekki notuð á endurstillingardagsetningu verður kvittunarnúmerið endurstillt næst þegar skráin er *er* notuð. Til dæmis, 3. desember 2019, velurðu **1. janúar 2020**, sem endurstillingardagsetningu. 1. janúar, þegar kassarnir gera fyrstu færslurnar, er kvittunarnúmerið endurstillt. Ein skrá er þó alls ekki notuð í desember og janúar en byrjar síðan að verða notuð í febrúar. Í þessu tilfelli, vegna þess að endurstilla aðgerð var skilgreind, verður kvittunarnúmer fyrir þá skrá endurstillt þegar skráin gerir fyrstu viðskipti sín í febrúar.

Þú getur notað **Hreinsa endurstillingar dagsetningu** virkni til að hreinsa framtíðarstillingardagsetningar. Hins vegar, ef endurstillingardagsetningin átti sér stað í fortíðinni, er ekki hægt að afturkalla það. Þess vegna mun núllstillingin eiga sér stað fyrir allar skrár þar sem núllstillingin hefur ekki enn átt sér stað.

> [!NOTE]
> Það fer eftir endurstillingardagsetningu sem þú velur og kvittunarsnið, þú gætir haft afrit kvittunarnúmera. Þrátt fyrir að sölustaðurinn (POS) kerfið geti sinnt þessum aðstæðum, eykur það tímann sem þarf til að vinna úr ávöxtun, því söluaðilar verða að velja meðal afritskvittana. Önnur flækjustig sem tengjast gagnahreinsun geta komið fram ef afritskvittanirnar voru ekki fyrirhugaðar afleiðingar. Þess vegna mælum við með því að þú notir kvika dagsetningarstafi (til dæmis, **ddd**, **MM**, **DD** og **JÁ**) til að koma í veg fyrir afritunarkvittunúmer eftir endurstillingu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
