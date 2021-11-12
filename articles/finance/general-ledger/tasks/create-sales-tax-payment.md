---
title: Stofna VSK-greiðslu
description: Jafna og bóka VSK vinnslan jafnar VSK stöður í VSK -lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700114"
---
# <a name="create-a-sales-tax-payment"></a>Stofna VSK-greiðslu

[!include [banner](../../includes/banner.md)]

Jafna og bóka VSK vinnslan jafnar VSK stöður í VSK -lykla og mótfærir þeim virðisaukaskattsuppgjör reiknings á tilteknu tímabili.

1. Fara á **Skattur > Skattframtöl > Virðisaukaskattur > Jafna og bóka vsk**.
2. Í reitnum **jöfnunartímabil** skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í reitnum **Frá dags.** færirði inn dagsetningu.
    - Ef valkosturinn **Taka leiðréttingar** með er ekki valin á síðunni **Færibreytur fjárhags**, getur jöfnun verið unnin fyrir mismunandi útgáfur. Upphaflegt er fyrsta jöfnun fyrir tímabilið og er einungis hægt að vinna einu sinni fyrir tímabil. Síðustu leiðréttingar jafna vsk-færslur sem hafa verið bókaðar eftir að upprunalega útgáfa hefur verið stofnuð.
5. Færa inn dagsetningu í reitinn **Færsludagsetning**.
6. Smellt er á **OK**.

## <a name="performance-consideration"></a>Almenn afkastaatriði

Það getur tekið langan tíma að ljúka VSK-greiðsluferlinu. Helstu þættir sem hafa áhrif á afköst ferlisins er fjöldi reikninga á jöfnunartímabilinu og fjöldi færslna sem þarf að bóka í fylgiskjali virðisaukauppgjörsins. Til að bæta afköst er hægt að sneiða framhjá sumum aðgerðum sem ekki eru nauðsynlegar í ferlinu.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Virkja eiginleikann Bætt afköst VSK-greiðslu

Eiginleikinn **Bætt afköst VSK-greiðslu** geta aukið afköst VSK-greiðsluferlisins með því að safna saman í eina línu upphæð bókhaldsgjaldmiðils og upphæð skýrslugjaldmiðils í fylgiskjalslínum VSK-greiðslu sem eru með sama aðallykil, fjárhagsvídd og gjaldmiðil.

1. Opna skal **Kerfisstjórnun** \> **Vinnusvæði** \> **Eiginleikastjórnun**.
2. Á flipanum **Allt** skal leita að og velja **Bætt afköst VSK-greiðslu**.
3. Veljið **Virkja**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Koma í veg fyrir að mótfærsluskattafærslur myndist

Fylgiskjal VSK-greiðslu bókar mótfærsluskattafærslur sjálfgefið á móti hverri VSK-færslu sem er jöfnuð í VSK-greiðsluferlinu. Þessar mótfærslur VSK-færslna eru hafðar með í skýrslunni **Afstemming virðisaukaskatts/fjárhags**. Þær sýna eftirstöðvar VSK-færslna sem eru ekki jafnaðar á tímabilinu.

Hinsvegar geta mótfærslur VSK-færslna aukið byrðina á VSK-greiðsluferlinu. Þar af leiðandi er hægt að virkja forútgáfu sem kallast **TaxReportGenOffsetTaxTransPerRecordSetFlighting** eftir þörfum. Þessi forútgáfa getur aukið afköst fyrir myndun mótfærslur skattafærslu fyrir lönd og svæði fyrir utan Taíland, Pólland, Ungverjaland, Litháen, Malasíu, Indland, Ítalíu, Rússland, Tékkland, Eistland og Lettland.

> [!NOTE]
> Ef sérsniðnir reitir eru í skattfærslutöflunni er ekki hægt að virkja forútgáfuna.

Þar sem skýrslan **Afstemming virðisaukaskatts/fjárhags** er yfirleitt aðeins notuð fyrir innri stýringu og er ekki nauðsynleg í mörgum skattkerfum, er hægt að velja að mynda ekki mótfærslur VSK-færslna í fylgiskjali VSK-greiðslna.

1. Farðu í **Skattur** \> **Óbeinir skattar** \> **Virðisaukaskattur** \> **VSK-uppgjörstímabil**.
2. Veldu uppgjörstímabil.
3. Á flýtiflipanum **Almennt** skal stilla valkostinn **Koma í veg fyrir að mótfærsluskattafærslur myndist** á **Já**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
