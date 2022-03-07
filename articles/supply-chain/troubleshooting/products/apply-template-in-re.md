---
title: Þú getur ekki notað sniðmát á útgefna vöru
description: Þú getur ekki notað sniðmát á útgefna vöru.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760395"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Þú getur ekki notað sniðmát til að búa til útgefna vöru

KB númer: 4612097

## <a name="symptoms"></a>Einkenni

Þegar ný útgefin vara er stofnuð með því að nota gluggann **Ný útgefin afurð** er hægt að velja sniðmát. Sniðmátið á að gefa sjálfgefnar stillingar fyrir marga reiti í nýju útgefnu vörunni. Sumir eða allir reitir eru þó ekki stilltir eftir að sniðmátið er valið.

## <a name="cause"></a>Orsök

Margar í Microsoft Dynamics 365 Supply Chain Management gera notendum kleift að stofna sniðmát sem setur upphafsstillingar fyrir færslurnar sem eru sýndar á þeim síðum. Hægt er að stofna eitt af þessum sniðmátum með því að velja **Færsluupplýsingar** í flipanum **Valkostir** á aðgerðasvæðinu. Hins vegar eru útgefnar vörur mun flóknari en flestar aðrar gerðir færslna. Þó að hægt sé að velja **Skráningarupplýsingar** á síðunni **Útgefinar vörur** til að stofna sniðmát, og þó hægt sé að velja það sniðmát þegar útgefin vara er stofnuð, mun sniðmátið ekki veita væntanleg reitargildi fyrir nýju útgefnu vöruna. Því er ekki hægt að nota sniðmát fyrir „skráningarupplýsingar“ fyrir útgefnar vörur. Þess í stað verður að stofna sérstök vörusniðmát.

## <a name="resolution"></a>Upplausn

Til að búa til sniðmát vöru skal nota valmyndina **Sniðmát** á flipanum **Vara** á aðgerðasvæði, ekki hnappinn **Skrá upplýsingar** á flipanum **Valkostir**.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Nýtt**, skal velja **Sniðmát** og velja svo **Búa til persónulegt sniðmát** eða **Stofna samnýtt sniðmát** eftir því sem við á.
