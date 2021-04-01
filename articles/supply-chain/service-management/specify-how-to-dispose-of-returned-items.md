---
title: Tilgreint hvernig losa eigi skilaðar vörur
description: Tilgreina hvernig losa eigi skilavörur.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242374"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Tilgreint hvernig losa eigi skilaðar vörur 

[!include [banner](../includes/banner.md)]


Þegar skilapöntun er meðhöndluð þarf að tilgreina ástæðukóða skila til að taka það fram af hverju verið er að skila. Einnig þarf að tilgreina ráðstöfunarkóða og ráðstöfunaraðgerð til að ákvarða hvað gera skal við sjálfa skiluðu afurðina.

Hægt er að nota ráðstöfunarkóða þegar stofnuð er skilapöntun, koma skráningarvöru eða þegar vörukoma er fylgiseðilsuppfærð og endi er bundinn á biðgeymslupöntun.

Hægt er að skilgreina alla ráðstöfunarkóða sem þarf til að styðja viðskiptaferlin. Eftirfarandi tafla veitir safn af mikið notuðum kóðum til að úthluta ráðstöfun skilavöru.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ráðstöfunargerð</p></th>
<th><p>Algengur kóði</p></th>
<th><p>lýsing</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Losun</p></td>
<td><p>RE</p></td>
<td><p>Rýra/Eyða</p></td>
</tr>
<tr class="even">
<td><p>Losun</p></td>
<td><p>GL</p></td>
<td><p>Gefa til líknarmála</p></td>
</tr>
<tr class="odd">
<td><p>Losun</p></td>
<td><p>LA</p></td>
<td><p>Losun þriðja aðila</p></td>
</tr>
<tr class="even">
<td><p>Losun</p></td>
<td><p>HR</p></td>
<td><p>Hrak</p></td>
</tr>
<tr class="odd">
<td><p>Losun</p></td>
<td><p>SA</p></td>
<td><p>Sala þriðja aðila (aukamarkaðir)</p></td>
</tr>
<tr class="even">
<td><p>Laga/Breyta</p></td>
<td><p>EN</p></td>
<td><p>Endurvinna</p></td>
</tr>
<tr class="odd">
<td><p>Laga/Breyta</p></td>
<td><p>EL</p></td>
<td><p>Endurframleiða/Laga</p></td>
</tr>
<tr class="even">
<td><p>Laga/Breyta</p></td>
<td><p>BR</p></td>
<td><p>Breyta</p></td>
</tr>
<tr class="odd">
<td><p>Laga/Breyta</p></td>
<td><p>LG</p></td>
<td><p>Laga</p></td>
</tr>
<tr class="even">
<td><p>Laga/Breyta</p></td>
<td><p>SL</p></td>
<td><p>Skila til lánadrottins</p></td>
</tr>
<tr class="odd">
<td><p>Annað</p></td>
<td><p>NE</p></td>
<td><p>Nota eins og er</p></td>
</tr>
<tr class="even">
<td><p>Annað</p></td>
<td><p>ES</p></td>
<td><p>Endursala</p></td>
</tr>
<tr class="odd">
<td><p>Annað</p></td>
<td><p>GE</p></td>
<td><p>Gengi</p></td>
</tr>
<tr class="even">
<td><p>Annað</p></td>
<td><p>YM</p></td>
<td><p>Ýmislegt</p></td>
</tr>
</tbody>
</table>


Fyrir hvern ráðstöfunarkóða sem skilgreindur er verður að velja ráðstöfunaraðgerð. Ráðstöfunaraðgerðin ákvarðar efnisleg og fjárhagsleg áhrif af ráðstöfunarkóða. Til dæmis ákvarðar ráðstöfunaraðgerðin efnislega meðhöndlun skiluðu vörunnar, fjárhagsleg áhrif skiluðu vörunnar og hvort senda verði skiptivöru til viðskiptamanns. Hægt er að skilgreina ótakmarkaðan fjölda ráðstöfunarkóða, allt eftir rekstrarþörfum, en einungis er hægt að velja úr sex fyrirfram skilgreindum ráðstöfunaraðgerðum. Eftirfarandi tafla sýnir ráðstöfunaraðgerðirnar og skilgreiningar þeirra.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ráðstöfunaraðgerð</p></th>
<th><p>lýsing</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kredit</strong></p></td>
<td><p>Skila vörunni í birgðir og tekjufæra viðskiptamann.</p></td>
</tr>
<tr class="even">
<td><p><strong>Aðeins kredit</strong></p></td>
<td><p>viðskiptamanns tekjufærður án þess að þess sé krafist eða vænst að vörunni sé skilað.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Rýrnun</strong></p></td>
<td><p>Rýra vöruna og tekjufæra viðskiptamann.</p></td>
</tr>
<tr class="even">
<td><p><strong>Skrifa yfir og setja í kredit</strong></p></td>
<td><p>Skila vörunni í birgðir, stofna skiptipöntun og tekjufæra viðskiptamanninn.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Skrifa yfir og eyða</strong></p></td>
<td><p>Rýra vöruna, stofna skiptipöntun og tekjufæra viðskiptamanninn.</p></td>
</tr>
<tr class="even">
<td><p><strong>Skila til viðskiptavinar</strong></p></td>
<td><p>Hafna skilavörunni og skila henni aftur til viðskiptamannsins.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Veljið ráðstöfunarkóða fyrir biðgeymslupöntun

1.  Smelltu á **Birgðastjórnun** \> **Reglubundið** \> **Gæðastjórnun** \> **Biðgeymslupantanir**.

2.  Fyrir núverandi biðgeymslupöntun skal velja aðgerð í reitnum **Ráðstöfunarkóði** á flipanum **Yfirlit**.



## <a name="see-also"></a>Sjá einnig

[Biðgeymslupöntun (skjámynd)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[Ráðstöfunarkóðar (skjámynd)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]