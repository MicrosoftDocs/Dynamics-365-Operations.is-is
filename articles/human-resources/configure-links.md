---
title: Búðu til tengla úr mannauði í annað umhverfi
description: Þessi grein útskýrir hvernig á að búa til tengil frá Microsoft Dynamics 365 Human Resources í annað Dynamics 365 umhverfi.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065294"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Búðu til tengla úr mannauði í annað fjármálaumhverfi

Viðskiptavinur gæti verið með tvö Dynamics 365 umhverfi sem hann er að vinna í. Sem dæmi gæti viðskiptavinurinn haft a Dynamics 365 Human Resources umhverfi á Finance innviðum og þarf að tengjast öðru Dynamics 365 Finance umhverfi. 

Þessi eiginleiki mun leyfa hlekki frá mannauðssíðu á tiltekna síðu í öðru fjármálaumhverfi. Þegar hlekkirnir eru stilltir geturðu tilgreint hvar hlekkurinn verður fáanlegur í Human Resources og marksíðuna sem verður opnuð í hinu umhverfinu.

> [!Note] 
> Þú verður að kveikja **Upplifun mannauðs notenda** inn **Eiginleikastjórnun** til að fá þennan eiginleika.

## <a name="configure-target-systems"></a>Grunnstilla markkerfi

Í Human Resources geta kerfisstjórar skilgreint tengla sem munu birtast á **Mannauður** síður. Hlutar stillingarinnar eru fjármálaumhverfi sem þú vilt fara í sem miða á tengilinn. 

Til að stilla markkerfið:
1. Á **Stilla tengla** síðu, veldu **Stilla markkerfi**.  
2. Sláðu inn markkerfisheitið og gefðu upp slóð fjármálaumhverfisins. Eftir að þú hefur stillt markkerfin þín geturðu skilgreint hlekkina þína.

## <a name="configure-links"></a>Samskipa tengla

Hver hlekkur sem þú býrð til mun hafa eftirfarandi upplýsingar skilgreindar:
 - **Tengill** : Nafn á hlekknum. Aðeins notað til auðkenningar.
 - **Virkjaðu þennan tengil** : Stilltu á **Já** ef þú vilt birta hlekkinn til mannauðsnotenda.
 - **Birta nafn** : Sláðu inn nafnið sem mun birtast sem tengill á aukaumhverfið. 
 - **Yfirborðshlekkur á eyðublaði** : Veldu hvaða síðu þú vilt birta hlekkinn á. Tenglar geta aðeins komið upp á yfirborðið **Sjálfsafgreiðsla starfsmanna** vinnurými og **Job**, **·**, **·**, og **Straumlínulagaður starfsmaður** síður.
 - **Hópur** : Þú getur skipulagt tenglana þína með því að nota hópa. Veldu núverandi hóp eða búðu til nýjan með því að nota **Hópur** dálki.
 - **Markkerfi** : Veldu markkerfið sem var búið til með því að nota **Stilla markkerfi** valmöguleika. Þetta verður aukaumhverfið sem verður notað þegar þú ferð með hlekknum.
 - **Notaðu núverandi fyrirtæki notandans** : Veldu **Já** að nota núverandi fyrirtæki notandans þegar farið er í Finance. Veldu **Nei** að velja fyrirtæki sem nota á.
 - **Skotmark** valmyndaratriði: Sláðu inn valmyndaratriðið úr fjármálaumhverfinu sem tengillinn ætti að nota þegar þú vafrar. Valmyndaratriði sem þú getur farið beint á til eru tiltæk. 

   Til að finna valmyndaratriðið sem þarf:
   1. Farðu í fjármálaumhverfið og opnaðu síðuna sem er markmið flakksins. 
   2. Afritaðu valmyndaratriðið úr vefslóðinni. Til dæmis, ef þú vilt að tengillinn fari með þig á starfsmannalistann í fjármálum og rekstri skaltu slá inn gildið sem birtist á eftir „&mi“ í vefslóðinni. 
   3. Valmyndaratriðið til að vafra um listasíðu starfsmannsins í þessu dæmi er: HcmWorkerListPage_Employees.

 - **Tengill á gagnagjafa** : Veldu uppsprettu gagna sem hlekkurinn vísar til. Algengustu veitur eins og **Starfskraftur** og **Staða** eru tiltækar.

### <a name="access-to-links"></a>Aðgangur að tenglum

Kerfisstjórar munu sjá nýstofnaða tengla á skilgreindum síðum, jafnvel þótt **Virkja þennan tengil** valkost sé stillt á **Nei**. Þetta er hægt að nota til að prófa tengla áður en þau eru flutt til annarra starfsmanna. Öll önnur hlutverk munu aðeins sjá stilltu tenglana á eftir **Virkjaðu þennan tengil** valkostur er stilltur á **Já**. Starfsmenn sem hafa aðgang að síðum þar sem tenglarnir birtast munu hafa aðgang að tenglum.

Notendur verða einnig að hafa öryggisréttindi innan aukaumhverfisins sem skilgreint er til að fá aðgang að síðunum í því umhverfi. Ef það gerist ekki birtist öryggissvargluggi þegar tengilinn er notaður.


