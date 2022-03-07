---
title: Gefa út rafræna reikninga í Finance and Supply Chain Management
description: Í þessu efnisatriði er útskýrt hvernig á að gefa út rafræna reikninga í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management í gegnum viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 099ebb56710e920f7b1453f32f23f59a80486ebf
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5486954"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Gefa út rafræna reikninga í Finance and Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að gefa út rafræna reikninga í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management í gegnum viðbót rafrænnar reikningsfærslu.


## <a name="feature-activation"></a>Aðgerð virkjun

Til gefa út rafræna reikninga í gegnum viðbót rafrænnar reikningsfærslu þarf að virkja eiginleikann í Finance and Supply Chain Management.

Hver eiginleiki samsvarar tilteknum eiginleika rafrænnar reikningsfærslu sem fylgir kröfum rafrænnar reikningsfærslu fyrir land/svæði.

Eftirfarandi tafla sýnir lista yfir eiginleika sem viðbót rafrænnar reikningsfærslu kann að styðja.

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

Þegar til staðar er eldri eiginleiki rafrænnar reikningsfærslu sem er studdur í staðbundnu umfangi lands/svæðis mun virkjun eins þessara eiginleika slökkva á eldri eiginleikanum og virkja rafræna reikninga til að vera gefna út í gegnum viðbót rafrænnar reikningsfærslu.

> [!IMPORTANT]
> Þegar samþættingareiginleiki viðbótar rafrænnar reikningsfærslu er virkjaður er sjálfgefið slökkt á upplifun nýrrar rafrænnar reikningsfærslu. Hægt er að nota hugmynd eiginleikans til að velja hvaða upplifanir eigi að virkja fyrir lögaðila með því að nota lands-/svæðisbundna virkni. Valkosturinn **Altækt** stýrir nýju upplifuninni fyrir hin löndin/svæðin sem eru ekki sérstaklega tilgreind í töflunni.

## <a name="submit-electronic-documents"></a>Senda inn rafræn skjöl

Ferlið við að senda inn rafræn skjöl stendur fyrir einn samskiptapunkt milli Finance and Supply Chain Management og viðbótar rafrænnar reikningsfærslu. Á meðan á hverju tilviki innsendingar stendur ganga samskiptin í báðar áttir:

- **Frá Finance and Supply Chain Management til viðbótar rafrænnar reikningsfærslu** – Finance and Supply Chain Management senda útdrætti reikninganna til viðbótar rafrænnar reikningsfærslu. Eftir þörfum sendir það líka innihald færibreyta sem voru skilgreindar sem hluti af eiginleikum rafrænnar reikningsfærslu.
- **Frá viðbót rafrænnar reikningsfærslu til Finance and Supply Chain Management** – Háð eiginleika rafrænnar reikningsfærslu mun Finance and Supply Chain Management fá uppfærslur frá viðbót rafrænnar reikningsfærslu um niðurstöður fyrir úrvinnslu reikninga sem voru sendir inn áður. Hún fær líka innihald færibreyta sem voru skilgreindar sem hluti af eiginleikum rafrænnar reikningsfærslu.

Til að senda rafræn skjöl til viðbótar rafrænnar reikningsfærslu, í Finance and Supply Chain Management, skal fara í **Fyrirtækisstjórnun &gt; Reglubundið &gt; Rafræn skjöl &gt; Senda inn rafræn skjöl**.

Upphafsstaðurinn er bókaður reikningur. Þessi reikningur getur komið frá mismunandi uppruna, t.d. sölupöntunum, verkreikningum eða reikningum með frjálsum texta.

Hægt er að keyra sendingarferlið handvirkt eða í bakgrunni.

- **Handvirk framk** – Fyrir handvirka framkvæmd þarf að nota valkostinn **Sía** til að skilgreina umfang skjala sem á að senda inn. Á síðunni **Síur** er hægt að skilgreina eigin fyrirspurn til að velja bókaða reikninga sem á að senda inn. Þegar búið er að velja þarf að hefja framkvæmd úrvinnslunnar handvirkt og bíða eftir að henni ljúki. Þegar vinnslunni er lokið sýna skilaboð í aðgerðamiðstöðinni fjölda rafrænna skjala sem hafa verið send inn.
- **Bakgrunnsvinnsla** – Bakgrunnsvinnsla keyrir án þess að þurfa að vera skráður inn eða halda svarglugga innsendingar opnum. Hægt er að tímasetja keyrslu ferlisins og skilgreina tíðni framkvæmdar.

## <a name="view-the-submission-logs"></a>Skoða innsendingarkladda

Í Finance and Supply Chain Management er hægt að nota innsendingarkladda til að skoða niðurstöður fyrir úrvinnslu innsendingar til viðbótar rafrænnar reikningsfærslu. Farið í **Fyrirtækisstjórnun &gt; Reglubundið &gt; Rafræn skjöl &gt; Innsending rafræns skjals** og síðan, í reitnum **Gerð skjals**, skal velja gildi til að sía gerð reikninga sem kladdinn á að sýna.

Þrjár mögulegar stöður innsendingar eru í boði:

- **Áætlað** – Viðbót rafrænnar reikningsfærslu fékk innsendinguna frá Finance and Supply Chain Management og úrvinnsla á eiginleika rafrænnar reikningsfærslu er í vinnslu.
- **Lokið** – Viðbót rafrænnar reikningsfærslu tókst að vinna úr eiginleika rafrænnar reikningsfærslu þar sem hún skilgreind til að keyra hann.
- **Mistókst** – Villa kom upp í viðbót rafrænnar reikningsfærslu og var stöðvuð af undantekningu við úrvinnslu á eiginleika rafrænnar reikningsfærslu.

> [!IMPORTANT]
> Staða innsendingar vísar í stöðu úrvinnslunnar sem viðbót rafrænnar reikningsfærslu gerir á eiginleika rafrænnar reikningsfærslu. Hún vísar ekki í lokastöðuna á sjálfum rafræna reikningnum.
>
> Ef til dæmis þarf að senda rafrænan reikning til ytri vefþjónustu til samþykktar, þá gæti staða innsendingar verið **Lokið**, en staða rafræna reikningsins gæti verið **Hafnað**. Í þessu tilviki gat viðbót rafrænnar reikningsfærslu unnið úr eiginleika rafrænnar reikningsfærslu vegna þess að hún var skilgreind til að vinna úr þeim eiginleika. Hins vegar var rafræna reikningnum hafnað vegna þess að hann uppfyllti ekki skilyrðið sem vefþjónustan setti fyrir samþykkt reiknings.

Innsendingarkladdarnir innihalda að auki eftirfarandi aðgerðir:

- **Upplýsingar um sendingu** – Skoða upplýsingar um aðalsendinguna. Myndræna framsetningin sýnir allar aðgerðir keyrslukladdans sem eru skilgreindar í eiginleika rafrænnar reikningsfærslu. Hann gerir notendum einnig kleift að sækja skrár sem eru búnar til meðan á úrvinnslu stendur. Í aðstæðum þar sem ytri vefþjónusta þarf að samþykkja reikninginn gerir hann notendum líka kleift að skoða stöðu reikningsins.
- **Tengdar sendingar** – Skoða upplýsingar fyrir sendingar undireininga.
- **Hætta við sendingar** – Þessi aðgerð virkjar sérstakt sendingarferli í aðstæðum þar sem ytri vefþjónusta þarf að samþykkja rafrænan reikning. Hún segir viðbót rafrænnar reikningsfærslu að senda vefþjónustunni ákveðin skilaboð sem ætluð eru til að hætta við stöðu samþykkts rafræns reiknings í gagnagrunni vefþjónustunnar.
- **Endursenda skjal** – Endursenda rafrænt skjal sem hefur þegar verið sent til viðbótar rafrænnar reikningsfærslu. Nýr kladdi er búinn til á síðunni **Upplýsingar um sendingu**.
- **Senda tengdar sendingar**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
