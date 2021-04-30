---
title: Þjappa stórum skjölum sem eru mynduð í rafrænni skýrslugerð
description: Þetta efnisatriði útskýrir hvernig á að þjappa stórum skjölum sem mynduð eru með sniði rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 899af54fbe34841c9b9b6e96b78db96773cf0203
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894173"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Þjappa stórum skjölum sem eru mynduð í rafrænni skýrslugerð 

[!include [banner](../includes/banner.md)]

Hægt er að nota [Ramma rafrænnar skýrslugerðar](general-electronic-reporting.md) til að skilgreina lausn sem sækir færslugögn til að mynda skjal á útleið. Þetta myndaða skjal gæti verið nokkuð stórt. Þegar þessi gerð skjals er mynduð er minnið [Þjónn hugbúnaðarhluta (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) notað til að halda því. Á einhverjum tímapunkti þarf að sækja skjalið úr Microsoft Dynamics 365 Finance-forritinu. Sem stendur takmarkast hámarksstærð eins skjals sem myndað er í rafrænni skýrslugerð við 2 GB. Þar að auki [takmarkar](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) Finance stærð sóttrar skráar við 1 GB sem stendur. Þess vegna þarf að skilgreina lausn rafrænnar skýrslugerðar sem dregur úr líkunum á að farið verði yfir þessar takmarkanir og að undantekningin **Streymi var of langt** eða **Yfirflæði eða undirflæði í reikniaðgerðinni** komi upp.

Þegar lausn er skilgreind er hægt að stilla snið rafrænnar skýrslugerðar í aðgerðarhönnuði með því að bæta við rótareiningu af gerðinni **Mappa** til að þjappa saman efninu sem er myndað af einhverri faldaðri einingu. Þjöppunin virkar „í tæka tíð“ þannig að hægt sé að minnka hámarks minnisnotkun og stærð skráarinnar sem verður hlaðið niður.

> [!NOTE]
> Skráarþjöppun tekur viðbótarprósentu af notkun örgjörvans.

Fyrir frekari upplýsingar um þessa aðferð skal ljúka dæminu í þessu efnisatriði.

## <a name="example-compress-an-outbound-document"></a>Dæmi: Þjappa skjali á útleið

Þetta dæmi sýnir hvernig notandi sem er úthlutað **Kerfisstjóri** eða **Hagnýtur ráðgjafi rafrænnar skýrslugerðar** hlutverki getur skilgreint snið rafrænnar skýrslugerðar til að þjappa saman myndað skjal.

### <a name="prerequisites"></a>Forkröfur

Áður en ferlið í þessu efnisatriði er klárað þarf að ljúka eftirfarandi skrefum.

1. [Virkja skilgreiningarveitu](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Flytja inn dæmið um skilgreiningar rafrænnar skýrslugerðar](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Yfirfara innflutt snið.](er-defer-xml-element.md#review-the-imported-format)

> [!NOTE]
> Sem stendur byrjar sniðsskipulagið á einingunni **Skýrsla** af gerðinni **Skrá** og inniheldur XML-einingar. Þess vegna verður skjal á útleið myndað á XML-sniði og engin þjöppun verður notuð.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Mynda snið rafrænnar skýrslugerðar til að sækja ósamþjappað skjal

1. [Keyra innflutt snið](er-defer-xml-element.md#run-the-imported-format).
2. Takið eftir að stærð myndaða skjalsins á XML-sniði er 3 KB.

    ![Forskoðun á ósamþjöppuðu skjali á útleið](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Breyta sniðinu til að þjappa mynduðu úttaki

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Stillingar** í stillingatrénu stækkarðu **Líkan til að læra frestuðum þætti**.
3. Veljið skilgreininguna **Snið til að læra frestaðar XML-einingar**.
4. Veljið **Hönnuður** til að breyta sniðsskipulaginu.
5. Á síðunni **Sniðshönnuður**, í flipanum **Snið**, skal velja **Bæta við rót** til að bæta við einingu rótarsniðs.
6. Í svarglugganum **Bæta við** skal velja **Almenn\\Mappa**.
7. Veljið **Í lagi** til að staðfesta viðbót nýrrar rótareiningar.
8. Veljið **Vista**.

> [!NOTE]
> Sniðsskipanin byrjar á einingunni af gerðinni **Mappa**. Þessi eining myndar úttak sem þjappaða (zip) skrá. Þegar skjal sem er myndað af einingunni **Skýrsla** er sett í zip-skrá á útleið, verður efni þess þjappað til að draga úr stærð skráarinnar á útleið.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Mynda snið rafrænnar skýrslugerðar til að fá þjappað skjal

1. Á síðunni **Sniðshönnuður** skal velja **Keyra**.
2. Sækið zip-skrána sem vafrinn býður upp á og opnið hana til að yfirfara.
3. Takið eftir að stærð myndaða skjalsins á ZIP-sniðinu er 1 KB.

    > [!NOTE] 
    > Þjöppunarhlutfall XML-skrárinnar sem þessi zip-skrá inniheldur er 87 prósent. Þjöppunarhlutfallið veltur á gögnunum sem verið er að þjappa.

    ![Forskoðun á þjöppuðu skjali á útleið](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Ef [endastaður](electronic-reporting-destinations.md) rafrænnar skýrslugerðar fyrir sniðseininguna sem myndar úttak (einingin **Skýrsla** í þessu dæmi), verður þjöppun úttaksins sleppt.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Áfangastaðir fyrir rafræna skýrslugerð](electronic-reporting-destinations.md)

[Fresta keyrslu XML-eininga á sniði rafrænnar skýrslugerðar](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]