---
title: Skilgreiningar lánardrottinsbeiðni
description: Þetta efnisatriði lýsir svæðunum sem nauðsynlegt er að fylla í nýrri lánardrottnabeiðni.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a78ec681ff9bfe9f7792da04553e4b543bf4a183
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809303"
---
# <a name="vendor-request-configurations"></a>Skilgreiningar lánardrottinsbeiðni
[!include [banner](../includes/banner.md)]

Til að ljúka lánardrottnabeiðni þarf tengiliður lánardrottins að fara í gegnum leiðsagnarforrit fyrir skráningu væntanlegs lánardrottins.

Í **Grunnstillingar lánardrottinsbeiðni** skjámyndinni getur þú stofnað forstillingar sem tilgreina svæði og sýnilegar svæði í leiðsagnarforriti fyrir skráningu væntanlegs lánardrottins.

Leiðsagnarforrit fyrir skráningu lánardrottins byrjar á því að spyrja væntanlegan lánardrottin hvaða land/svæði lánardrottinn á viðskipti í. Þessar upplýsingar ákvarða viðeigandi grunnstillingu. Ef engin ákveðin grunnstilling er skilgreind fyrir land/svæði verður sjálfgefið grunnstillingar notað.

### <a name="set-up-a-vendor-request-configuration"></a>Setja upp grunnstillingar lánardrottinsbeiðni

Sjálfgefið er að lánardrottins grunnstilling sé tiltæk í skjámynd grunnstillinga lánardrottinsbeiðni.

Ekki er hægt að velja land/svæði fyrir sjálfgefna grunnstillingu, þannig að ekki er hægt að breyta **Löndum/svæðum**.

1. Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.
2. Smelltu á flipann **Svæði** til að stilla staða skráðra svæða.
3. Falið (ekki sýnilegt)
4. Sýnt (sýnilegt en ekki skylt)
5. Nauðsynlegt (sýnilegt og skylt)
6. Smelltu á flipann **Innihald** til að tilgreina hvort textinn á að sjást í leiðsagnarforritinu og hvort það ætti að vera viðurkenning á því að væntanlegur lánardrottna notandi verður að samþykkja þetta áður en hann fer í næsta skref í leiðsagnarforritinu. Beðið verður um viðurkenninguna fyrir hvaða skilmála og skilyrði sem notandinn verður að samþykkja til að halda áfram.

Þú getur einnig slegið inn staðfestingarskilaboð sem munu birtast þegar búið er að fara í gegnum leiðsagnarforritið, og þú getur bætt við einni eða fleiri spurningalistum.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Búa til grunnstillingar lánardrottins fyrir tiltekna land/svæði
1.  Smelltu á **Innkaup og aðföng** > **Uppsetning** > **Lánardrottnar**, og smelltu síðan á **Grunnstillingar lánardrottinsbeiðni**.
2.  Smellt er á **Ný** til að búa til nýjar grunnstillingu, og nafn á grunnstillinguna.
3.  Smellið á **Vista**.
4.  Opnaðu flipann **Land/svæði** til að velja landið/svæðið sem á að nota grunnstillinguna fyrir.
5.  Ljúktu grunnstillingunni með því að fylgja leiðbeiningunum um sjálfgefna grunnstillingu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]