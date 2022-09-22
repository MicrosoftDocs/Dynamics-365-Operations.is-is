---
title: Notaðu loturáðstöfunarkóða til að merkja lotur sem tiltækar eða ekki tiltækar
description: Þessi grein lýsir því hvernig á að setja upp og nota loturáðstöfunarkóða til að merkja lotur sem tiltækar eða ekki tiltækar til notkunar við aðalskipulagningu, pöntun, tínslu og/eða sendingu.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542907"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Notaðu loturáðstöfunarkóða til að merkja lotur sem tiltækar eða ekki tiltækar

Þessi grein lýsir því hvernig á að setja upp og nota *loturáðstöfunarkóðar*. Hver lotuúthlutunarkóði hefur stöðuna annað hvort *Laus* eða *Ekki tiltækt*. Þú úthlutar runuafgreiðslukóðum á birgðalotur til að gefa til kynna hvort hver lota sé tiltæk fyrir aðalskipulagningu, pöntun, tínslu og/eða sendingu.

Til að nota lotuúthlutunarkóða verður þú að setja upp kóðana og úthluta þeim á runurnar sem þú vilt stjórna.

## <a name="set-up-batch-disposition-codes"></a>Settu upp loturáðstöfunarkóða

Þú verður að setja upp hvern lotuúthlutunarkóða sem þú vilt nota í kerfinu þínu. Þú getur búið til eins marga kóða og þú vilt. (Til dæmis geturðu búið til kóða til að bera kennsl á mismunandi ástæður fyrir því að lota gæti verið tiltæk eða ekki tiltæk). Hins vegar muntu oft hafa bara tvo kóða: einn fyrir *laus* og einn fyrir *ófáanlegt*. Þú getur líka búið til sérsniðna kóða sem gera kleift að nota runu fyrir sumar aðgerðir en ekki aðrar.

Fylgdu þessum skrefum til að setja upp loturáðstöfunarkóða.

1. Fara til **Vörustjórnun \> Uppsetning \> Hópur \> Hópráðstöfunarstjóri**.
1. The **Hópráðstöfunarstjóri** síða sýnir núverandi loturáðstöfunarkóða og gerir þér kleift að búa til, eyða og breyta þeim. Fylgið einu af eftirfarandi skrefum:

    - Til að breyta núverandi kóða skaltu velja hann á listaglugganum.
    - Til að búa til nýjan kóða skaltu velja **Nýtt** á aðgerðasvæðinu.

1. Stilltu eftirfarandi reiti í haus nýja eða valda kóðans:

    - **Kóði fyrir loturáðstöfun** – Sláðu inn skjáheitið fyrir kóðann.
    - **Lýsing** – Lýstu því hvernig ætti að nota kóðann.
    - **Staða loturáðstöfunar** – Veldu stöðuna sem á við um lotur sem kóðanum er úthlutað:

        - *Ekki tiltækt* – Ekki er hægt að nota loturnar fyrir aðalskipulagningu, pöntun, tínslu eða sendingu. Þegar þú velur þetta gildi munu öll **Block** valkostir á **Uppsetning** Flýtiflipar eru stilltir á *Já*, og öll **Nettablettur** valkostir eru stilltir á *Nei*. Hins vegar geturðu breytt sumum þessara stillinga til að bæta við undantekningum.
        - *Laus* – Hægt er að nota loturnar fyrir aðalskipulagningu, pöntun, tínslu og/eða sendingu. Þegar þú velur þetta gildi munu öll **Block** valkostir á **Uppsetning** Flýtiflipar eru stilltir á *Nei*, og öll **Nettablettur** valkostir eru stilltir á *Já*. Þessar stillingar verða eingöngu skriflegar á meðan **Staða loturáðstöfunar** reiturinn er stilltur á *Laus*.

1. Ef þú stillir **Staða loturáðstöfunar** sviði til *Ekki tiltækt*, þú getur sérsniðið blokkarstöðu hverrar aðgerðar (forða, tína og senda) fyrir hverja tegund pöntunar (sala, flutningur og framleiðsla). Fyrir framleiðslupantanir geturðu valið að loka fyrir eða opna framleiðslutínslubókina. Þú getur líka valið að loka á eða opna aðalskipulagningu. Notaðu valkostina á **Uppsetning** Flýtiflipa til að loka fyrir eða opna hverja aðgerð eftir þörfum. Stilltu **Nettablettur** valmöguleika til *Já* til að virkja aðalskipulag, eða stilla það á *Nei* að hindra aðalskipulag.

## <a name="assign-batch-disposition-codes-to-batches"></a>Úthlutaðu loturáðstöfunarkóðum til runum

Eftir að þú hefur skilgreint loturáðstöfunarkóðana sem þú þarfnast skaltu fylgja þessum skrefum til að úthluta þeim á runur.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Birgðir \> Lotur**.
1. Veldu eina eða fleiri lotur til að úthluta loturáðstöfunarkóða til.
1. Á aðgerðarrúðunni, á **Endurstilla** flipa, veldu **Endurstilla lotuúthlutunarkóða**.
1. Í **Breyttu takmörkunum á birgðalotunni** valmynd, stilltu **Nýr lotuúthlutunarkóði** reitnum við nafn kóðans sem þú vilt úthluta.
1. Veldu **Allt í lagi** til að nota nýju stillinguna og vista breytinguna þína.

    Á **Lotur** síðu, gildin í **Kóði fyrir loturáðstöfun** og **Staða loturáðstöfunar** dálkar eru uppfærðir þannig að þeir endurspegli nýju stillingarnar fyrir valdar lotur.

## <a name="master-planning-example"></a>Aðalskipulagsdæmi

Þetta dæmi sýnir hvernig runuráðstöfunarkóðar geta haft áhrif á aðalskipulagningu.

Fyrir þetta dæmi eru loturáðstöfunarkóðar settir upp á eftirfarandi hátt:

- *P-Fáanlegt:*

    - **Staða loturáðstöfunar:** *Laus*
    - **Nettafla:** *Já*

- *P-ófáanlegt:*

    - **Staða loturáðstöfunar:** *Ekki tiltækt*
    - **Nettafla:** *Nei*

Það er vara (*Vara-1*) sem hefur tvær lotur: *Hópur-A* og *Hópur-B*. Þessar lotur eru settar upp á eftirfarandi hátt:

- *Lota-A:*

    - **Kóði fyrir loturáðstöfun:** *P-Fáanlegt*
    - **Magn á lager:** 1

- *Batch-B:*

    - **Kóði fyrir loturáðstöfun:** *P-Ótiltækt*
    - **Magn á lager:** 1

Það er sölupöntun (*SO1*) fyrir magn af 2 vöru *Vara-1*. Afhendingardagur er þrír dagar frá deginum í dag.

Þú keyrir aðalskipulagningu og stillir eftirfarandi gildi sem eiga við þetta dæmi:

- **Fyrirhuguð pöntun:** *Pöntun*
- **Endurnýjunarstefna:** *Krafa*
- **Afhendingartími:** *0*

Sem afleiðing af áætlanagerðinni notar kerfið tiltæka lotuna (*Hópur-A*) til að ná yfir magn af 1 vöru *Vara-1* fyrir sölupöntun *SO1*. Hins vegar getur það ekki notað lotu *Hópur-B* vegna þess að sú lota er merkt sem ekki tiltæk til áætlanagerðar. Þess vegna stofnar kerfið fyrirhugaða innkaupapöntun til að standa undir því magni sem eftir er (*PPO1*) fyrir nýja vörulotu *Vara-1*.

Eftirfarandi mynd sýnir tímalínu fyrir niðurstöðu skipulags.

![Dæmi sem sýnir hvernig loturáðstöfunarkóðar geta haft áhrif á aðalskipulagningu.](media/batch-codes-planning-example.png "Dæmi sem sýnir hvernig loturáðstöfunarkóðar geta haft áhrif á aðalskipulagningu")
