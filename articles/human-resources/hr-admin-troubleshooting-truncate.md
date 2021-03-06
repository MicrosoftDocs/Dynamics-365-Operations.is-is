---
title: Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio
description: Þessi grein útskýrir hvernig á að leysa mál þar sem nöfn einstaklinga og stöður eru styttar þegar viðskiptamenn skoða stöðustigveldið í Microsoft Dynamics 365 Human Resources. Stýfing á texta getur gert það erfitt að taka skjámynd eða prenta stigveldið.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a03c8f340e8ebb2fb0440518c154ed3bdd0197f6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053252"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

Þegar viðskiptavinur skoðar stöðustigveldið í Microsoft Dynamics 365 Human Resources, eru nöfn á einstaklingum og stöðum stytt. Því getur reynst erfitt að taka skjámynd eða að prenta og dreifa stigveldinu.

![Stöðustigveldi](media/position-h.png)

**Orsök**

Þessi hegðun er samkvæmt hönnuninni.

**Upplausn**

Því miður geta notendur ekki breytt stærð textans á auðveldan hátt. Hins vegar er hægt að flytja stöðustigveldið út úr Human Resources og flytja það síðan inn í Microsoft Visio. Þrátt fyrir að eftirfarandi grein hafi verið skrifuð fyrir Microsoft Dynamics AX 2012, gildir ferlið samt sem áður fyrir Human Resources: [Flytja út stöðustigveldi í Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Fylgið þessum skrefum til að flytja út í Visio.

1. Opnaðu í Human Resources **Stöður** listasíðu.

    Til að bæta frekar upplýsingum við skipurit fyrirtækis skal bæta reitum við listann **Stöður** svo þeir séu tiltækir þegar leiðsagnarforritið er notað síðar í þessu ferli.

2. Í aðgerðasvæðinu skal velja hnappinn **Opna í Microsoft Office** og síðan, undir **Flytja út í Excel**, skal velja **Stöður**. Einnig er hægt að ýta á Ctrl+T.

    ![Flytjið út listasíðuna Stöður í Excel](media/org-admin.png)

3. Vistið Excel-skrána sem er flutt út.

    ![Flytjið út í svarglugga Excel](media/export-excel.png)

4. Í Visio skal velja **Visio - Búa til nýja** og síðan velja sniðmátsflokkinn **Viðskipti**.

    ![Ný skýringarmynd](media/new.png)

5. Veljið **Leiðsagnarforrit fyrir myndrit fyrirtækis** og síðan **Búa til**.

    ![Svargluggi leiðsagnarforrits fyrir myndrit fyrirtækis](media/orgchart-wizard.png)

6. Veljið **Upplýsingar sem eru þegar vistaðar í skrá eða gagnagrunni** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 1](media/orgchart-wizard7.png)

7. Veljið **Texta, „Org Plus“ (\*.txt) eða Excel-skrá** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 2](media/orgchart-wizard3.png)

8. Flettið til að velja útfluttu Excel-skrána sem inniheldur stöðustigveldið og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 3](media/orgchart-wizard2.png)

9. Stillið reitinn **Heiti** á **Staða**, stillið reitinn **Skýrslur til að** á **Skýrslur til að staðsetja** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 4](media/orgchart-wizard1.png)

10. Veljið reitina sem á að sýna á hverjum hnút og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 5](media/orgchart-wizard5.png)

11. Bætið dálknum **Staða** við listann **Móta gagnareiti** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 6](media/orgchart-wizard6.png)

12. Myndir eru ekki í boði eins og er. Á næstu síðu skal því velja **Næsta**.
13. Veljið **Ég vil að leiðsagnarforritið raði myndriti fyrirtækisins sjálfkrafa niður á margar síður**.

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 7](media/orgchart-wizard4.png)

14. Veljið **Ljúka**.

    Ef einhverjar stöður eru ekki í skipulaginu verður notandi beðinn um að bæta þeim við skýringarmyndina.

Skýringarmyndin sem er búin til í Visio birtir hvern yfirmann á aðskildu vinnublaði.

Þegar Visio-skráin er búin til birtir hver hnútur viðeigandi upplýsingar sem byggjast á reitunum sem voru valdir til að hafa með á skýringarmyndinni.

![Stigveldi skýringarmyndar](media/hierarchy.png)

**Frekari valkostir**

Í Human Resources er hugsanlega líka hægt að nota vinnusvæðið **Fólk** til að skoða stigveldistengdar upplýsingar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]