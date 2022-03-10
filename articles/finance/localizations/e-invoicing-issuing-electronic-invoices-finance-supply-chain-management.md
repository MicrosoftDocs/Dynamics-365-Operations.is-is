---
title: Gefa út rafræna reikninga í Finance and Supply Chain Management
description: Í þessu efnisatriði er útskýrt hvernig á að gefa út rafræna reikninga í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management í gegnum rafræna reikningsfærslu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 24909c2a2505724c159e939535c1d57cb66e48629862bebb32b3d72c0eb06c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752127"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Gefa út rafræna reikninga í Finance and Supply Chain Management

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að gefa út rafræna reikninga í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management í gegnum rafræna reikningsfærslu.


## <a name="feature-activation"></a>Aðgerð virkjun

Til gefa út rafræna reikninga í gegnum rafræna reikningsfærslu þarf að virkja eiginleikann í Finance and Supply Chain Management.

Hver eiginleiki samsvarar tilteknum eiginleika rafrænnar reikningsfærslu sem fylgir kröfum rafrænnar reikningsfærslu fyrir land/svæði.

Eftirfarandi tafla sýnir lista yfir eiginleika sem rafræn reikningsfærsla kann að styðja.

| Nafn                                              | Land/svæði |
|---------------------------------------------------|----------------|
|Austurrískur rafrænn reikningur                        |Austurríki         |
|Belgískur rafrænn reikningur                         |Belgía         |
|NF-e Ríki - rafrænn reikningur fyrir Brasilíu       |Brasilía          |
|NFS-e - Brasilísk Þjónusta (borg) rafrænn reikningur|Brasilía          |
|Danskur rafrænn reikningur                          |Danmörk         |
|Egypskur rafrænn reikningur                        |Egyptaland           |
|Eistneskur rafrænn reikningur                        |Eistland         |
|Finnskur rafrænn reikningur                         |Finnland         |
|Franskur rafrænn reikningur                          |Frakkland          |
|Þýskur rafrænn reikningur                          |Þýskaland         |
|PEPPOL - altækur rafrænn reikningur                 |Altæk          |
|Ítalskur rafrænn reikningur                         |Ítalía           |
|CFDI - Mexíkóskur rafrænn reikningur                  |Mexíkó          |
|Hollenskur rafrænn reikningur                           |Holland     |
|Norskur rafrænn reikningur                       |Noregur          |
|Spænskur rafrænn reikningur                         |Spánn           |

Þegar til staðar er eldri eiginleiki rafrænnar reikningsfærslu sem er studdur í staðbundnu umfangi lands/svæðis mun virkjun eins þessara eiginleika slökkva á eldri eiginleikanum og virkja rafræna reikninga til að vera gefna út í gegnum rafræna reikningsfærslu.

> [!IMPORTANT]
> Þegar samþættingareiginleiki rafrænnar reikningsfærslu er virkjaður er sjálfgefið slökkt á upplifun nýrrar rafrænnar reikningsfærslu. Hægt er að nota hugmynd eiginleikans til að velja hvaða upplifanir eigi að virkja fyrir lögaðila með því að nota lands-/svæðisbundna virkni. Valkosturinn **Altækt** stýrir nýju upplifuninni fyrir hin löndin/svæðin sem eru ekki sérstaklega tilgreind í töflunni.

## <a name="submit-electronic-documents"></a>Senda inn rafræn skjöl

Ferlið við að senda inn rafræn skjöl stendur fyrir einn samskiptapunkt milli Finance and Supply Chain Management og rafræna reikningsfærslu. Á meðan á hverju tilviki innsendingar stendur ganga samskiptin í báðar áttir:

- **Frá Finance and Supply Chain Management til rafrænnar reikningsfærslu** – Finance and Supply Chain Management senda útdrætti reikninganna til rafrænnar reikningsfærslu. Eftir þörfum sendir það líka innihald færibreyta sem voru skilgreindar sem hluti af eiginleikum rafrænnar reikningsfærslu.
- **Frá rafrænnar reikningsfærslu til Finance and Supply Chain Management** – Háð eiginleika rafrænnar reikningsfærslu mun Finance and Supply Chain Management fá uppfærslur frá rafrænni reikningsfærslu um niðurstöður fyrir úrvinnslu reikninga sem voru sendir inn áður. Hún fær líka innihald færibreyta sem voru skilgreindar sem hluti af eiginleikum rafrænnar reikningsfærslu.

Til að senda rafræn skjöl til rafrænnar reikningsfærslu, í Finance and Supply Chain Management, skal fara í **Fyrirtækisstjórnun &gt; Reglubundið &gt; Rafræn skjöl &gt; Senda inn rafræn skjöl**.

Upphafsstaðurinn er bókaður reikningur. Þessi reikningur getur komið frá mismunandi uppruna, t.d. sölupöntunum, verkreikningum eða reikningum með frjálsum texta.

Hægt er að keyra sendingarferlið handvirkt eða í bakgrunni.

- **Handvirk framk** – Fyrir handvirka framkvæmd þarf að nota valkostinn **Sía** til að skilgreina umfang skjala sem á að senda inn. Á síðunni **Síur** er hægt að skilgreina eigin fyrirspurn til að velja bókaða reikninga sem á að senda inn. Þegar búið er að velja þarf að hefja framkvæmd úrvinnslunnar handvirkt og bíða eftir að henni ljúki. Þegar vinnslunni er lokið sýna skilaboð í aðgerðamiðstöðinni fjölda rafrænna skjala sem hafa verið send inn.
- **Bakgrunnsvinnsla** – Bakgrunnsvinnsla keyrir án þess að þurfa að vera skráður inn eða halda svarglugga innsendingar opnum. Hægt er að tímasetja keyrslu ferlisins og skilgreina tíðni framkvæmdar.

## <a name="view-the-submission-logs"></a>Skoða innsendingarkladda

Í Finance and Supply Chain Management er hægt að nota innsendingarkladda til að skoða niðurstöður fyrir úrvinnslu innsendingar til rafrænnar reikningsfærslu. Farið í **Fyrirtækisstjórnun &gt; Reglubundið &gt; Rafræn skjöl &gt; Innsending rafræns skjals** og síðan, í reitnum **Gerð skjals**, skal velja gildi til að sía gerð reikninga sem kladdinn á að sýna.

Þrjár mögulegar stöður innsendingar eru í boði:

- **Áætlað** – Rafræn reikningsfærsla fékk innsendinguna frá Finance and Supply Chain Management og úrvinnsla á eiginleika rafrænnar reikningsfærslu er í vinnslu.
- **Lokið** – Rafrænni reikningsfærslu tókst að vinna úr eiginleika rafrænnar reikningsfærslu þar sem hún skilgreind til að keyra hann.
- **Mistókst** – Villa kom upp í rafrænni reikningsfærslu og var stöðvuð af undantekningu við úrvinnslu á eiginleika rafrænnar reikningsfærslu.

> [!IMPORTANT]
> Staða innsendingar vísar í stöðu úrvinnslunnar sem reikningsfærsla gerir á eiginleika rafrænnar reikningsfærslu. Hún vísar ekki í lokastöðuna á sjálfum rafræna reikningnum.
>
> Ef til dæmis þarf að senda rafrænan reikning til ytri vefþjónustu til samþykktar, þá gæti staða innsendingar verið **Lokið**, en staða rafræna reikningsins gæti verið **Hafnað**. Í þessu tilviki gat reikningsfærsla unnið úr eiginleika rafrænnar reikningsfærslu vegna þess að hún var skilgreind til að vinna úr þeim eiginleika. Hins vegar var rafræna reikningnum hafnað vegna þess að hann uppfyllti ekki skilyrðið sem vefþjónustan setti fyrir samþykkt reiknings.

Innsendingarkladdarnir innihalda að auki eftirfarandi aðgerðir:

- **Upplýsingar um sendingu** – Skoða upplýsingar um aðalsendinguna. Myndræna framsetningin sýnir allar aðgerðir keyrslukladdans sem eru skilgreindar í eiginleika rafrænnar reikningsfærslu. Hann gerir notendum einnig kleift að sækja skrár sem eru búnar til meðan á úrvinnslu stendur. Í aðstæðum þar sem ytri vefþjónusta þarf að samþykkja reikninginn gerir hann notendum líka kleift að skoða stöðu reikningsins.
- **Tengdar sendingar** – Skoða upplýsingar fyrir sendingar undireininga.
- **Hætta við sendingar** – Þessi aðgerð virkjar sérstakt sendingarferli í aðstæðum þar sem ytri vefþjónusta þarf að samþykkja rafrænan reikning. Hún segir rafrænni reikningsfærslu að senda vefþjónustunni ákveðin skilaboð sem ætluð eru til að hætta við stöðu samþykkts rafræns reiknings í gagnagrunni vefþjónustunnar.
- **Endursenda skjal** – Endursenda rafrænt skjal sem hefur þegar verið sent til rafrænnar reikningsfærslu. Nýr kladdi er búinn til á síðunni **Upplýsingar um sendingu**.
- **Senda tengdar sendingar**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
