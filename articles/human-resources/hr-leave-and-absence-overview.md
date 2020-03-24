---
title: Yfirlit
description: Í Dynamics 365 Human Resources veitir vinnusvæðið **Leyfi og fjarvera** sveigjanlegan ramma til að stofna nýjar orlofsáætlanir, verkflæði til að stjórna beiðnum og innsæi sjálfsþjónustusíða þar sem starfsmenn geta beðið um frí.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091749"
---
# <a name="overview"></a>Yfirlit

Dynamics 365 Human Resources hjálpar þér að veita starfsmönnum þínum mikinn orlof. Vinnusvæðið **Leyfi og fjarvera** býður upp á sveigjanlegan ramma til að búa til ný orlofsáætlun, verkflæði til að stjórna beiðnum og innsæi sjálfsþjónustusíða þar sem starfsmenn geta beðið um frí. Greining hjálpar fyrirtækinu þínu að mæla og fylgjast með orlofshlutfalli og notkun vegna orlofssókna.

## <a name="set-up-leave-and-absence"></a>Setja upp leyfi og fjarvistir

Áður en þú getur búið til orlof fyrir starfsmenn þína þarftu að gera nokkur uppsetningarskref:

- [Grunnstilla færibreytur leyfis og fjarvista](hr-leave-and-absence-parameters.md)
- [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md)
- [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Stofnun og umsjón með orlofsáætlunum

Áður en þú býrð til orlofsáætlun fyrir starfsmenn þína þarftu að búa til orlofs- og fjarverutegundir. Eftir að þú hefur búið til orlofssamninga geturðu síðan skráð starfsmenn í áætlunina. Þú getur einnig keyrt uppsöfnunarferlið, búið til viðvaranir og skoðað greiningar fyrir áætlanir þínar.

- [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)
- [Búa til leyfis- og fjarvistaáætlun](hr-leave-and-absence-plans.md)
- [Úthluta starfsmönnum á leyfisáætlun](hr-leave-and-absence-enroll.md)
- [Uppsöfnunaráætlanir fyrir leyfi og fjarvistir](hr-leave-and-absence-accrue.md)
- [Skoða greiningu á leyfum og fjarvistum](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Biðja um frí og hafa umsjón með beiðnum

Starfsmenn þínir geta sent inn beiðnir um frí og þú getur stjórnað þeim í **Sjálfsafgreiðsla starfsmanna** vinnusvæði.

- [Biðja um frí](hr-employee-self-service-request-time-off.md)
- [Vinna með beiðnir um leyfi og fjarvistir](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Forskoðunareiginleikar leyfis og fjarveru

Þú getur prófað nýja forskoðunareiginleika leyfis og fjarveru í **Sandkassi** umhverfi. Upplýsingar um stillingu forútgáfueiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md). Forskoðunareiginleikar eru:

- **Orlof og fjarvistardagatal** - Færibreytur í leyfi og fjarveru flytjast úr **Færibreytur Human Resources** á nýjan skjá sem heitir **Færibreytur leyfis og fjarveru**. Nýi skjárinn inniheldur nýja flipann **Dagatal**. Þessi forskoðun gerir aðeins kleift að setja undirhóp færibreytanna. Þú getur fengið aðgang að nýjum skjá af flipanum **Tenglar** á vinnusvæðinu **Leyfi og fjarvera**. Dagatölin innihalda:
  - **Fyrirtækjadagatal** - sýnir allar beiðnir um frí frá starfsmönnum. Fólk með hlutverkið **Human Resources** getur fengið aðgang að þessu dagatali á flipanum **Tenglar** á vinnusvæðinu **Leyfi og fjarvera**.
  - **Dagatal stjórnanda** - sýnir beiðni um beinar skýrslur um tímalengd. Stjórnendur geta nálgast dagatalið á flipanum **Liðið mitt** í sjálfsafgreiðslu starfsmanna undir **Leyfi og fjarvera**. 

- **Frídagatal vegna orlofs og fjarveru** - Leyfistegundir fela í sér nýjan valkosti **Frí**, notaður í tengslum við vinnutímadagatalið. Dagar skilgreindir með hátíðum og lokunum eru nú tilnefndir **Frí** þegar vinnudagar eru búnir til. Þegar unnið er úr áföllum eru gerðar leiðréttingar á starfsmönnum sem eru úthlutaðir á dagatalið til að gera grein fyrir hátíðum sem falla á virkum degi.

- **Skildu eftir endurskoðun** - Nýr skjár gerir þér kleift að skoða hvenær áföll hafa verið afgreidd og eytt, bæði af öllum starfsmönnum og einstökum starfsmönnum. Þú getur fengið aðgang að þessum nýja skjá af flipanum **Tenglar** á vinnusvæðinu **Leyfi og fjarvera**.

- **Eyðing leyfisuppsöfnunar** - Þú getur nú eytt uppsöfnunargögnum fyrir tiltekin orlofsáætlun. Þú getur fengið aðgang að þessum nýja valkosti af flipanum **Tenglar** á vinnusvæðinu **Leyfi og fjarvera**. Fyrir einstaka starfsmenn birtist þessi valkostur í flokkuninni **Leyfi og fjarvera** í starfsmannasniðinu. 

- **Uppsöfnunarnámundun leyfis** - Nýir möguleikar fyrir **Gerð leyfis** skilgreina hvaða gerð námundunaruppsöfnunar skuli nota, auk aukafræðilegs nákvæmni námundunarinnar meðan á uppsöfnunarferlinu stendur. Þegar unnið er úr uppsöfnunum er námundun og nákvæmni beitt á rekstrarreikningana. 

- **Stilltu margar orlofstegundir á einni orlofssamþykkt** - Nýr dálkur í áætlun orlofssöfnunar fyrir orlofstegundir gerir þér kleift að skilgreina margar orlofstegundir í orlofs- og fjarveruáætlun með mismunandi uppsöfnunaráætlunum. Fyrri reiturinn **Gerð leyfis** er fjarlægður. Við innritun starfsmanna birtast nú jafnvægi fyrir orlofstegundirnar í töflu í staðinn fyrir efst á skjánum.

  > [!IMPORTANT]
  > Þú getur ekki slökkt á þessum eiginleika eftir að þú hefur gert það virkt.

- **Notaðu stöðugildi starfsmanns (FTE) til uppsöfnunar** - nýr dálkur á áætlun orlofssöfnunar gerir kleift að nota FTE til uppsöfnunar. Þegar uppsöfnun er afgreidd notar forritið aðalstöðu starfsmanns og FTE skilgreint til að ákvarða hlutfallslega uppsöfnunarfjárhæðina.

  > [!NOTE]
  > Þessi aðgerð er aðeins tiltæk ef þú gerir það virkt **Stilla margar orlofstegundir á hverja orlofsáætlun**. 
