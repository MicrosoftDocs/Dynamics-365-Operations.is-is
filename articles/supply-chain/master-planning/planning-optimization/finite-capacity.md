---
title: Skipulag og áætlun með takmarkaða getu
description: Endanleg afkastagetuáætlun og tímasetning hjálpar þér að skilja hversu mikla vinnu er hægt að framleiða á tilteknu tímabili þegar takmarkanir á mismunandi tilföngum eru teknar með í reikninginn.
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
ms.openlocfilehash: 3d116b5f7f456630415378e6cc069907e339068b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689694"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Skipulag og áætlun með takmarkaða getu

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Endanleg getu er nálgun sem hjálpar þér að skilja hversu mikla vinnu er hægt að framleiða á tilteknu tímabili þegar takmarkanir á mismunandi auðlindum eru teknar með í reikninginn. Tilgangur tímasetningar með takmörkuðum afkastagetu er að tryggja að vinna gangi á jöfnum og skilvirkum hraða í öllu verksmiðjunni.

Endanleg afkastagetu áætlanagerð og tímasetning skapar raunhæfari áætlun fyrir framleiðsluferlana en óendanlega hleðsluaðferðin skapar. Ef það er ekki nóg afkastagetu á tilföngunum verður afhendingardegi ýtt út og verkið verður tímasett þegar það er nóg afkastagetu.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Stuðningur við hagræðingu áætlanagerðar fyrir endanlega getuáætlun

Endanleg afkastagetu áætlanagerð og tímasetning virkar á næstum sama hátt, óháð því hvort þú notar áætlanagerð fínstillingu eða innbyggðu skipulagsvélina. Hins vegar notar Planning Optimization ekki **Flöskuháls tími** girðingarbreytu. Þegar þú notar áætlanagerð fínstillingu eru flöskuhálstilföng alltaf tímasett með því að nota sömu tímagirðingu og tilföng sem ekki eru flöskuháls (eins og gefið er til kynna með tímamörkum með takmarkaðan getu).

## <a name="set-up-finite-capacity-functionality"></a>Settu upp takmarkaða getuvirkni

Til að nota takmarkaða afkastagetu virkni verður þú að virkja afkastagetuáætlanagerð á heimsvísu og þú verður að virkja takmarkaða afkastagetuáætlun bæði fyrir aðaláætlunina þar sem þú vilt nota hana og fyrir hverja tilföng þar sem hún á við. Fyrir áætlanir og tilföng þar sem takmörkuð afkastageta er virkjuð mun tímasetning fyrirhugaðra framleiðslupantana taka til greina getu sem þegar hefur verið frátekin. Áætlaðar framleiðslupantanir eru áætlaðar afturábak frá kröfudagsetningu. Ef afkastageta er ekki tiltæk til að uppfylla ákjósanlega áætlun mun kerfið reyna að krefjast íhluta á fyrri dagsetningu. Ef afkastageta þín getur breyst eftir því sem kröfur breytast (til dæmis þegar þú ert að vinna á vöktum) ættir þú ekki að nota endanlegt afkastagetuvirkni, vegna þess að reiknaðir vinnslutímar verða ekki réttir. Tímasetning tekur aðeins til getu sem þegar er frátekin fyrir tilföng þar sem takmörkuð getu er virkjuð. Með því að virkja takmarkaða afkastagetu fyrir tilföng gerirðu það mögulegt að breyta tímamörkum fyrir endanlegt afkastagetu.

### <a name="activate-master-planning-parameters"></a>Virkjaðu aðalskipulagsfæribreytur

Til að nota takmarkaða getuvirkni verður þú að virkja getuáætlun á **Aðalskipulagsbreytur** síðu.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.
1. Á **Skipulagðar pantanir** flipa, í **Skipulagsgeta** kafla, stilltu **Framleiðsla** valmöguleika til *Já*.

### <a name="activate-a-master-plan"></a>Virkjaðu aðalskipulag

Þú verður að virkja takmarkaða getuáætlun og tímasetningu fyrir hverja aðaláætlun þar sem þú vilt nota hana.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Í listarúðunni, veldu aðaláætlun sem þú vilt setja upp til að nota endanlega getuáætlun og tímasetningu.
1. Á **Almennt** Flýtiflipi, í **Fyrirhugaðar framleiðslupantanir** kafla, stilltu **Endanleg getu** valmöguleika til *Já*.
1. Endurtaktu skref 2 og 3 fyrir hvert viðbótar aðalskipulag sem þú vilt setja upp.

### <a name="activate-resources"></a>Virkjaðu auðlindir

Þú verður að virkja endanlega getuáætlun og tímasetningu fyrir hverja tilföng þar sem þú vilt nota hana.

1. Opnið **Framleiðslustýring \> Uppsetning \> Tilföng \> Tilföng**.
1. Í listarúðunni, veldu tilföng sem þú vilt setja upp til að nota endanlega getuáætlun og tímasetningu.
1. Á **Aðgerð** Flýtiflipi, í **Afkastagetuhnappur** kafla, stilltu **Endanleg getu** valmöguleika til *Já*.
1. Endurtaktu skref 2 og 3 fyrir hvert viðbótartilfang sem þú vilt setja upp.

## <a name="examples"></a>Dæmi

Þessi hluti veitir eftirfarandi dæmi sem sýna hvernig á að vinna með bæði óendanlega og takmarkaða getuáætlun og tímasetningu:

- Dæmi 1 – Óendanleg getuáætlun
- Dæmi 2 – Endanleg afkastagetuáætlun með tímagirðingu upp á einn dag
- Dæmi 3 – Endanleg afkastagetuáætlun með tveggja daga tímagirðingu

### <a name="preconditions"></a>Skilyrði

Öll þrjú dæmin gera ráð fyrir þeim forsendum sem lýst er í þessum kafla.

Vara *Vara 1* er með leið sem inniheldur eftirfarandi aðgerðir.

| Aðgerð nr. | Nafn aðgerðar | Tilföng        | Keyrslutími | Vinnslumagn. | Næsta |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Suðu        | Suðulína    | 1        | 2            | 20   |
| 20            | Samsetning     | Samsetningarlína | 1        | 4            |      |

Starfsmenn hjá fyrirtækinu þínu vinna á einni vakt í átta klukkustundir (8:00–16:00).

Það er áætluð framleiðslupöntun fyrir *24 stk* af *Vara 1*. Það hefur afhendingardag á *Í dag + 3 dagar*.

Sem afleiðing af áætlanagerð hleður kerfið tilföngunum á eftirfarandi hátt:

- **Suðulína:** Þetta tilfang er hlaðið frá *Í dag klukkan 8:00* þar til *Í dag + 1 kl 12:00*.
- **Samsetningarlína:** Þetta tilfang er hlaðið frá *Í dag + 1 kl 12:00* þar til *Í dag + 2 kl 10:00*.

Eftirfarandi mynd sýnir Gantt-töfluna sem myndast (veldu það til að fá stærri mynd).

[![Gantt mynd sem sýnir forsendur.](media/finite-examples-conditions-small.png "Gantt mynd sem sýnir forsendur")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Dæmi 1 – Óendanleg getuáætlun

Þetta dæmi sýnir áætlunarniðurstöðurnar þegar þú notar óendanlega afkastagetuáætlun í stað endanlegrar getuáætlunar.

Aðalskipulagið hefur eftirfarandi viðeigandi stillingu, sem slekkur á endanlega getuáætlun fyrir áætlunina:

- **Endanleg getu:** *Nei*

The **Endanleg getu** valkostur er einnig stilltur á *Nei* fyrir bæði viðeigandi úrræði til að slökkva á endanlegri getuáætlun fyrir þau:

- Suðulína
- Samsetningarlína

Þú bætir nú við nýrri sölupöntun fyrir *8 stk* af *Vara 1* og keyra áætlunina. Fyrir vikið hleður kerfið suðulínuna frá *Í dag klukkan 8:00* þar til *12:00 í dag*. Eftir að aðgerðum á suðulínunni er lokið mun kerfið hlaða samsetningarlínunni frá *12:00 í dag* þar til *14:00 í dag*.

Eftirfarandi mynd sýnir Gantt-töfluna sem myndast (veldu það til að fá stærri mynd).

[![Gantt töflu sem sýnir óendanlega getuáætlunardæmi.](media/finite-examples-example1-small.png "Gantt töflu sem sýnir óendanlega getuáætlunardæmi")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Dæmi 2 – Endanleg afkastagetuáætlun með tímagirðingu upp á einn dag

Þetta dæmi sýnir áætlunarniðurstöður þegar þú notar endanlega afkastagetuáætlun og tímagirðingu upp á einn dag.

Aðalskipulagið hefur eftirfarandi viðeigandi stillingar sem gera kleift að skipuleggja endanlega afkastagetu og setja tímagirðingu fyrir áætlunina:

- **Endanleg getu:** *Já*
- **Takmörkuð tímagirðing:** *1*

The **Endanleg getu** valkostur er einnig stilltur á *Já* fyrir bæði viðeigandi auðlindir til að gera endanlega getuáætlun fyrir þau:

- Suðulína
- Samsetningarlína

Þú bætir nú við nýrri sölupöntun fyrir *8 stk* af *Vara 1* og keyra áætlunina. Fyrir vikið hleður kerfið suðulínuna frá *Í dag + 1 kl 8:00* þar til *Í dag + 1 kl 12:00*. Eftir að aðgerðum á suðulínunni er lokið mun kerfið hlaða samsetningarlínunni frá *Í dag + 1 kl 12:00* þar til *Í dag + 1 kl 14:00*. Kerfið telur takmarkaða getu í aðeins einn dag.

Eftirfarandi mynd sýnir Gantt-töfluna sem myndast (veldu það til að fá stærri mynd).

[![Gantt mynd sem sýnir takmarkaða getuáætlun með tímagirðingu upp á einn dag.](media/finite-examples-example2-small.png "Gantt mynd sem sýnir takmarkaða getuáætlun með tímagirðingu upp á einn dag")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Dæmi 3 – Endanleg afkastagetuáætlun með tveggja daga tímagirðingu

Þetta dæmi sýnir áætlunarniðurstöður þegar þú notar takmarkaða afkastagetuáætlun og tveggja daga tímagirðingu.

Aðalskipulagið hefur eftirfarandi viðeigandi stillingar sem gera kleift að skipuleggja endanlega afkastagetu og setja tímagirðingu fyrir áætlunina:

- **Endanleg getu:** *Já*
- **Takmörkuð tímagirðing:** *2*

The **Endanleg getu** valkostur er einnig stilltur á *Já* fyrir bæði viðeigandi auðlindir til að gera endanlega getuáætlun fyrir þau:

- Suðulína
- Samsetningarlína

Þú bætir nú við nýrri sölupöntun fyrir *8 stk* af *Vara 1* og keyra áætlunina. Fyrir vikið hleður kerfið suðulínuna frá *Í dag + 1 kl 12:00* þar til *Í dag + 1 kl 16:00*. Eftir að aðgerðum á suðulínunni er lokið mun kerfið hlaða samsetningarlínunni frá *Í dag + 2 kl 8:00* þar til *Í dag + 2 kl 10:00*. Kerfið telur takmarkaða getu í aðeins tvo daga.

Eftirfarandi mynd sýnir Gantt-töfluna sem myndast (veldu það til að fá stærri mynd).

[![Gantt-rit sem sýnir takmarkaða afkastagetuáætlun með tveggja daga tímagirðingu.](media/finite-examples-example3-small.png "Gantt-rit sem sýnir takmarkaða afkastagetuáætlun með tveggja daga tímagirðingu")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Þú ættir alltaf að stilla tímagirðinguna með endanlegri getu eins og krafist er til að passa við þarfir fyrirtækisins. Dæmin sem gefin eru upp í þessari grein sýna aðeins virknina. Í raun og veru er eins dags tímagirðing líklega of lág fyrir flesta framleiðendur sem nota takmarkaða afkastagetuáætlun.
