---
title: Ósamræmi í gögnum innkaupapöntunarlínu
description: Þú sérð gagnamisræmi eða gagnaspillingu á innkaupapöntunarlínum þínum.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100782"
---
# <a name="purchase-order-line-data-discrepancies"></a>Ósamræmi í gögnum innkaupapöntunarlínu

## <a name="symptoms"></a>Einkenni

Þegar þú skoðar línur innkaupapöntunar tekur þú eftir einu eða fleiri af eftirfarandi vandamálum:

- Það er gagnamisræmi eða spilling í afgangum innkaupapöntunarlínu (afhending eða reikningur).
- Það er spilling í innkaupapöntunarlínu eða hausstöðu.
- Þú getur ekki reikningsfært innkaupapöntun vegna þess að þú færð til dæmis eitt eða fleiri af eftirfarandi villuboðum:

    - "Stöðvað (villa): Færslan hefur þegar verið færð."
    - "Ekki er hægt að reikningsfæra magnið vegna þess að birgðafærslur með stöðuna Móttekið eru ófullnægjandi."
    - „Ófullnægjandi birgðafærslur með stöðuna „Keypt“ fyrir vöru%0 magni%1 ."

- Þú getur ekki gengið frá eða lokað innkaupapöntun vegna til dæmis eins af eftirfarandi vandamálum:

    - The **Loka** hnappur er ekki tiltækur.
    - Þú getur ekki afturkallað pantað magn innkaupapöntunarlínu fyrir innkaupapöntun sem er í staðfestu og mótteknu ástandi.

## <a name="cause"></a>Orsök

Þessi vandamál eru venjulega af völdum spillingar á gögnum eða misræmis í eftirstandandi magni fyrir eina eða fleiri innkaupapöntunarlínur.

## <a name="resolution"></a>Upplausn

Þú getur venjulega lagað þessi vandamál með því að uppfæra innkaupastöðu, afhendingarafganga og/eða reikningsafganga fyrir viðkomandi innkaupapöntunarlínur, eins og lýst er í eftirfarandi ferli.

1. Fara til **Innkaup og innkaup \> Reglubundin verkefni \> Hreinsun \> Leiðréttu innkaupapöntunarlínur handvirkt**.
1. Í **Pöntun** reit, finndu og veldu innkaupapöntunina sem veldur þér vandræðum.
1. Í **Innkaupapöntunarlínur** kafla, veldu línu þar sem þú fannst ósamræmi.
1. Í **Birgðaviðskipti** kafla, skoðaðu gögnin sem sýnd eru. Ef þú tekur eftir einhverju ósamræmi á milli innkaupapöntunarlínu og birgðafærslur hennar skaltu velja eina af eftirfarandi skipunum á aðgerðarrúðunni, eftir því hvar þú sérð ósamræmið:

    - **Endurreikna \> Endurreikna afhendingarafgang** - Uppfærðu sjálfkrafa stöðu innkaupapöntunarlínu og haus. Þessi aðgerð virkar aðeins fyrir birgðir innkaupapöntunarlínur (þ.e. línur þar sem varan er á lager). Vörur sem ekki eru á lager og vörur með aflaþyngd eru ekki studdar eins og er.
    - **Endurreikna \> Endurreiknaðu afgang reiknings** - Uppfærðu sjálfkrafa stöðu innkaupapöntunarlínu og haus. Þessi aðgerð virkar aðeins fyrir birgðir innkaupapöntunarlínur (þ.e. línur þar sem varan er á lager). Vörur sem ekki eru á lager og vörur með aflaþyngd eru ekki studdar eins og er.
    - **Endurreikna \> Endurreikna stöðuna** - Endurreiknaðu stöðu valda línu. Þessi útreikningur er byggður á núverandi rökfræði. Þess vegna verður staða innkaupapöntunarhaus uppfærð eftir þörfum, byggt á nýju innkaupapöntunarlínustöðunni.

1. Ef þú sérð enn ósamræmi í magni sem eftir er geturðu notað eftirfarandi reiti til að breyta þeim beint eftir þörfum:

    - Eftirstöðvar afhendingar
    - Eftirstöðvar afhendingar birgða
    - Reikningsafgangur
    - Birgðareikningsafgangur
