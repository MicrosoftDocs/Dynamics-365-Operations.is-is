---
title: Takmörkuð afkastagetuáætlun og skipulagning
description: Takmörkuð áætlanagerð er aðferð sem hjálpar þér að skilja hversu mikil vinna getur farið fram á tilteknu tímabili þegar tekið er tillit til takmarkana á mismunandi tilföngum.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 5f02ec58c88cfd0d663a97de4e3e4dff1cdd5e90
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740087"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Takmörkuð afkastagetuáætlun og skipulagning

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Takmörkuð geta er aðferð sem hjálpar þér að skilja hversu mikil vinna getur farið fram á tilteknu tímabili þegar tekið er tillit til takmarkana á mismunandi tilföngum. Tilgangur takmarkaðrar áætlanagerðar er að tryggja að vinna gangi fyrir sig á jöfnum og skilvirkum hraða í gegnum stöðina.

Skipulagning takmarkaðrar getu og áætlanagerð skapar raunhæfari áætlun fyrir framleiðsluferlið en óendanleg afkastageta skapar. Ef ekki er nægilega geta fyrir tilföngin verður afhendingardegi ýtt aftur og verkið verður skipulagt þegar það eru nægileg tilföng.

> [!NOTE]
> Takmörkuð afkastagetuáætlun og skipulagning vinnu næstum á sama hátt burtséð frá því hvort notuð er fínstilling áætlanagerðar eða úrelt aðaláætlunarvél. Hins vegar notar fínstilling skipulagningar ekki **Flöskuháls tíma** breytu fyrir takmrök. Þegar fínstilling áætlanagerðar er notuð eru flöskuhálsatilföng alltaf tímasett með því að nota tímamörk sem önnur tilföng en flöskuhálsa (eins og er gefið í skyn með tímamörkum takmarkaðrar afkastagetu).

## <a name="set-up-finite-capacity-functionality"></a>Setja upp virkni fyrir takmarkaða getu

Til að nota virkni takmarkaðrar afkastagetu þarf að virkja afkastagetuáætlun yfir allt og virkja þarf takmarkaða afkastagetuáætlun bæði fyrir aðaláætlunina þar sem á að nota hana og fyrir hvert tilfang þar sem það er notað. Fyrir áætlanir og tilföng þar sem takmörkuð afkastageta er virkjuð mun tímasetning á áætluðum framleiðslupöntunum taka til greina afköst sem þegar er búið að taka frá. Áætluðum framleiðslupöntunum er afturraðað frá þarfadagsetningu. Ef getan er ekki til staðar til að fullnægja ákjósanlegri áætlun mun kerfið reyna að krefjast íhlutar fyrr. Ef geta getur breyst eftir því sem kröfurnar breytast (til dæmis þegar unnið er með vaktir) ættir þú ekki að nota virkni fyrir takmarkaða getu því útreiknaður vinnslutími verður ekki réttur. Áætlanagerð tekur aðeins til afkastagetu sem þegar er frátekin fyrir tilföng þar sem endanleg afkastageta er virkjuð. Með því að virkja takmarkaða getu fyrir tilfang gerir þú það mögulegt að breyta takmarkaðri getu tímamarkanna.

### <a name="activate-master-planning-parameters"></a>Virkja færibreytur aðaláætlanagerðar

Til að nota endanlega getuvirkni verður að virkja afkastagetuáætlun á **Færibreytur áætlanagerðar** síðunni.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.
1. Í flipanum **Áætlaðar pantanir**, í hlutanum **Afkastagetuáætlun** skal stilla valkostinn **Framleiðsla** á *Já*.

### <a name="activate-a-master-plan"></a>Virkja aðaláætlun

Þú verður að leyfa endanlegt skipulag og áætlanagerð fyrir hvert aðalskipulag þar sem þú vilt nota það.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Í listaglugganum skal velja aðalskipulag sem á að setja upp til að nota skipulagningu endanlegrar afkastagetu.
1. Í flýtflipanum **Almennt**, í hlutanum **Áætlaðar framleiðslupantanir**, skal stilla valkostinn **Takmörkuð afkastageta** á *Já*.
1. Endurtaka skal þrep 2 til 3 fyrir hverja aðaláætlun sem á að setja upp til viðbótar.

### <a name="activate-resources"></a>Virkja tilföng

Þú verður að leyfa endanlegt skipulag og áætlanagerð fyrir hvert tilfang þar sem þú vilt nota það.

1. Opnið **Framleiðslustýring \> Uppsetning \> Tilföng \> Tilföng**.
1. Í listaglugganum skal velja tilfang sem á að setja upp til að nota skipulagningu endanlegrar afkastagetu.
1. Á flýtiflipanum **Virkni** í hlutanum **Geta**, stillir þú valkostinn **Endanleg geta** á *Já*.
1. Endurtaka skal þrep 2 til 3 fyrir hvert tilfang sem á að setja upp til viðbótar.

## <a name="examples"></a>Dæmi

Í þessum hluta eru eftirfarandi dæmi sem sýna hvernig unnið er með bæði óendanlega og takmarkaða getu við skipulagningu og áætlanagerð:

- Dæmi 1 – Endalaus afkastagetuáætlun
- Dæmi 2 – Skipulagning á takmarkaðri getu með tímamörkum í einn dag
- Dæmi 3 – Skipulagning á takmarkaðri getu með tímamörkum í tvo daga

### <a name="preconditions"></a>Skilyrði

Öll þrjú dæmin gera ráð fyrir þeim forsendum sem lýst er í þessum kafla.

Vara *1* hefur leið sem inniheldur eftirfarandi aðgerðir.

| Aðgerðarnr. | Nafn aðgerðar | Tilföng        | Keyrslutími | Vinnslumagn. | Næsta |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Samsett        | Rafsuðulína    | 1        | 2            | 20   |
| 20            | Samsetning     | Samsetningarlína | 1        | 4            |      |

Starfsmenn hjá fyrirtækinu vinna á einni vakt í átta klukkustundir (8:00–16:00).

Framleiðslupöntun er áætluð fyrir *24 stk.* af *Afurð1*. Afhendingardagsetning er *Í dag + 3 dagar*.

Vegna áætlanagerðar hleður kerfið tilföngin á eftirfarandi hátt:

- **Samtengingarlína:** Þetta tilfang er hlaðið frá *Í dag kl. 8:00* til *Í dag + 1 kl. 12:00*.
- **Samsetningarlína:** Þetta tilfang er hlaðið frá *Í dag + 1 kl. 12:00* til *Í dag + 2 kl. 10:00*.

Eftirfarandi mynd sýnir Gantt línuritið (veldu það til að fá stærri sýn).

[![Gantt-línurit sem sýnir forsendur.](media/finite-examples-conditions-small.png "Gantt-línurit sem sýnir forsendur")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Dæmi 1 – Endalaus afkastagetuáætlun

Þetta dæmi sýnir niðurstöður áætlanagerðar þegar takmörkuð afkastagetuáætlun er notuð í staðinn fyrir takmarkaða afkastagetuáætlun.

Aðalskipulagið hefur eftirfarandi viðeigandi stillingu, sem gerir skipulagningu takmarkaðrar getu óvirka:

- **Takmörkuð geta:** *Nei*

Valkosturinn **Takmörkuð geta** er einnig stilltur á *Nei* fyrir bæði viðeigandi tilföng til að óvirkja endanlega afkastagetuáætlun fyrir þau:

- Rafsuðulína
- Samsetningarlína

Nú er hægt að bæta við nýrri sölupöntun fyrir *8 stk* af *vöru1* og keyra þá áætlunina. Kerfið hleður því inn á rafsuðulínuna frá *Í dag kl. 8:00* til *Í dag kl. 12:00*. Eftir að framkvæmdum á rafsuðulínunni er lokið mun kerfið hlaða samsetningarlínuna frá *Í dag kl. 12:00* til *Í dag kl. 14:00*.

Eftirfarandi mynd sýnir Gantt línuritið (veldu það til að fá stærri sýn).

[![Gantt-rit sem sýnir dæmi um óendanlega afkastagetuáætlun.](media/finite-examples-example1-small.png "Gantt graf sem sýnir óendanlegt getuskipulagningardæmi")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Dæmi 2 – Skipulagning á takmarkaðri getu með tímamörkum í einn dag

Þetta dæmi sýnir áætlanagerð þegar þú notar takmarkaða getu og tímamörk í einn dag.

Aðaláætlunin er með eftirfarandi viðeigandi stillingar sem virkja takmarkaða afkastagetuáætlun og velja tímamörk fyrir áætlunina:

- **Takmörkuð geta:** *Já*
- **Takmörkuð tímamörk afkastagetu:** *1*

Valkosturinn **Takmörkuð geta** er einnig stilltur á *Já* fyrir bæði viðeigandi tilföng til að virkja endanlega afkastagetuáætlun fyrir þau:

- Rafsuðulína
- Samsetningarlína

Nú er hægt að bæta við nýrri sölupöntun fyrir *8 stk* af *vöru1* og keyra þá áætlunina. Þar af leiðandi hleður kerfið rafsuðulínuna frá *Í dag +1 kl. 8:00* til *Í dag +1 kl. 12:00*. Eftir að aðgerðum á rafsuðulínunni er lokið mun kerfið hlaða samsetningarlínuna frá *Í dag +1 kl. 12:00* til *Í dag +1 kl. 14:00*. Kerfið telur takmarkaða getu fyrir aðeins einn dag.

Eftirfarandi mynd sýnir Gantt línuritið (veldu það til að fá stærri sýn).

[![Gantt línurit sem sýnir endanlegt skipulag með tímamörk upp á einn dag.](media/finite-examples-example2-small.png "Gantt línurit sem sýnir endanlegt skipulag með tímamörkum í einn dag")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Dæmi 3 – Skipulagning á takmarkaðri getu með tímamörkum í tvo daga

Þetta dæmi sýnir áætlanagerð þegar þú notar takmarkaða getu og tímamörkum í tvo daga.

Aðaláætlunin er með eftirfarandi viðeigandi stillingar sem virkja takmarkaða afkastagetuáætlun og velja tímamörk fyrir áætlunina:

- **Takmörkuð geta:** *Já*
- **Takmörkuð tímamörk afkastagetu:** *2*

Valkosturinn **Takmörkuð geta** er einnig stilltur á *Já* fyrir bæði viðeigandi tilföng til að virkja endanlega afkastagetuáætlun fyrir þau:

- Rafsuðulína
- Samsetningarlína

Nú er hægt að bæta við nýrri sölupöntun fyrir *8 stk* af *vöru1* og keyra þá áætlunina. Þar af leiðandi hleður kerfið rafsuðulínuna frá *Í dag +1 kl. 12:00* til *Í dag +1 kl. 16:00*. Eftir að aðgerðum á rafsuðulínunni er lokið mun kerfið hlaða samsetningarlínuna frá *Í dag + 2 kl. 8:00* til *Í dag + 2 kl. 10:00*. Kerfið telur aðeins takmarkaða getu fyrir tvo daga.

Eftirfarandi mynd sýnir Gantt línuritið (veldu það til að fá stærri sýn).

[![Gantt línurit sem sýnir endanlegt skipulag með tímamörkum í tvo daga.](media/finite-examples-example3-small.png "Gantt línurit sem sýnir endanlegt skipulag með tímamörkum í tvo daga")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Þú ættir alltaf að setja upp takmörkuð tímamörk eins og þörf er á. Dæmin sem koma fram í þessari grein sýna einungis virknina. Í raun er eins dags tímagirðing líklega of lítil fyrir flesta framleiðendur sem nota takmarkaða afkastagetuáætlun.
