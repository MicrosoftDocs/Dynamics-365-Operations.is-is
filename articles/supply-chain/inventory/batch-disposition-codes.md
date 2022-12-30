---
title: Nota keyrsluráðstöfunarkóða til að merkja keyrslur sem tiltækar eða ekki í boði
description: Þessi grein útskýrir hvernig á að setja upp og nota ráðstöfunarkóða runu til að merkja runur sem tiltækar eða ekki tiltækar fyrir notkun í aðaláætlanagerð, frátekningu, tínslu og/eða afhendingu.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542907"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Nota keyrsluráðstöfunarkóða til að merkja keyrslur sem tiltækar eða ekki í boði

Þessi grein útskýrir hvernig á að setja upp og nota *ráðstöfunarkóða runu*. Hver ráðstöfunarkóði runu er með stöðu sem er annaðhvort *Tiltæk* eða *Ekki tiltæk*. Þú úthlutar ráðstöfunarkóðum runu á birgðarunur til að tilgreina hvort hver runa sé tiltæk fyrir aðaláætlanagerð, frátekningu, tínslu og/eða afhendingu.

Til að nota ráðstöfunarkóða runu þarf að setja upp kóðana og úthluta þeim á runur sem á að stjórna.

## <a name="set-up-batch-disposition-codes"></a>Setja upp ráðstöfunarkóða runu

Þú verður að setja upp hvern ráðstöfunarkóða runu fyrir sig sem þú vilt nota í kerfinu. Hægt er að búa til eins marga kóða og þörf krefur. (Til dæmis er hægt að búa til kóða til að bera kennsl á mismunandi ástæður þess að lotan gæti verið tiltæk eða ekki tiltæk). Hins vegar eru oft bara tveir kóðar í boði: einn fyrir *í boði* og einn fyrir *ekki í boði*. Einnig er hægt að búa til sérsniðna kóða sem gera kleift að nota runu fyrir sumar aðgerðir en ekki aðrar.

Fylgdu þessum skrefum til að setja upp ráðstöfunarkóða runu.

1. Farðu í **Birgðastjórnun \> Uppsetning \> Runa \> Aðalrunuráðstöfun**.
1. Síðan **Aðalrunuráðstöfun** sýnir núverandi ráðstöfunarkóða runu og gerir þér kleift að stofna, eyða eða breyta þeim. Fylgið einu af eftirfarandi skrefum:

    - Til að breyta fyrirliggjandi kóða skal velja hann á listasvæðinu.
    - Til að stofna nýjan kóða er valið **Nýr** á aðgerðasvæðinu.

1. Í haus nýja eða valda kóðans skal stilla eftirfarandi reiti:

    - **Ráðstöfunarkóði runu** – Sláðu inn birtingarheiti fyrir kóðann.
    - **Lýsing** – Lýsir því hvernig kóðinn á að vera notaður.
    - **Ráðstöfunarstaða runu** – Veldu stöðuna sem á við lotur sem kóðanum er úthlutað:

        - *Ekki tiltækt* – Ekki er hægt að nota runurnar fyrir aðaláætlanagerð, frátekningu, tínslu eða afhendingu. Þegar þú velur þetta gildi eru allir valkostirnir **Útiloka** í flýtiflipanum **Uppsetning** stilltir á *Já* og allir valkostirnir **Nettó** stilltir á *Nei*. Hins vegar er hægt að breyta sumum þessara stillinga til að bæta við undantekningum.
        - *Tiltækt* – Ekki er hægt að nota runurnar fyrir aðaláætlanagerð, frátekningu, tínslu og/eða afhendingu. Þegar þetta gildi er valið eru allir valkostirnir **Útiloka** í flýtiflipanum **Uppsetning** stilltir á *Nei* og allir valkostirnir **Nettó** eru stilltir á *Nei*. Þessar stillingar verða skrifvarðar á meðan reiturinn **Ráðstöfunarstaða runu** er stilltur á *Tiltækt*.

1. Ef þú stillir reitinn **Ráðstöfunarstaða runu** á *Ekki tiltækt* er hægt að sérsníða útilokunarstöðu hverrar aðgerðar (frátekning, tínsla og afhending) fyrir hverja gerð af pöntun (sölu, flutning og framleiðslu). Fyrir framleiðslupantanir er hægt að loka eða opna tínslubók framleiðslu. Einnig er hægt að velja að útiloka eða opna á aðaláætlanagerð. Notaðu valkostina í flýtiflipanum **Uppsetning** til að loka eða opna á hverja aðgerð eftir þörfum. Stilltu valkostinn **Nettó** á *Já* til að virkja aðaláætlanagerð eða stilltu hann á *Nei* til að útiloka aðaláætlanagerð.

## <a name="assign-batch-disposition-codes-to-batches"></a>Úthluta ráðstöfunarkóðum runu á runur

Eftir að þú hefur skilgreint lotukóðana sem þú krefst skaltu fylgja þessum skrefum til að úthluta þeim í lotur.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Runur**.
1. Velja eina eða fleiri lotur til að úthluta ráðstöfunarkóða lotu á.
1. Á aðgerðasvæðinu, í flipanum **Endurstilla**, skal velja **Endurstilla ráðstöfunarkóða runu**.
1. Í svarglugganum **Breyta takmörkunum á birgðarunu** skal stilla reitinn **Nýr ráðstöfunarkóði runu** á heiti kóðans sem þú vilt úthluta.
1. Veldu **Í lagi** til að nota nýju stillinguna og vista breytinguna þína.

    Á síðunni **Runur** eru gildin í dálkunum **Ráðstöfunarkóði runu** og **Ráðstöfunarstaða runu** uppfærð þannig að þau endurspegli nýju stillingarnar fyrir valdar runur.

## <a name="master-planning-example"></a>Dæmi um aðaláætlanagerð

Þetta dæmi sýnir hvernig ráðstöfunarkóðar runu geta haft áhrif á aðalskipulag.

Fyrir þetta dæmi eru ráðstöfunarkóðar runu settir upp á eftirfarandi hátt:

- *P-tiltækt:*

    - **Ráðstöfunarstaða runu:** *Tiltækt*
    - **Nettó:** *Já*

- *P-ekki í boði:*

    - **Ráðstöfunarstaða runu:** *Ekki tiltækt*
    - **Nettó:** *Nei*

Það er til vara (*Vara-1*) sem er með tvær runur: *Runa-A* og *Runa-B*. Þessar lotur eru settar upp á eftirfarandi hátt:

- *Lota-A:*

    - **Ráðstöfunarkóði runu:** *P-tiltækt*
    - **Lagerbirgðir:** 1

- *Lota-B:*

    - **Ráðstöfunarkóði runu:** *P-ekki tiltækt*
    - **Lagerbirgðir:** 1

Það er til sölupöntun (*SO1*) fyrir magn upp á 2 af vörunni *Vara-1*. Afhendingardagurinn er þrír dagar frá deginum í dag.

Þú verður að keyra aðaláætlanagerð og stilla eftirfarandi gildi sem tengjast þessu dæmi:

- **Áætluð pöntun:** *Innkaupapöntun*
- **Áfyllingaráætlun:** *Krafa*
- **Afhendingartími:** *0*

Í kjölfar áætlunarkeyrslunnar notar kerfið tiltæka runu (*Runu-A*) til að ná yfir magn 1 af vörunni *Vara-1* fyrir sölupöntun *SO1*. Hins vegar getur það ekki notað lotu *Batch-B* þar sem sú lota er merkt sem ekki í boði fyrir skipulagningu. Til að ná yfir eftirstandandi magn stofnar kerfið þar af leiðandi áætlaða innkaupapöntun (*PPO1*) fyrir nýja runu af vörunni *Vara-1*.

Eftirfarandi skýringarmynd sýnir tímalínu fyrir áætlunarniðurstöðuna.

![Dæmi sem sýnir hvernig ráðstöfunarkóðar runu geta haft áhrif á aðalskipulag](media/batch-codes-planning-example.png "Dæmi sem sýnir hvernig ráðstöfunarkóðar runu geta haft áhrif á aðalskipulag")
