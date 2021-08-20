---
title: Fjárhagur altæks birgðabókhalds
description: Í þessu efnisatriði er fjárhagsbókum altæks birgðabókhalds lýst, sem eru skilgreindar út frá samsetningu gjaldmiðils, dagatals, viðtekinni reglu og tengingu við lögaðila.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e956bac61df4b694ef347b804fed139e9e22e6f95d1bac7ea483a07946cb110f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722440"
---
# <a name="global-inventory-accounting-ledger"></a>Fjárhagur altæks birgðabókhalds

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Altækt birgðabókhald er með eigin söfn af fjárhagsbókum. Í hvert sinn sem unnið er úr birgðatengdri færslu fyrir viðeigandi lögaðila getur kerfið reiknað þá færslu í eins mörgum fjárhagsbókum altæks birgðabókhalds og þarf.

Fjárhagur er skrá yfir debet-og kreditráðstafanir. Þessar ráðstafanir eru flokkaðar með því að nota kostnaðareiningar og fjárhagslykla undirbókar. Fjárhagur altæks birgðabókhalds er skilgreindur eftir samsetningunni af gjaldmiðli, dagatali, viðtekinni reglu og tengingu við lögaðila.

Til að setja upp fjárhagsbækur altæks birgðabókhalds skal fara í **Altækt birgðabókhald \> Uppsetning \> Fjárhagir altæks birgðabókhalds**. Fyrir hvern fjárhag skal stilla eftirfarandi reiti:

- **Heiti** - Færið inn heiti fjárhagsins.
- **Lýsing** - Færið inn lýsingu á fjárhagnum.
- **Fjárhagsdagatal** – Tilgreinið fjárhagsdagatal fyrir fjárhaginn.
- **Gjaldmiðill og gerð gengis** – Notið reitina í þessum flýtiflipa til að velja bókhaldsgjaldmiðil sem fjárhagurinn notar og gerð gengir. Gjaldmiðillinn sem þú velur getur verið annar en gjaldmiðillinn sem lögaðilinn notar. Í altæku birgðabókhaldi geta notendur skilgreint eins margar fjárhagsbækur kostnaðar og þarf til. Altækt birgðabókhald styður birgðabókhald í mörgum gjaldmiðlum og í margs konar verðmati. Stilltu eftirfarandi reiti:

    - **Gjaldmiðill** – Veljið þann kostnaðargjaldmiðil þar sem unnið er með birgðatengd gildi. Þessi gildi eru birgðavirði, kostnaður seldra vara, birgðir í flutningi og alls kyns frávik.
    - **Gerð gengis** – Veljið gengið sem kerfið á að nota til að umreikna færsluupphæðinni í færslugjaldmiðilinn og staðalkostnað varanna í kostnaðargjaldmiðilinn.

- **Heiti viðtekinnar reglu** – Tilgreinið viðtekna reglu. Viðtekin regla er safn af reglum sem ákvarðar hvernig kostnaður verður færður inn í fjárhag.
- **Lögaðili** – Fjárhagurinn mun gera grein fyrir skjölunum sem bókuð eru í völdum lögaðila.
- **Undirbúningur** – Veljið hvort birgðafærslur sem voru stofnaðar áður en fjárhagurinn var stofnaður eigi að vera unnar í samræmi við gjaldmiðil og viðtekna reglu í fjárhagnum. Veljið eitt af eftirfarandi gildum:

    - **Virkjað** – Fjárhagurinn á að vinna úr færslum sem voru stofnaðar áður en fjárhagurinn var stofnaður.
    - **Óvirkjað** – Fjárhagurinn á aðeins að vinna úr færslum sem eru stofnaðar eftir að fjárhagurinn var stofnaður.

    > [!IMPORTANT]
    > Þú getur **ekki** komið aftur og stillt þennan reit eftir að þú hefur slegið inn ný skjöl.

- **Staða** – Kerfið stillir sjálfkrafa stöðu nýlega stofnaðra fjárhagsbóka á *Undirbúa*.
